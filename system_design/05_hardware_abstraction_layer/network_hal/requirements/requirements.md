# Network Interface Adapter / HAL Requirements — Platform Baseline v2

## Functional requirements
- NETWORK_HAL-FR-001: Platform integration shall satisfy the portable contract required above it.
- NETWORK_HAL-FR-002: Product Profile shall select OS/vendor/board compatibility.
- NETWORK_HAL-FR-003: Unsupported hardware/capability shall be detected deterministically.

## Interface requirements
- NETWORK_HAL-IR-001: Kernel/vendor-specific interfaces shall remain below the portability boundary.
- NETWORK_HAL-IR-002: Resource ownership, reset, and stable error mapping shall be defined.
- NETWORK_HAL-IR-003: Upper product services shall not access raw device controls directly.

## Security requirements
- NETWORK_HAL-SR-001: Privileged device access shall follow OS/platform isolation policy.
- NETWORK_HAL-SR-002: Required firmware/driver trust checks shall follow security profile.
- NETWORK_HAL-SR-003: Security-relevant faults shall be auditable.

## Reliability requirements
- NETWORK_HAL-RR-001: Device/driver reset and unavailable states shall be defined.
- NETWORK_HAL-RR-002: Compatibility mismatch shall fail before unsafe operation.

## Design acceptance criteria
- NETWORK_HAL-AC-001: Network Service works using standard OS networking without this adapter when vendor control is unnecessary.
- NETWORK_HAL-AC-002: Cloud/provider APIs do not appear in Network HAL.
- NETWORK_HAL-AC-003: Reset/error state maps to stable Network Service status.
- NETWORK_HAL-AC-004: Vendor interface replacement preserves portable connectivity behavior.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
