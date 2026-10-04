# Power Management / Platform Integration Requirements — Platform Baseline v2

## Functional requirements
- POWER_MANAGEMENT-FR-001: Product Profile shall declare whether the capability is required or optional.
- POWER_MANAGEMENT-FR-002: Hardware shall satisfy documented measurable qualification constraints.
- POWER_MANAGEMENT-FR-003: Unsupported capability shall be detected before product release/use.

## Interface requirements
- POWER_MANAGEMENT-IR-001: Upper product contracts shall not expose supplier-specific hardware interfaces.
- POWER_MANAGEMENT-IR-002: Compatible OS/driver/runtime versions shall be recorded in the Product Profile.
- POWER_MANAGEMENT-IR-003: Capability/status exposed upward shall be provider-neutral.

## Security requirements
- POWER_MANAGEMENT-SR-001: Required trust/isolation capabilities shall satisfy the selected security profile.
- POWER_MANAGEMENT-SR-002: Security-relevant hardware faults shall be auditable.

## Reliability requirements
- POWER_MANAGEMENT-RR-001: Reset/thermal/power/failure behavior shall be specified.
- POWER_MANAGEMENT-RR-002: Optional capability absence shall follow profile fallback/unavailable behavior.

## Design acceptance criteria
- POWER_MANAGEMENT-AC-001: Power transition is blocked/deferred when recording durability requirements are not met.
- POWER_MANAGEMENT-AC-002: Resume restores required service state deterministically.
- POWER_MANAGEMENT-AC-003: Thermal constraint maps to profile-defined degradation.
- POWER_MANAGEMENT-AC-004: Requirement IDs use globally unique POWER_MANAGEMENT prefix.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
