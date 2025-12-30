---
title: "Basic Usage"
description: "Learn the fundamental Nexus commands and workflows"
---

This guide covers the essential commands and workflows you'll use daily with Nexus.

## Project Lifecycle

Every Nexus project follows a simple lifecycle:

1. **Initialize** — Create a new project
2. **Develop** — Write code with hot reload
3. **Test** — Run your test suite
4. **Build** — Create production bundle
5. **Deploy** — Ship to production

## Working with Commands

### Getting Help

View all available commands:

```bash
nexus --help
```

Get help for a specific command:

```bash
nexus init --help
```

### Command Structure

All Nexus commands follow this pattern:

```bash
nexus <command> [subcommand] [options] [arguments]
```

Examples:

```bash
nexus init my-app              # Create new project
nexus dev --port 4000          # Dev server on port 4000
nexus build --minify           # Build with minification
nexus deploy --preview         # Preview deployment
```

## Environment Variables

Nexus reads environment variables from `.env` files:

```bash
# .env
DATABASE_URL=postgres://localhost/mydb
API_KEY=sk_live_xxx
```

Access in your code:

```javascript
const db = connect(process.env.DATABASE_URL);
```

### Environment-specific files

Nexus loads environment files in order:

1. `.env` — Default values
2. `.env.local` — Local overrides (git-ignored)
3. `.env.development` — Development only
4. `.env.production` — Production only

## Working with Dependencies

### Adding packages

```bash
nexus add lodash
nexus add -D vitest   # Dev dependency
```

### Removing packages

```bash
nexus remove lodash
```

### Updating packages

```bash
nexus update           # Update all
nexus update lodash    # Update specific
```

## Scripts

Define custom scripts in `nexus.config.js`:

```javascript
module.exports = {
  scripts: {
    lint: 'eslint src/',
    format: 'prettier --write src/',
    typecheck: 'tsc --noEmit',
  },
};
```

Run with:

```bash
nexus run lint
nexus run format
```

## Workspaces (Monorepo)

For monorepo setups, define workspaces:

```javascript
// nexus.config.js
module.exports = {
  workspaces: [
    'packages/*',
    'apps/*',
  ],
};
```

Run commands across all packages:

```bash
nexus test --all          # Test everything
nexus build --all         # Build everything
nexus run lint --all      # Lint everything
```

Or target specific packages:

```bash
nexus test --filter=@myorg/api
nexus build --filter=web-app
```

## Caching

Nexus caches build artifacts for faster subsequent builds:

```bash
nexus build              # First build: 12s
nexus build              # Cached build: 0.8s
```

Clear the cache if needed:

```bash
nexus cache clear
```

## Debugging

### Verbose output

Enable detailed logging:

```bash
nexus build --verbose
```

### Debug mode

For troubleshooting:

```bash
DEBUG=nexus:* nexus build
```

### Inspect config

View resolved configuration:

```bash
nexus config show
```

## Next Steps

- Explore specific guides for your use case
- Check the [API Reference](/docs/api/01-reference/) for all options
- Visit the [FAQ](/docs/90-faq/) for common issues

