# Kernel Bus Detailed Design

## Component
`kernel_bus`

## Purpose
Defines the approved **Internal Interfaces** communication boundary between **Linux Kernel** and **Hardware Platform**.

## Relationship overview
![Kernel Bus relationship](./kernel_bus_relationship.svg)

## Upper-side participants
- Camera Driver
- NPU Driver
- Display Driver
- USB Driver
- Storage Driver
- Network Driver
- Power Management

## Lower-side participants
- Camera Sensor
- NPU / AI Accelerator
- Display
- Storage eMMC / SSD
- Ethernet / Wi-Fi
- Other Peripherals

## Boundary responsibilities
- Define stable operations and ownership rules appropriate to Internal Interfaces.
- Validate capabilities, parameters, lifecycle state, and resource ownership.
- Return stable status/errors without leaking uncontrolled implementation details upward.
- Prevent direct bypass of the owning kernel, HAL, or hardware boundary.

## Security controls
- Secure Boot / Measured Boot
- Hardware Root of Trust
- Kernel Hardening
- Security Logging / Audit

## Failure behavior
- hardware device unavailable
- bus transaction failure
- device reset or timeout

## Open design items
- exact interface/protocol versioning and compatibility rules
- timeout, reset, and recovery behavior
- observability and fault-correlation identifiers
- power/lifecycle interaction across the boundary

## Changelog
- 2026-10-04: Added detailed communication-boundary design and relationship diagram.
