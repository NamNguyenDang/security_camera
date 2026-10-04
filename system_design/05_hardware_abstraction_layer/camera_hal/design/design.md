# Camera Capture Adapter / HAL Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera platform adapter**

## Purpose and ownership
Retain as a primary supplier-replacement contract between Camera Service/Media Framework and selected camera/OS/vendor integration.

## Portable contract
Portable Capture Adapter contract with frame/buffer ownership, formats, timing, concurrency, lifecycle, cancellation, stable errors, and capability/version negotiation.

## Relationship overview
![Camera Capture Adapter / HAL relationship](./camera_hal_relationship.svg)

## Review-driven decisions
- Portable capture semantics are separated from Linux/vendor implementation.
- Frame/buffer ownership is explicit.
- Concurrent sessions and arbitration capabilities are declared.
- Cancellation and reset behavior are stable.
- Supplier qualification uses design-level acceptance scenarios.

## Product Profile inputs
- capability presence and provider selection;
- compatible contract/provider versions;
- resource, timing, and reset budgets;
- fallback policy.

## Supplier qualification
A replacement adapter/provider must satisfy the same ownership, timing, lifecycle, cancellation/reset, and stable-error scenarios.

## Security
- untrusted input is validated at the boundary;
- protected resources remain behind OS/vendor isolation;
- security-relevant provider faults are auditable.

## Open decisions
- supplier/provider selections;
- exact numerical performance/resource limits.

## Design acceptance criteria
1. A new sensor/vendor capture adapter can replace the existing one without Camera Service changes.
2. Frame ownership has defined acquire/release semantics.
3. Unsupported mode is rejected through capability negotiation.
4. Reset/cancellation returns stable portable status.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and supplier-replacement review feedback.
