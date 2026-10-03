# Display HAL Detailed Design

## Component
`display_hal`

## Purpose
Abstracts display and rendering hardware capabilities from middleware and framework consumers.

## Relationship overview
![Display HAL relationship](./display_hal_relationship.svg)

## Relevant system path

### Application Layer
- Live View
- Playback
- Mobile / Web UI
### Application Framework
- View System
- Window Manager
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
- Secure HAL Interface
- Kernel Hardening

## Communication boundaries
- Middleware Bus
- HAL Bus
- Kernel Bus

## Dependency rules
- Preserve the stable HAL/driver boundary.
- Keep vendor-specific behavior private to the owning lower layer.
- Do not expose direct hardware access to upper layers.

## Failure behavior
- display unavailable
- unsupported mode
- driver error

## Changelog
- 2026-10-03: Added detailed relationship design.
