# Secure Hardware Access Boundary Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera platform/security boundary; exact isolation depends on OS/TEE/hardware profile**

## Purpose and ownership
Clarify which boundary provides actual security isolation; a library interface alone is not considered a security boundary.

## Security contract
SecureHardwareAccess contract defining caller identity source, authorization, parameter validation, protected operations, isolation mechanism, trust assumptions, and stable failures.

## Relationship overview
![Secure Hardware Access Boundary relationship](./secure_hal_interface_relationship.svg)

## Review-driven decisions
- Isolation may be process, OS privilege boundary, TEE, secure monitor, or hardware provider depending profile.
- Caller identity source is explicit.
- Permissions and protected operations are explicit.
- Validation occurs before entering trusted provider.
- Provider selection stays behind contract.

## Security Profile inputs
- required protection/isolation/evidence capabilities;
- selected OS/provider mechanism;
- compatible versions and qualification evidence;
- fallback/recovery/release behavior.

## Trust boundary rule
The design names the real isolation mechanism. A software API alone is not treated as a security boundary unless backed by process/OS/TEE/hardware enforcement.

## Open decisions
- selected platform/provider mechanisms;
- profile-specific evidence and release thresholds.

## Design acceptance criteria
1. A deployment states its actual isolation mechanism.
2. Unauthorized caller cannot invoke protected operation even if it can link to a library.
3. Invalid input is rejected before trusted operation.
4. Changing secure-hardware provider does not alter caller-facing authorization semantics.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and security-boundary review feedback.
