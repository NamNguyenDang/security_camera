# Device Identity

## Area

Security Services — cross-layer

## Purpose

Provides unique device identity based on certificates and protected cryptographic keys.

## Main responsibility

Provide this security capability as a reusable system control so individual components do not implement incompatible security mechanisms independently.

## Architectural rule

Consumers should depend on the approved security interface or policy boundary. Hardware- or vendor-specific security implementations must remain behind an abstraction boundary.
