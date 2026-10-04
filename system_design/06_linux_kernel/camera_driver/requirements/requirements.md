# Camera Driver / Platform Integration Requirements — Platform Baseline v2

## Functional requirements
- CAMERA_DRIVER-FR-001: Platform integration shall satisfy the portable contract required above it.
- CAMERA_DRIVER-FR-002: Product Profile shall select OS/vendor/board compatibility.
- CAMERA_DRIVER-FR-003: Unsupported hardware/capability shall be detected deterministically.

## Interface requirements
- CAMERA_DRIVER-IR-001: Kernel/vendor-specific interfaces shall remain below the portability boundary.
- CAMERA_DRIVER-IR-002: Resource ownership, reset, and stable error mapping shall be defined.
- CAMERA_DRIVER-IR-003: Upper product services shall not access raw device controls directly.

## Security requirements
- CAMERA_DRIVER-SR-001: Privileged device access shall follow OS/platform isolation policy.
- CAMERA_DRIVER-SR-002: Required firmware/driver trust checks shall follow security profile.
- CAMERA_DRIVER-SR-003: Security-relevant faults shall be auditable.

## Reliability requirements
- CAMERA_DRIVER-RR-001: Device/driver reset and unavailable states shall be defined.
- CAMERA_DRIVER-RR-002: Compatibility mismatch shall fail before unsafe operation.

## Design acceptance criteria
- CAMERA_DRIVER-AC-001: Supplier/upstream driver can be used without changing Camera Service.
- CAMERA_DRIVER-AC-002: Board/sensor qualification proves all required capture modes.
- CAMERA_DRIVER-AC-003: Reset recovers according to defined platform behavior.
- CAMERA_DRIVER-AC-004: Driver-specific handles never escape the platform adapter boundary.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
