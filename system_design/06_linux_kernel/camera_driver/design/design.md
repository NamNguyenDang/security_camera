# Camera Driver Detailed Design

## Component
`camera_driver`

## Purpose
Controls camera sensor/interface hardware and exposes the kernel-level device interface consumed by the Camera HAL.

## Relationship overview
![Camera Driver relationship](./camera_driver_relationship.svg)

## Relevant system path

### System Services
- Camera Service
- Media Service
### HAL
- Camera HAL
### Linux Kernel
- Camera Driver
### Hardware Platform
- Camera Sensor
- SoC / CPU

## Security context
- Secure Boot
- Kernel Hardening
- Root of Trust

## Communication boundaries
- HAL Bus
- Kernel Bus
- Hardware Bus

## Dependency rules
- Preserve the stable HAL/driver boundary.
- Keep vendor-specific behavior private to the owning lower layer.
- Do not expose direct hardware access to upper layers.

## Failure behavior
- sensor probe failure
- DMA/buffer failure
- hardware timeout

## Changelog
- 2026-10-03: Added detailed relationship design.
