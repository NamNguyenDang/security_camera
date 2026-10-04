# NPU / AI Accelerator Hardware Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Optional qualified hardware capability selected by Product Profile**

## Purpose and ownership
Treat neural acceleration as optional unless required by Product Profile and keep it distinct from dedicated video codec acceleration.

## Qualification contract
Accelerator qualification constraints for inference capability, runtime/model compatibility, memory, thermal, reset, isolation, and security.

## Relationship overview
![NPU / AI Accelerator Hardware relationship](./npu_ai_accelerator_relationship.svg)

## Review-driven decisions
- NPU is not the general video encoder/decoder contract.
- Upper services use inference contracts rather than hardware assumptions.
- Model/runtime compatibility is qualified.
- Memory/thermal/reset/security criteria are explicit.
- Absence follows profile fallback/unavailable behavior.

## Product Profile inputs
- hardware capability required/optional;
- operating envelope and resource budgets;
- compatible OS/driver/runtime/toolchain;
- security and fallback policy.

## Qualification model
Hardware is selected by measurable capability and compatibility criteria. Supplier replacement is permitted after qualification while preserving upper product contracts.

## Security
- hardware trust/isolation capabilities are declared, not assumed;
- mandatory protection requirements come from the security profile;
- security-relevant hardware faults are auditable.

## Open decisions
- concrete supplier targets;
- numerical compute/thermal/power/resource thresholds.

## Design acceptance criteria
1. Product profile without NPU remains valid when inference fallback is allowed.
2. Codec path does not require NPU.
3. New accelerator preserves upper inference contracts after qualification.
4. Thermal/reset behavior satisfies declared product limits.

## Changelog
- 2026-10-04: Reworked as Product Profile / hardware qualification design for Platform Architecture Baseline v2.
