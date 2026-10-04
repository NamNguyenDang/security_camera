# Security Hardware Provider Requirements — Platform Baseline v2

## Functional requirements
- SECURITY_CHIP_TPM_HSM-FR-001: Product/Security Profile shall declare required and optional capabilities.
- SECURITY_CHIP_TPM_HSM-FR-002: Hardware/provider shall satisfy documented qualification constraints.
- SECURITY_CHIP_TPM_HSM-FR-003: Unsupported capability shall be detected before protected use.

## Interface requirements
- SECURITY_CHIP_TPM_HSM-IR-001: Supplier-specific interfaces shall remain behind platform/provider adapters.
- SECURITY_CHIP_TPM_HSM-IR-002: Capabilities and status exposed upward shall be provider-neutral.
- SECURITY_CHIP_TPM_HSM-IR-003: Compatible driver/firmware/provider versions shall be recorded.

## Security requirements
- SECURITY_CHIP_TPM_HSM-SR-001: Required protection outcomes shall be enforced independently of supplier choice.
- SECURITY_CHIP_TPM_HSM-SR-002: Security-relevant lifecycle/fault state shall be auditable.

## Reliability requirements
- SECURITY_CHIP_TPM_HSM-RR-001: Reset/power/provider failure behavior shall be documented.
- SECURITY_CHIP_TPM_HSM-RR-002: Optional capability absence shall follow Product/Security Profile.

## Design acceptance criteria
- SECURITY_CHIP_TPM_HSM-AC-001: A provider lacking optional attestation can qualify for a profile that does not require attestation.
- SECURITY_CHIP_TPM_HSM-AC-002: Mandatory protected-key operations satisfy the selected security profile.
- SECURITY_CHIP_TPM_HSM-AC-003: Provider failure maps to stable security-service status.
- SECURITY_CHIP_TPM_HSM-AC-004: Changing security hardware does not change application-facing identity/encryption contracts.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
