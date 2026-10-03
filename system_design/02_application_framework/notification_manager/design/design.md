# Notification Manager Detailed Design

## Component
`notification_manager`

## Purpose
Coordinates system and application notifications and routes them to approved presentation or alert channels.

## Relationship overview
![Notification Manager relationship](./notification_manager_relationship.svg)

## Relevant system path

### Application Layer
- Alarm
- Settings
- Mobile / Web UI
### Application Framework
- Notification Manager
- View System
### System Services
- Device Management
- Network Service
### Middleware
- Database
- SSL / TLS
### HAL
- Audio HAL
- Display HAL
### Linux Kernel
- Audio Driver
- Display Driver
### Hardware Platform
- Audio
- Display
- SoC / CPU

## Security context
- IAM / RBAC
- Security Policy
- Audit

## Communication boundaries
- Application Bus
- System Service Bus

## Dependency rules
- Use approved interfaces and buses.
- Keep lower-layer implementation details outside this component.
- Do not depend on another component's private `src/`.

## Failure behavior
- channel unavailable
- duplicate notification
- policy suppression

## Changelog
- 2026-10-03: Added detailed relationship design.
