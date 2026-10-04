# Telephony Capability Adapter Requirements — Platform Baseline v2

## Functional requirements
- TELEPHONY_MANAGER-FR-001: Product Profile shall explicitly declare capability availability.
- TELEPHONY_MANAGER-FR-002: Capability absence shall have supported deterministic behavior.
- TELEPHONY_MANAGER-FR-003: Portable behavior shall remain independent of selected native/provider implementation.

## Interface requirements
- TELEPHONY_MANAGER-IR-001: Expose a versioned portable contract.
- TELEPHONY_MANAGER-IR-002: Keep native/provider-specific types behind adapters.

## Security requirements
- TELEPHONY_MANAGER-SR-001: Access to sensitive capability/data shall follow approved authorization/privacy policy.
- TELEPHONY_MANAGER-SR-002: Security-relevant changes and failures shall be auditable where applicable.

## Reliability requirements
- TELEPHONY_MANAGER-RR-001: Provider/device absence or loss shall map to stable product-level state.
- TELEPHONY_MANAGER-RR-002: Recovery behavior shall be bounded by Product Profile.

## Design acceptance criteria
- TELEPHONY_MANAGER-AC-001: Core camera behavior works with telephony absent.
- TELEPHONY_MANAGER-AC-002: A profile can enable cellular data without enabling calls/messages.
- TELEPHONY_MANAGER-AC-003: Provider replacement does not alter product-level telephony semantics.
- TELEPHONY_MANAGER-AC-004: Requirement IDs are globally unique.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
