# Security Logging / Audit Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera local audit mandatory for standalone; Gateway/Backend aggregation optional**

## Purpose and ownership
Define a stable audit event model and bounded local behavior so logging/export outages do not create undefined system-wide behavior.

## Security contract
AuditEvent contract with actor/device/resource scope, timestamp/ordering, correlation, redaction, integrity, retention, access rules, buffering, and export status.

## Relationship overview
![Security Logging / Audit relationship](./security_logging_audit_relationship.svg)

## Review-driven decisions
- Audit schema is stable and versioned.
- Actor/device/resource scope is explicit.
- Time/order/correlation fields are defined.
- Sensitive-field redaction and integrity expectations are defined.
- Local buffering is bounded.
- Behavior when storage/export is unavailable defines which operations continue or stop.

## Security Profile inputs
- required protection/audit/key outcomes;
- placement/provider selection;
- lifecycle/rotation/retention/recovery policy;
- offline/buffering behavior;
- compatible contract/provider versions.

## Provider separation
Product protection requirements remain stable while cryptographic, key-store, hardware, and audit providers are replaceable through qualified adapters.

## Open decisions
- concrete cryptographic/key/audit providers;
- numerical retention, buffer, rotation, and recovery limits.

## Design acceptance criteria
1. Standalone camera retains bounded local audit evidence.
2. Audit export outage does not silently discard unlimited events.
3. Protected operations that require audit fail according to explicit profile policy when audit cannot be recorded.
4. Changing audit backend does not change event schema semantics.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and security-review feedback.
