# Transport Security (TLS / mTLS Policy) Requirements — Platform Baseline v2

## Functional requirements
- TRANSPORT_SECURITY-FR-001: The security control shall preserve mandatory product protection outcomes independently of provider choice.
- TRANSPORT_SECURITY-FR-002: Product/Security Profile shall declare enforcement placement and compatible policy/provider versions.
- TRANSPORT_SECURITY-FR-003: Offline/stale/unavailable state shall have defined safe behavior.

## Interface requirements
- TRANSPORT_SECURITY-IR-001: Security contracts shall use provider-neutral identity/policy/credential references.
- TRANSPORT_SECURITY-IR-002: Provider-specific SDK/hardware details shall remain behind adapters.
- TRANSPORT_SECURITY-IR-003: Policy/identity/transport state shall be versioned where applicable.

## Security requirements
- TRANSPORT_SECURITY-SR-001: Required protections shall fail closed or fail safely according to Security Profile.
- TRANSPORT_SECURITY-SR-002: Insecure fallback shall not bypass mandatory protection.
- TRANSPORT_SECURITY-SR-003: Security-relevant decisions/failures shall be auditable.

## Reliability requirements
- TRANSPORT_SECURITY-RR-001: Provider/backend outage shall not create undefined security state.
- TRANSPORT_SECURITY-RR-002: Renewal/recovery/revocation behavior shall be deterministic.

## Design acceptance criteria
- TRANSPORT_SECURITY-AC-001: Changing TLS library does not change transport-security obligations.
- TRANSPORT_SECURITY-AC-002: Expired/invalid peer identity fails safely.
- TRANSPORT_SECURITY-AC-003: Required protected endpoint never silently downgrades to plaintext.
- TRANSPORT_SECURITY-AC-004: Credential renewal can occur without redefining product service APIs.

## Changelog
- 2026-10-04: Reworked with globally unique requirement IDs for Platform Architecture Baseline v2.
