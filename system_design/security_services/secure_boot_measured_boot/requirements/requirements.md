# Secure Boot / Measured Boot / Attestation Requirements — Platform Baseline v2

## Functional requirements
- BOOT_TRUST-FR-001: Security Profile shall declare required capabilities and enforcement/isolation mechanism.
- BOOT_TRUST-FR-002: Protection semantics shall remain stable across qualified provider/OS implementations.
- BOOT_TRUST-FR-003: Unsupported required capability shall have explicit release/failure behavior.

## Interface requirements
- BOOT_TRUST-IR-001: Trust/isolation boundaries shall be documented explicitly.
- BOOT_TRUST-IR-002: Provider/OS-specific controls shall remain behind platform security adapters.
- BOOT_TRUST-IR-003: Evidence/state exposed upward shall be provider-neutral where possible.

## Security requirements
- BOOT_TRUST-SR-001: Required protected operations shall be enforced by an actual isolation boundary.
- BOOT_TRUST-SR-002: Required boot/hardening/security failures shall fail safely.
- BOOT_TRUST-SR-003: Security-relevant state and failures shall be auditable/evidenced.

## Reliability requirements
- BOOT_TRUST-RR-001: Provider/measurement/control unavailability shall have defined behavior.
- BOOT_TRUST-RR-002: Recovery/rollback/reset behavior shall be explicit where applicable.

## Design acceptance criteria
- BOOT_TRUST-AC-001: A profile requiring only secure boot can use a provider without remote attestation.
- BOOT_TRUST-AC-002: Unauthorized firmware fails verification before activation.
- BOOT_TRUST-AC-003: Rollback/recovery follows approved signed policy.
- BOOT_TRUST-AC-004: Missing measurement evidence is surfaced rather than fabricated.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
