# Device Management Requirements — Platform Baseline v2

## Functional requirements
- DEVICE_MANAGEMENT-FR-001: The service shall preserve product semantics across local, gateway, and backend/provider selections where applicable.
- DEVICE_MANAGEMENT-FR-002: Product Profile shall declare placement, provider, compatible version, and offline policy.
- DEVICE_MANAGEMENT-FR-003: Lifecycle and recovery states shall be explicit.

## Interface requirements
- DEVICE_MANAGEMENT-IR-001: Product contracts shall not expose provider paths, SDK types, or hardware-specific details.
- DEVICE_MANAGEMENT-IR-002: Contract versions shall be validated before use.
- DEVICE_MANAGEMENT-IR-003: Local and remote implementations shall map errors to stable product-level status.

## Security requirements
- DEVICE_MANAGEMENT-SR-001: Protected operations shall enforce local authorization at the executing deployment.
- DEVICE_MANAGEMENT-SR-002: Credentials/keys shall be obtained through approved security contracts.
- DEVICE_MANAGEMENT-SR-003: Security-relevant state changes shall be auditable.

## Reliability requirements
- DEVICE_MANAGEMENT-RR-001: Offline behavior shall be explicitly defined.
- DEVICE_MANAGEMENT-RR-002: Recovery after restart/provider failure shall be deterministic.

## Design acceptance criteria
- DEVICE_MANAGEMENT-AC-001: Standalone camera can manage its local lifecycle without backend.
- DEVICE_MANAGEMENT-AC-002: Desired/reported state converges predictably after offline periods.
- DEVICE_MANAGEMENT-AC-003: Ownership transfer does not leave stale authorization.
- DEVICE_MANAGEMENT-AC-004: Retired device behavior is explicit and auditable.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
