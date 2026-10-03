# Window Manager Detailed Design

## Component

`window_manager`

## Purpose

Owns application surfaces, focus, and window lifecycle while delegating rendering and hardware control to lower layers.

## Relationship overview

![Window Manager relationship](./window_manager_relationship.svg)

## Relevant system path

### Application Layer
- Live View
- Playback
- Settings

### Application Framework
- Window Manager
- View System
- Activity Manager

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

- Use approved interfaces and buses; do not bypass owning layers.
- Keep lower-layer and vendor implementation details outside this component.
- Another component's private `src/` directory is not a dependency surface.

## Failure behavior

- display unavailable
- surface allocation failure
- application termination

## Open design items

- final API and data contract
- lifecycle and concurrency behavior
- performance and observability limits

## Changelog

- 2026-10-03: Added detailed relationship design.
