# Telephony Manager Detailed Design

## Component
`telephony_manager`

## Purpose
Provides a controlled abstraction for telephony capabilities when a product variant includes them, without coupling applications to modem-specific implementation.

## Relationship overview
![Telephony Manager relationship](./telephony_manager_relationship.svg)

## Relevant system path

### Application Layer
- Alarm
- Mobile / Web UI
### Application Framework
- Telephony Manager
- Notification Manager
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
- Other Peripherals
- SoC / CPU

## Security context
- IAM / RBAC
- Device Identity
- Audit

## Communication boundaries
- Application Bus
- System Service Bus
- Data Bus

## Dependency rules
- Use approved interfaces and buses.
- Keep lower-layer implementation details outside this component.
- Do not depend on another component's private `src/`.

## Failure behavior
- telephony unavailable
- network unavailable
- unsupported hardware variant

## Changelog
- 2026-10-03: Added detailed relationship design.
