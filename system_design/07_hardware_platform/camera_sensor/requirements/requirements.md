# Camera Sensor Hardware Requirements — Platform Baseline v2

## Functional requirements
- CAMERA_SENSOR-FR-001: Product Profile shall declare whether the hardware capability is required or optional.
- CAMERA_SENSOR-FR-002: Hardware shall satisfy measurable qualification constraints.
- CAMERA_SENSOR-FR-003: Unsupported/incompatible hardware shall fail qualification before release.

## Interface requirements
- CAMERA_SENSOR-IR-001: Supplier-specific interfaces shall remain behind the platform adapter/driver.
- CAMERA_SENSOR-IR-002: Capability and health/status exposed upward shall be provider-neutral.
- CAMERA_SENSOR-IR-003: Compatible board/driver/adapter versions shall be recorded.

## Security requirements
- CAMERA_SENSOR-SR-001: Hardware security/privacy obligations shall follow the selected security profile.
- CAMERA_SENSOR-SR-002: Relevant integrity/security faults shall be surfaced for audit/recovery.

## Reliability requirements
- CAMERA_SENSOR-RR-001: Reset/power-loss/fault behavior shall be documented and testable.
- CAMERA_SENSOR-RR-002: Replacement hardware shall preserve the upper portable contract after qualification.

## Design acceptance criteria
- CAMERA_SENSOR-AC-001: Replacement sensor preserves required capture modes after qualification.
- CAMERA_SENSOR-AC-002: Unsupported electrical/timing combinations fail qualification.
- CAMERA_SENSOR-AC-003: Calibration assets/process have an explicit owner.
- CAMERA_SENSOR-AC-004: Requirement IDs use CAMERA_SENSOR prefix.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
