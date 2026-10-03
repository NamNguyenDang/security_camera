# View System Detailed Design

## Component
`view_system`

## Purpose
Provides reusable UI view, layout, rendering, and interaction primitives to application components.

## Relationship overview
![View System relationship](./view_system_relationship.svg)

## Relevant system path

### Application Layer
- Live View
- Playback
- Alarm
- Settings
### Application Framework
- View System
- Window Manager
- Resource Manager
### Middleware
- OpenGL ES
- Vulkan
### HAL
- Display HAL
### Linux Kernel
- Display Driver
### Hardware Platform
- Display
- SoC / CPU

## Security context
- Security Policy
- Audit

## Communication boundaries
- Application Bus
- Middleware Bus
- HAL Bus

## Dependency rules
- Use approved interfaces and buses.
- Keep lower-layer implementation details outside this component.
- Do not depend on another component's private `src/`.

## Failure behavior
- rendering failure
- surface unavailable
- resource load failure

## Changelog
- 2026-10-03: Added detailed relationship design.
