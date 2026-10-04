# Platform Storage Adapter / HAL Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera platform adapter**

## Purpose and ownership
Limit this component to platform storage access/control and health, separate from filesystem semantics and recording/metadata persistence.

## Portable contract
PlatformStorage contract with durability capability, health, power-loss/error semantics, lifecycle, and approved low-level operations.

## Relationship overview
![Platform Storage Adapter / HAL relationship](./storage_hal_relationship.svg)

## Review-driven decisions
- Recording Repository owns recording semantics.
- Metadata Repository owns structured data semantics.
- Filesystem/OS storage services may satisfy most operations.
- Raw storage is never exposed to applications.
- Power-loss and health capabilities are explicit.

## Product Profile inputs
- capability present/absent;
- selected provider and compatible version;
- performance/resource/power constraints;
- recovery and security profile.

## Supplier qualification
Provider replacement is qualified against ownership, lifecycle, timing/durability, reset/error, and capability scenarios.

## Security
- raw device/provider controls are not exposed to applications;
- access is mediated by owning platform/service boundaries;
- security-relevant failures are auditable.

## Open decisions
- selected OS/vendor provider;
- numerical capability and recovery constraints.

## Design acceptance criteria
1. Recording Service does not depend on raw block/storage handles.
2. Platform storage provider can change without changing recording identity semantics.
3. Power-loss durability capability is explicitly reported.
4. Health/error status maps to stable upper-layer states.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and supplier-replacement review feedback.
