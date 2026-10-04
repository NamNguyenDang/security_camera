# Notification Policy / Delivery Routing Requirements — Platform Baseline v2

## Functional requirements
- NOTIFICATION_MANAGER-FR-001: Product behavior shall remain independent of selected native/provider implementation.
- NOTIFICATION_MANAGER-FR-002: Product Profile shall declare capability placement and optionality.
- NOTIFICATION_MANAGER-FR-003: Failure and unavailable states shall be explicit.

## Interface requirements
- NOTIFICATION_MANAGER-IR-001: Portable contracts shall be versioned.
- NOTIFICATION_MANAGER-IR-002: Native/platform SDK types shall not escape adapters.
- NOTIFICATION_MANAGER-IR-003: Cross-deployment behavior shall not assume one operating system.

## Security requirements
- NOTIFICATION_MANAGER-SR-001: Security-sensitive actions shall enforce approved policy.
- NOTIFICATION_MANAGER-SR-002: Security-relevant state changes and failures shall be auditable.

## Reliability requirements
- NOTIFICATION_MANAGER-RR-001: Interrupted or unavailable-provider behavior shall be deterministic.
- NOTIFICATION_MANAGER-RR-002: Recovery/rollback/retry behavior shall be bounded by Product Profile.

## Design acceptance criteria
- NOTIFICATION_MANAGER-AC-001: Alarm semantics remain unchanged when notification provider changes.
- NOTIFICATION_MANAGER-AC-002: Remote-only products work without camera audio/display.
- NOTIFICATION_MANAGER-AC-003: Duplicate notifications are bounded by deduplication policy.
- NOTIFICATION_MANAGER-AC-004: Offline delivery transitions through defined pending/failed/expired states.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
