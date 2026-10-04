# Wi-Fi / Bluetooth Platform Integration Requirements — Platform Baseline v2

## Functional requirements
- WIFI_BT_DRIVER-FR-001: Platform integration shall satisfy the portable contract above it.
- WIFI_BT_DRIVER-FR-002: Product Profile shall declare supported capability and compatible driver/firmware.
- WIFI_BT_DRIVER-FR-003: Unavailable or incompatible hardware shall be reported deterministically.

## Interface requirements
- WIFI_BT_DRIVER-IR-001: Driver-specific controls/types shall not escape the platform integration boundary.
- WIFI_BT_DRIVER-IR-002: Reset, resource, timing, and stable error mapping shall be defined.
- WIFI_BT_DRIVER-IR-003: Product services shall consume portable capabilities rather than raw device APIs.

## Security requirements
- WIFI_BT_DRIVER-SR-001: Privileged device access shall follow platform security policy.
- WIFI_BT_DRIVER-SR-002: Security-relevant radio/device state changes shall be auditable where applicable.

## Reliability requirements
- WIFI_BT_DRIVER-RR-001: Reset/reconnect/restart behavior shall be defined.
- WIFI_BT_DRIVER-RR-002: Firmware/driver incompatibility shall fail safely.

## Design acceptance criteria
- WIFI_BT_DRIVER-AC-001: Ethernet-only profile omits radio integration.
- WIFI_BT_DRIVER-AC-002: Bluetooth can be enabled for enrollment without becoming a general network dependency.
- WIFI_BT_DRIVER-AC-003: Firmware mismatch is detected before unsafe use.
- WIFI_BT_DRIVER-AC-004: Radio reset maps to stable connectivity/enrollment state.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
