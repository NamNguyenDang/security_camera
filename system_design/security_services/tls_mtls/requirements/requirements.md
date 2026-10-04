# TLS / mTLS — Transport Security Requirements

## Component
`tls_mtls`

## Functional requirements
- TM-FR-001: The security service shall establish approved encrypted sessions.
- TM-FR-002: The security service shall authenticate peers according to policy.
- TM-FR-003: The security service shall support mutual authentication where required.
- TM-FR-004: The security service shall report certificate and handshake failures.

## Interface requirements
- TM-IR-001: Expose stable security interfaces to approved consumers only.
- TM-IR-002: Keep protected implementation details and key material outside consumer control.

## Security requirements
- TM-SR-001: Fail closed or fail safely for authorization, identity, policy, or trust failures as applicable.
- TM-SR-002: Generate audit evidence for security-relevant operations and failures.

## Reliability requirements
- TM-RR-001: Provide defined safe behavior for certificate validation failure.
- TM-RR-002: Provide defined safe behavior for handshake timeout.
- TM-RR-003: Provide defined safe behavior for key unavailable.

## Changelog
- 2026-10-04: Added detailed requirements baseline.
