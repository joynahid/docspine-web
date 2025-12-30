---
title: "Contributing"
description: "How to contribute to Nexus"
---

# Contributing

Thank you for your interest in contributing to Nexus! This guide will help you get started.

## Code of Conduct

Please read and follow our [Code of Conduct](https://github.com/nexus-cli/nexus/blob/main/CODE_OF_CONDUCT.md). We're committed to providing a welcoming and inclusive experience for everyone.

## Ways to Contribute

### Report Bugs

Found a bug? Please [open an issue](https://github.com/nexus-cli/nexus/issues/new) with:

- Clear description of the problem
- Steps to reproduce
- Expected behavior
- Actual behavior
- Nexus version (`nexus --version`)
- Operating system and version

### Suggest Features

Have an idea? [Start a discussion](https://github.com/nexus-cli/nexus/discussions/new) to propose new features. Please search existing discussions first to avoid duplicates.

### Improve Documentation

Documentation improvements are always welcome. You can:

- Fix typos or unclear explanations
- Add examples
- Improve guides

Click "Edit on GitHub" on any page to suggest changes.

### Submit Code

Ready to code? Here's how to contribute:

## Development Setup

### Prerequisites

- Rust 1.70+
- Node.js 18+
- Git

### Clone the Repository

```bash
git clone https://github.com/nexus-cli/nexus.git
cd nexus
```

### Install Dependencies

```bash
cargo build
npm install
```

### Run Tests

```bash
cargo test
npm test
```

### Run Locally

```bash
cargo run -- dev
```

## Submitting Changes

### 1. Fork the Repository

Click "Fork" on GitHub to create your own copy.

### 2. Create a Branch

```bash
git checkout -b feature/my-feature
# or
git checkout -b fix/my-bugfix
```

### 3. Make Your Changes

- Follow existing code style
- Add tests for new functionality
- Update documentation if needed

### 4. Commit Your Changes

We use [Conventional Commits](https://www.conventionalcommits.org/):

```bash
git commit -m "feat: add new template option"
git commit -m "fix: resolve path handling on Windows"
git commit -m "docs: clarify installation steps"
```

Types:
- `feat` — New feature
- `fix` — Bug fix
- `docs` — Documentation
- `refactor` — Code refactoring
- `test` — Tests
- `chore` — Maintenance

### 5. Push and Create PR

```bash
git push origin feature/my-feature
```

Then open a Pull Request on GitHub.

## Pull Request Guidelines

### Before Submitting

- [ ] Tests pass (`cargo test && npm test`)
- [ ] Code is formatted (`cargo fmt`)
- [ ] No linting errors (`cargo clippy`)
- [ ] Documentation updated if needed
- [ ] Commit messages follow conventional commits

### PR Description

Include:
- What the PR does
- Why it's needed
- How to test it
- Screenshots (for UI changes)

### Review Process

1. Maintainers will review your PR
2. Address any feedback
3. Once approved, a maintainer will merge

## Project Structure

```
nexus/
├── src/
│   ├── commands/    # CLI commands
│   ├── config/      # Configuration handling
│   ├── core/        # Core functionality
│   └── main.rs      # Entry point
├── tests/           # Integration tests
├── docs/            # Documentation site
└── packages/        # npm packages
```

## Getting Help

- [GitHub Discussions](https://github.com/nexus-cli/nexus/discussions) — Questions and ideas
- [GitHub Issues](https://github.com/nexus-cli/nexus/issues) — Bug reports

## Recognition

Contributors are recognized in:
- Release notes
- [Contributors page](https://github.com/nexus-cli/nexus/graphs/contributors)

Thank you for contributing to Nexus!

