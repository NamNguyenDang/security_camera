# Camera HAL Requirements

## Component
`camera_hal`

## Functional requirements
- CH-FR-001: The component shall enumerate camera capabilities.
- CH-FR-002: The component shall configure approved capture modes.
- CH-FR-003: The component shall start and stop capture streams.
- CH-FR-004: The component shall translate vendor errors to stable status.

## Interface requirements
- CH-IR-001: Use only approved upper/lower interfaces.
- CH-IR-002: Hide vendor-specific implementation from consumers.

## Security requirements
- CH-SR-001: Use approved security services and policies for protected operations.
- CH-SR-002: Report security-relevant failures for audit.

## Reliability requirements
- CH-RR-001: Provide defined behavior for sensor absent.
- CH-RR-002: Provide defined behavior for unsupported mode.
- CH-RR-003: Provide defined behavior for driver error.

## Changelog
- 2026-10-03: Added detailed requirements baseline.
