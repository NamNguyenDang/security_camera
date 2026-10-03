# Location Manager

## Layer

Application Framework

## Purpose

Provides controlled access to location capabilities when the platform supports or requires them.

## Main responsibility

Own this capability behind a clear component boundary and expose it through stable interfaces rather than leaking implementation details.

## Dependency direction

Dependencies should follow the approved layer model. Cross-layer shortcuts should be avoided unless explicitly documented and reviewed.

## Security considerations

Use approved cross-layer security services where applicable. Do not introduce unmanaged identity, secret, authorization, or cryptographic mechanisms.
