# Camera Sensor Hardware Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Qualified camera hardware target**

## Purpose and ownership
Define sensor qualification and integration requirements beneath the portable Capture contract.

## Qualification contract
Sensor qualification constraints for supported modes, timing, electrical compatibility, calibration/image-quality ownership, fault behavior, and board dependencies.

## Relationship overview
![Camera Sensor Hardware relationship](./camera_sensor_relationship.svg)

## Review-driven decisions
- Sensor replacement requires qualification while preserving Capture/Camera Service contracts.
- Supported modes and timing are measurable.
- Electrical/board compatibility is explicit.
- Calibration/image-quality ownership is assigned.
- Fault behavior and reset capability are declared.

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
1. Replacement sensor preserves required capture modes after qualification.
2. Unsupported electrical/timing combinations fail qualification.
3. Calibration assets/process have an explicit owner.
4. Requirement IDs use CAMERA_SENSOR prefix.

## Changelog
- 2026-10-04: Reworked as hardware qualification design for Platform Architecture Baseline v2.
