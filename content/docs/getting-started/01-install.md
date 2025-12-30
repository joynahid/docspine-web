---
title: "Install"
description: "Install Nexus on macOS, Linux, or Windows"
---

# Installation

Nexus can be installed on macOS, Linux, and Windows. Choose your preferred method below.

## Homebrew (macOS & Linux)

The recommended way to install Nexus on macOS and Linux:

```bash
brew install nexus-cli/tap/nexus
```

## npm

Install globally via npm:

```bash
npm install -g @nexus-cli/nexus
```

## Binary Download

Download the latest release from [GitHub Releases](https://github.com/nexus-cli/nexus/releases).

### macOS (Apple Silicon)

```bash
curl -L https://github.com/nexus-cli/nexus/releases/latest/download/nexus-darwin-arm64.tar.gz | tar xz
sudo mv nexus /usr/local/bin/
```

### macOS (Intel)

```bash
curl -L https://github.com/nexus-cli/nexus/releases/latest/download/nexus-darwin-amd64.tar.gz | tar xz
sudo mv nexus /usr/local/bin/
```

### Linux

```bash
curl -L https://github.com/nexus-cli/nexus/releases/latest/download/nexus-linux-amd64.tar.gz | tar xz
sudo mv nexus /usr/local/bin/
```

### Windows

Download `nexus-windows-amd64.zip` from [releases](https://github.com/nexus-cli/nexus/releases) and add to your PATH.

## Verify Installation

Check that Nexus is installed correctly:

```bash
nexus --version
```

You should see output like:

```
nexus 2.4.1
```

## Shell Completions

Enable tab completions for your shell:

### Bash

```bash
nexus completion bash >> ~/.bashrc
```

### Zsh

```bash
nexus completion zsh >> ~/.zshrc
```

### Fish

```bash
nexus completion fish > ~/.config/fish/completions/nexus.fish
```

## Next Steps

Now that Nexus is installed, continue to the [Quick Start guide](/docs/getting-started/02-quickstart/) to create your first project.

