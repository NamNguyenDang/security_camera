# Live View Detailed Design — Platform Baseline v2

## Status

Revised against the deployment-first platform architecture proposed in PR #77.

## Deployment placement

**Client + Camera; optional Site Gateway and Backend**

## Purpose and ownership

Own the user-facing live-view session contract while keeping client presentation, camera streaming, optional relay/backend signaling, and optional local display separate.

## Product-owned contract

LiveViewSession contract: session ownership, capability negotiation, authorization/revocation, reconnect state, and explicit control/media channels.

## Relationship overview

![Live View relationship](./live_view_relationship.svg)

## Interaction model

- **Command / control:** session and lifecycle operations use stable product contracts.
- **State / events:** state changes and durable domain events are separate from media payloads.
- **Media / high-bandwidth data:** video/audio data uses an explicit bounded media path where applicable.
- **Deployment transport:** in-process, local IPC, direct network, gateway relay, or backend relay is selected by the Product Profile and must not change product semantics.

## Review-driven design decisions

- Remote client does not depend on camera Window Manager/View System.
- Control signaling and video/media path are separate.
- Direct client↔camera and relayed client↔gateway/backend↔camera paths are product-profile selections.
- Local camera display is optional and never required for remote live view.
- Latency and buffering budgets are selected by product profile and exposed as acceptance criteria.

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

1. A headless standalone camera can serve an authorized remote client without backend/gateway.
2. Revocation terminates or blocks the session according to the selected security profile.
3. Reconnect behavior is deterministic after transient camera/network loss.
4. Media path meets the selected profile latency/buffering budget.
5. Replacing the camera capture/media provider does not change the client contract.

## Changelog

- 2026-10-04: Reworked for Platform Architecture Baseline v2 and design-review feedback.
