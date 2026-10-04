# Storage Hardware (eMMC / SSD) Requirements — Platform Baseline v2

## Functional requirements
- STORAGE_EMMC_SSD-FR-001: Product Profile shall declare whether the hardware capability is required or optional.
- STORAGE_EMMC_SSD-FR-002: Hardware shall satisfy measurable qualification constraints.
- STORAGE_EMMC_SSD-FR-003: Unsupported/incompatible hardware shall fail qualification before release.

## Interface requirements
- STORAGE_EMMC_SSD-IR-001: Supplier-specific interfaces shall remain behind the platform adapter/driver.
- STORAGE_EMMC_SSD-IR-002: Capability and health/status exposed upward shall be provider-neutral.
- STORAGE_EMMC_SSD-IR-003: Compatible board/driver/adapter versions shall be recorded.

## Security requirements
- STORAGE_EMMC_SSD-SR-001: Hardware security/privacy obligations shall follow the selected security profile.
- STORAGE_EMMC_SSD-SR-002: Relevant integrity/security faults shall be surfaced for audit/recovery.

## Reliability requirements
- STORAGE_EMMC_SSD-RR-001: Reset/power-loss/fault behavior shall be documented and testable.
- STORAGE_EMMC_SSD-RR-002: Replacement hardware shall preserve the upper portable contract after qualification.

## Design acceptance criteria
- STORAGE_EMMC_SSD-AC-001: Storage device meets profile capacity/endurance targets.
- STORAGE_EMMC_SSD-AC-002: Power-loss guarantee is documented and testable.
- STORAGE_EMMC_SSD-AC-003: Hardware health degradation is observable through Platform Storage contract.
- STORAGE_EMMC_SSD-AC-004: Changing storage supplier does not alter Recording Repository semantics.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
