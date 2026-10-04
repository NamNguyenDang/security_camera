# Media Service Requirements — Platform Baseline v2

## Functional requirements
- MEDIA_SERVICE-FR-001: The service shall own product behavior independently of selected provider/runtime/hardware implementation.
- MEDIA_SERVICE-FR-002: Product Profile shall declare placement, optionality, and resource limits.
- MEDIA_SERVICE-FR-003: Lifecycle and failure states shall be deterministic.

## Interface requirements
- MEDIA_SERVICE-IR-001: The service shall expose versioned portable contracts.
- MEDIA_SERVICE-IR-002: Provider/vendor types shall not appear in the product contract.
- MEDIA_SERVICE-IR-003: Control/state/media channels shall be separated where their semantics differ.

## Security requirements
- MEDIA_SERVICE-SR-001: Protected service actions shall require approved authorization.
- MEDIA_SERVICE-SR-002: Security-relevant actions/failures shall be auditable.
- MEDIA_SERVICE-SR-003: Standalone camera operation shall preserve mandatory local security behavior.

## Reliability requirements
- MEDIA_SERVICE-RR-001: Provider failure shall map to stable product-level status.
- MEDIA_SERVICE-RR-002: Restart/recovery/reconnect behavior shall be defined.

## Design acceptance criteria
- MEDIA_SERVICE-AC-001: Recording completion is not acknowledged until selected repository durability criteria are satisfied.
- MEDIA_SERVICE-AC-002: Interrupted recording has a recoverable segment/metadata state.
- MEDIA_SERVICE-AC-003: Capture provider replacement does not change recording orchestration behavior.
- MEDIA_SERVICE-AC-004: Media buffers do not travel through a generic durable-event channel.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
