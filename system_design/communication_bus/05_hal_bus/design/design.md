# HAL Bus Detailed Design

## Component
`hal_bus`

## Purpose
Defines the approved **Standard Interfaces** communication boundary between **Hardware Abstraction Layer** and **Linux Kernel**.

## Relationship overview
![HAL Bus relationship](./hal_bus_relationship.svg)

## Upper-side participants
- Camera HAL
- AI / NPU HAL
- Audio HAL
- Display HAL
- Storage HAL
- Network HAL

## Lower-side participants
- Camera Driver
- NPU Driver
- Audio Driver
- Display Driver
- Storage Driver
- Network Driver

## Boundary responsibilities
- Define stable operations and ownership rules appropriate to Standard Interfaces.
- Validate capabilities, parameters, lifecycle state, and resource ownership.
- Return stable status/errors without leaking uncontrolled implementation details upward.
- Prevent direct bypass of the owning kernel, HAL, or hardware boundary.

## Security controls
- Secure HAL Interface
- Device Identity
- Secure Boot / Measured Boot
- Secrets / Key Management

## Failure behavior
- driver unavailable
- unsupported capability
- kernel interface mismatch

## Open design items
- exact interface/protocol versioning and compatibility rules
- timeout, reset, and recovery behavior
- observability and fault-correlation identifiers
- power/lifecycle interaction across the boundary

## Changelog
- 2026-10-04: Added detailed communication-boundary design and relationship diagram.
