# Network Interface Adapter / HAL Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera platform adapter only where vendor-specific interface control is required**

## Purpose and ownership
Separate vendor-specific interface controls from portable sockets/connectivity and from cloud/provider integration.

## Integration contract
NetworkInterfaceControl contract for hardware capabilities, link/radio state, reset, power, and stable hardware errors.

## Relationship overview
![Network Interface Adapter / HAL relationship](./network_hal_relationship.svg)

## Review-driven decisions
- Network Service owns portable connectivity semantics.
- Ordinary socket/network operations use OS networking facilities where appropriate.
- Cloud integration is separate.
- Vendor-specific controls are exposed only when required.
- Capability/state/reset/error ownership is explicit.

## Product Profile inputs
- selected OS/vendor/board target;
- capability requirement or optionality;
- compatible driver/firmware version;
- reset, resource, security, and performance constraints.

## Qualification
Platform integration is qualified against the portable contract above it. Supplier/upstream drivers are preferred where they satisfy the required guarantees.

## Security
- privileged/raw device access remains below OS/platform isolation;
- required firmware/driver authenticity follows security profile;
- security-relevant faults are auditable.

## Open decisions
- concrete OS/vendor driver selections;
- board-specific numerical timing/resource limits.

## Design acceptance criteria
1. Network Service works using standard OS networking without this adapter when vendor control is unnecessary.
2. Cloud/provider APIs do not appear in Network HAL.
3. Reset/error state maps to stable Network Service status.
4. Vendor interface replacement preserves portable connectivity behavior.

## Changelog
- 2026-10-04: Re-scoped as OS/vendor integration for Platform Architecture Baseline v2.
