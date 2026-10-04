# Platform Storage Adapter / HAL Requirements — Platform Baseline v2

## Functional requirements
- STORAGE_HAL-FR-001: Product Profile shall declare capability presence and selected provider.
- STORAGE_HAL-FR-002: The adapter shall expose portable capability/lifecycle semantics.
- STORAGE_HAL-FR-003: Unsupported capability shall fail deterministically.

## Interface requirements
- STORAGE_HAL-IR-001: Buffer/resource/device ownership shall be explicit where applicable.
- STORAGE_HAL-IR-002: Provider/OS-specific types shall remain behind the adapter.
- STORAGE_HAL-IR-003: Reset/error/capability mapping shall be stable.

## Security requirements
- STORAGE_HAL-SR-001: Raw privileged device operations shall not be exposed to untrusted upper layers.
- STORAGE_HAL-SR-002: Security-relevant provider faults shall be auditable.

## Reliability requirements
- STORAGE_HAL-RR-001: Provider/device failure shall map to stable product-level status.
- STORAGE_HAL-RR-002: Optional capability absence shall be a supported state.

## Design acceptance criteria
- STORAGE_HAL-AC-001: Recording Service does not depend on raw block/storage handles.
- STORAGE_HAL-AC-002: Platform storage provider can change without changing recording identity semantics.
- STORAGE_HAL-AC-003: Power-loss durability capability is explicitly reported.
- STORAGE_HAL-AC-004: Health/error status maps to stable upper-layer states.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
