# AI / NPU HAL Requirements

## Component
`ai_npu_hal`

## Functional requirements
- ANH-FR-001: The component shall enumerate accelerator capabilities.
- ANH-FR-002: The component shall submit approved inference workloads.
- ANH-FR-003: The component shall manage supported accelerator resources.
- ANH-FR-004: The component shall translate vendor failures to stable status.

## Interface requirements
- ANH-IR-001: Use only approved upper/lower interfaces.
- ANH-IR-002: Hide vendor-specific implementation from consumers.

## Security requirements
- ANH-SR-001: Use approved security services and policies for protected operations.
- ANH-SR-002: Report security-relevant failures for audit.

## Reliability requirements
- ANH-RR-001: Provide defined behavior for accelerator unavailable.
- ANH-RR-002: Provide defined behavior for unsupported graph.
- ANH-RR-003: Provide defined behavior for driver timeout.

## Changelog
- 2026-10-03: Added detailed requirements baseline.
