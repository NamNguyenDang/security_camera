# Physical Interconnect Qualification Requirements — Platform Baseline v2

## Functional requirements
- HW_BUS-FR-001: The boundary shall expose stable guarantees appropriate to its integration/physical role.
- HW_BUS-FR-002: Product Profile shall declare selected OS/board/protocol/provider and compatible versions.
- HW_BUS-FR-003: Unsupported/incompatible configuration shall fail qualification or initialization deterministically.

## Interface requirements
- HW_BUS-IR-001: Upper product contracts shall not expose raw driver/register/electrical implementation details.
- HW_BUS-IR-002: Ownership of reset, errors, lifecycle, and capability translation shall be explicit.
- HW_BUS-IR-003: Physical protocol and software service semantics shall not be conflated.

## Security requirements
- HW_BUS-SR-001: Security assumptions and isolation ownership shall be documented.
- HW_BUS-SR-002: Mandatory protection shall be enforced by actual security boundaries, not fictional bus features.
- HW_BUS-SR-003: Security-relevant faults shall be surfaced for audit/recovery where applicable.

## Reliability requirements
- HW_BUS-RR-001: Reset/power/error behavior shall be documented and testable.
- HW_BUS-RR-002: Replacement platform/board implementation shall preserve portable upper guarantees after qualification.

## Design acceptance criteria
- HW_BUS-AC-001: Board qualification names actual protocols used.
- HW_BUS-AC-002: Timing/electrical limits are testable.
- HW_BUS-AC-003: Hardware interconnect has no fake software authorization/version API.
- HW_BUS-AC-004: Requirement IDs use HW_BUS prefix.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
