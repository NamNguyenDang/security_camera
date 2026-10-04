# Media Framework Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera/Gateway media middleware; provider backend selected by Product Profile**

## Purpose and ownership
Define reusable media primitives while keeping the selected vendor/open-source backend replaceable and product orchestration above it.

## Portable contract
MediaPrimitive contract for buffers, timestamps, synchronization, format negotiation, backpressure, ownership, and copy constraints.

## Relationship overview
![Media Framework relationship](./media_framework_relationship.svg)

## Review-driven decisions
- Media Service owns product orchestration.
- Buffer ownership and release rules are explicit.
- Format negotiation and timestamp domains are defined.
- Backpressure/drop behavior is bounded.
- Copy/zero-copy constraints are capabilities, not assumptions.
- Backend replacement is validated by conformance scenarios.

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
1. Two qualified media backends produce equivalent contract behavior.
2. Buffer ownership has no ambiguous double-release/leak state.
3. Timestamp/synchronization semantics survive backend replacement.
4. Backpressure behavior is deterministic under overload.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and provider-replacement review feedback.
