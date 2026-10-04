# Security Chip (TPM / HSM) Requirements

## Component
`security_chip_tpm_hsm`

## Functional requirements
- SCTH-FR-001: The hardware component shall protect hardware-backed keys.
- SCTH-FR-002: The hardware component shall perform supported trusted cryptographic operations.
- SCTH-FR-003: The hardware component shall provide required measurements or attestation data.
- SCTH-FR-004: The hardware component shall report chip health and availability.

## Interface requirements
- SCTH-IR-001: Interact through approved hardware, driver, and HAL interfaces.
- SCTH-IR-002: Advertise only supported capabilities and status.

## Security requirements
- SCTH-SR-001: Participate in approved boot, trust, identity, and protection mechanisms where applicable.
- SCTH-SR-002: Surface security-relevant status and failures to the owning driver or service.

## Reliability requirements
- SCTH-RR-001: Provide defined behavior for security chip unavailable.
- SCTH-RR-002: Provide defined behavior for key operation failure.
- SCTH-RR-003: Provide defined behavior for measurement or attestation failure.

## Changelog
- 2026-10-04: Added detailed requirements baseline.
