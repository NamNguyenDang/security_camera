# Location Context Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Client, Camera, Gateway, or Backend depending Product Profile and source**

## Purpose and ownership
Separate geographic location from customer/site/area/device grouping; installation grouping is a distinct product-domain contract.

## Product-owned contract
LocationContext contract with source, accuracy/freshness, privacy classification, static/dynamic mode, and relocation state.

## Relationship overview
![Location Context relationship](./location_manager_relationship.svg)

## Review-driven decisions
- Organization/site/area hierarchy is not a geographic sensor API.
- No positioning sensor is assumed.
- Static configured location is supported.
- Freshness and privacy are explicit.
- Relocation behavior and authorization are defined.

## Product Profile inputs
- capability optionality and deployment;
- provider/platform adapter;
- compatible contract version;
- privacy/security/offline behavior.

## Design rules
- optional platform capabilities do not become dependencies of the common camera core;
- portable state/contracts remain independent of native SDK types;
- headless/feature-absent products remain valid.

## Design acceptance criteria
1. A product without GPS/location hardware can use static configured location.
2. Site/area access control does not depend on coordinates.
3. Stale location is reported explicitly.
4. Changing location provider does not change product grouping semantics.

## Open decisions
- exact native/provider adapter selections;
- profile-specific capability limits.

## Changelog
- 2026-10-04: Re-scoped for Platform Architecture Baseline v2 and review feedback.
