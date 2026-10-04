# Physical Interconnect Qualification Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Board/vendor hardware qualification only**

## Purpose and ownership
Treat physical interconnects as board/vendor qualification specifications separate from software message buses.

## Boundary contract
PhysicalInterconnect qualification for selected protocols, electrical/timing/reset constraints, error ownership, power sequencing, and security assumptions.

## Relationship overview
![Physical Interconnect Qualification relationship](./hardware_bus_relationship.svg)

## Review-driven decisions
- Protocols are product/board selected, not generic software buses.
- Electrical and timing constraints are explicit.
- Reset/power sequencing is explicit.
- Error ownership between device/driver/platform is assigned.
- Security assumptions are documented without pretending hardware bus implements authorization/version negotiation.

## Product Profile inputs
- selected OS/board/protocol/provider;
- compatible versions/capabilities;
- reset/power/error ownership;
- security and qualification constraints.

## Boundary rule
Implementation and physical boundaries expose stable guarantees upward but are not modeled as mandatory product services unless a concrete deployment requires one.

## Open decisions
- concrete OS/board/protocol selections;
- numerical electrical/timing/reset limits.

## Design acceptance criteria
1. Board qualification names actual protocols used.
2. Timing/electrical limits are testable.
3. Hardware interconnect has no fake software authorization/version API.
4. Requirement IDs use HW_BUS prefix.

## Changelog
- 2026-10-04: Re-scoped from generic bus model to Platform Architecture Baseline v2 boundary/qualification model.
