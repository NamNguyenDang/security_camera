# Camera Capture Adapter / HAL Requirements — Platform Baseline v2

## Functional requirements
- CAMERA_HAL-FR-001: The adapter shall expose portable capability and lifecycle semantics independent of selected supplier.
- CAMERA_HAL-FR-002: Product Profile shall select provider/version and capability presence.
- CAMERA_HAL-FR-003: Unsupported capability shall be reported before use.

## Interface requirements
- CAMERA_HAL-IR-001: Buffer/resource ownership and lifecycle shall be explicit.
- CAMERA_HAL-IR-002: Vendor/driver-specific types shall not escape the adapter.
- CAMERA_HAL-IR-003: Cancellation, timeout, reset, and stable error mapping shall be defined.

## Security requirements
- CAMERA_HAL-SR-001: Boundary inputs shall be validated before provider execution.
- CAMERA_HAL-SR-002: Security-relevant faults shall be auditable.

## Reliability requirements
- CAMERA_HAL-RR-001: Provider reset/unavailability shall map to stable product-level status.
- CAMERA_HAL-RR-002: Optional adapter absence shall follow Product Profile fallback/unavailable policy.

## Design acceptance criteria
- CAMERA_HAL-AC-001: A new sensor/vendor capture adapter can replace the existing one without Camera Service changes.
- CAMERA_HAL-AC-002: Frame ownership has defined acquire/release semantics.
- CAMERA_HAL-AC-003: Unsupported mode is rejected through capability negotiation.
- CAMERA_HAL-AC-004: Reset/cancellation returns stable portable status.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
