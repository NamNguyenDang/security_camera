# Inference Acceleration Adapter / HAL Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Optional Camera platform adapter selected by Product Profile**

## Purpose and ownership
Separate the portable inference-acceleration contract from vendor runtime/driver adapters and keep its boundary with AI Runtime explicit.

## Portable contract
InferenceAcceleration contract with workload/buffer ownership, synchronization, capabilities, errors, timeout/reset, and version compatibility.

## Relationship overview
![Inference Acceleration Adapter / HAL relationship](./ai_npu_hal_relationship.svg)

## Review-driven decisions
- AI Runtime owns model/runtime abstraction; this adapter only exposes accelerator capability.
- Accelerator absence is profile-defined.
- Vendor workload types do not escape upward.
- Timeout/reset and synchronization behavior are explicit.
- Version compatibility is qualified.

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
1. AI Runtime can operate without this adapter when profile allows fallback.
2. Changing NPU vendor does not change inference service contracts.
3. Timeout/reset has bounded deterministic behavior.
4. Unsupported workload capability is reported before execution.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and supplier-replacement review feedback.
