# Camera Service Requirements — Platform Baseline v2

## Functional requirements
- CAMERA_SERVICE-FR-001: The service shall own product behavior independently of selected provider/runtime/hardware implementation.
- CAMERA_SERVICE-FR-002: Product Profile shall declare placement, optionality, and resource limits.
- CAMERA_SERVICE-FR-003: Lifecycle and failure states shall be deterministic.

## Interface requirements
- CAMERA_SERVICE-IR-001: The service shall expose versioned portable contracts.
- CAMERA_SERVICE-IR-002: Provider/vendor types shall not appear in the product contract.
- CAMERA_SERVICE-IR-003: Control/state/media channels shall be separated where their semantics differ.

## Security requirements
- CAMERA_SERVICE-SR-001: Protected service actions shall require approved authorization.
- CAMERA_SERVICE-SR-002: Security-relevant actions/failures shall be auditable.
- CAMERA_SERVICE-SR-003: Standalone camera operation shall preserve mandatory local security behavior.

## Reliability requirements
- CAMERA_SERVICE-RR-001: Provider failure shall map to stable product-level status.
- CAMERA_SERVICE-RR-002: Restart/recovery/reconnect behavior shall be defined.

## Design acceptance criteria
- CAMERA_SERVICE-AC-001: Two competing capture requests receive deterministic policy outcomes.
- CAMERA_SERVICE-AC-002: Vendor adapter replacement preserves session contract behavior.
- CAMERA_SERVICE-AC-003: Timeout/reset maps to stable errors.
- CAMERA_SERVICE-AC-004: Requirement IDs use CAMERA_SERVICE prefix.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
