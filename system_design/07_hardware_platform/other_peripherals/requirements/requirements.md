# Qualified Peripheral Extensions Requirements — Platform Baseline v2

## Functional requirements
- OTHER_PERIPHERALS-FR-001: Product/Security Profile shall declare capability, placement, and provider selection.
- OTHER_PERIPHERALS-FR-002: Portable semantics shall remain independent of provider implementation.
- OTHER_PERIPHERALS-FR-003: Offline/unavailable-provider behavior shall be defined.

## Interface requirements
- OTHER_PERIPHERALS-IR-001: Contracts shall use provider-neutral identity/resource/capability references.
- OTHER_PERIPHERALS-IR-002: Policy/contract versions shall be explicit.
- OTHER_PERIPHERALS-IR-003: Provider-specific SDK/hardware details shall remain behind adapters.

## Security requirements
- OTHER_PERIPHERALS-SR-001: Protected actions shall be enforced at the execution boundary.
- OTHER_PERIPHERALS-SR-002: Revocation/failure/stale-policy behavior shall fail safely according to Security Profile.
- OTHER_PERIPHERALS-SR-003: Security-relevant decisions and failures shall be auditable.

## Reliability requirements
- OTHER_PERIPHERALS-RR-001: Backend/provider outage shall not create undefined authorization/security state.
- OTHER_PERIPHERALS-RR-002: Recovery/synchronization shall preserve stable product semantics.

## Design acceptance criteria
- OTHER_PERIPHERALS-AC-001: Unknown/unqualified peripherals do not become implicit product dependencies.
- OTHER_PERIPHERALS-AC-002: Each peripheral has a named adapter owner.
- OTHER_PERIPHERALS-AC-003: Supplier bus/register details are absent from shared middleware.
- OTHER_PERIPHERALS-AC-004: Removing an optional peripheral leaves common product behavior valid.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
