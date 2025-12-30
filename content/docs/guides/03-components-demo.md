---
title: "Components Demo"
description: "Examples of steps, callouts, and other components"
weight: 3
---

## Steps Component

Create beautiful step-by-step tutorials:

{{< steps >}}

{{< step >}}
**Choose a component**

Find the component you want to override in the [Overrides Reference](/docs/api/reference).

{{< callout type="tip" >}}
Not sure which component to override? Use the interactive tool to discover component names.
{{< /callout >}}
{{< /step >}}

{{< step >}}
**Create your replacement**

Create an Astro component to replace the Starlight component with:

```astro
---
// src/components/EmailLink.astro
const email = 'houston@example.com';
---

<a href={`mailto:${email}`}>E-mail Me</a>
```
{{< /step >}}

{{< step >}}
**Register the override**

Add your custom component to the `components` configuration in `astro.config.mjs`:

```javascript
import { defineConfig } from 'astro/config';
import starlight from '@astrojs/starlight';

export default defineConfig({
  integrations: [
    starlight({
      title: 'My Docs',
      components: {
        SocialIcons: './src/components/EmailLink.astro',
      },
    }),
  ],
});
```
{{< /step >}}

{{< /steps >}}

## Callout Types

### Tip

{{< callout type="tip" >}}
Use tips to highlight helpful information or best practices.
{{< /callout >}}

### Note

{{< callout type="note" >}}
Notes provide additional context or important information.
{{< /callout >}}

### Warning

{{< callout type="warning" >}}
Warnings alert users to potential issues or things to be careful about.
{{< /callout >}}

### Caution

{{< callout type="caution" >}}
Cautions indicate actions that might have significant consequences.
{{< /callout >}}

### Danger

{{< callout type="danger" >}}
Danger alerts indicate critical issues that could cause data loss or security problems.
{{< /callout >}}

## Custom Titles

{{< callout type="tip" title="Pro Tip" >}}
You can customize the title of any callout by adding a `title` parameter!
{{< /callout >}}

## Code Tabs

{{< code-tabs >}}
{{< code-tab "JavaScript" >}}
```javascript
async function fetchData() {
  const response = await fetch('/api/data');
  return await response.json();
}
```
{{< /code-tab >}}
{{< code-tab "Python" >}}
```python
import requests

def fetch_data():
    response = requests.get('/api/data')
    return response.json()
```
{{< /code-tab >}}
{{< /code-tabs >}}

