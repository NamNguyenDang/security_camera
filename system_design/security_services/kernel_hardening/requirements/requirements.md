# Kernel / OS Hardening Requirements — Platform Baseline v2

## Functional requirements
- KERNEL_HARDENING-FR-001: Security Profile shall declare required capabilities and enforcement/isolation mechanism.
- KERNEL_HARDENING-FR-002: Protection semantics shall remain stable across qualified provider/OS implementations.
- KERNEL_HARDENING-FR-003: Unsupported required capability shall have explicit release/failure behavior.

## Interface requirements
- KERNEL_HARDENING-IR-001: Trust/isolation boundaries shall be documented explicitly.
- KERNEL_HARDENING-IR-002: Provider/OS-specific controls shall remain behind platform security adapters.
- KERNEL_HARDENING-IR-003: Evidence/state exposed upward shall be provider-neutral where possible.

## Security requirements
- KERNEL_HARDENING-SR-001: Required protected operations shall be enforced by an actual isolation boundary.
- KERNEL_HARDENING-SR-002: Required boot/hardening/security failures shall fail safely.
- KERNEL_HARDENING-SR-003: Security-relevant state and failures shall be auditable/evidenced.

## Reliability requirements
- KERNEL_HARDENING-RR-001: Provider/measurement/control unavailability shall have defined behavior.
- KERNEL_HARDENING-RR-002: Recovery/rollback/reset behavior shall be explicit where applicable.

## Design acceptance criteria
- KERNEL_HARDENING-AC-001: A non-Linux platform can satisfy the same common protection outcomes with different mechanisms.
- KERNEL_HARDENING-AC-002: Missing required hardening control blocks qualification unless approved alternative exists.
- KERNEL_HARDENING-AC-003: Configuration evidence is reviewable per product build.
- KERNEL_HARDENING-AC-004: Applications do not depend on Linux-specific hardening settings.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
