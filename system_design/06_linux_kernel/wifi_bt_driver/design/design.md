# Wi-Fi / Bluetooth Platform Integration Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Optional camera OS/vendor radio integration**

## Purpose and ownership
Separate Wi-Fi connectivity from Bluetooth enrollment/other capabilities and clarify ownership relative to the generic Network Driver.

## Integration contract
RadioIntegration contract with supported radios, firmware lifecycle, pairing/association policy hooks, reset, capability reporting, and stable errors.

## Relationship overview
![Wi-Fi / Bluetooth Platform Integration relationship](./wifi_bt_driver_relationship.svg)

## Review-driven decisions
- Wi-Fi link operation integrates with Network Service.
- Bluetooth may be used for enrollment or other profile-selected capabilities.
- Supported radios and optionality are explicit.
- Firmware lifecycle and compatibility are qualified.
- Pairing/association policy belongs to product/security services, not raw driver logic.

## Product Profile inputs
- optionality and supported interfaces/radios/devices;
- OS/vendor/board and compatible firmware/driver versions;
- reset, resource, power, and security constraints.

## Platform qualification
The selected driver/integration must satisfy stable upper adapter/service semantics. Product code must not depend on driver-specific controls.

## Security
- privileged device access remains behind OS/platform isolation;
- radio/pairing/security policy is enforced above raw driver mechanics;
- relevant faults and state changes are auditable.

## Open decisions
- concrete driver/firmware selections;
- numerical queue/resource/reset limits.

## Design acceptance criteria
1. Ethernet-only profile omits radio integration.
2. Bluetooth can be enabled for enrollment without becoming a general network dependency.
3. Firmware mismatch is detected before unsafe use.
4. Radio reset maps to stable connectivity/enrollment state.

## Changelog
- 2026-10-04: Re-scoped as OS/vendor integration for Platform Architecture Baseline v2.
