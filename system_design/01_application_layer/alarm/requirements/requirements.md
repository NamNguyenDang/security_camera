# Alarm Requirements — Platform Baseline v2

## Requirement ID policy

Requirement IDs use the globally unique prefix `ALARM`.

## Functional requirements

- ALARM-FR-001: The component shall implement its product-owned behavior independently of selected operating-system, vendor, database, cloud, or hardware providers.
- ALARM-FR-002: The component shall support the deployment placements enabled by the selected Product Profile.
- ALARM-FR-003: The component shall expose deterministic lifecycle and failure states.
- ALARM-FR-004: Optional capabilities shall have defined unavailable behavior.

## Interface requirements

- ALARM-IR-001: Cross-component dependencies shall use documented product contracts.
- ALARM-IR-002: Control/state/event contracts shall be separated from high-bandwidth media paths where applicable.
- ALARM-IR-003: Provider-specific paths, handles, SDK types, and private implementation details shall not appear in portable product contracts.
- ALARM-IR-004: Contract version compatibility shall be selected and validated by Product Profile.

## Security requirements

- ALARM-SR-001: Authorization shall be enforced at the deployment that performs the protected action.
- ALARM-SR-002: Standalone camera operation shall retain required local authentication/authorization behavior.
- ALARM-SR-003: Security-relevant operations and failures shall be auditable.
- ALARM-SR-004: Ordinary user configuration shall not disable mandatory security obligations.

## Reliability requirements

- ALARM-RR-001: Offline or unavailable gateway/backend behavior shall be defined.
- ALARM-RR-002: Provider failure shall map to stable product-level status.
- ALARM-RR-003: Recovery/reconnect behavior shall be bounded by the selected Product Profile.

## Design acceptance criteria

- ALARM-AC-001: Remote-only alert products work without local display or audio.
- ALARM-AC-002: Duplicate source events do not create uncontrolled duplicate alarms.
- ALARM-AC-003: Acknowledgement identity and scope are auditable.
- ALARM-AC-004: Offline camera/gateway behavior is deterministic.
- ALARM-AC-005: Notification provider replacement does not change alarm-domain semantics.

## Changelog

- 2026-10-04: Reworked for Platform Architecture Baseline v2 and globally unique requirement IDs.
