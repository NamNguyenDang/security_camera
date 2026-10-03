# Database Detailed Design

## Component
`database`

## Purpose
Provides structured local persistence for configuration, metadata, indexes, and non-media data through a controlled storage abstraction.

## Relationship overview
![Database relationship](./database_relationship.svg)

## Relevant system path

### Application Layer
- Event Search
- Settings
- User Management
### System Services
- Storage Service
- Device Management
### Middleware
- Database
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
- Data Bus
- Middleware Bus
- HAL Bus

## Dependency rules
- Expose stable interfaces upward and keep implementation private.
- Keep vendor-specific behavior below the appropriate abstraction boundary.
- Do not depend on another component's private `src/`.

## Failure behavior
- database corruption
- storage full
- transaction failure

## Changelog
- 2026-10-03: Added detailed relationship design.
