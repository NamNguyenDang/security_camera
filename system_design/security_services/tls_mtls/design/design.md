# Transport Security (TLS / mTLS Policy) Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Cross-deployment security policy; provider adapter implemented by secure transport provider**

## Purpose and ownership
Own transport-security requirements and policy while treating the middleware TLS provider as a replaceable implementation.

## Security contract
TransportSecurityPolicy contract defining protected endpoints, peer identity validation, authentication mode, renewal/failure behavior, and no-insecure-fallback requirement.

## Relationship overview
![Transport Security (TLS / mTLS Policy) relationship](./tls_mtls_relationship.svg)

## Review-driven decisions
- Sensitive connections require protection.
- Endpoint classes define device/user/service authentication expectations.
- Mutual authentication applies where Security Profile requires it.
- Provider/library is replaceable.
- Failure/renewal behavior is explicit.
- No insecure fallback is permitted; exact algorithms remain open until profile selection.

## Product / Security Profile inputs
- required protections and enforcement placement;
- compatible policy/provider versions;
- offline/stale/revocation behavior;
- selected mechanism/provider where implementation choice is allowed.

## Enforcement model
Security obligations are mandatory where selected by the baseline/profile. Replaceable providers implement those obligations but do not redefine them.

## Open decisions
- exact mechanism/provider selections;
- numerical TTL/renewal/propagation limits;
- profile-specific endpoint classifications.

## Design acceptance criteria
1. Changing TLS library does not change transport-security obligations.
2. Expired/invalid peer identity fails safely.
3. Required protected endpoint never silently downgrades to plaintext.
4. Credential renewal can occur without redefining product service APIs.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and security-design review feedback.
