# Network (Ethernet / Wi-Fi) Detailed Design

## Component
`network_ethernet_wifi`

## Purpose
Provides physical and link-layer network connectivity for local management, remote viewing, playback, telemetry, and device-cloud communication.

## Relationship overview
![Network (Ethernet / Wi-Fi) relationship](./network_ethernet_wifi_relationship.svg)

## Relevant system path

### Application Layer
- Live View
- Playback
- Device Config
- Mobile / Web UI
### System Services
- Network Service
- Device Management
### Middleware
- SSL / TLS
### HAL
- Network HAL
### Linux Kernel
- Network Driver
- Wi-Fi / BT Driver
### Hardware Platform
- Ethernet / Wi-Fi
- SoC / CPU

## Security context
- Device Identity
- TLS / mTLS
- Kernel Hardening
- Secure Boot

## Communication boundaries
- HAL Bus
- Kernel Bus
- Hardware Bus

## Dependency rules
- Hardware shall be accessed only through approved driver, HAL, and service ownership.
- Platform-specific behavior shall remain below the appropriate abstraction boundary.
- Upper layers shall consume declared capabilities rather than raw device details.

## Failure behavior
- link unavailable
- radio hardware fault
- interface reset

## Changelog
- 2026-10-04: Added detailed relationship design.
