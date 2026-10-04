# NPU Driver / Platform Integration Requirements — Platform Baseline v2

## Functional requirements
- NPU_DRIVER-FR-001: Platform integration shall satisfy the portable contract required above it.
- NPU_DRIVER-FR-002: Product Profile shall select OS/vendor/board compatibility.
- NPU_DRIVER-FR-003: Unsupported hardware/capability shall be detected deterministically.

## Interface requirements
- NPU_DRIVER-IR-001: Kernel/vendor-specific interfaces shall remain below the portability boundary.
- NPU_DRIVER-IR-002: Resource ownership, reset, and stable error mapping shall be defined.
- NPU_DRIVER-IR-003: Upper product services shall not access raw device controls directly.

## Security requirements
- NPU_DRIVER-SR-001: Privileged device access shall follow OS/platform isolation policy.
- NPU_DRIVER-SR-002: Required firmware/driver trust checks shall follow security profile.
- NPU_DRIVER-SR-003: Security-relevant faults shall be auditable.

## Reliability requirements
- NPU_DRIVER-RR-001: Device/driver reset and unavailable states shall be defined.
- NPU_DRIVER-RR-002: Compatibility mismatch shall fail before unsafe operation.

## Design acceptance criteria
- NPU_DRIVER-AC-001: Product runs without NPU driver when fallback profile permits.
- NPU_DRIVER-AC-002: Changing NPU driver/vendor preserves the upper acceleration contract.
- NPU_DRIVER-AC-003: Firmware incompatibility is detected before workload execution.
- NPU_DRIVER-AC-004: Requirement IDs are globally unique using NPU_DRIVER prefix.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
