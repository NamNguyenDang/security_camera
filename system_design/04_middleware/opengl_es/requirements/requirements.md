# OpenGL ES Adapter Requirements — Platform Baseline v2

## Functional requirements
- OPENGL_ES-FR-001: Product Profile shall declare whether this adapter is present.
- OPENGL_ES-FR-002: Portable behavior shall remain independent of selected provider implementation.
- OPENGL_ES-FR-003: Unsupported capability shall be reported deterministically.

## Interface requirements
- OPENGL_ES-IR-001: Provider-specific API types shall not escape the adapter boundary.
- OPENGL_ES-IR-002: Portable contracts shall be versioned and capability-aware.
- OPENGL_ES-IR-003: Provider replacement shall preserve defined product semantics.

## Security requirements
- OPENGL_ES-SR-001: Security-sensitive behavior shall follow the owning security profile/policy.
- OPENGL_ES-SR-002: Required protections shall not fall back to insecure modes.
- OPENGL_ES-SR-003: Security-relevant failures shall be auditable.

## Reliability requirements
- OPENGL_ES-RR-001: Provider loss or initialization failure shall map to stable product state.
- OPENGL_ES-RR-002: Optional capability absence shall remain a supported state.

## Design acceptance criteria
- OPENGL_ES-AC-001: Headless camera profile omits OpenGL ES.
- OPENGL_ES-AC-002: A client can use a different native graphics API without product contract changes.
- OPENGL_ES-AC-003: Local camera display can use OpenGL ES only when profile selects it.
- OPENGL_ES-AC-004: Unsupported rendering features produce stable capability status.

## Changelog
- 2026-10-04: Reworked with globally unique IDs for Platform Architecture Baseline v2.
