# Local Display Adapter / HAL Requirements — Platform Baseline v2

## Functional requirements
- DISPLAY_HAL-FR-001: Product Profile shall declare capability presence and selected provider.
- DISPLAY_HAL-FR-002: The adapter shall expose portable capability/lifecycle semantics.
- DISPLAY_HAL-FR-003: Unsupported capability shall fail deterministically.

## Interface requirements
- DISPLAY_HAL-IR-001: Buffer/resource/device ownership shall be explicit where applicable.
- DISPLAY_HAL-IR-002: Provider/OS-specific types shall remain behind the adapter.
- DISPLAY_HAL-IR-003: Reset/error/capability mapping shall be stable.

## Security requirements
- DISPLAY_HAL-SR-001: Raw privileged device operations shall not be exposed to untrusted upper layers.
- DISPLAY_HAL-SR-002: Security-relevant provider faults shall be auditable.

## Reliability requirements
- DISPLAY_HAL-RR-001: Provider/device failure shall map to stable product-level status.
- DISPLAY_HAL-RR-002: Optional capability absence shall be a supported state.

## Design acceptance criteria
- DISPLAY_HAL-AC-001: Headless camera has no display dependency.
- DISPLAY_HAL-AC-002: Changing local graphics/display backend does not alter camera product services.
- DISPLAY_HAL-AC-003: Client presentation remains independent of camera Display HAL.
- DISPLAY_HAL-AC-004: Surface/buffer lifecycle has no ambiguous ownership.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
