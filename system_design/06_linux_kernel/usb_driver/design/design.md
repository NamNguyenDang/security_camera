# USB Platform Integration Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Optional OS/vendor integration selected by Product Profile**

## Purpose and ownership
Separate generic operating-system USB support from product-specific peripheral adapters and qualification.

## Integration contract
USB integration policy with permitted device classes, attach/detach lifecycle, trust/resource limits, and stable errors.

## Relationship overview
![USB Platform Integration relationship](./usb_driver_relationship.svg)

## Review-driven decisions
- USB is optional per product.
- Permitted device classes are profile-defined.
- Controller details do not escape shared product code.
- Newly attached devices are subject to trust/resource policy.
- Disconnect behavior is explicit.

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
1. A product with no USB peripherals omits USB-specific product dependencies.
2. Unapproved device class is rejected or ignored per policy.
3. Disconnect during use produces deterministic adapter state.
4. Changing USB controller implementation does not change product peripheral contracts.

## Open decisions
- selected OS/vendor driver;
- board-specific numerical limits.

## Changelog
- 2026-10-04: Re-scoped as OS/vendor integration for Platform Architecture Baseline v2.
