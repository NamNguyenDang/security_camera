# Audio HAL Detailed Design

## Component
`audio_hal`

## Purpose
Abstracts audio capture and playback hardware behind a stable product-owned interface.

## Relationship overview
![Audio HAL relationship](./audio_hal_relationship.svg)

## Relevant system path

### Application Layer
- Alarm
- Mobile / Web UI
### System Services
- Media Service
### Middleware
- Media Framework
### HAL
- Audio HAL
### Linux Kernel
- Audio Driver
### Hardware Platform
- Audio
- SoC / CPU

## Security context
- Secure HAL Interface
- Audit

## Communication boundaries
- Middleware Bus
- HAL Bus
- Kernel Bus

## Dependency rules
- Preserve the stable HAL/driver boundary.
- Keep vendor-specific behavior private to the owning lower layer.
- Do not expose direct hardware access to upper layers.

## Failure behavior
- audio device unavailable
- unsupported format
- driver error

## Changelog
- 2026-10-03: Added detailed relationship design.
