# Secrets / Key Management Detailed Design

## Component
`secrets_key_management`

## Purpose
Controls generation, storage, retrieval, rotation, revocation, and use of secrets and cryptographic keys across the platform.

## Relationship overview
![Secrets / Key Management relationship](./secrets_key_management_relationship.svg)

## Cross-layer relationship

### Application Layer
- User Management
- Device Config
### System Services
- Device Management
- Network Service
- Storage Service
### Middleware
- SSL / TLS
- Database
- Encryption Services
### HAL
- Secure HAL Interface
### Hardware Platform
- Security Chip / TPM
- SoC / CPU

## Related security services
- Hardware Root of Trust
- Device Identity
- Device Provisioning
- Audit

## Communication / enforcement boundaries
- System Service Bus
- Data Bus
- Middleware Bus
- HAL Bus

## Design rules
- Consumers shall use approved security interfaces rather than implement private alternatives.
- Protected keys, measurements, or trust state shall remain behind the owning secure boundary.
- Security failures shall fail safely and preserve auditability.

## Failure behavior
- protected key store unavailable
- rotation failure
- revoked or expired key

## Changelog
- 2026-10-04: Added detailed cross-layer relationship design.
