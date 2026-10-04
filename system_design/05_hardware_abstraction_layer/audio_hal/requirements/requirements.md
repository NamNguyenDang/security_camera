# Audio Adapter / HAL Requirements — Platform Baseline v2

## Functional requirements
- AUDIO_HAL-FR-001: Product Profile shall declare capability presence and selected provider.
- AUDIO_HAL-FR-002: The adapter shall expose portable capability/lifecycle semantics.
- AUDIO_HAL-FR-003: Unsupported capability shall fail deterministically.

## Interface requirements
- AUDIO_HAL-IR-001: Buffer/resource/device ownership shall be explicit where applicable.
- AUDIO_HAL-IR-002: Provider/OS-specific types shall remain behind the adapter.
- AUDIO_HAL-IR-003: Reset/error/capability mapping shall be stable.

## Security requirements
- AUDIO_HAL-SR-001: Raw privileged device operations shall not be exposed to untrusted upper layers.
- AUDIO_HAL-SR-002: Security-relevant provider faults shall be auditable.

## Reliability requirements
- AUDIO_HAL-RR-001: Provider/device failure shall map to stable product-level status.
- AUDIO_HAL-RR-002: Optional capability absence shall be a supported state.

## Design acceptance criteria
- AUDIO_HAL-AC-001: A no-audio camera profile omits this adapter.
- AUDIO_HAL-AC-002: Changing camera audio supplier does not change upper media contracts.
- AUDIO_HAL-AC-003: Buffer overrun/underrun maps to stable status.
- AUDIO_HAL-AC-004: Client audio implementation is not constrained by camera Audio HAL.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
