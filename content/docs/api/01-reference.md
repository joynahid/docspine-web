---
title: "Reference"
description: "Complete command reference for Nexus CLI"
---

# API Reference

Complete documentation for all Nexus commands.

## nexus init

Initialize a new Nexus project.

```bash
nexus init [name] [options]
```

### Arguments

| Argument | Description |
|----------|-------------|
| `name` | Project name (optional, defaults to current directory) |

### Options

| Option | Description |
|--------|-------------|
| `-t, --template <name>` | Use a specific template |
| `--no-git` | Skip git initialization |
| `--no-install` | Skip dependency installation |
| `-y, --yes` | Accept all defaults |

### Examples

```bash
# Interactive setup
nexus init my-app

# Use specific template
nexus init my-api --template api

# Quick setup with defaults
nexus init my-app -y
```

---

## nexus dev

Start the development server with hot reload.

```bash
nexus dev [options]
```

### Options

| Option | Description | Default |
|--------|-------------|---------|
| `-p, --port <number>` | Server port | `3000` |
| `-H, --host <host>` | Server host | `localhost` |
| `--open` | Open browser automatically | `false` |
| `--no-hmr` | Disable hot module replacement | - |

### Examples

```bash
# Default dev server
nexus dev

# Custom port
nexus dev --port 4000

# Open browser
nexus dev --open
```

---

## nexus build

Create a production build.

```bash
nexus build [options]
```

### Options

| Option | Description | Default |
|--------|-------------|---------|
| `-o, --outDir <dir>` | Output directory | `dist` |
| `--minify` | Minify output | `true` |
| `--sourcemap` | Generate source maps | `true` |
| `--no-clean` | Don't clean output dir | - |
| `--analyze` | Analyze bundle size | `false` |

### Examples

```bash
# Standard build
nexus build

# Custom output
nexus build --outDir build

# With bundle analysis
nexus build --analyze
```

---

## nexus test

Run the test suite.

```bash
nexus test [pattern] [options]
```

### Arguments

| Argument | Description |
|----------|-------------|
| `pattern` | Test file pattern (optional) |

### Options

| Option | Description | Default |
|--------|-------------|---------|
| `--watch` | Watch mode | `false` |
| `--coverage` | Collect coverage | `false` |
| `--ui` | Open test UI | `false` |
| `--bail` | Stop on first failure | `false` |

### Examples

```bash
# Run all tests
nexus test

# Run specific tests
nexus test auth

# Watch mode
nexus test --watch

# With coverage
nexus test --coverage
```

---

## nexus deploy

Deploy to production.

```bash
nexus deploy [options]
```

### Options

| Option | Description | Default |
|--------|-------------|---------|
| `--preview` | Create preview deployment | `false` |
| `--prod` | Deploy to production | `true` |
| `--platform <name>` | Target platform | auto-detect |

### Supported Platforms

- Vercel
- Netlify
- Cloudflare Pages
- AWS Amplify

### Examples

```bash
# Production deploy
nexus deploy

# Preview deploy
nexus deploy --preview

# Specific platform
nexus deploy --platform netlify
```

---

## nexus add

Add a dependency.

```bash
nexus add <packages...> [options]
```

### Options

| Option | Description |
|--------|-------------|
| `-D, --dev` | Add as dev dependency |
| `-E, --exact` | Save exact version |

### Examples

```bash
nexus add lodash
nexus add -D vitest @types/node
nexus add react@18.2.0 --exact
```

---

## nexus remove

Remove a dependency.

```bash
nexus remove <packages...>
```

### Examples

```bash
nexus remove lodash
nexus remove react react-dom
```

---

## nexus run

Run a custom script.

```bash
nexus run <script> [options]
```

### Options

| Option | Description |
|--------|-------------|
| `--all` | Run in all workspaces |
| `--filter <pattern>` | Filter workspaces |

### Examples

```bash
nexus run lint
nexus run test --all
nexus run build --filter=@myorg/api
```

---

## Configuration

### nexus.config.js

```javascript
module.exports = {
  // Project info
  name: 'my-project',
  version: '1.0.0',
  
  // Build configuration
  build: {
    target: 'node18',      // Build target
    outDir: 'dist',        // Output directory
    minify: true,          // Minify output
    sourcemap: true,       // Generate sourcemaps
  },
  
  // Development server
  dev: {
    port: 3000,            // Server port
    host: 'localhost',     // Server host
    open: false,           // Open browser
  },
  
  // Test configuration
  test: {
    include: ['tests/**/*.test.js'],
    coverage: false,
  },
  
  // Custom scripts
  scripts: {
    lint: 'eslint src/',
    format: 'prettier --write .',
  },
  
  // Monorepo workspaces
  workspaces: [
    'packages/*',
  ],
};
```

### Environment Variables

| Variable | Description |
|----------|-------------|
| `NEXUS_DEBUG` | Enable debug logging |
| `NEXUS_NO_COLOR` | Disable colored output |
| `NEXUS_CACHE_DIR` | Custom cache directory |

