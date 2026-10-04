# Window Manager / Surface Adapter Requirements — Platform Baseline v2

## Functional requirements
- WINDOW_MANAGER-FR-001: The component shall expose portable product semantics independent of native platform implementation.
- WINDOW_MANAGER-FR-002: The Product Profile shall declare whether and where the capability is used.
- WINDOW_MANAGER-FR-003: Unsupported capability shall have deterministic behavior.

## Interface requirements
- WINDOW_MANAGER-IR-001: The portable contract shall be versioned and smaller than provider/native APIs.
- WINDOW_MANAGER-IR-002: Platform/provider-specific types shall stay behind adapters.
- WINDOW_MANAGER-IR-003: Cross-deployment calls shall not assume local IPC.

## Security requirements
- WINDOW_MANAGER-SR-001: Protected operations shall validate caller authorization.
- WINDOW_MANAGER-SR-002: Security-relevant failures shall be auditable.

## Reliability requirements
- WINDOW_MANAGER-RR-001: Native/platform unavailability shall map to stable product-level failure.
- WINDOW_MANAGER-RR-002: Restart/recovery behavior shall be defined where applicable.

## Design acceptance criteria
- WINDOW_MANAGER-AC-001: Remote clients render without depending on camera display/window services.
- WINDOW_MANAGER-AC-002: Headless product profiles contain no window/display dependency.
- WINDOW_MANAGER-AC-003: Surface loss and recreation are deterministic.
- WINDOW_MANAGER-AC-004: Switching graphics backend does not change upper presentation semantics.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
