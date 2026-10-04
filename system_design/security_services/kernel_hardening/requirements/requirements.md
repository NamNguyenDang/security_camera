# Kernel Hardening Requirements

## Component
`kernel_hardening`

## Functional requirements
- KH-FR-001: The security control shall enforce approved kernel security configuration.
- KH-FR-002: The security control shall restrict privileged device and memory access.
- KH-FR-003: The security control shall enable supported exploit mitigations.
- KH-FR-004: The security control shall report security-relevant kernel violations.

## Interface requirements
- KH-IR-001: Expose security/trust status through approved interfaces only.
- KH-IR-002: Keep protected trust state, credentials, and privileged controls inaccessible to unauthorized consumers.

## Security requirements
- KH-SR-001: Fail safely when required trust, provisioning, or hardening controls cannot be established.
- KH-SR-002: Generate audit evidence for security-relevant operations and failures.

## Reliability requirements
- KH-RR-001: Provide defined safe behavior for required hardening control unavailable.
- KH-RR-002: Provide defined safe behavior for policy/configuration mismatch.
- KH-RR-003: Provide defined safe behavior for security violation detected.

## Changelog
- 2026-10-04: Added detailed requirements baseline.
