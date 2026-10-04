# Audio Hardware Requirements — Platform Baseline v2

## Functional requirements
- AUDIO-FR-001: Product/Security Profile shall declare required and optional capabilities.
- AUDIO-FR-002: Hardware/provider shall satisfy documented qualification constraints.
- AUDIO-FR-003: Unsupported capability shall be detected before protected use.

## Interface requirements
- AUDIO-IR-001: Supplier-specific interfaces shall remain behind platform/provider adapters.
- AUDIO-IR-002: Capabilities and status exposed upward shall be provider-neutral.
- AUDIO-IR-003: Compatible driver/firmware/provider versions shall be recorded.

## Security requirements
- AUDIO-SR-001: Required protection outcomes shall be enforced independently of supplier choice.
- AUDIO-SR-002: Security-relevant lifecycle/fault state shall be auditable.

## Reliability requirements
- AUDIO-RR-001: Reset/power/provider failure behavior shall be documented.
- AUDIO-RR-002: Optional capability absence shall follow Product/Security Profile.

## Design acceptance criteria
- AUDIO-AC-001: A video-only profile omits all camera audio hardware.
- AUDIO-AC-002: Microphone-only profile does not require speaker capability.
- AUDIO-AC-003: Audio supplier replacement preserves declared formats/timing after qualification.
- AUDIO-AC-004: Privacy-control capability required by profile is verified.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
