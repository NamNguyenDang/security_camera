# Kernel Hardening

## Area

Security Services — cross-layer

## Purpose

Reduces kernel attack surface and enforces kernel-level security controls.

## Main responsibility

Provide this security capability as a reusable system control so individual components do not implement incompatible security mechanisms independently.

## Architectural rule

Consumers should depend on the approved security interface or policy boundary. Hardware- or vendor-specific security implementations must remain behind an abstraction boundary.
