# Secure Transport Provider Adapter Requirements — Platform Baseline v2

## Functional requirements
- SSL_TLS-FR-001: Product Profile shall declare whether this adapter is present.
- SSL_TLS-FR-002: Portable behavior shall remain independent of selected provider implementation.
- SSL_TLS-FR-003: Unsupported capability shall be reported deterministically.

## Interface requirements
- SSL_TLS-IR-001: Provider-specific API types shall not escape the adapter boundary.
- SSL_TLS-IR-002: Portable contracts shall be versioned and capability-aware.
- SSL_TLS-IR-003: Provider replacement shall preserve defined product semantics.

## Security requirements
- SSL_TLS-SR-001: Security-sensitive behavior shall follow the owning security profile/policy.
- SSL_TLS-SR-002: Required protections shall not fall back to insecure modes.
- SSL_TLS-SR-003: Security-relevant failures shall be auditable.

## Reliability requirements
- SSL_TLS-RR-001: Provider loss or initialization failure shall map to stable product state.
- SSL_TLS-RR-002: Optional capability absence shall remain a supported state.

## Design acceptance criteria
- SSL_TLS-AC-001: A TLS library can be replaced without changing transport-security policy.
- SSL_TLS-AC-002: Invalid peer identity fails according to security policy.
- SSL_TLS-AC-003: Provider never silently falls back to insecure transport.
- SSL_TLS-AC-004: Credential rotation does not require changes to product callers.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
