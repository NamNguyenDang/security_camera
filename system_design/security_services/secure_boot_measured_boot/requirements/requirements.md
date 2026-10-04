# Secure Boot / Measured Boot Requirements

## Component
`secure_boot_measured_boot`

## Functional requirements
- SBMB-FR-001: The security service shall verify boot-stage authenticity and integrity.
- SBMB-FR-002: The security service shall enforce approved boot policy.
- SBMB-FR-003: The security service shall record supported boot measurements.
- SBMB-FR-004: The security service shall expose boot trust state to approved consumers.

## Interface requirements
- SBMB-IR-001: Expose stable security interfaces to approved consumers only.
- SBMB-IR-002: Keep protected implementation, keys, measurements, and trust state outside unauthorized consumer control.

## Security requirements
- SBMB-SR-001: Fail closed or fail safely for trust, key, authorization, integrity, or verification failures as applicable.
- SBMB-SR-002: Generate audit evidence for security-relevant operations and failures.

## Reliability requirements
- SBMB-RR-001: Provide defined safe behavior for signature verification failure.
- SBMB-RR-002: Provide defined safe behavior for measurement storage unavailable.
- SBMB-RR-003: Provide defined safe behavior for rollback or unauthorized image detected.

## Changelog
- 2026-10-04: Added detailed requirements baseline.
