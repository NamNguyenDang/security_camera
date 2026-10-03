# Network (Ethernet / Wi-Fi)

## Layer

Hardware Platform

## Purpose

Provides physical and link-layer network connectivity.

## Main responsibility

Own this capability behind a clear component boundary and expose it through stable interfaces rather than leaking implementation details.

## Dependency direction

Dependencies should follow the approved layer model. Cross-layer shortcuts should be avoided unless explicitly documented and reviewed.

## Security considerations

Use approved cross-layer security services where applicable. Do not introduce unmanaged identity, secret, authorization, or cryptographic mechanisms.
