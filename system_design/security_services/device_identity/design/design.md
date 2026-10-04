# Device Identity Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera mandatory; Gateway/Backend consume identity proofs; provider selected by Security Profile**

## Purpose and ownership
Keep unique authenticated device identity mandatory while making the contract independent of certificate-only or specific security-chip implementations.

## Security contract
DeviceIdentity contract with provider-neutral identity reference, proof/authentication operations, enrollment, renewal, revocation, transfer, and retirement state.

## Relationship overview
![Device Identity relationship](./device_identity_relationship.svg)

## Review-driven decisions
- Identity proof is separate from boot attestation.
- Identity is separate from recording encryption keys.
- Provider selection is profile-driven.
- Enrollment/renewal/revocation/ownership transfer/retirement are explicit.
- Certificate is one possible mechanism, not the contract.

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
1. A device can change identity provider without changing Device Management semantics.
2. Revoked identity cannot authenticate after defined propagation boundary.
3. Ownership transfer preserves device identity while changing authorization ownership as designed.
4. Standalone camera can prove identity without backend always online.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and security-design review feedback.
