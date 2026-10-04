# Location Context Requirements — Platform Baseline v2

## Functional requirements
- LOCATION_MANAGER-FR-001: Product Profile shall explicitly declare capability availability.
- LOCATION_MANAGER-FR-002: Capability absence shall have supported deterministic behavior.
- LOCATION_MANAGER-FR-003: Portable behavior shall remain independent of selected native/provider implementation.

## Interface requirements
- LOCATION_MANAGER-IR-001: Expose a versioned portable contract.
- LOCATION_MANAGER-IR-002: Keep native/provider-specific types behind adapters.

## Security requirements
- LOCATION_MANAGER-SR-001: Access to sensitive capability/data shall follow approved authorization/privacy policy.
- LOCATION_MANAGER-SR-002: Security-relevant changes and failures shall be auditable where applicable.

## Reliability requirements
- LOCATION_MANAGER-RR-001: Provider/device absence or loss shall map to stable product-level state.
- LOCATION_MANAGER-RR-002: Recovery behavior shall be bounded by Product Profile.

## Design acceptance criteria
- LOCATION_MANAGER-AC-001: A product without GPS/location hardware can use static configured location.
- LOCATION_MANAGER-AC-002: Site/area access control does not depend on coordinates.
- LOCATION_MANAGER-AC-003: Stale location is reported explicitly.
- LOCATION_MANAGER-AC-004: Changing location provider does not change product grouping semantics.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
