# Database Adapter Requirements — Platform Baseline v2

## Functional requirements
- DATABASE-FR-001: The adapter shall preserve portable product semantics across qualified providers.
- DATABASE-FR-002: Product Profile shall select compatible provider capabilities and versions.
- DATABASE-FR-003: Unsupported capability shall return deterministic status.

## Interface requirements
- DATABASE-IR-001: Provider-specific types shall not escape the adapter boundary.
- DATABASE-IR-002: Ownership, lifecycle, error, and compatibility semantics shall be documented.
- DATABASE-IR-003: Replacement providers shall satisfy the same conformance scenarios.

## Security requirements
- DATABASE-SR-001: Protected operations/data shall use approved security policy and key/identity references.
- DATABASE-SR-002: Security-relevant provider failures shall be auditable.

## Reliability requirements
- DATABASE-RR-001: Provider initialization/runtime failure shall map to stable status.
- DATABASE-RR-002: Recovery/fallback shall follow Product Profile.

## Design acceptance criteria
- DATABASE-AC-001: A database engine can be replaced without changing repository query semantics.
- DATABASE-AC-002: Migration failure leaves a defined recoverable state.
- DATABASE-AC-003: Local and backend adapters satisfy the same repository acceptance scenarios.
- DATABASE-AC-004: Requirement IDs use DATABASE prefix semantics.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
