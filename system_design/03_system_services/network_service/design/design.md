# Network Service Detailed Design

## Component
`network_service`

## Purpose
Owns device networking state and controlled network configuration while exposing stable connectivity services to higher layers.

## Relationship overview
![Network Service relationship](./network_service_relationship.svg)

## Relevant system path

### Application Layer
- Live View
- Playback
- Device Config
### System Services
- Network Service
- Device Management
### Middleware
- SSL / TLS
### HAL
- Network HAL
### Linux Kernel
- Network Driver
- Wi-Fi / BT Driver
### Hardware Platform
- Ethernet / Wi-Fi
- SoC / CPU

## Security context
- TLS / mTLS
- Device Identity
- Security Policy
- Audit

## Communication boundaries
- System Service Bus
- Data Bus
- Middleware Bus
- HAL Bus

## Dependency rules
- Use approved interfaces and buses.
- Keep vendor and lower-layer implementation behind owning boundaries.
- Do not depend on another component's private `src/`.

## Failure behavior
- link unavailable
- configuration invalid
- authentication failure

## Changelog
- 2026-10-03: Added detailed relationship design.
