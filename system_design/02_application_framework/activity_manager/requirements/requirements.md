# Activity Manager / Lifecycle Adapter Requirements — Platform Baseline v2

## Functional requirements
- ACTIVITY_MANAGER-FR-001: The component shall expose portable product semantics independent of native platform implementation.
- ACTIVITY_MANAGER-FR-002: The Product Profile shall declare whether and where the capability is used.
- ACTIVITY_MANAGER-FR-003: Unsupported capability shall have deterministic behavior.

## Interface requirements
- ACTIVITY_MANAGER-IR-001: The portable contract shall be versioned and smaller than provider/native APIs.
- ACTIVITY_MANAGER-IR-002: Platform/provider-specific types shall stay behind adapters.
- ACTIVITY_MANAGER-IR-003: Cross-deployment calls shall not assume local IPC.

## Security requirements
- ACTIVITY_MANAGER-SR-001: Protected operations shall validate caller authorization.
- ACTIVITY_MANAGER-SR-002: Security-relevant failures shall be auditable.

## Reliability requirements
- ACTIVITY_MANAGER-RR-001: Native/platform unavailability shall map to stable product-level failure.
- ACTIVITY_MANAGER-RR-002: Restart/recovery behavior shall be defined where applicable.

## Design acceptance criteria
- ACTIVITY_MANAGER-AC-001: A headless camera does not require an Activity Manager.
- ACTIVITY_MANAGER-AC-002: Android/iOS/Web can map lifecycle semantics to native mechanisms.
- ACTIVITY_MANAGER-AC-003: Camera services continue independently of client navigation lifecycle.
- ACTIVITY_MANAGER-AC-004: Restart recovery has deterministic portable states.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
