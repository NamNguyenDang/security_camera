# AI Inference Service Requirements — Platform Baseline v2

## Functional requirements
- AI_INFERENCE_SERVICE-FR-001: The service shall own product behavior independently of selected provider/runtime/hardware implementation.
- AI_INFERENCE_SERVICE-FR-002: Product Profile shall declare placement, optionality, and resource limits.
- AI_INFERENCE_SERVICE-FR-003: Lifecycle and failure states shall be deterministic.

## Interface requirements
- AI_INFERENCE_SERVICE-IR-001: The service shall expose versioned portable contracts.
- AI_INFERENCE_SERVICE-IR-002: Provider/vendor types shall not appear in the product contract.
- AI_INFERENCE_SERVICE-IR-003: Control/state/media channels shall be separated where their semantics differ.

## Security requirements
- AI_INFERENCE_SERVICE-SR-001: Protected service actions shall require approved authorization.
- AI_INFERENCE_SERVICE-SR-002: Security-relevant actions/failures shall be auditable.
- AI_INFERENCE_SERVICE-SR-003: Standalone camera operation shall preserve mandatory local security behavior.

## Reliability requirements
- AI_INFERENCE_SERVICE-RR-001: Provider failure shall map to stable product-level status.
- AI_INFERENCE_SERVICE-RR-002: Restart/recovery/reconnect behavior shall be defined.

## Design acceptance criteria
- AI_INFERENCE_SERVICE-AC-001: A CPU/software backend can satisfy the contract when profile allows fallback.
- AI_INFERENCE_SERVICE-AC-002: NPU absence produces profile-defined behavior.
- AI_INFERENCE_SERVICE-AC-003: Result references preserve source frame/timestamp identity.
- AI_INFERENCE_SERVICE-AC-004: Invalid/unapproved model fails before execution.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
