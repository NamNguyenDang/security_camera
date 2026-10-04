# Hardware Root of Trust Requirements — Platform Baseline v2

## Functional requirements
- HARDWARE_ROOT_OF_TRUST-FR-001: Product/Security Profile shall declare required capability/transport and placement.
- HARDWARE_ROOT_OF_TRUST-FR-002: Portable semantics shall remain independent of selected provider/transport.
- HARDWARE_ROOT_OF_TRUST-FR-003: Invalid or unsupported state/capability/version shall fail deterministically.

## Interface requirements
- HARDWARE_ROOT_OF_TRUST-IR-001: Portable contracts shall be versioned.
- HARDWARE_ROOT_OF_TRUST-IR-002: Provider/transport-specific details shall remain behind adapters.
- HARDWARE_ROOT_OF_TRUST-IR-003: Identity/ownership/error semantics shall be explicit where applicable.

## Security requirements
- HARDWARE_ROOT_OF_TRUST-SR-001: Protected operations/transitions shall require approved authorization/trust.
- HARDWARE_ROOT_OF_TRUST-SR-002: Security-relevant state/failures shall be auditable.
- HARDWARE_ROOT_OF_TRUST-SR-003: Provider/transport choice shall not weaken mandatory security obligations.

## Reliability requirements
- HARDWARE_ROOT_OF_TRUST-RR-001: Provider/transport interruption shall have defined recovery/failure behavior.
- HARDWARE_ROOT_OF_TRUST-RR-002: Compatibility mismatch shall be detected before unsafe operation.

## Design acceptance criteria
- HARDWARE_ROOT_OF_TRUST-AC-001: Provider lacking attestation can qualify for a profile that does not require attestation.
- HARDWARE_ROOT_OF_TRUST-AC-002: Required protected-key/boot-anchor guarantees are verified.
- HARDWARE_ROOT_OF_TRUST-AC-003: Provider replacement does not alter upper security-service contracts.
- HARDWARE_ROOT_OF_TRUST-AC-004: Provider failure produces explicit safe degradation/failure.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
