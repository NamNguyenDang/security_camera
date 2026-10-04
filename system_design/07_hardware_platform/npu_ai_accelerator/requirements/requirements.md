# NPU / AI Accelerator Hardware Requirements — Platform Baseline v2

## Functional requirements
- NPU_AI_ACCELERATOR-FR-001: Product Profile shall declare whether the capability is required or optional.
- NPU_AI_ACCELERATOR-FR-002: Hardware shall satisfy documented measurable qualification constraints.
- NPU_AI_ACCELERATOR-FR-003: Unsupported capability shall be detected before product release/use.

## Interface requirements
- NPU_AI_ACCELERATOR-IR-001: Upper product contracts shall not expose supplier-specific hardware interfaces.
- NPU_AI_ACCELERATOR-IR-002: Compatible OS/driver/runtime versions shall be recorded in the Product Profile.
- NPU_AI_ACCELERATOR-IR-003: Capability/status exposed upward shall be provider-neutral.

## Security requirements
- NPU_AI_ACCELERATOR-SR-001: Required trust/isolation capabilities shall satisfy the selected security profile.
- NPU_AI_ACCELERATOR-SR-002: Security-relevant hardware faults shall be auditable.

## Reliability requirements
- NPU_AI_ACCELERATOR-RR-001: Reset/thermal/power/failure behavior shall be specified.
- NPU_AI_ACCELERATOR-RR-002: Optional capability absence shall follow profile fallback/unavailable behavior.

## Design acceptance criteria
- NPU_AI_ACCELERATOR-AC-001: Product profile without NPU remains valid when inference fallback is allowed.
- NPU_AI_ACCELERATOR-AC-002: Codec path does not require NPU.
- NPU_AI_ACCELERATOR-AC-003: New accelerator preserves upper inference contracts after qualification.
- NPU_AI_ACCELERATOR-AC-004: Thermal/reset behavior satisfies declared product limits.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
