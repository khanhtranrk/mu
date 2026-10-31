# Shared MU documentation

This directory is reserved for cross-repository architecture, integration contracts and decisions that concern both MU components. Keep implementation-specific documentation in the owning repository.

## Canonical references

- [MU CLI specification and execution](../mu-cli/docs/spec-format/README.md)
- [MU CLI README](../mu-cli/README.md)
- [MasterFlow architecture and data model](../mu-masterflow/docs/architecture.md)
- [MasterFlow YAML spec editor](../mu-masterflow/docs/spec-yaml.md)
- [MasterFlow worker HTTP hooks](../mu-masterflow/docs/worker-hooks.md)
- [MasterFlow request artifacts](../mu-masterflow/docs/request-artifacts.md)
- [MasterFlow development](../mu-masterflow/docs/development.md)

When changing shared YAML semantics or worker HTTP contracts, check both repositories for compatibility and update the relevant canonical docs rather than copying them here.
