# Device Config Requirements — Platform Baseline v2

## Functional requirements
- DEVICE_CONFIG-FR-001: The component shall implement portable product behavior independent of selected platform providers.
- DEVICE_CONFIG-FR-002: The component shall honor Product Profile capability and deployment selections.
- DEVICE_CONFIG-FR-003: The component shall expose deterministic validation/lifecycle/failure state as applicable.

## Interface requirements
- DEVICE_CONFIG-IR-001: Cross-component interactions shall use documented versioned contracts.
- DEVICE_CONFIG-IR-002: Provider-specific SDK types, hardware details, paths, and private implementation shall not appear in portable contracts.
- DEVICE_CONFIG-IR-003: Contract revision conflicts or incompatible versions shall be reported explicitly.

## Security requirements
- DEVICE_CONFIG-SR-001: Protected actions shall require approved authorization.
- DEVICE_CONFIG-SR-002: Mandatory security policy shall not be weakened by ordinary user configuration.
- DEVICE_CONFIG-SR-003: Security-relevant changes and failures shall be auditable.

## Reliability requirements
- DEVICE_CONFIG-RR-001: Offline/unavailable backend behavior shall be defined.
- DEVICE_CONFIG-RR-002: Provider failure shall map to stable product-level state.

## Design acceptance criteria
- DEVICE_CONFIG-AC-001: A client can edit desired state without direct hardware access.
- DEVICE_CONFIG-AC-002: Stale revision writes are rejected or reconciled deterministically.
- DEVICE_CONFIG-AC-003: Partial apply produces explicit per-field status.
- DEVICE_CONFIG-AC-004: Offline camera changes reconcile according to defined precedence.
- DEVICE_CONFIG-AC-005: Product Profile cannot be modified through ordinary device configuration.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
