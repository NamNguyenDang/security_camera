# Device Provisioning Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Manufacturing + Camera enrollment + optional Gateway/Backend ownership workflows**

## Purpose and ownership
Separate manufacturing identity establishment from customer/site enrollment and later ownership transfer/decommissioning.

## Portable contract
ProvisioningState contract covering manufacturing identity, enrollment, ownership assignment/transfer, interrupted provisioning, duplicate/cloned identity detection, credential renewal/revocation, and retirement.

## Relationship overview
![Device Provisioning relationship](./device_provisioning_relationship.svg)

## Review-driven decisions
- Manufacturing and customer enrollment are separate phases.
- Authorized provisioning states/transitions are explicit.
- Interrupted provisioning is recoverable.
- Duplicate/cloned identity is detected and rejected/quarantined.
- Credential renewal/revocation and decommissioning are explicit.
- Outsourced manufacturer responsibilities are documented.
- Mechanisms are selected by Security Profile.

## Product / Security Profile inputs
- required capability/transport and placement;
- compatible contract/provider versions;
- trust, offline, and failure policy;
- qualification evidence where applicable.

## Design rule
Portable product semantics are defined independently of specific transports, operating systems, hardware providers, or manufacturing mechanisms.

## Open decisions
- concrete transport/provider mechanisms;
- profile-specific TTL, version, and qualification limits.

## Design acceptance criteria
1. Interrupted provisioning cannot leave an ambiguously owned device.
2. Duplicate/cloned identity is detected before trusted enrollment.
3. Ownership transfer changes authorization without silently replacing device identity.
4. Decommissioned device cannot rejoin using retired credentials.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and review feedback.
