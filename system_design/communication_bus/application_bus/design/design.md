# Application Bus Detailed Design

## Component
`application_bus`

## Purpose
Defines the approved **IPC / Binder** communication boundary between **Application Layer** and **Application Framework**.

## Relationship overview
![Application Bus relationship](./application_bus_relationship.svg)

## Upper-side participants
- Live View
- Playback
- Alarm
- Settings
- User Management
- Event Search
- Device Config
- Mobile / Web UI

## Lower-side participants
- Activity Manager
- Window Manager
- Content Providers
- Resource Manager
- Notification Manager
- View System

## Boundary responsibilities
- Define stable request, response, event, message, or stream contracts appropriate to IPC / Binder.
- Validate input crossing the boundary.
- Preserve ownership and lifecycle rules for transferred resources.
- Return stable errors without leaking implementation-specific details.
- Prevent uncontrolled direct dependencies that bypass this boundary.

## Security controls
- IAM
- RBAC
- Device Identity
- Security Logging / Audit

## Failure behavior
- endpoint unavailable
- message validation failure
- permission denied

## Open design items
- exact interface definition language and versioning policy
- timeout, retry, flow-control, and backpressure behavior
- observability and tracing identifiers
- compatibility rules during rolling software updates

## Changelog
- 2026-10-04: Added detailed communication-boundary design and relationship diagram.
