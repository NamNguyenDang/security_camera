# Display Driver / Platform Integration Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Optional camera-local display platform integration only**

## Purpose and ownership
Limit this driver integration to product profiles with a camera-local display; remote client displays use their own operating-system integration.

## Integration contract
Local display driver guarantees for modes, surface/buffer handoff, reset/power behavior, and stable errors beneath Display Adapter.

## Relationship overview
![Display Driver / Platform Integration relationship](./display_driver_relationship.svg)

## Review-driven decisions
- Camera-local and client displays are separate.
- Headless profiles omit the dependency.
- Graphics/display ownership and surface-buffer handling are explicit.
- Supported modes and reset behavior are qualified.
- Linux/driver details stay below portability boundary.

## Product Profile inputs
- capability optionality and permitted devices/modes;
- OS/vendor/board selection;
- compatible driver/firmware versions;
- reset, resource, power, and security limits.

## Platform qualification
The integration is qualified against the portable adapter above it. Generic OS/upstream facilities are reused when they satisfy required behavior.

## Security
- raw device access remains below OS isolation;
- attached/peripheral resources follow explicit trust/resource policy where applicable;
- security-relevant device faults are auditable.

## Design acceptance criteria
1. Headless camera builds without this integration.
2. Client rendering has no dependency on camera display driver.
3. Buffer handoff ownership is deterministic.
4. Driver reset maps to stable Display Adapter state.

## Open decisions
- selected OS/vendor driver;
- board-specific numerical limits.

## Changelog
- 2026-10-04: Re-scoped as OS/vendor integration for Platform Architecture Baseline v2.
