# Mobile / Web UI Requirements — Platform Baseline v2

## Functional requirements
- MOBILE_WEB_UI-FR-001: The component shall implement portable product behavior independent of selected platform providers.
- MOBILE_WEB_UI-FR-002: The component shall honor Product Profile capability and deployment selections.
- MOBILE_WEB_UI-FR-003: The component shall expose deterministic validation/lifecycle/failure state as applicable.

## Interface requirements
- MOBILE_WEB_UI-IR-001: Cross-component interactions shall use documented versioned contracts.
- MOBILE_WEB_UI-IR-002: Provider-specific SDK types, hardware details, paths, and private implementation shall not appear in portable contracts.
- MOBILE_WEB_UI-IR-003: Contract revision conflicts or incompatible versions shall be reported explicitly.

## Security requirements
- MOBILE_WEB_UI-SR-001: Protected actions shall require approved authorization.
- MOBILE_WEB_UI-SR-002: Mandatory security policy shall not be weakened by ordinary user configuration.
- MOBILE_WEB_UI-SR-003: Security-relevant changes and failures shall be auditable.

## Reliability requirements
- MOBILE_WEB_UI-RR-001: Offline/unavailable backend behavior shall be defined.
- MOBILE_WEB_UI-RR-002: Provider failure shall map to stable product-level state.

## Design acceptance criteria
- MOBILE_WEB_UI-AC-001: The same product workflow can be implemented on Android, iOS, and Web without camera OS dependencies.
- MOBILE_WEB_UI-AC-002: Remote client live view renders through native client media surfaces.
- MOBILE_WEB_UI-AC-003: A headless camera works with remote clients.
- MOBILE_WEB_UI-AC-004: Replacing client platform adapters does not change camera product contracts.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
