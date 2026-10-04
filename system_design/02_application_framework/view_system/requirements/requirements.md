# Presentation State / Media Surface Contract Requirements — Platform Baseline v2

## Functional requirements
- VIEW_SYSTEM-FR-001: Product Profile shall explicitly declare capability availability.
- VIEW_SYSTEM-FR-002: Capability absence shall have supported deterministic behavior.
- VIEW_SYSTEM-FR-003: Portable behavior shall remain independent of selected native/provider implementation.

## Interface requirements
- VIEW_SYSTEM-IR-001: Expose a versioned portable contract.
- VIEW_SYSTEM-IR-002: Keep native/provider-specific types behind adapters.

## Security requirements
- VIEW_SYSTEM-SR-001: Access to sensitive capability/data shall follow approved authorization/privacy policy.
- VIEW_SYSTEM-SR-002: Security-relevant changes and failures shall be auditable where applicable.

## Reliability requirements
- VIEW_SYSTEM-RR-001: Provider/device absence or loss shall map to stable product-level state.
- VIEW_SYSTEM-RR-002: Recovery behavior shall be bounded by Product Profile.

## Design acceptance criteria
- VIEW_SYSTEM-AC-001: Android/iOS/Web map presentation state to native UI frameworks.
- VIEW_SYSTEM-AC-002: Headless camera profile has no presentation dependency.
- VIEW_SYSTEM-AC-003: Graphics backend can change without changing shared product behavior.
- VIEW_SYSTEM-AC-004: Media surface lifecycle is deterministic.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
