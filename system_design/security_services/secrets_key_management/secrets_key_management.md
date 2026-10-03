# Secrets / Key Management

## Area

Security Services — cross-layer

## Purpose

Controls the lifecycle, storage, rotation, and use of secrets and cryptographic keys.

## Main responsibility

Provide this security capability as a reusable system control so individual components do not implement incompatible security mechanisms independently.

## Architectural rule

Consumers should depend on the approved security interface or policy boundary. Hardware- or vendor-specific security implementations must remain behind an abstraction boundary.
