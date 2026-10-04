# Security Camera Platform Architecture — Baseline v2

## Status

This document is the proposed **platform architecture baseline v2** for the Security Camera product.

Version 1 is intentionally preserved at:

`system_design/docs/security_camera_system_architecture_v1.svg`

Version 1 remains a historical architecture snapshot and lesson-learned reference. Version 2 does **not** replace or rewrite it.

## Why v2 exists

Version 1 was useful for decomposing the camera software stack into layers, but detailed design review exposed several limitations:

- it treated the Android-style application/framework stack too much like a universal product architecture;
- client, camera, site gateway, and cloud/backend deployments were not clearly separated;
- optional product capabilities such as display, audio, NPU, telephony, gateway, and backend were shown too much like mandatory dependencies;
- backend absence did not explicitly preserve local authentication, authorization, recording metadata, events, and recovery;
- storage responsibilities were too broad and mixed recording objects, structured metadata, and physical/platform storage;
- "bus" concepts were too generic and did not distinguish control calls, durable events, and high-bandwidth media data;
- Linux and specific technology choices appeared too close to product behavior rather than behind replaceable platform contracts.

Version 2 establishes a deployment-first, contract-first platform model.

## Core architecture principle

**Shared product behavior and middleware are the product core. Technology providers, operating systems, hardware suppliers, cloud providers, databases, media backends, security providers, and device drivers are replaceable through qualified contracts, adapters, and product profiles.**

## Deployment model

The product is divided into four separately reasoned deployments:

1. **Client Deployment**
   - Android, iOS, Web, and other supported clients.
   - Owns presentation and client interaction.
   - Uses client platform adapters for lifecycle, media presentation, notifications, and credential storage.
   - Does not inherit camera-device display, windowing, driver, or board assumptions.

2. **Camera Device**
   - Owns device-local capture, media, recording, inference, networking, device lifecycle, security enforcement, and standalone behavior.
   - Must remain valid when no backend or gateway is present.

3. **Optional Site Gateway**
   - A separately deployable site component.
   - May provide local aggregation, recording cache/relay, site-level event routing, local device management, offline backend proxy behavior, and site policy cache.
   - It is not treated as equivalent to the cloud backend.

4. **Optional Backend / Cloud**
   - May provide enterprise identity/policy source, fleet management, cloud recording repository, metadata/event repository, notification routing, remote management, analytics, and search.
   - Backend absence must not remove mandatory standalone camera capabilities.

## Product Profile

A **Product Profile** is a first-class cross-cutting architecture artifact.

A profile selects and constrains:

- supported capabilities;
- component placement;
- optional deployments;
- adapter/provider selections;
- compatible contract versions;
- hardware and operating-system targets;
- storage placement;
- security profile;
- offline/standalone behavior;
- product-specific performance and resource budgets.

Example profiles may include:

- standalone indoor camera;
- cloud-connected camera;
- gateway-managed multi-camera site;
- headless camera;
- camera with local display;
- camera with or without audio;
- camera with or without NPU acceleration.

Optional capability selection must not weaken mandatory security obligations.

## Standalone camera profile

A standalone camera must operate independently under a defined standalone profile.

When backend and gateway are absent, ownership is assigned as follows:

| Capability | Standalone owner |
| --- | --- |
| Device identity | Camera |
| Local user authentication | Camera |
| Authorization and permissions | Camera |
| Recording metadata | Camera metadata repository |
| Recording objects | Camera recording repository |
| Event generation and local event history | Camera |
| Configuration | Camera |
| Audit trail | Camera with bounded local retention |
| Recording protection and key access | Camera security services |
| Recovery after restart or power loss | Camera |
| Offline credential/session policy | Camera security policy |
| Remote client access | Direct camera connection when the product profile permits it |
| Backend synchronization | Optional when backend becomes available |

Backend IAM may remain the authoritative enterprise source for a connected profile, but the camera retains explicit local enforcement and offline behavior.

## Camera product services

The camera device contains product-owned services such as:

- Camera Service
- Media Service
- Recording Orchestration
- AI Inference Service
- Network Service
- Device Management
- local event handling
- local authorization enforcement
- local audit/security event handling

These services depend on stable product contracts rather than vendor-specific APIs.

## Device security

Security is explicit on the camera device, not only in the backend.

Required camera-side security responsibilities include:

- device authentication;
- local authorization enforcement;
- protected key access;
- recording/data protection;
- transport-security enforcement;
- security logging and audit;
- secure update/boot trust according to the selected security profile;
- safe offline behavior.

The exact security mechanisms and providers remain selectable, but the protection outcomes are mandatory where required by the product security profile.

## Platform adapters

Product-owned services use replaceable adapters and provider contracts such as:

- Capture Adapter
- Codec Adapter
- Inference Adapter
- Network Adapter
- Secure Transport Provider
- Secure Hardware Provider
- Optional Display Adapter
- Optional Audio Adapter

These adapters isolate supplier and operating-system details from product behavior.

## Persistence model

Persistence is split into three separate concerns.

### Recording Repository Contract

Owns recording objects and recording-specific semantics.

Possible implementations:

- camera-local recording store;
- gateway recording store;
- cloud object store.

Responsibilities may include recording object identity, segment lifecycle, durable completion, retrieval, retention coordination, and integrity status.

### Metadata Repository Contract

Owns structured metadata and query semantics.

Possible implementations:

- local embedded database;
- gateway repository;
- backend/cloud database.

Responsibilities may include events, recording metadata, indexes, configuration state, and schema/version behavior.

### Platform Storage Contract

Owns platform-level storage access and health.

Possible implementations:

- filesystem;
- block storage;
- eMMC;
- SSD;
- operating-system storage APIs.

It exposes storage capability, durability, health, power-loss, and error semantics upward without defining recording-domain behavior.

## Operating-System / Vendor Integration

The architecture does not require Linux as the universal platform.

The integration layer is defined as:

**Operating-System / Vendor Integration**

Possible selected implementations may include:

- Linux;
- Android-derived platform;
- RTOS;
- vendor operating system;
- supplier SDK/runtime;
- other qualified platform.

Linux remains a valid example and may be the selected implementation for a product, but it is not the portable product contract.

## Hardware qualification

Hardware is a qualified target rather than an application dependency.

Qualification areas include:

- SoC / CPU;
- camera sensor;
- NPU / AI accelerator;
- storage;
- Ethernet / Wi-Fi;
- audio;
- optional display;
- security provider;
- additional qualified peripherals.

Supplier replacement may require platform qualification while preserving upper product contracts.

## Communication model

Version 2 no longer treats every interaction as the same generic bus.

The architecture distinguishes:

### Command / service calls

Used for request/response control operations.

Examples:

- start capture;
- apply configuration;
- query recording metadata;
- request authorization decision.

### Control and state events

Used for non-durable state transitions and operational signaling.

Examples:

- connectivity changed;
- session disconnected;
- camera unavailable.

### Durable domain events

Used for events that require persistence, correlation, replay, or audit.

Examples:

- alarm event;
- recording completed;
- device ownership changed;
- security-relevant administration event.

### Media / high-bandwidth data paths

Used for video/audio frames and media streams.

These paths require explicit ownership, timing, buffering, backpressure/drop policy, latency, and copy constraints and must not be forced through a generic message bus.

### Platform contracts

Used between product services, middleware, adapters, operating-system integration, and hardware-specific implementations.

## Camera ↔ Gateway / Backend communication

Camera communication with gateway and backend is explicit.

Depending on the selected product profile, paths may include:

- device registration and ownership;
- management commands;
- desired/reported configuration;
- events and alarm state;
- audit/security events;
- recording upload or relay;
- metadata synchronization;
- live-view signaling;
- media relay;
- software/update state;
- health and telemetry.

The gateway and backend are modeled separately because they have different trust, availability, deployment, and operational responsibilities.

## Design rules for component PRs

Every detailed component design is expected to identify:

- deployment placement;
- product-owned responsibility;
- replaceable provider/adapter boundary;
- product-profile optionality;
- control path;
- event path;
- media/data path where applicable;
- trust boundaries;
- local/offline behavior;
- explicit failure behavior;
- globally unique requirement identifiers;
- decisions;
- open decisions;
- design-level acceptance criteria.

Relationship diagrams should show labeled directed interactions rather than only grouping components by layer.

## Requirement identifier rule

Requirement IDs must be globally unambiguous.

Examples:

- `LIVE_VIEW-FR-001`
- `ALARM-FR-001`
- `CAMERA_SERVICE-IR-001`
- `NETWORK_DRIVER-RR-001`
- `TRANSPORT_SECURITY-SR-001`
- `HW_BUS-IR-001`

## Architecture evolution

### Version 1

Version 1 captured the initial layered decomposition and was useful for exposing the major software/hardware areas.

### Version 2

Version 2 preserves the useful component decomposition while changing the architectural interpretation to:

- deployment-first;
- contract-first;
- product-profile driven;
- standalone-capable;
- supplier-replaceable;
- operating-system selectable;
- persistence-separated;
- security-explicit;
- data-plane aware.

The v1 artifact remains in the repository so future reviews can understand how and why the architecture evolved.

## Changelog

- 2026-10-04: Added platform architecture baseline v2. Preserved v1 unchanged as a lesson-learned architecture snapshot.
