# AI Runtime Requirements — Platform Baseline v2

## Functional requirements
- AI_RUNTIME-FR-001: The adapter shall preserve portable product semantics across qualified providers.
- AI_RUNTIME-FR-002: Product Profile shall select compatible provider capabilities and versions.
- AI_RUNTIME-FR-003: Unsupported capability shall return deterministic status.

## Interface requirements
- AI_RUNTIME-IR-001: Provider-specific types shall not escape the adapter boundary.
- AI_RUNTIME-IR-002: Ownership, lifecycle, error, and compatibility semantics shall be documented.
- AI_RUNTIME-IR-003: Replacement providers shall satisfy the same conformance scenarios.

## Security requirements
- AI_RUNTIME-SR-001: Protected operations/data shall use approved security policy and key/identity references.
- AI_RUNTIME-SR-002: Security-relevant provider failures shall be auditable.

## Reliability requirements
- AI_RUNTIME-RR-001: Provider initialization/runtime failure shall map to stable status.
- AI_RUNTIME-RR-002: Recovery/fallback shall follow Product Profile.

## Design acceptance criteria
- AI_RUNTIME-AC-001: CPU and NPU runtimes can satisfy the same upper contract when profile permits.
- AI_RUNTIME-AC-002: Unsupported graphs fail deterministically.
- AI_RUNTIME-AC-003: Provider-specific tensor/device handles do not appear in service interfaces.
- AI_RUNTIME-AC-004: Resource-limit violation is reported predictably.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
