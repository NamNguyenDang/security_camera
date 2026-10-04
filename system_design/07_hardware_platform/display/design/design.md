# Local Display Hardware Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Optional camera-local display hardware only**

## Purpose and ownership
Retain only for product profiles with a camera-local display; remote client screens are a separate deployment concern.

## Qualification contract
Display hardware qualification constraints for modes, interfaces, lifecycle/power behavior, reset, and compatibility with the Local Display Adapter.

## Relationship overview
![Local Display Hardware relationship](./display_relationship.svg)

## Review-driven decisions
- Headless cameras omit display hardware.
- Client screens are not camera hardware.
- Required modes and power/lifecycle behavior are explicit.
- Display supplier is qualified behind Display Adapter.
- Failure/reset behavior is measurable.

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
1. Headless profile has no display hardware dependency.
2. Replacement panel/display preserves required local modes after qualification.
3. Power/reset behavior satisfies declared profile.
4. Requirement IDs use globally unique DISPLAY_HW semantics via DISPLAY component prefix.

## Changelog
- 2026-10-04: Reworked as hardware qualification design for Platform Architecture Baseline v2.
