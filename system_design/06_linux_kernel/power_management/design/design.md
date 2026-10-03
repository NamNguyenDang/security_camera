# Power Management Detailed Design

## Component
`power_management`

## Purpose
Coordinates kernel-level power states, suspend/resume, clocks, and device power controls for the camera platform.

## Relationship overview
![Power Management relationship](./power_management_relationship.svg)

## Relevant system path

### System Services
- Device Management
- Camera Service
- Network Service
### Linux Kernel
- Power Management
- Device Drivers
### Hardware Platform
- SoC / CPU
- Camera Sensor
- NPU / AI Accelerator
- Storage eMMC / SSD
- Other Peripherals

## Security context
- Secure Boot
- Kernel Hardening
- Audit

## Communication boundaries
- Kernel Bus
- Hardware Bus

## Dependency rules
- Expose only approved kernel interfaces upward.
- Keep hardware-specific behavior private to the driver or power subsystem.
- Upper layers shall not bypass HAL/service ownership.

## Failure behavior
- resume failure
- device refuses suspend
- thermal or power constraint

## Changelog
- 2026-10-03: Added detailed relationship design.
