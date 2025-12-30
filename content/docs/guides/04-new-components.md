---
title: "New Components Demo"
description: "Examples of tabs, file tree, badges, details, and inline icons"
weight: 4
---

# New Components Demo

This page demonstrates all the newly added components in the DocSpine theme.

## Tabs Component

Use tabs to organize content into different sections that users can switch between.

{{< tabs >}}

{{< tab "Installation" >}}

### Installing the Package

```bash
npm install @docspine/core
```

After installation, you can import and use it:

```javascript
import { DocSpine } from '@docspine/core';
```

{{< /tab >}}

{{< tab "Configuration" >}}

### Basic Configuration

Create a config file in your project root:

```javascript
// docspine.config.js
export default {
  title: 'My Documentation',
  theme: 'default',
  sidebar: true
};
```

{{< /tab >}}

{{< tab "Usage" >}}

### Using the Component

Here's a quick example:

```javascript
const docs = new DocSpine({
  root: './docs',
  output: './dist'
});

await docs.build();
```

{{< /tab >}}

{{< /tabs >}}

---

## File Tree Component

Display directory structures and file hierarchies clearly.

{{< file-tree >}}
- project-root/
  - src/
    - components/
      - Button.tsx
      - Input.tsx
      - Modal.tsx
    - utils/
      - helpers.ts
      - validators.ts
    - app.ts
  - public/
    - images/
    - styles/
  - package.json
  - tsconfig.json
  - README.md
{{< /file-tree >}}

---

## Badge Component

Use badges to highlight status, versions, or important labels.

### Basic Badges

{{< badge >}}Default{{< /badge >}}
{{< badge type="success" >}}New{{< /badge >}}
{{< badge type="info" >}}Beta{{< /badge >}}
{{< badge type="warning" >}}Deprecated{{< /badge >}}
{{< badge type="danger" >}}Breaking{{< /badge >}}

### In Context

This feature is {{< badge type="success" >}}available{{< /badge >}} in version 2.0 and above.

The old API is {{< badge type="warning" >}}deprecated{{< /badge >}} and will be removed in v3.0.

This action is {{< badge type="danger" >}}irreversible{{< /badge >}} - use with caution!

### With Icons

{{< badge type="success" >}}{{< icon "check" >}} Stable{{< /badge >}}
{{< badge type="info" >}}{{< icon "info" >}} Documentation{{< /badge >}}
{{< badge type="warning" >}}{{< icon "warning" >}} Experimental{{< /badge >}}

---

## Details / Accordion Component

Create expandable sections for optional or advanced information.

### Basic Usage

{{< details title="Show Advanced Options" >}}

These advanced options are for power users:

- `--verbose` - Enable detailed logging
- `--force` - Skip confirmation prompts
- `--experimental` - Enable experimental features

{{< callout type="warning" >}}
Experimental features may be unstable!
{{< /callout >}}

{{< /details >}}

### Multiple Sections

{{< details title="What are CSS Custom Properties?" >}}

CSS Custom Properties (also called CSS variables) allow you to define reusable values:

```css
:root {
  --primary-color: #4a5ae8;
  --spacing: 1rem;
}

.button {
  background: var(--primary-color);
  padding: var(--spacing);
}
```

{{< /details >}}

{{< details title="How to Override Theme Colors?" >}}

Create a `custom.css` file:

```css
:root {
  --color-accent: #10b981;
  --color-accent-hover: #059669;
}
```

The theme will automatically pick up these overrides!

{{< /details >}}

{{< details title="Browser Support" open="true" >}}

DocSpine supports all modern browsers:

- ✅ Chrome/Edge (latest 2 versions)
- ✅ Firefox (latest 2 versions)  
- ✅ Safari (latest 2 versions)
- ✅ Mobile browsers

{{< /details >}}

---

## Inline Icon Component

Use inline icons to reference UI elements or add visual cues in your text.

### Available Icons

Click the {{< icon "settings" >}} **Settings** button to configure your preferences.

Press {{< icon "search" >}} **Search** or use the keyboard shortcut.

Check the {{< icon "check" >}} **checkbox** to enable this feature.

Click {{< icon "external" >}} to open the link in a new window.

View the {{< icon "file" >}} **file** or {{< icon "folder" >}} **folder** in the sidebar.

Open the {{< icon "terminal" >}} **terminal** to run commands.

Read the {{< icon "book" >}} **documentation** for more details.

Use {{< icon "code" >}} **code** snippets to illustrate examples.

Copy {{< icon "copy" >}} the text to your clipboard.

Follow this {{< icon "link" >}} **link** for more information.

### Icon Reference

Available icon names:
- `settings` {{< icon "settings" >}}
- `check` {{< icon "check" >}}
- `x` {{< icon "x" >}}
- `warning` {{< icon "warning" >}}
- `info` {{< icon "info" >}}
- `external` {{< icon "external" >}}
- `arrow-right` {{< icon "arrow-right" >}}
- `file` {{< icon "file" >}}
- `folder` {{< icon "folder" >}}
- `code` {{< icon "code" >}}
- `terminal` {{< icon "terminal" >}}
- `book` {{< icon "book" >}}
- `link` {{< icon "link" >}}
- `copy` {{< icon "copy" >}}
- `search` {{< icon "search" >}}

---

## Combining Components

You can mix and match components for rich documentation:

{{< tabs >}}

{{< tab "macOS" >}}

{{< details title="Installation Steps" >}}

{{< steps >}}

{{< step >}}
### Download the Package

{{< badge type="info" >}}64-bit{{< /badge >}}

Download from the {{< icon "external" >}} [releases page](https://github.com/example/releases).
{{< /step >}}

{{< step >}}
### Extract Files

```bash
tar -xzf docspine-macos.tar.gz
cd docspine
```

{{< file-tree >}}
- docspine/
  - bin/
    - docspine
  - lib/
  - README.md
{{< /file-tree >}}

{{< /step >}}

{{< step >}}
### Run Installation

```bash
./install.sh
```

{{< callout type="tip" >}}
Add the binary to your PATH for easy access!
{{< /callout >}}
{{< /step >}}

{{< /steps >}}

{{< /details >}}

{{< /tab >}}

{{< tab "Linux" >}}

{{< details title="Installation Steps" >}}

Similar to macOS, but with Linux-specific binaries.

{{< badge type="success" >}}Supported{{< /badge >}}

Download the appropriate version for your distribution.

{{< /details >}}

{{< /tab >}}

{{< tab "Windows" >}}

{{< details title="Installation Steps" >}}

{{< badge type="warning" >}}Beta{{< /badge >}}

Windows support is currently in beta. Download the `.exe` installer.

{{< /details >}}

{{< /tab >}}

{{< /tabs >}}

---

## Summary

You now have access to these powerful components:

1. {{< icon "check" >}} **Tabs** - Organize content in switchable panels
2. {{< icon "check" >}} **File Tree** - Display directory structures  
3. {{< icon "check" >}} **Badges** - Highlight status and labels
4. {{< icon "check" >}} **Details** - Create expandable sections
5. {{< icon "check" >}} **Icons** - Add inline visual cues

{{< callout type="success" >}}
All components are fully responsive and support dark mode automatically!
{{< /callout >}}

