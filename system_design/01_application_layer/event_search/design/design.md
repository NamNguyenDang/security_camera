# Event Search Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Client + Camera/Gateway/Backend repositories selected by Product Profile**

## Purpose and ownership
Provide a product-owned event query contract independent of database engine and repository placement.

## Product-owned contract
EventQuery contract with scoped filters, stable event identity, stable recording references, pagination, and time semantics.

## Relationship overview
![Event Search relationship](./event_search_relationship.svg)

## Interaction model
- Commands use stable product contracts.
- State and durable domain events are separate from provider APIs.
- Deployment transport is selected by Product Profile.
- Provider and operating-system details remain behind adapters.

## Review-driven design decisions
- Search is independent of local database APIs.
- Scope includes customer/site/area/device permissions.
- Pagination and time-zone/timestamp semantics are explicit.
- Stale indexes and deleted recordings have defined outcomes.
- Local camera, gateway, and cloud query deployments preserve one contract.

## Product Profile inputs
- deployment placement and optional backend/gateway;
- capability and compatible contract versions;
- provider/adapter selection;
- security and offline policy.

## Security
- camera-side enforcement remains explicit for standalone operation;
- mandatory security policy cannot be disabled by ordinary preferences;
- protected operations are auditable.

## Decisions
- Shared product behavior is provider independent.
- Optional capabilities are profile-selected.
- No private `src/` dependency is a product contract.

## Open decisions
- exact provider/transport selections;
- profile-specific limits and retention/version policies.

## Design acceptance criteria
1. Database replacement does not change query semantics.
2. Permission filtering occurs before results are exposed.
3. Deleted recordings leave a stable event result with defined recording availability.
4. Pagination is deterministic for a fixed query snapshot.
5. Requirement IDs use EVENT_SEARCH prefix.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and review feedback.
