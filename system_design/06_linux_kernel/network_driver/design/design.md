# Network Driver / Platform Integration Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera OS/board network integration**

## Purpose and ownership
Scope to the selected operating-system/board network implementation, separate from portable connectivity and transport-security policy.

## Integration contract
Platform network-driver guarantees for link state, reset, resource pressure, capability reporting, and stable errors beneath Network Interface/Service contracts.

## Relationship overview
![Network Driver / Platform Integration relationship](./network_driver_relationship.svg)

## Review-driven decisions
- Driver-specific controls are not exposed to product services.
- Overlap with Wi-Fi/Bluetooth integration is explicitly split.
- Link/reset/resource-error behavior is stable.
- Portable sockets/connectivity remain above the driver.
- Requirement IDs use NETWORK_DRIVER prefix.

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
1. Network Service does not depend on driver-specific APIs.
2. Link/reset failure maps to stable connectivity state.
3. Ethernet driver can change without cloud/media protocol changes.
4. Wi-Fi/Bluetooth-specific radio lifecycle remains in its own integration.

## Changelog
- 2026-10-04: Re-scoped as OS/vendor integration for Platform Architecture Baseline v2.
