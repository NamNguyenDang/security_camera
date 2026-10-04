# OpenGL ES Adapter Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Optional client or camera-local display implementation selected by Product Profile**

## Purpose and ownership
Classify OpenGL ES as an optional rendering implementation beneath a portable presentation/rendering capability contract.

## Portable contract
RenderingCapability contract independent of OpenGL ES types and separate for client display versus optional camera-local display.

## Relationship overview
![OpenGL ES Adapter relationship](./opengl_es_relationship.svg)

## Review-driven decisions
- OpenGL ES is not mandatory common middleware.
- Client and camera display deployments are distinct.
- Products with no graphics backend remain valid.
- Graphics API selection is an adapter decision.
- Shared product behavior does not use OpenGL ES types.

## Product Profile inputs
- enable/omit decision;
- deployment placement;
- provider/backend and compatible version;
- security/capability profile;
- resource limits.

## Provider qualification
Providers are qualified against the portable contract; provider-specific API types remain below the adapter.

## Security
- mandatory security outcomes are defined outside optional convenience APIs;
- insecure fallback is not permitted where protection is required;
- provider failures are auditable.

## Open decisions
- exact provider/API selection per profile;
- numerical resource and performance constraints.

## Design acceptance criteria
1. Headless camera profile omits OpenGL ES.
2. A client can use a different native graphics API without product contract changes.
3. Local camera display can use OpenGL ES only when profile selects it.
4. Unsupported rendering features produce stable capability status.

## Changelog
- 2026-10-04: Re-scoped for Platform Architecture Baseline v2 and review feedback.
