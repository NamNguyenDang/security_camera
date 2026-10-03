# Vulkan Detailed Design

## Component
`vulkan`

## Purpose
Provides explicit low-level graphics and compute primitives where high-performance rendering or compute control is required.

## Relationship overview
![Vulkan relationship](./vulkan_relationship.svg)

## Relevant system path

### Application Layer
- Live View
- Playback
### Application Framework
- View System
- Window Manager
### Middleware
- Vulkan
### HAL
- Display HAL
### Linux Kernel
- Display Driver
### Hardware Platform
- Display
- SoC / CPU

## Security context
- Kernel Hardening
- Security Policy

## Communication boundaries
- Middleware Bus
- HAL Bus
- Kernel Bus

## Dependency rules
- Keep the public contract stable and implementation private.
- Keep vendor-specific behavior behind the abstraction boundary.
- Do not depend on another component's private `src/`.

## Failure behavior
- device lost
- resource allocation failure
- unsupported feature

## Changelog
- 2026-10-03: Added detailed relationship design.
