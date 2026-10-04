# Encryption Services Detailed Design

## Component
`encryption_services`

## Purpose
Provides approved encryption capabilities for data at rest and in transit so individual components do not implement incompatible cryptography.

## Relationship overview
![Encryption Services relationship](./encryption_services_relationship.svg)

## Cross-layer relationship

### Application Layer
- Playback
- Event Search
- User Management
### System Services
- Storage Service
- Network Service
- Device Management
### Middleware
- Database
- Media Framework
- SSL / TLS
### HAL
- Storage HAL
- Network HAL
### Linux Kernel
- Storage Driver
- Network Driver
### Hardware Platform
- Storage eMMC / SSD
- Security Chip / TPM

## Related security services
- Secrets / Key Management
- Hardware Root of Trust
- Audit

## Communication / enforcement boundaries
- Data Bus
- Middleware Bus
- HAL Bus

## Design rules
- Consumers shall use approved security interfaces rather than implement private alternatives.
- Protected keys, measurements, or trust state shall remain behind the owning secure boundary.
- Security failures shall fail safely and preserve auditability.

## Failure behavior
- key unavailable
- unsupported algorithm policy
- cryptographic operation failure

## Changelog
- 2026-10-04: Added detailed cross-layer relationship design.
