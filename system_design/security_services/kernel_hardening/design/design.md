# Kernel / OS Hardening Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Operating-System / platform security implementation beneath common protection requirements**

## Purpose and ownership
Scope kernel hardening as OS/platform-specific implementation rather than a universal application/middleware dependency.

## Security contract
OSHardeningProfile contract defining required control categories, privilege/device isolation, exploit mitigations, configuration evidence, and unsupported-control behavior.

## Relationship overview
![Kernel / OS Hardening relationship](./kernel_hardening_relationship.svg)

## Review-driven decisions
- Common security requirements sit above OS-specific settings.
- Privilege/device isolation requirements are explicit.
- Configuration evidence is required for qualification.
- Unsupported controls have profile-defined release behavior.
- Linux-specific knobs do not leak into portable product contracts.

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
1. A non-Linux platform can satisfy the same common protection outcomes with different mechanisms.
2. Missing required hardening control blocks qualification unless approved alternative exists.
3. Configuration evidence is reviewable per product build.
4. Applications do not depend on Linux-specific hardening settings.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and security-boundary review feedback.
