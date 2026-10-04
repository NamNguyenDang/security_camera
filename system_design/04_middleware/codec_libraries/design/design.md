# Codec Backend Adapter Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera/Gateway/Client media adapter selected by Product Profile**

## Purpose and ownership
Replace the incorrect NPU inference path with a portable encoder/decoder backend interface supporting qualified software codecs or dedicated video-codec hardware.

## Portable contract
CodecBackend contract with formats, buffer ownership, timestamps, capability negotiation, resource limits, errors, and malformed-stream behavior.

## Relationship overview
![Codec Backend Adapter relationship](./codec_libraries_relationship.svg)

## Review-driven decisions
- Neural inference acceleration is not a generic codec contract.
- Software and dedicated video hardware are alternate qualified backends.
- Buffer ownership and timing are explicit.
- Resource limits and capability negotiation are explicit.
- Malformed streams fail safely and deterministically.

## Product Profile inputs
- capability presence and provider selection;
- compatible contract/provider versions;
- resource, timing, and reset budgets;
- fallback policy.

## Supplier qualification
A replacement adapter/provider must satisfy the same ownership, timing, lifecycle, cancellation/reset, and stable-error scenarios.

## Security
- untrusted input is validated at the boundary;
- protected resources remain behind OS/vendor isolation;
- security-relevant provider faults are auditable.

## Open decisions
- supplier/provider selections;
- exact numerical performance/resource limits.

## Design acceptance criteria
1. Codec operation does not require AI/NPU HAL.
2. Software and hardware codec backends preserve the same portable contract.
3. Malformed input cannot escape validation/error handling.
4. Unsupported formats are rejected during capability negotiation.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and supplier-replacement review feedback.
