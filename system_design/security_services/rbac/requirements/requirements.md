# Role-Based Access Control (RBAC) Requirements — Platform Baseline v2

## Functional requirements
- RBAC-FR-001: Product/Security Profile shall declare capability, placement, and provider selection.
- RBAC-FR-002: Portable semantics shall remain independent of provider implementation.
- RBAC-FR-003: Offline/unavailable-provider behavior shall be defined.

## Interface requirements
- RBAC-IR-001: Contracts shall use provider-neutral identity/resource/capability references.
- RBAC-IR-002: Policy/contract versions shall be explicit.
- RBAC-IR-003: Provider-specific SDK/hardware details shall remain behind adapters.

## Security requirements
- RBAC-SR-001: Protected actions shall be enforced at the execution boundary.
- RBAC-SR-002: Revocation/failure/stale-policy behavior shall fail safely according to Security Profile.
- RBAC-SR-003: Security-relevant decisions and failures shall be auditable.

## Reliability requirements
- RBAC-RR-001: Backend/provider outage shall not create undefined authorization/security state.
- RBAC-RR-002: Recovery/synchronization shall preserve stable product semantics.

## Design acceptance criteria
- RBAC-AC-001: A permission on one site does not implicitly authorize another.
- RBAC-AC-002: Explicit deny precedence is deterministic.
- RBAC-AC-003: Ownership transfer removes stale inherited access.
- RBAC-AC-004: Offline authorization behavior is defined and auditable.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
