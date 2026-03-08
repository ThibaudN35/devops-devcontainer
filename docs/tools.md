# Tools

This devcontainer provides a lightweight set of tools commonly used in
DevOps workflows for static analysis, automation, and scripting.

The goal is to provide a consistent environment for linting, validation,
and development tasks.

---

## Ansible

### ansible

Automation tool used to manage infrastructure and configuration.

Example:

```
ansible-playbook playbook.yml
```

Documentation: https://docs.ansible.com/

### ansible-lint

Checks Ansible playbooks against best practices.

Example:

```
ansible-lint playbook.yml
```

Documentation: https://ansible-lint.readthedocs.io/

## YAML

### yamllint

Linter for YAML files used to detect syntax errors and enforce style rules.

Example:

```
yamllint playbook.yml
```

Documentation: https://yamllint.readthedocs.io/

## Python

### pylint

Static analysis tool for Python code that detects errors and potential issues.

Example:

```
pylint main.py
```

Documentation: https://pylint.readthedocs.io/

### ruff

Fast Python linter and formatter.

Example:

```
ruff check main.py
```

## Shell

### shellcheck

Static analysis tool for shell scripts.

Example:

```
shellcheck script.sh
```

Documentation: https://www.shellcheck.net/

## Docker

### hadolint

Linter for Dockerfiles that helps enforce best practices and security
recommendations.

Example:

```
hadolint Dockerfile
```

Documentation: https://github.com/hadolint/hadolint

## CLI utilities

The devcontainer also includes useful command line tools commonly used
in scripting and automation.

### jq

Command-line JSON processor.

Example:

```
jq '.name' file.json
```

Documentation: https://jqlang.github.io/jq/

### yq

Command-line YAML processor.

Example:

```
yq '.name' file.yaml
```

Documentation: https://mikefarah.gitbook.io/yq/

### curl

Tool for transferring data from or to a server using various protocols.

Example:

```
curl https://example.com
```

Documentation: https://curl.se/docs/

### git

Distributed version control system.

Example:

```
git status
```

Documentation: https://git-scm.com/doc

### make

Build automation tool commonly used to run development tasks.

Example:

```
make lint
```

Documentation: https://www.gnu.org/software/make/