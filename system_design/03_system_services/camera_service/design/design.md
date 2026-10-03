# Camera Service Detailed Design

## Component
`camera_service`

## Purpose
Owns camera capture-session control and provides a stable camera capability boundary to applications and media services.

## Relationship overview
![Camera Service relationship](./camera_service_relationship.svg)

## Relevant system path

### Application Layer
- Live View
- Device Config
### System Services
- Camera Service
- Media Service
- Device Management
### Middleware
- Media Framework
### HAL
- Camera HAL
### Linux Kernel
- Camera Driver
### Hardware Platform
- Camera Sensor
- SoC / CPU

## Security context
- Security Policy
- Secure HAL
- Audit

## Communication boundaries
- System Service Bus
- Data Bus
- HAL Bus

## Dependency rules
- Use approved interfaces and buses.
- Keep vendor and lower-layer implementation behind owning boundaries.
- Do not depend on another component's private `src/`.

## Failure behavior
- sensor unavailable
- configuration rejected
- capture timeout

## Changelog
- 2026-10-03: Added detailed relationship design.
