# Device Management Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera product service + optional Gateway/Backend fleet-management modules**

## Purpose and ownership
Separate device-local lifecycle control from backend fleet registration, customer ownership, provisioning, and update orchestration while keeping shared product contracts.

## Product-owned contract
DeviceLifecycle + DesiredReportedState + Ownership/Enrollment contracts with explicit reconciliation.

## Relationship overview
![Device Management relationship](./device_management_relationship.svg)

## Review-driven decisions
- Local lifecycle state remains on the camera.
- Backend fleet state is optional and separately deployed.
- Desired and reported configuration are distinct.
- Ownership transfer, retirement, and decommissioning are explicit states.
- Offline reconciliation is deterministic.
- Product Profile declares required adapters and security decisions.

## Product Profile inputs
- placement, repository/provider selections, and contract versions;
- offline behavior and recovery policy;
- durability/reconnect/reconciliation budgets;
- security profile.

## Security
- standalone camera keeps required local identity/authorization enforcement;
- provider credentials and keys are referenced through security services;
- management/storage/network changes are auditable.

## Decisions
- cloud and local implementations are peers behind product contracts, not different product semantics;
- platform/physical health is separated from domain persistence and orchestration.

## Open decisions
- exact repository/cloud providers;
- numerical durability, retry, and reconciliation budgets.

## Design acceptance criteria
1. Standalone camera can manage its local lifecycle without backend.
2. Desired/reported state converges predictably after offline periods.
3. Ownership transfer does not leave stale authorization.
4. Retired device behavior is explicit and auditable.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and review feedback.
