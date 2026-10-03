# Live View

## Layer

Application Layer

## Purpose

Presents live camera video to users and provides the entry point for real-time viewing.

## Main responsibility

Own this capability behind a clear component boundary and expose it through stable interfaces rather than leaking implementation details.

## Dependency direction

Dependencies should follow the approved layer model. Cross-layer shortcuts should be avoided unless explicitly documented and reviewed.

## Security considerations

Use approved cross-layer security services where applicable. Do not introduce unmanaged identity, secret, authorization, or cryptographic mechanisms.
