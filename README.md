# devops-devcontainer

Reproducible development environment for infrastructure automation and DevOps workflows.

This devcontainer provides a lightweight toolset for **linting, validation and automation**, including Ansible tooling, Dockerfile analysis and common CLI utilities.

## Features

- **Ansible tooling**: `ansible`, `ansible-lint`
- **Code quality**: `ruff`, `pylint`, `yamllint`, `shellcheck`
- **Dockerfile linting**: `hadolint`
- **CLI utilities**: `git`, `curl`, `jq`, `yq`, `make`

## Usage

Open the repository in **VS Code** and start the Dev Container.

```
Dev Containers: Reopen in Container
```

The environment will automatically build and provide all tools.

## Examples

Minimal examples demonstrating linting and validation tools are available in:

```
examples/
```

These examples illustrate typical checks that could run in a CI pipeline or used in your developement workflow.

## Documentation

- Tool description: `docs/TOOLS.md`
- Usage example: `examples/`
