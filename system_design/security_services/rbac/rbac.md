# RBAC

## Area

Security Services — cross-layer

## Purpose

Provides Role-Based Access Control so permissions are assigned through defined roles rather than ad-hoc access.

## Main responsibility

Provide this security capability as a reusable system control so individual components do not implement incompatible security mechanisms independently.

## Architectural rule

Consumers should depend on the approved security interface or policy boundary. Hardware- or vendor-specific security implementations must remain behind an abstraction boundary.
