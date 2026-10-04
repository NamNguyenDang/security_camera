# Network (Ethernet / Wi-Fi) Requirements

## Component
`network_ethernet_wifi`

## Functional requirements
- NEW-FR-001: The hardware component shall provide supported wired and wireless connectivity.
- NEW-FR-002: The hardware component shall report physical/link status.
- NEW-FR-003: The hardware component shall support approved interface power states.
- NEW-FR-004: The hardware component shall expose required hardware capabilities to drivers.

## Interface requirements
- NEW-IR-001: Interact through approved hardware, driver, and HAL interfaces.
- NEW-IR-002: Advertise only supported capabilities and status.

## Security requirements
- NEW-SR-001: Participate in approved boot, trust, identity, and protection mechanisms where applicable.
- NEW-SR-002: Surface security-relevant status and failures to the owning driver or service.

## Reliability requirements
- NEW-RR-001: Provide defined behavior for link unavailable.
- NEW-RR-002: Provide defined behavior for radio hardware fault.
- NEW-RR-003: Provide defined behavior for interface reset.

## Changelog
- 2026-10-04: Added detailed requirements baseline.
