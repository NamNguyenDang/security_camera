# Middleware Bus Detailed Design

## Component
`middleware_bus`

## Purpose
Defines the approved **API / IPC** communication boundary between **Middleware** and **Hardware Abstraction Layer**.

## Relationship overview
![Middleware Bus relationship](./middleware_bus_relationship.svg)

## Upper-side participants
- Media Framework
- AI Runtime
- Database
- OpenGL ES
- Vulkan
- SSL / TLS
- Codec Libraries

## Lower-side participants
- Camera HAL
- AI / NPU HAL
- Audio HAL
- Display HAL
- Storage HAL
- Network HAL

## Boundary responsibilities
- Define stable request, response, event, message, or stream contracts appropriate to API / IPC.
- Validate input crossing the boundary.
- Preserve ownership and lifecycle rules for transferred resources.
- Return stable errors without leaking implementation-specific details.
- Prevent uncontrolled direct dependencies that bypass this boundary.

## Security controls
- Secrets / Key Management
- Security Logging / Audit
- Security Policy Enforcement

## Failure behavior
- HAL endpoint unavailable
- unsupported capability
- parameter validation failure

## Open design items
- exact interface definition language and versioning policy
- timeout, retry, flow-control, and backpressure behavior
- observability and tracing identifiers
- compatibility rules during rolling software updates

## Changelog
- 2026-10-04: Added detailed communication-boundary design and relationship diagram.
