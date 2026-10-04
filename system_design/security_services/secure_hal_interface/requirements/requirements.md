# Secure Hardware Access Boundary Requirements — Platform Baseline v2

## Functional requirements
- SECURE_HAL-FR-001: Security Profile shall declare required capabilities and enforcement/isolation mechanism.
- SECURE_HAL-FR-002: Protection semantics shall remain stable across qualified provider/OS implementations.
- SECURE_HAL-FR-003: Unsupported required capability shall have explicit release/failure behavior.

## Interface requirements
- SECURE_HAL-IR-001: Trust/isolation boundaries shall be documented explicitly.
- SECURE_HAL-IR-002: Provider/OS-specific controls shall remain behind platform security adapters.
- SECURE_HAL-IR-003: Evidence/state exposed upward shall be provider-neutral where possible.

## Security requirements
- SECURE_HAL-SR-001: Required protected operations shall be enforced by an actual isolation boundary.
- SECURE_HAL-SR-002: Required boot/hardening/security failures shall fail safely.
- SECURE_HAL-SR-003: Security-relevant state and failures shall be auditable/evidenced.

## Reliability requirements
- SECURE_HAL-RR-001: Provider/measurement/control unavailability shall have defined behavior.
- SECURE_HAL-RR-002: Recovery/rollback/reset behavior shall be explicit where applicable.

## Design acceptance criteria
- SECURE_HAL-AC-001: A deployment states its actual isolation mechanism.
- SECURE_HAL-AC-002: Unauthorized caller cannot invoke protected operation even if it can link to a library.
- SECURE_HAL-AC-003: Invalid input is rejected before trusted operation.
- SECURE_HAL-AC-004: Changing secure-hardware provider does not alter caller-facing authorization semantics.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
