# SoC / CPU Platform Target Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Qualified hardware platform target selected by Product Profile**

## Purpose and ownership
Treat processor/board selection as a qualified target independent of shared product logic and separately from operating-system choice.

## Qualification contract
PlatformTarget qualification constraints for compute/memory, media acceleration, trust capabilities, power/thermal budgets, toolchain, and driver compatibility.

## Relationship overview
![SoC / CPU Platform Target relationship](./soc_cpu_relationship.svg)

## Review-driven decisions
- SoC selection is not embedded in product-service contracts.
- OS choice is separate.
- Required compute/memory/media capabilities are measurable.
- Trust capabilities and power/thermal budgets are explicit.
- Toolchain/driver compatibility is part of qualification.

## Product Profile inputs
- hardware capability required/optional;
- operating envelope and resource budgets;
- compatible OS/driver/runtime/toolchain;
- security and fallback policy.

## Qualification model
Hardware is selected by measurable capability and compatibility criteria. Supplier replacement is permitted after qualification while preserving upper product contracts.

## Security
- hardware trust/isolation capabilities are declared, not assumed;
- mandatory protection requirements come from the security profile;
- security-relevant hardware faults are auditable.

## Open decisions
- concrete supplier targets;
- numerical compute/thermal/power/resource thresholds.

## Design acceptance criteria
1. A new qualified SoC can run the same shared product contracts.
2. Insufficient compute/memory capability fails qualification before release.
3. OS/toolchain compatibility is recorded independently from product logic.
4. Thermal/power limits have profile-defined operating envelopes.

## Changelog
- 2026-10-04: Reworked as Product Profile / hardware qualification design for Platform Architecture Baseline v2.
