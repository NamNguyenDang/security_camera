# Client Resource Manager Requirements — Platform Baseline v2

## Functional requirements
- RESOURCE_MANAGER-FR-001: Product behavior shall remain independent of selected native/provider implementation.
- RESOURCE_MANAGER-FR-002: Product Profile shall declare capability placement and optionality.
- RESOURCE_MANAGER-FR-003: Failure and unavailable states shall be explicit.

## Interface requirements
- RESOURCE_MANAGER-IR-001: Portable contracts shall be versioned.
- RESOURCE_MANAGER-IR-002: Native/platform SDK types shall not escape adapters.
- RESOURCE_MANAGER-IR-003: Cross-deployment behavior shall not assume one operating system.

## Security requirements
- RESOURCE_MANAGER-SR-001: Security-sensitive actions shall enforce approved policy.
- RESOURCE_MANAGER-SR-002: Security-relevant state changes and failures shall be auditable.

## Reliability requirements
- RESOURCE_MANAGER-RR-001: Interrupted or unavailable-provider behavior shall be deterministic.
- RESOURCE_MANAGER-RR-002: Recovery/rollback/retry behavior shall be bounded by Product Profile.

## Design acceptance criteria
- RESOURCE_MANAGER-AC-001: Web/iOS/Android clients resolve resources without camera storage services.
- RESOURCE_MANAGER-AC-002: Missing resource behavior is deterministic.
- RESOURCE_MANAGER-AC-003: Changing client packaging mechanism does not change product presentation state contract.
- RESOURCE_MANAGER-AC-004: Headless cameras do not require this client resource component.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
