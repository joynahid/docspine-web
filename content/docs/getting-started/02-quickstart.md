---
title: "Quick Start"
description: "Create your first Nexus project in 5 minutes"
---

# Quick Start

This guide walks you through creating your first project with Nexus.

## Prerequisites

- Nexus installed ([Installation guide](/docs/getting-started/01-install/))
- Node.js 18+ (for JavaScript projects)

## Create a New Project

Initialize a new project with the `init` command:

```bash
nexus init my-project
```

Nexus will prompt you to select a template:

```
? Select a template:
❯ minimal    - Bare bones starter
  api        - REST API with Express
  fullstack  - Next.js + API
  cli        - Command-line tool
```

Choose `minimal` for this guide.

## Project Structure

After initialization, your project will look like this:

```
my-project/
├── nexus.config.js
├── src/
│   └── index.js
├── tests/
│   └── index.test.js
└── package.json
```

## Configuration

The `nexus.config.js` file contains your project settings:

```javascript
module.exports = {
  name: 'my-project',
  version: '0.1.0',
  
  // Build settings
  build: {
    target: 'node18',
    outDir: 'dist',
  },
  
  // Development server
  dev: {
    port: 3000,
    watch: ['src/**/*.js'],
  },
};
```

## Run Development Server

Start the development server with hot reload:

```bash
cd my-project
nexus dev
```

Output:

```
✓ Development server started
  → Local:   http://localhost:3000
  → Network: http://192.168.1.100:3000
  
  Watching for changes...
```

## Build for Production

Create an optimized production build:

```bash
nexus build
```

Output:

```
✓ Build completed in 1.2s
  → Output: dist/index.js (12.4 KB)
  → Output: dist/index.js.map
```

## Run Tests

Execute your test suite:

```bash
nexus test
```

Output:

```
 PASS  tests/index.test.js
  ✓ should return hello world (2ms)

Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Time:        0.847s
```

## Deploy

Deploy to production with a single command:

```bash
nexus deploy
```

Nexus will detect your platform and deploy automatically:

```
✓ Detected platform: Vercel
✓ Building project...
✓ Uploading files...
✓ Deployed to https://my-project.vercel.app

Ready in 23s
```

## Next Steps

{{< ref-card 
  url="/docs/guides/01-basic-usage/" 
  title="Basic Usage Guide" 
  description="Learn the fundamental concepts and common workflows."
  icon="book"
>}}

{{< ref-card 
  url="/docs/api/01-reference/" 
  title="API Reference" 
  description="Complete documentation of all commands and options."
  icon="file"
>}}

