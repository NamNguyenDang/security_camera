# Alarm Detailed Design — Platform Baseline v2

## Status

Revised against the deployment-first platform architecture proposed in PR #77.

## Deployment placement

**Client + Camera; optional Site Gateway and Backend**

## Purpose and ownership

Own alarm-domain presentation and acknowledgement contracts while separating event/rule evaluation, acknowledgement state, escalation policy, and delivery adapters.

## Product-owned contract

AlarmEvent + AlarmAcknowledgement + AlarmDelivery contracts with scoped resource identity.

## Relationship overview

![Alarm relationship](./alarm_relationship.svg)

## Interaction model

- **Command / control:** session and lifecycle operations use stable product contracts.
- **State / events:** state changes and durable domain events are separate from media payloads.
- **Media / high-bandwidth data:** video/audio data uses an explicit bounded media path where applicable.
- **Deployment transport:** in-process, local IPC, direct network, gateway relay, or backend relay is selected by the Product Profile and must not change product semantics.

## Review-driven design decisions

- Camera may create local alarm events; backend/gateway may evaluate broader rules.
- Client presentation is separate from notification delivery.
- Deduplication, acknowledgement identity, offline behavior, and delivery failure are defined.
- Customer/site/area/device scope is explicit.
- Display/audio outputs are optional product capabilities.

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

1. Remote-only alert products work without local display or audio.
2. Duplicate source events do not create uncontrolled duplicate alarms.
3. Acknowledgement identity and scope are auditable.
4. Offline camera/gateway behavior is deterministic.
5. Notification provider replacement does not change alarm-domain semantics.

## Changelog

- 2026-10-04: Reworked for Platform Architecture Baseline v2 and design-review feedback.
