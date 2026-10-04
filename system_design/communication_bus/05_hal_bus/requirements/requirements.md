# Platform HAL / OS Integration Boundary Requirements — Platform Baseline v2

## Functional requirements
- HAL_BOUNDARY-FR-001: The boundary shall expose stable guarantees appropriate to its integration/physical role.
- HAL_BOUNDARY-FR-002: Product Profile shall declare selected OS/board/protocol/provider and compatible versions.
- HAL_BOUNDARY-FR-003: Unsupported/incompatible configuration shall fail qualification or initialization deterministically.

## Interface requirements
- HAL_BOUNDARY-IR-001: Upper product contracts shall not expose raw driver/register/electrical implementation details.
- HAL_BOUNDARY-IR-002: Ownership of reset, errors, lifecycle, and capability translation shall be explicit.
- HAL_BOUNDARY-IR-003: Physical protocol and software service semantics shall not be conflated.

## Security requirements
- HAL_BOUNDARY-SR-001: Security assumptions and isolation ownership shall be documented.
- HAL_BOUNDARY-SR-002: Mandatory protection shall be enforced by actual security boundaries, not fictional bus features.
- HAL_BOUNDARY-SR-003: Security-relevant faults shall be surfaced for audit/recovery where applicable.

## Reliability requirements
- HAL_BOUNDARY-RR-001: Reset/power/error behavior shall be documented and testable.
- HAL_BOUNDARY-RR-002: Replacement platform/board implementation shall preserve portable upper guarantees after qualification.

## Design acceptance criteria
- HAL_BOUNDARY-AC-001: A non-Linux platform can implement the same portable hardware contracts.
- HAL_BOUNDARY-AC-002: No separately deployed HAL bus is required by default.
- HAL_BOUNDARY-AC-003: Driver/HAL error translation has one owner.
- HAL_BOUNDARY-AC-004: Incompatible capability/version fails before operation.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
