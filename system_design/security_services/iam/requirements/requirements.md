# Identity & Access Management (IAM) Requirements — Platform Baseline v2

## Functional requirements
- IAM-FR-001: Product/Security Profile shall declare capability, placement, and provider selection.
- IAM-FR-002: Portable semantics shall remain independent of provider implementation.
- IAM-FR-003: Offline/unavailable-provider behavior shall be defined.

## Interface requirements
- IAM-IR-001: Contracts shall use provider-neutral identity/resource/capability references.
- IAM-IR-002: Policy/contract versions shall be explicit.
- IAM-IR-003: Provider-specific SDK/hardware details shall remain behind adapters.

## Security requirements
- IAM-SR-001: Protected actions shall be enforced at the execution boundary.
- IAM-SR-002: Revocation/failure/stale-policy behavior shall fail safely according to Security Profile.
- IAM-SR-003: Security-relevant decisions and failures shall be auditable.

## Reliability requirements
- IAM-RR-001: Backend/provider outage shall not create undefined authorization/security state.
- IAM-RR-002: Recovery/synchronization shall preserve stable product semantics.

## Design acceptance criteria
- IAM-AC-001: Standalone camera authenticates and authorizes according to local profile.
- IAM-AC-002: Connected camera can consume authoritative backend identity without losing local enforcement.
- IAM-AC-003: Revoked sessions follow defined propagation/offline policy.
- IAM-AC-004: Changing identity provider does not change product principal/resource semantics.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
