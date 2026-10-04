# USB Platform Integration Requirements — Platform Baseline v2

## Functional requirements
- USB_DRIVER-FR-001: Platform integration shall satisfy the portable contract above it.
- USB_DRIVER-FR-002: Product Profile shall declare capability/device/mode support.
- USB_DRIVER-FR-003: Unsupported or unavailable hardware shall be reported deterministically.

## Interface requirements
- USB_DRIVER-IR-001: Driver/controller-specific types shall remain below the portability boundary.
- USB_DRIVER-IR-002: Ownership, reset, and error mapping shall be documented.
- USB_DRIVER-IR-003: Upper product services shall not access raw device controls directly.

## Security requirements
- USB_DRIVER-SR-001: Privileged device access shall follow OS/platform security policy.
- USB_DRIVER-SR-002: Security-relevant faults/attachments shall be auditable as applicable.

## Reliability requirements
- USB_DRIVER-RR-001: Reset/disconnect/power-loss states shall have defined outcomes.
- USB_DRIVER-RR-002: Compatibility mismatch shall fail before unsafe operation.

## Design acceptance criteria
- USB_DRIVER-AC-001: A product with no USB peripherals omits USB-specific product dependencies.
- USB_DRIVER-AC-002: Unapproved device class is rejected or ignored per policy.
- USB_DRIVER-AC-003: Disconnect during use produces deterministic adapter state.
- USB_DRIVER-AC-004: Changing USB controller implementation does not change product peripheral contracts.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
