# Inference Acceleration Adapter / HAL Requirements — Platform Baseline v2

## Functional requirements
- AI_NPU_HAL-FR-001: The adapter shall expose portable capability and lifecycle semantics independent of selected supplier.
- AI_NPU_HAL-FR-002: Product Profile shall select provider/version and capability presence.
- AI_NPU_HAL-FR-003: Unsupported capability shall be reported before use.

## Interface requirements
- AI_NPU_HAL-IR-001: Buffer/resource ownership and lifecycle shall be explicit.
- AI_NPU_HAL-IR-002: Vendor/driver-specific types shall not escape the adapter.
- AI_NPU_HAL-IR-003: Cancellation, timeout, reset, and stable error mapping shall be defined.

## Security requirements
- AI_NPU_HAL-SR-001: Boundary inputs shall be validated before provider execution.
- AI_NPU_HAL-SR-002: Security-relevant faults shall be auditable.

## Reliability requirements
- AI_NPU_HAL-RR-001: Provider reset/unavailability shall map to stable product-level status.
- AI_NPU_HAL-RR-002: Optional adapter absence shall follow Product Profile fallback/unavailable policy.

## Design acceptance criteria
- AI_NPU_HAL-AC-001: AI Runtime can operate without this adapter when profile allows fallback.
- AI_NPU_HAL-AC-002: Changing NPU vendor does not change inference service contracts.
- AI_NPU_HAL-AC-003: Timeout/reset has bounded deterministic behavior.
- AI_NPU_HAL-AC-004: Unsupported workload capability is reported before execution.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
