# SSL / TLS Detailed Design

## Component
`ssl_tls`

## Purpose
Provides secure transport protocol primitives used by approved networking components and higher-level services.

## Relationship overview
![SSL / TLS relationship](./ssl_tls_relationship.svg)

## Relevant system path

### Application Layer
- Live View
- Playback
- User Management
### System Services
- Network Service
- Device Management
### Middleware
- SSL / TLS
### HAL
- Network HAL
### Linux Kernel
- Network Driver
### Hardware Platform
- Ethernet / Wi-Fi
- Security Chip / TPM
- SoC / CPU

## Security context
- TLS / mTLS
- Device Identity
- Secrets / Key Management

## Communication boundaries
- Data Bus
- Middleware Bus
- HAL Bus

## Dependency rules
- Keep the public contract stable and implementation private.
- Keep vendor-specific behavior behind the abstraction boundary.
- Do not depend on another component's private `src/`.

## Failure behavior
- certificate invalid
- handshake failure
- key unavailable

## Changelog
- 2026-10-03: Added detailed relationship design.
