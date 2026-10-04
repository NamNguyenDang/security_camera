# Repository / Query Access Contract Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Client, Camera, Gateway, or Backend depending repository placement**

## Purpose and ownership
Preserve controlled data access but re-scope Android-style Content Provider into product-owned repository/query contracts.

## Product-owned contract
RepositoryAccess and Query contracts with authorization scope, schema/version compatibility, and local/remote deployment adapters.

## Relationship overview
![Repository / Query Access Contract relationship](./content_providers_relationship.svg)

## Review-driven decisions
- Storage Service owns persistence orchestration; Database is an implementation adapter, not the product contract.
- Authorization scope is enforced before data exposure.
- Schema/version compatibility is explicit.
- Local and remote repository access preserve the same product semantics.
- Provider-specific APIs remain in adapters.

## Product Profile inputs
- whether this capability exists in the product;
- deployment placement and compatible contract version;
- selected native/platform adapter;
- security and offline behavior.

## Design rules
- platform/framework names do not imply a mandatory Android implementation;
- portable contracts remain smaller than native platform APIs;
- client and camera platform concerns are separated;
- private/provider implementation is not exposed upward.

## Security
- caller identity and authorization are enforced at protected operations;
- security-relevant lifecycle/data actions are auditable;
- standalone camera behavior does not depend on backend availability.

## Open decisions
- native adapter choices per supported platform;
- exact compatibility/versioning and resource limits.

## Design acceptance criteria
1. Replacing the database/provider does not change repository semantics.
2. The same query contract can target local camera or backend repository.
3. Unauthorized fields/resources are not exposed.
4. Schema incompatibility is detected explicitly.

## Changelog
- 2026-10-04: Re-scoped for Platform Architecture Baseline v2 and review feedback.
