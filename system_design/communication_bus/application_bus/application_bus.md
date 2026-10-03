# Application Bus

## Purpose

Provides the approved IPC / Binder communication boundary between the Application Layer and Application Framework.

## Connects

- Upper / consumer side: **Application Layer**
- Lower / provider side: **Application Framework**

## Communication rule

Components should use defined interfaces on this boundary rather than uncontrolled direct cross-layer dependencies.

## Linked security services

- `iam`
- `rbac`
- `device_identity`
- `security_logging_audit`
