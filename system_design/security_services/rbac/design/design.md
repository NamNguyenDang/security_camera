# Role-Based Access Control (RBAC) Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Policy evaluation may occur on Camera, Gateway, Backend, or Client-facing service; enforcement occurs where action executes**

## Purpose and ownership
Extend role-to-permission mapping with resource scope and stable policy-evaluation semantics independent of policy source.

## Portable contract
AuthorizationDecision contract including principal, role/permission, customer/site/area/device/recording scope, inheritance, explicit deny, policy version, and offline state.

## Relationship overview
![Role-Based Access Control (RBAC) relationship](./rbac_relationship.svg)

## Review-driven decisions
- Resource scope is first-class.
- Permission inheritance and explicit deny precedence are defined.
- Ownership transfer changes effective scope.
- Revocation propagation is explicit.
- Offline policy semantics are explicit.
- Policy source is replaceable while evaluation contract remains stable.

## Product / Security Profile inputs
- placement and provider selection;
- compatible contract/policy version;
- offline and revocation behavior;
- mandatory/optional capability and trust requirements.

## Security model
Security outcomes remain product obligations even when providers are replaceable. Enforcement occurs at the deployment performing the protected action.

## Open decisions
- concrete identity/policy/provider technologies;
- profile-specific TTL, propagation, and qualification limits.

## Design acceptance criteria
1. A permission on one site does not implicitly authorize another.
2. Explicit deny precedence is deterministic.
3. Ownership transfer removes stale inherited access.
4. Offline authorization behavior is defined and auditable.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and review feedback.
