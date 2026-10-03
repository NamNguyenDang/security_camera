# NPU Driver Detailed Design

## Component
`npu_driver`

## Purpose
Controls the neural-processing accelerator and exposes the kernel interface consumed by the AI/NPU HAL.

## Relationship overview
![NPU Driver relationship](./npu_driver_relationship.svg)

## Relevant system path

### System Services
- AI Inference Service
### Middleware
- AI Runtime
### HAL
- AI / NPU HAL
### Linux Kernel
- NPU Driver
### Hardware Platform
- NPU / AI Accelerator
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
- Expose only approved kernel interfaces upward.
- Keep hardware-specific implementation private to the driver.
- Do not allow user/application layers to bypass HAL/service ownership.

## Failure behavior
- accelerator probe failure
- execution timeout
- memory mapping failure

## Changelog
- 2026-10-03: Added detailed relationship design.
