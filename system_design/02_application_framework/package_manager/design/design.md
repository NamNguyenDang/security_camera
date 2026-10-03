# Package Manager Detailed Design

## Component

`package_manager`

## Purpose

Manages installed software package metadata, lifecycle, and package-level permissions using controlled storage and security policy.

## Relationship overview

![Package Manager relationship](./package_manager_relationship.svg)

## Relevant system path

### Application Layer
- Applications

### Application Framework
- Package Manager
- Activity Manager

### System Services
- Storage Service
- Device Management

### Middleware
- Database

### HAL
- Storage HAL

### Linux Kernel
- Storage Driver

### Hardware Platform
- Storage eMMC / SSD
- SoC / CPU

## Security context

- Security Policy
- IAM / RBAC
- Secure Boot
- Audit

## Communication boundaries

- Application Bus
- System Service Bus

## Dependency rules

- Use approved interfaces and buses; do not bypass owning layers.
- Keep lower-layer and vendor implementation details outside this component.
- Another component's private `src/` directory is not a dependency surface.

## Failure behavior

- invalid package
- storage failure
- policy rejection

## Open design items

- final API and data contract
- lifecycle and concurrency behavior
- performance and observability limits

## Changelog

- 2026-10-03: Added detailed relationship design.
