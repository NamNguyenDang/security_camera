# Storage Driver / Platform Integration Requirements — Platform Baseline v2

## Functional requirements
- STORAGE_DRIVER-FR-001: Platform integration shall satisfy the portable contract above it.
- STORAGE_DRIVER-FR-002: Product Profile shall declare capability/device/mode support.
- STORAGE_DRIVER-FR-003: Unsupported or unavailable hardware shall be reported deterministically.

## Interface requirements
- STORAGE_DRIVER-IR-001: Driver/controller-specific types shall remain below the portability boundary.
- STORAGE_DRIVER-IR-002: Ownership, reset, and error mapping shall be documented.
- STORAGE_DRIVER-IR-003: Upper product services shall not access raw device controls directly.

## Security requirements
- STORAGE_DRIVER-SR-001: Privileged device access shall follow OS/platform security policy.
- STORAGE_DRIVER-SR-002: Security-relevant faults/attachments shall be auditable as applicable.

## Reliability requirements
- STORAGE_DRIVER-RR-001: Reset/disconnect/power-loss states shall have defined outcomes.
- STORAGE_DRIVER-RR-002: Compatibility mismatch shall fail before unsafe operation.

## Design acceptance criteria
- STORAGE_DRIVER-AC-001: Recording repository can move to another platform storage implementation without domain changes.
- STORAGE_DRIVER-AC-002: Power loss has documented persistence guarantees.
- STORAGE_DRIVER-AC-003: I/O failure and health degradation map to stable Platform Storage status.
- STORAGE_DRIVER-AC-004: Driver replacement does not alter recording object identity semantics.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
