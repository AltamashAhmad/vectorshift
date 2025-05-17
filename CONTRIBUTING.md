# Contributing to VectorShift

Thank you for your interest in contributing to the VectorShift project! This document provides guidelines for contributing to this repository.

## Git Workflow

### Commit Message Conventions

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification for commit messages. This leads to more readable messages that are easy to follow when looking through the project history.

Each commit message should be structured as follows:
```
<type>(<scope>): <subject>

<body>

<footer>
```

#### Types
* **feat**: A new feature
* **fix**: A bug fix
* **docs**: Documentation changes
* **style**: Changes that do not affect the meaning of the code (white-space, formatting, etc)
* **refactor**: Code changes that neither fixes a bug nor adds a feature
* **perf**: Changes that improve performance
* **test**: Adding missing tests or correcting existing tests
* **chore**: Changes to the build process or auxiliary tools

#### Examples

```
feat(frontend): Add HubSpot integration UI component

Implement React component for HubSpot OAuth integration with popup window handling
```

```
fix(backend): Correct state handling in OAuth callback

Fix issue where state parameter was not being properly validated in callback
```

```
docs: Update README with setup instructions

Add comprehensive documentation for installation and configuration
```

## Pull Request Process

1. Ensure any install or build dependencies are removed before the end of the layer when doing a build
2. Update the README.md with details of changes to the interface, including new environment variables, exposed ports, useful file locations and container parameters
3. Increase the version numbers in any examples files and the README.md to the new version that this Pull Request would represent
4. The Pull Request will be merged once it receives approval from maintainers

## Code Style

* **Python**: Follow PEP 8 style guide
* **JavaScript**: Follow the ESLint configuration in the project

## Setting Up Development Environment

Please refer to the README.md for instructions on setting up your development environment. 