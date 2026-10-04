# Activity Manager / Lifecycle Adapter Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Client platform adapter; optional camera-local application host only when a product needs it**

## Purpose and ownership
Re-scope lifecycle management as a small portable lifecycle contract mapped to native client/platform mechanisms rather than a mandatory Android-style camera framework.

## Product-owned contract
ApplicationLifecycle contract: foreground/background, start/stop, recover/restart, ownership of navigation versus service lifecycle.

## Relationship overview
![Activity Manager / Lifecycle Adapter relationship](./activity_manager_relationship.svg)

## Review-driven decisions
- Client navigation belongs to the client application.
- Background behavior maps to platform adapters.
- Process restart is a platform concern with portable recovery semantics.
- Camera service lifecycle is owned by camera services/device management, not client activity navigation.
- No new universal OS framework is required.

## Product Profile inputs
- whether this capability exists in the product;
- deployment placement and compatible contract version;
- selected native/platform adapter;
- security and offline behavior.

## Design rules
- platform/framework names do not imply a mandatory Android implementation;
- portable contracts remain smaller than native platform APIs;
- client and camera platform concerns are separated;
- private/provider implementation is not exposed upward.

## Security
- caller identity and authorization are enforced at protected operations;
- security-relevant lifecycle/data actions are auditable;
- standalone camera behavior does not depend on backend availability.

## Open decisions
- native adapter choices per supported platform;
- exact compatibility/versioning and resource limits.

## Design acceptance criteria
1. A headless camera does not require an Activity Manager.
2. Android/iOS/Web can map lifecycle semantics to native mechanisms.
3. Camera services continue independently of client navigation lifecycle.
4. Restart recovery has deterministic portable states.

## Changelog
- 2026-10-04: Re-scoped for Platform Architecture Baseline v2 and review feedback.
