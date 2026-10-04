# Package / Update Adapter Requirements — Platform Baseline v2

## Functional requirements
- PACKAGE_MANAGER-FR-001: Product behavior shall remain independent of selected native/provider implementation.
- PACKAGE_MANAGER-FR-002: Product Profile shall declare capability placement and optionality.
- PACKAGE_MANAGER-FR-003: Failure and unavailable states shall be explicit.

## Interface requirements
- PACKAGE_MANAGER-IR-001: Portable contracts shall be versioned.
- PACKAGE_MANAGER-IR-002: Native/platform SDK types shall not escape adapters.
- PACKAGE_MANAGER-IR-003: Cross-deployment behavior shall not assume one operating system.

## Security requirements
- PACKAGE_MANAGER-SR-001: Security-sensitive actions shall enforce approved policy.
- PACKAGE_MANAGER-SR-002: Security-relevant state changes and failures shall be auditable.

## Reliability requirements
- PACKAGE_MANAGER-RR-001: Interrupted or unavailable-provider behavior shall be deterministic.
- PACKAGE_MANAGER-RR-002: Recovery/rollback/retry behavior shall be bounded by Product Profile.

## Design acceptance criteria
- PACKAGE_MANAGER-AC-001: A product can use native client package mechanisms without camera dependency.
- PACKAGE_MANAGER-AC-002: Camera update remains valid without Android-style Package Manager.
- PACKAGE_MANAGER-AC-003: Interrupted update has a deterministic recovery state.
- PACKAGE_MANAGER-AC-004: Unauthorized or incompatible update is rejected before activation.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
