# Device Config Detailed Design

## Component

`device_config`

## Purpose

provides user-facing device configuration while delegating validation, policy enforcement, persistence, and hardware-specific effects to owning lower layers.

## Relationship overview

![Device Config relationship](./device_config_relationship.svg)

## Relevant system path

### Application Layer
- Device Config
- Settings
- Mobile / Web UI

### Application Framework
- Content Providers
- Notification Manager

### System Services
- Device Management
- Network Service
- Storage Service

### Middleware
- Database
- SSL / TLS

### HAL
- Camera HAL
- Network HAL
- Storage HAL

### Linux Kernel
- Camera Driver
- Network Driver
- Storage Driver

### Hardware Platform
- Camera Sensor
- Ethernet / Wi-Fi
- Storage eMMC / SSD
- SoC / CPU

## Communication boundaries

- Application Bus
- System Service Bus
- Data Bus
- HAL Bus

## Security context

- IAM / RBAC
- Security Policy Enforcement
- Device Identity
- Audit

## Dependency rules

- Use approved APIs and buses rather than bypassing layer ownership.
- Application logic shall not absorb lower-layer implementation responsibilities.
- Vendor-specific details remain behind the owning abstraction boundary.
- Another component's private `src/` directory is not a supported dependency surface.

## Failure behavior

- unsupported option
- device busy
- policy rejection
- partial apply failure

## Open detailed-design topics

- final API contract and data model
- timing, concurrency, and lifecycle behavior
- observability and audit events
- component-specific performance limits

## Changelog

- 2026-10-03: Added component-specific detailed design and relationship diagram.
