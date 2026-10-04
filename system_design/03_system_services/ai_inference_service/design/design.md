# AI Inference Service Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera product service; optional Gateway/Backend inference placement by Product Profile**

## Purpose and ownership
Own inference orchestration independently of selected runtime and accelerator; AI features may be mandatory or optional per Product Profile.

## Product-owned contract
InferenceRequest/Result contract with model/version, preprocessing, frame/timestamp association, resource budget, result schema, integrity state, and fallback policy.

## Relationship overview
![AI Inference Service relationship](./ai_inference_service_relationship.svg)

## Interaction/data planes
- **Control:** commands and lifecycle operations.
- **State/events:** operational state and durable product events.
- **Media/data:** bounded high-bandwidth buffers/streams where applicable.
- Provider transports are selected behind adapters.

## Review-driven decisions
- Runtime/backend and accelerator are replaceable.
- Unsupported capability follows explicit fallback/unavailable behavior.
- Model/version and preprocessing are product contracts.
- Frame/timestamp association is preserved.
- Resource budgets and result integrity checks are explicit.

## Product Profile inputs
- placement and optional capabilities;
- compatible contract versions;
- adapter/backend selection;
- performance/resource/security budgets.

## Security
- authorization is enforced at protected service operations;
- standalone camera operation retains required local enforcement;
- protected models/recordings/credentials use approved security services.

## Open decisions
- exact provider technologies;
- numerical product-profile budgets;
- deployment-specific scaling and retry limits.

## Design acceptance criteria
1. A CPU/software backend can satisfy the contract when profile allows fallback.
2. NPU absence produces profile-defined behavior.
3. Result references preserve source frame/timestamp identity.
4. Invalid/unapproved model fails before execution.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and review feedback.
