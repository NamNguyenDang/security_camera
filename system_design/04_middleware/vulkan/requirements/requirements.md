# Vulkan Adapter Requirements — Platform Baseline v2

## Functional requirements
- VULKAN-FR-001: Product Profile shall declare whether this adapter is present.
- VULKAN-FR-002: Portable behavior shall remain independent of selected provider implementation.
- VULKAN-FR-003: Unsupported capability shall be reported deterministically.

## Interface requirements
- VULKAN-IR-001: Provider-specific API types shall not escape the adapter boundary.
- VULKAN-IR-002: Portable contracts shall be versioned and capability-aware.
- VULKAN-IR-003: Provider replacement shall preserve defined product semantics.

## Security requirements
- VULKAN-SR-001: Security-sensitive behavior shall follow the owning security profile/policy.
- VULKAN-SR-002: Required protections shall not fall back to insecure modes.
- VULKAN-SR-003: Security-relevant failures shall be auditable.

## Reliability requirements
- VULKAN-RR-001: Provider loss or initialization failure shall map to stable product state.
- VULKAN-RR-002: Optional capability absence shall remain a supported state.

## Design acceptance criteria
- VULKAN-AC-001: Product logic runs with Vulkan absent.
- VULKAN-AC-002: Rendering backend can switch between Vulkan and another qualified backend.
- VULKAN-AC-003: Unsupported extension/capability is reported before use.
- VULKAN-AC-004: Client and camera-local graphics remain separately qualified.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
