# Application Contract Boundary Requirements — Platform Baseline v2

## Functional requirements
- APPLICATION_CONTRACT-FR-001: Product/Security Profile shall declare required capability/transport and placement.
- APPLICATION_CONTRACT-FR-002: Portable semantics shall remain independent of selected provider/transport.
- APPLICATION_CONTRACT-FR-003: Invalid or unsupported state/capability/version shall fail deterministically.

## Interface requirements
- APPLICATION_CONTRACT-IR-001: Portable contracts shall be versioned.
- APPLICATION_CONTRACT-IR-002: Provider/transport-specific details shall remain behind adapters.
- APPLICATION_CONTRACT-IR-003: Identity/ownership/error semantics shall be explicit where applicable.

## Security requirements
- APPLICATION_CONTRACT-SR-001: Protected operations/transitions shall require approved authorization/trust.
- APPLICATION_CONTRACT-SR-002: Security-relevant state/failures shall be auditable.
- APPLICATION_CONTRACT-SR-003: Provider/transport choice shall not weaken mandatory security obligations.

## Reliability requirements
- APPLICATION_CONTRACT-RR-001: Provider/transport interruption shall have defined recovery/failure behavior.
- APPLICATION_CONTRACT-RR-002: Compatibility mismatch shall be detected before unsafe operation.

## Design acceptance criteria
- APPLICATION_CONTRACT-AC-001: The same application contract can run in-process, over local IPC, or remotely where allowed.
- APPLICATION_CONTRACT-AC-002: Remote client does not require Binder.
- APPLICATION_CONTRACT-AC-003: Transport replacement does not change service semantics.
- APPLICATION_CONTRACT-AC-004: Incompatible contract versions fail explicitly.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
