# Middleware-to-Adapter Contract Catalogue Requirements — Platform Baseline v2

## Functional requirements
- MIDDLEWARE_CONTRACT-FR-001: Communication semantics shall be defined independently of selected transport/process implementation.
- MIDDLEWARE_CONTRACT-FR-002: Product Profile shall select deployment/transport/channel behavior where configurable.
- MIDDLEWARE_CONTRACT-FR-003: Unsupported/unavailable endpoint or channel shall fail deterministically.

## Interface requirements
- MIDDLEWARE_CONTRACT-IR-001: Contracts shall be versioned.
- MIDDLEWARE_CONTRACT-IR-002: Ownership, lifecycle, errors, and delivery semantics shall be explicit.
- MIDDLEWARE_CONTRACT-IR-003: Provider/transport-specific implementation details shall not define product semantics.

## Security requirements
- MIDDLEWARE_CONTRACT-SR-001: Identity/authorization/integrity context shall cross boundaries where required.
- MIDDLEWARE_CONTRACT-SR-002: Security-relevant communication failures shall be auditable.
- MIDDLEWARE_CONTRACT-SR-003: Transport selection shall not weaken mandatory protection.

## Reliability requirements
- MIDDLEWARE_CONTRACT-RR-001: Timeout/backpressure/recovery/unavailable behavior shall be bounded and documented.
- MIDDLEWARE_CONTRACT-RR-002: Compatibility mismatch shall be detected before unsafe exchange.

## Design acceptance criteria
- MIDDLEWARE_CONTRACT-AC-001: Each middleware dependency maps to a named contract rather than 'the bus'.
- MIDDLEWARE_CONTRACT-AC-002: Ordinary database/filesystem/network operations use appropriate platform abstractions.
- MIDDLEWARE_CONTRACT-AC-003: Process boundary choices are documented separately from contract semantics.
- MIDDLEWARE_CONTRACT-AC-004: Provider replacement can be qualified per adapter contract.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
