# Playback Detailed Design — Platform Baseline v2

## Status

Revised against the deployment-first platform architecture proposed in PR #77.

## Deployment placement

**Client + Camera; optional Site Gateway and Backend**

## Purpose and ownership

Own the playback-session contract while separating client presentation from recording lookup/delivery and from optional local-device playback.

## Product-owned contract

RecordingRepository + PlaybackSession contracts independent of local filesystem, database engine, or cloud provider.

## Relationship overview

![Playback relationship](./playback_relationship.svg)

## Interaction model

- **Command / control:** session and lifecycle operations use stable product contracts.
- **State / events:** state changes and durable domain events are separate from media payloads.
- **Media / high-bandwidth data:** video/audio data uses an explicit bounded media path where applicable.
- **Deployment transport:** in-process, local IPC, direct network, gateway relay, or backend relay is selected by the Product Profile and must not change product semantics.

## Review-driven design decisions

- Recording lookup returns stable recording identity, not storage paths.
- Recording repository may be local camera, gateway, or cloud.
- Deletion during playback has defined snapshot/lease/not-found behavior.
- Authorization scope covers customer/site/area/device/recording.
- Corruption, buffering limits, and event-to-recording identity are explicit.

## Product Profile inputs

- deployment placement and optional gateway/backend participation;
- capability availability;
- compatible contract versions;
- adapter/provider selection;
- security profile;
- offline behavior;
- latency, buffering, storage, and resource budgets where applicable.

## Security

- device-side authentication and authorization remain defined for standalone profiles;
- backend identity/policy may be authoritative for connected profiles, but camera enforcement and offline behavior remain explicit;
- credentials, keys, and recording protection are accessed through approved security contracts;
- security-relevant actions are auditable.

## Decisions

- Product behavior is independent of operating-system, database, cloud, media, and hardware suppliers.
- Client hardware/OS is separate from camera hardware/OS.
- Optional capabilities are enabled only by Product Profile.
- No component may bypass a product contract to depend on another component's private implementation.

## Open decisions

- exact transport/provider selections for each product profile;
- product-specific numerical performance budgets;
- provider qualification evidence and compatibility matrix.

## Design acceptance criteria

1. The same playback contract works with local or cloud recording repositories.
2. Deleted or expired recordings produce deterministic behavior during active playback.
3. Corrupt media is reported without exposing provider internals.
4. Unauthorized recording access is denied consistently offline and online.
5. Buffering remains within the selected product-profile budget.

## Changelog

- 2026-10-04: Reworked for Platform Architecture Baseline v2 and design-review feedback.
