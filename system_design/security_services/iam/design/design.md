# Identity & Access Management (IAM) Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Client + Camera + optional Gateway/Backend responsibilities; authoritative source depends on Product Profile**

## Purpose and ownership
Separate human, service, and device identity flows while preserving explicit local camera enforcement and offline operation.

## Portable contract
Identity contract for principals, credentials/session references, authentication result, scope, lifecycle/revocation state, and provider-independent identity references.

## Relationship overview
![Identity & Access Management (IAM) relationship](./iam_relationship.svg)

## Review-driven decisions
- Human, service, and device identity are distinct.
- Client/backend/camera responsibilities are explicit.
- Customer/site/area scope is modeled.
- Credential/session lifecycle and revocation are explicit.
- Authentication/MFA policy is selected by security profile.
- Local operations do not require always-online backend dependency.

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
1. Standalone camera authenticates and authorizes according to local profile.
2. Connected camera can consume authoritative backend identity without losing local enforcement.
3. Revoked sessions follow defined propagation/offline policy.
4. Changing identity provider does not change product principal/resource semantics.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and review feedback.
