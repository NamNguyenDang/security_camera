# Service Contract Boundary Requirements — Platform Baseline v2

## Functional requirements
- SERVICE_CONTRACT-FR-001: Communication semantics shall be defined independently of selected transport/process implementation.
- SERVICE_CONTRACT-FR-002: Product Profile shall select deployment/transport/channel behavior where configurable.
- SERVICE_CONTRACT-FR-003: Unsupported/unavailable endpoint or channel shall fail deterministically.

## Interface requirements
- SERVICE_CONTRACT-IR-001: Contracts shall be versioned.
- SERVICE_CONTRACT-IR-002: Ownership, lifecycle, errors, and delivery semantics shall be explicit.
- SERVICE_CONTRACT-IR-003: Provider/transport-specific implementation details shall not define product semantics.

## Security requirements
- SERVICE_CONTRACT-SR-001: Identity/authorization/integrity context shall cross boundaries where required.
- SERVICE_CONTRACT-SR-002: Security-relevant communication failures shall be auditable.
- SERVICE_CONTRACT-SR-003: Transport selection shall not weaken mandatory protection.

## Reliability requirements
- SERVICE_CONTRACT-RR-001: Timeout/backpressure/recovery/unavailable behavior shall be bounded and documented.
- SERVICE_CONTRACT-RR-002: Compatibility mismatch shall be detected before unsafe exchange.

## Design acceptance criteria
- SERVICE_CONTRACT-AC-001: A service can move process/deployment without changing portable service semantics.
- SERVICE_CONTRACT-AC-002: No universal bus implementation is required.
- SERVICE_CONTRACT-AC-003: Unavailable service returns defined status/timeouts.
- SERVICE_CONTRACT-AC-004: Transport changes preserve authorization and compatibility semantics.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
