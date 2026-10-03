# Activity Manager Requirements

## Component

`activity_manager`

## Functional requirements

- AM-FR-001: The component shall track application lifecycle state.
- AM-FR-002: The component shall coordinate start/stop transitions.
- AM-FR-003: The component shall recover defined state after restart.
- AM-FR-004: The component shall prevent invalid lifecycle transitions.

## Interface requirements

- AM-IR-001: The component shall use approved interfaces and buses.
- AM-IR-002: The component shall not depend on another component's private implementation.

## Security requirements

- AM-SR-001: Security-relevant access shall use approved identity, authorization, and policy services where applicable.
- AM-SR-002: Security-relevant actions and failures shall be auditable.

## Reliability requirements

- AM-RR-001: Defined behavior shall exist for application crash.
- AM-RR-002: Defined behavior shall exist for resource exhaustion.
- AM-RR-003: Defined behavior shall exist for invalid lifecycle request.

## Changelog

- 2026-10-03: Added detailed requirements baseline.
