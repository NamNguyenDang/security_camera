# Client Resource Manager Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Client platform area; optional local-display UI on Camera only when selected**

## Purpose and ownership
Limit this component to packaged UI resources and configuration-dependent client assets; it does not own camera compute, memory, or media budgets.

## Product-owned contract
ClientResource contract for resolving profile/platform-specific UI assets and missing-resource behavior.

## Relationship overview
![Client Resource Manager relationship](./resource_manager_relationship.svg)

## Review-driven decisions
- Camera compute/memory/media resource management belongs elsewhere.
- Resource selection depends on client/platform and Product Profile.
- Database/device storage service is not required for every client.
- Missing assets have deterministic fallback/error behavior.
- Native packaging remains an adapter concern.

## Product Profile inputs
- capability optionality and placement;
- compatible contract version;
- selected platform/provider adapter;
- security, rollback/retry, and offline policy.

## Design rules
- portable product behavior is separated from native package/resource/notification mechanisms;
- client and camera lifecycles are distinct;
- mandatory security policy is not delegated to a convenience framework component.

## Open decisions
- provider/platform selection per profile;
- numerical retry, cache, retention, and compatibility limits.

## Design acceptance criteria
1. Web/iOS/Android clients resolve resources without camera storage services.
2. Missing resource behavior is deterministic.
3. Changing client packaging mechanism does not change product presentation state contract.
4. Headless cameras do not require this client resource component.

## Changelog
- 2026-10-04: Re-scoped for Platform Architecture Baseline v2 and review feedback.
