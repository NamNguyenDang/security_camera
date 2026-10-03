# Storage Service Detailed Design

## Component
`storage_service`

## Purpose
Provides controlled access to media and metadata persistence while hiding physical storage, filesystem, and vendor implementation details.

## Relationship overview
![Storage Service relationship](./storage_service_relationship.svg)

## Relevant system path

### Application Layer
- Playback
- Event Search
- Settings
### System Services
- Storage Service
- Media Service
- Device Management
### Middleware
- Database
- Media Framework
- Encryption
### HAL
- Storage HAL
### Linux Kernel
- Storage Driver
### Hardware Platform
- Storage eMMC / SSD
- SoC / CPU

## Security context
- Encryption Services
- Secrets / Key Management
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
- storage full
- media corruption
- device unavailable

## Changelog
- 2026-10-03: Added detailed relationship design.
