# Secrets / Key Management Requirements

## Component
`secrets_key_management`

## Functional requirements
- SKM-FR-001: The security service shall provision and retrieve approved key references.
- SKM-FR-002: The security service shall rotate and revoke keys according to lifecycle policy.
- SKM-FR-003: The security service shall prevent raw secret exposure to unauthorized consumers.
- SKM-FR-004: The security service shall report key state and operation failures.

## Interface requirements
- SKM-IR-001: Expose stable security interfaces to approved consumers only.
- SKM-IR-002: Keep protected implementation, keys, measurements, and trust state outside unauthorized consumer control.

## Security requirements
- SKM-SR-001: Fail closed or fail safely for trust, key, authorization, integrity, or verification failures as applicable.
- SKM-SR-002: Generate audit evidence for security-relevant operations and failures.

## Reliability requirements
- SKM-RR-001: Provide defined safe behavior for protected key store unavailable.
- SKM-RR-002: Provide defined safe behavior for rotation failure.
- SKM-RR-003: Provide defined safe behavior for revoked or expired key.

## Changelog
- 2026-10-04: Added detailed requirements baseline.
