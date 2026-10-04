# Device Provisioning Requirements — Platform Baseline v2

## Functional requirements
- DEVICE_PROVISIONING-FR-001: Product/Security Profile shall declare required capability/transport and placement.
- DEVICE_PROVISIONING-FR-002: Portable semantics shall remain independent of selected provider/transport.
- DEVICE_PROVISIONING-FR-003: Invalid or unsupported state/capability/version shall fail deterministically.

## Interface requirements
- DEVICE_PROVISIONING-IR-001: Portable contracts shall be versioned.
- DEVICE_PROVISIONING-IR-002: Provider/transport-specific details shall remain behind adapters.
- DEVICE_PROVISIONING-IR-003: Identity/ownership/error semantics shall be explicit where applicable.

## Security requirements
- DEVICE_PROVISIONING-SR-001: Protected operations/transitions shall require approved authorization/trust.
- DEVICE_PROVISIONING-SR-002: Security-relevant state/failures shall be auditable.
- DEVICE_PROVISIONING-SR-003: Provider/transport choice shall not weaken mandatory security obligations.

## Reliability requirements
- DEVICE_PROVISIONING-RR-001: Provider/transport interruption shall have defined recovery/failure behavior.
- DEVICE_PROVISIONING-RR-002: Compatibility mismatch shall be detected before unsafe operation.

## Design acceptance criteria
- DEVICE_PROVISIONING-AC-001: Interrupted provisioning cannot leave an ambiguously owned device.
- DEVICE_PROVISIONING-AC-002: Duplicate/cloned identity is detected before trusted enrollment.
- DEVICE_PROVISIONING-AC-003: Ownership transfer changes authorization without silently replacing device identity.
- DEVICE_PROVISIONING-AC-004: Decommissioned device cannot rejoin using retired credentials.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
