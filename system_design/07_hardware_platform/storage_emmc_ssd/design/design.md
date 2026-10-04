# Storage Hardware (eMMC / SSD) Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Qualified camera storage hardware target**

## Purpose and ownership
Define measurable physical-storage durability, endurance, capacity, health, and power-loss guarantees while leaving recording recovery/backup policy above the hardware layer.

## Qualification contract
Storage hardware qualification constraints exposed through Platform Storage Adapter.

## Relationship overview
![Storage Hardware (eMMC / SSD) relationship](./storage_emmc_ssd_relationship.svg)

## Review-driven decisions
- Durability/endurance/capacity are measurable.
- Health reporting capability is explicit.
- Power-loss guarantees are documented.
- Recording recovery/backup policy remains above hardware.
- Adapter exposes hardware guarantees without leaking supplier-specific details.

## Product Profile inputs
- required/optional capability;
- electrical/interface compatibility;
- measurable performance/endurance/power constraints;
- compatible board/driver/adapter versions;
- security/privacy requirements where applicable.

## Hardware qualification
Supplier replacement is allowed only after qualification against the same portable upper contract and Product Profile constraints.

## Security
- hardware does not define application authorization semantics;
- trust/privacy protections are supplied by the selected security profile and upper contracts;
- hardware faults relevant to security or integrity are surfaced upward.

## Open decisions
- concrete supplier and part selections;
- numerical qualification thresholds.

## Design acceptance criteria
1. Storage device meets profile capacity/endurance targets.
2. Power-loss guarantee is documented and testable.
3. Hardware health degradation is observable through Platform Storage contract.
4. Changing storage supplier does not alter Recording Repository semantics.

## Changelog
- 2026-10-04: Reworked as hardware qualification design for Platform Architecture Baseline v2.
