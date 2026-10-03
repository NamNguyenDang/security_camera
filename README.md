# Security Camera Design

System-design and implementation workspace for a modular security-camera platform.

## Design principles

- Small, explicit component responsibilities.
- Stable interfaces and APIs instead of direct implementation coupling.
- Controlled dependency direction across layers.
- Vendor implementations hidden behind abstraction boundaries.
- Components independently buildable and testable where practical.
- Cybersecurity treated as a cross-layer concern.
- Documentation, configuration, source, tests, and security evidence stay close to the component that owns them.
- Git-friendly structure and review through pull requests.

See [system_design/README.md](system_design/README.md).
