---
title: "FAQ"
description: "Frequently asked questions about Nexus"
---

# Frequently Asked Questions

Common questions and answers about Nexus.

## General

### What is Nexus?

Nexus is a command-line tool that simplifies modern development workflows. It provides a unified interface for project initialization, development, testing, building, and deployment.

### Is Nexus free?

Yes, Nexus is open source and free to use under the MIT license.

### What platforms does Nexus support?

Nexus runs on:
- macOS (Apple Silicon & Intel)
- Linux (x64 & ARM64)
- Windows (x64)

### What languages/frameworks does Nexus support?

Nexus currently supports:
- JavaScript/TypeScript
- Node.js applications
- React/Vue/Svelte frontends
- Express/Fastify APIs

More language support is planned for future releases.

---

## Installation

### How do I update Nexus?

Using Homebrew:

```bash
brew upgrade nexus-cli/tap/nexus
```

Using npm:

```bash
npm update -g @nexus-cli/nexus
```

### I get a "command not found" error

Make sure Nexus is in your PATH:

```bash
which nexus
```

If nothing is returned, add the installation directory to your PATH or reinstall using one of the recommended methods.

### How do I uninstall Nexus?

Homebrew:

```bash
brew uninstall nexus
```

npm:

```bash
npm uninstall -g @nexus-cli/nexus
```

---

## Development

### How do I change the dev server port?

Use the `--port` flag:

```bash
nexus dev --port 4000
```

Or configure it in `nexus.config.js`:

```javascript
module.exports = {
  dev: {
    port: 4000,
  },
};
```

### Can I use Nexus with an existing project?

Yes! Run `nexus init` in your existing project directory:

```bash
cd my-existing-project
nexus init .
```

Nexus will detect your project structure and create a compatible configuration.

### How do I add environment variables?

Create a `.env` file in your project root:

```bash
DATABASE_URL=postgres://localhost/mydb
API_KEY=your-key-here
```

These are automatically loaded during development and build.

---

## Building

### Why is my build slow?

Common causes:

1. **Large dependencies** — Use `nexus build --analyze` to identify large bundles
2. **No caching** — Ensure `.nexus/cache` isn't git-ignored
3. **Unoptimized imports** — Use tree-shakeable imports

### How do I reduce bundle size?

1. Enable minification (on by default)
2. Use dynamic imports for large dependencies
3. Analyze your bundle with `--analyze`

```bash
nexus build --analyze
```

### Can I customize the build output?

Yes, in `nexus.config.js`:

```javascript
module.exports = {
  build: {
    outDir: 'build',
    target: 'node18',
    minify: true,
    sourcemap: false,
  },
};
```

---

## Deployment

### What platforms can I deploy to?

Nexus auto-detects and deploys to:
- Vercel
- Netlify
- Cloudflare Pages
- AWS Amplify

### How do I set up deployment?

Most platforms work automatically. Just run:

```bash
nexus deploy
```

Nexus will detect your platform from existing config files or prompt you to select one.

### How do I create a preview deployment?

```bash
nexus deploy --preview
```

This creates a unique URL for testing before production.

---

## Troubleshooting

### My changes aren't showing up

1. Clear the cache:

```bash
nexus cache clear
```

2. Restart the dev server:

```bash
nexus dev
```

### I'm getting a "module not found" error

Try reinstalling dependencies:

```bash
rm -rf node_modules
nexus add
```

### How do I report a bug?

Open an issue on [GitHub](https://github.com/nexus-cli/nexus/issues) with:
- Nexus version (`nexus --version`)
- Operating system
- Steps to reproduce
- Expected vs actual behavior

---

## Still have questions?

- Check the [GitHub Discussions](https://github.com/nexus-cli/nexus/discussions)
- Read the [API Reference](/docs/api/01-reference/)
- Review the [Contributing guide](/docs/91-contributing/)

