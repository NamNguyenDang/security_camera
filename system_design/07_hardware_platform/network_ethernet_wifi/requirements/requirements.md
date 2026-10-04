# Network Hardware (Ethernet / Wi-Fi) Requirements — Platform Baseline v2

## Functional requirements
- NETWORK_ETHERNET_WIFI-FR-001: Product/Security Profile shall declare required and optional capabilities.
- NETWORK_ETHERNET_WIFI-FR-002: Hardware/provider shall satisfy documented qualification constraints.
- NETWORK_ETHERNET_WIFI-FR-003: Unsupported capability shall be detected before protected use.

## Interface requirements
- NETWORK_ETHERNET_WIFI-IR-001: Supplier-specific interfaces shall remain behind platform/provider adapters.
- NETWORK_ETHERNET_WIFI-IR-002: Capabilities and status exposed upward shall be provider-neutral.
- NETWORK_ETHERNET_WIFI-IR-003: Compatible driver/firmware/provider versions shall be recorded.

## Security requirements
- NETWORK_ETHERNET_WIFI-SR-001: Required protection outcomes shall be enforced independently of supplier choice.
- NETWORK_ETHERNET_WIFI-SR-002: Security-relevant lifecycle/fault state shall be auditable.

## Reliability requirements
- NETWORK_ETHERNET_WIFI-RR-001: Reset/power/provider failure behavior shall be documented.
- NETWORK_ETHERNET_WIFI-RR-002: Optional capability absence shall follow Product/Security Profile.

## Design acceptance criteria
- NETWORK_ETHERNET_WIFI-AC-001: A wired-only profile omits Wi-Fi hardware.
- NETWORK_ETHERNET_WIFI-AC-002: Transport-security policy remains unchanged when NIC/radio supplier changes.
- NETWORK_ETHERNET_WIFI-AC-003: Reset/power behavior satisfies declared product limits.
- NETWORK_ETHERNET_WIFI-AC-004: Upper Network Service receives provider-neutral capability/status.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
