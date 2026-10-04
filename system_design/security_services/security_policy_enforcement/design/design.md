# Security Policy Enforcement Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Cross-cutting enforcement on Client/Camera/Gateway/Backend trust boundaries**

## Purpose and ownership
Define a mandatory platform security baseline plus approved per-product security profiles, with explicit enforcement ownership at each trust boundary.

## Security contract
SecurityPolicy contract with policy version, required protections, enforcement point, stale/unavailable behavior, and release-compliance status.

## Relationship overview
![Security Policy Enforcement relationship](./security_policy_enforcement_relationship.svg)

## Review-driven decisions
- Mandatory baseline is separate from optional mechanisms.
- Per-product security profile may select mechanisms but not remove obligations.
- Policy versioning/distribution is explicit.
- Stale or unavailable policy behavior is defined.
- Release is rejected when required protections are missing.
- Enforcement ownership is assigned per trust boundary.

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
1. A product cannot ship with a required protection missing.
2. Offline camera has defined locally enforceable security policy.
3. Mechanism/provider changes do not weaken policy outcomes.
4. Stale policy state is visible and handled according to profile.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and security-design review feedback.
