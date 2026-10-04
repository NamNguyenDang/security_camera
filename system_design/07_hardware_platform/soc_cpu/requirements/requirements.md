# SoC / CPU Platform Target Requirements — Platform Baseline v2

## Functional requirements
- SOC_CPU-FR-001: Product Profile shall declare whether the capability is required or optional.
- SOC_CPU-FR-002: Hardware shall satisfy documented measurable qualification constraints.
- SOC_CPU-FR-003: Unsupported capability shall be detected before product release/use.

## Interface requirements
- SOC_CPU-IR-001: Upper product contracts shall not expose supplier-specific hardware interfaces.
- SOC_CPU-IR-002: Compatible OS/driver/runtime versions shall be recorded in the Product Profile.
- SOC_CPU-IR-003: Capability/status exposed upward shall be provider-neutral.

## Security requirements
- SOC_CPU-SR-001: Required trust/isolation capabilities shall satisfy the selected security profile.
- SOC_CPU-SR-002: Security-relevant hardware faults shall be auditable.

## Reliability requirements
- SOC_CPU-RR-001: Reset/thermal/power/failure behavior shall be specified.
- SOC_CPU-RR-002: Optional capability absence shall follow profile fallback/unavailable behavior.

## Design acceptance criteria
- SOC_CPU-AC-001: A new qualified SoC can run the same shared product contracts.
- SOC_CPU-AC-002: Insufficient compute/memory capability fails qualification before release.
- SOC_CPU-AC-003: OS/toolchain compatibility is recorded independently from product logic.
- SOC_CPU-AC-004: Thermal/power limits have profile-defined operating envelopes.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
