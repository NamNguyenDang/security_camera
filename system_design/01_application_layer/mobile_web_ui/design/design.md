# Mobile / Web UI Detailed Design — Platform Baseline v2

## Status
Revised against PR #77.

## Deployment placement
**Client only; Android/iOS/Web implementations with shared client contracts**

## Purpose and ownership
Re-scope as client presentation plus shared client contracts; camera-side display/windowing is not a dependency.

## Product-owned contract
ClientPresentation contract with platform adapters for lifecycle, media surface, notifications, secure credential storage, and native navigation.

## Relationship overview
![Mobile / Web UI relationship](./mobile_web_ui_relationship.svg)

## Review-driven decisions
- Android, iOS, and Web are separate client platforms sharing product contracts.
- Client hardware is distinct from camera hardware.
- Lifecycle/media-surface/notification/credential-storage behavior is implemented by client platform adapters.
- Camera Window Manager/View System are not remote-client dependencies.
- Headless cameras remain valid products.

## Interaction model
- product commands use versioned contracts;
- state and durable events are explicit;
- provider/platform details remain behind adapters;
- deployment transport is selected by Product Profile.

## Security
- authorization is enforced where the protected action occurs;
- standalone camera security remains explicit;
- credentials are held through approved client/device security providers;
- security-relevant actions are auditable.

## Decisions
- Client OS/hardware and camera OS/hardware are separate deployment concerns.
- Product Profile selects optional capabilities and placement.
- Private implementation directories are not dependency surfaces.

## Open decisions
- exact platform adapter technologies;
- product-specific retry, timeout, and resource budgets.

## Design acceptance criteria
1. The same product workflow can be implemented on Android, iOS, and Web without camera OS dependencies.
2. Remote client live view renders through native client media surfaces.
3. A headless camera works with remote clients.
4. Replacing client platform adapters does not change camera product contracts.

## Changelog
- 2026-10-04: Reworked for Platform Architecture Baseline v2 and review feedback.
