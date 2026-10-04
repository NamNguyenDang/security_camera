# Secrets / Key Management Requirements — Platform Baseline v2

## Functional requirements
- KEY_MANAGEMENT-FR-001: The security service shall preserve mandatory product protection semantics independently of provider choice.
- KEY_MANAGEMENT-FR-002: Security Profile shall declare placement, lifecycle, and recovery/retention behavior.
- KEY_MANAGEMENT-FR-003: Offline/unavailable-provider behavior shall be explicit.

## Interface requirements
- KEY_MANAGEMENT-IR-001: Portable contracts shall use provider-neutral references and schemas.
- KEY_MANAGEMENT-IR-002: Raw provider/hardware-specific secrets or implementation types shall not escape the security boundary.
- KEY_MANAGEMENT-IR-003: Contract/schema versions shall be explicit.

## Security requirements
- KEY_MANAGEMENT-SR-001: Protected operations/data shall follow purpose/scope/authorization policy.
- KEY_MANAGEMENT-SR-002: Required protection/integrity/audit obligations shall fail safely when unavailable.
- KEY_MANAGEMENT-SR-003: Security-relevant failures shall themselves be auditable where possible.

## Reliability requirements
- KEY_MANAGEMENT-RR-001: Provider/storage/hardware failure shall have defined recovery/degradation behavior.
- KEY_MANAGEMENT-RR-002: Bounded buffering/retention/resource behavior shall be defined.

## Design acceptance criteria
- KEY_MANAGEMENT-AC-001: Recording key cannot be substituted for device identity key purpose.
- KEY_MANAGEMENT-AC-002: Non-exportable key never appears in application memory when profile forbids export.
- KEY_MANAGEMENT-AC-003: Revoked key cannot be used after defined enforcement boundary.
- KEY_MANAGEMENT-AC-004: Hardware replacement/recovery follows documented ownership and recovery policy.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
