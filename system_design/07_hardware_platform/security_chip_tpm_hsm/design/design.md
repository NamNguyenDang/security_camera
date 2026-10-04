# Security Hardware Provider Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Qualified security provider selected by Security/Product Profile**

## Purpose and ownership
Treat TPM, HSM, and Secure Element as selectable provider families for required security capabilities rather than as universally interchangeable devices.

## Qualification contract
SecureHardwareProvider qualification contract for protected key operations, root-of-trust functions, provisioning/lifecycle, optional measurement/attestation, failure behavior, and evidence.

## Relationship overview
![Security Hardware Provider relationship](./security_chip_tpm_hsm_relationship.svg)

## Review-driven decisions
- Mandatory product protections are separated from optional measurements/attestation.
- Provider may support only a subset of security capabilities.
- Key protection and non-exportability requirements are explicit.
- Provisioning/lifecycle/replacement behavior is defined.
- Qualification evidence is required before provider selection.

## Product / Security Profile inputs
- required and optional capabilities;
- supplier/provider selection;
- compatible board/driver/firmware versions;
- measurable power/performance/security constraints.

## Qualification model
Supplier/provider replacement is permitted only when the selected implementation satisfies the same portable upper contracts and profile obligations.

## Security
- security outcomes are defined by the security profile, not by vendor marketing categories;
- hardware details remain below provider contracts;
- relevant faults and lifecycle events are auditable.

## Open decisions
- concrete supplier/provider selection;
- profile-specific measurable thresholds and evidence.

## Design acceptance criteria
1. A provider lacking optional attestation can qualify for a profile that does not require attestation.
2. Mandatory protected-key operations satisfy the selected security profile.
3. Provider failure maps to stable security-service status.
4. Changing security hardware does not change application-facing identity/encryption contracts.

## Changelog
- 2026-10-04: Reworked as hardware/provider qualification design for Platform Architecture Baseline v2.
