# AI Runtime Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera/Gateway/Backend adapter depending Product Profile**

## Purpose and ownership
Retain runtime/backend replacement behind a portable inference-runtime contract independent of accelerator/vendor-specific types.

## Portable contract
InferenceRuntime contract for model format, preprocessing, input/output buffers, capability reporting, errors, fallback, and resource limits.

## Relationship overview
![AI Runtime relationship](./ai_runtime_relationship.svg)

## Review-driven decisions
- Backend selection is approved by Product Profile.
- Unsupported graphs return stable capability status.
- Fallback policy is explicit.
- Accelerator-specific types do not escape upward.
- Resource limits are declared and enforceable.

## Product Profile inputs
- provider/backend selection;
- compatible contract version and capabilities;
- memory/latency/durability/resource budgets;
- fallback and recovery policy.

## Provider qualification
A replacement provider is acceptable only when it passes the design-level contract scenarios and preserves ownership, timing, error, and recovery semantics.

## Security
- protected data/models/credentials use approved security services;
- provider failures do not bypass policy;
- security-relevant failures are auditable.

## Open decisions
- exact provider technologies;
- numerical resource/performance limits;
- profile-specific qualification matrix.

## Design acceptance criteria
1. CPU and NPU runtimes can satisfy the same upper contract when profile permits.
2. Unsupported graphs fail deterministically.
3. Provider-specific tensor/device handles do not appear in service interfaces.
4. Resource-limit violation is reported predictably.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and provider-replacement review feedback.
