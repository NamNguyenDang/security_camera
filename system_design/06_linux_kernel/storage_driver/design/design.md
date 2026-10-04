# Storage Driver / Platform Integration Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Camera OS/vendor storage integration**

## Purpose and ownership
Retain as platform storage integration while clearly separating block-driver guarantees from filesystem behavior and recording-repository semantics.

## Integration contract
Platform storage driver guarantees for write completion, power-loss behavior, error/health reporting, reset, and recovery signals.

## Relationship overview
![Storage Driver / Platform Integration relationship](./storage_driver_relationship.svg)

## Review-driven decisions
- Recording Repository stays independent of Linux/block driver.
- Filesystem responsibilities are separate from block driver.
- Write durability/power-loss semantics are explicit.
- Health information and recovery ownership are defined.
- Upper storage contract does not expose driver details.

## Product Profile inputs
- capability optionality and permitted devices/modes;
- OS/vendor/board selection;
- compatible driver/firmware versions;
- reset, resource, power, and security limits.

## Platform qualification
The integration is qualified against the portable adapter above it. Generic OS/upstream facilities are reused when they satisfy required behavior.

## Security
- raw device access remains below OS isolation;
- attached/peripheral resources follow explicit trust/resource policy where applicable;
- security-relevant device faults are auditable.

## Design acceptance criteria
1. Recording repository can move to another platform storage implementation without domain changes.
2. Power loss has documented persistence guarantees.
3. I/O failure and health degradation map to stable Platform Storage status.
4. Driver replacement does not alter recording object identity semantics.

## Open decisions
- selected OS/vendor driver;
- board-specific numerical limits.

## Changelog
- 2026-10-04: Re-scoped as OS/vendor integration for Platform Architecture Baseline v2.
