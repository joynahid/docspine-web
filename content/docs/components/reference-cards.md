---
title: "Reference Cards"
draft: true
---

# Reference Cards Component

Use reference cards to link to other articles, pages, or external resources in a visually appealing way.

## Single Reference Card

```markdown
{{</* ref-card 
  url="/docs/getting-started/installation/" 
  title="Installation Guide" 
  description="Learn how to install and set up the project in your environment."
  icon="book"
*/>}}
```

{{< ref-card 
  url="/docs/getting-started/installation/" 
  title="Installation Guide" 
  description="Learn how to install and set up the project in your environment."
  icon="book"
>}}

## Available Icons

You can use different icons by setting the `icon` parameter:

- `arrow-right` (default) - Simple arrow pointing right
- `book` - Book icon for documentation
- `external` - External link icon
- `file` - File/document icon

### Book Icon Example

{{< ref-card 
  url="/docs/getting-started/quickstart/" 
  title="Quick Start" 
  description="Get up and running quickly with this step-by-step guide."
  icon="book"
>}}

### External Link Icon Example

{{< ref-card 
  url="https://github.com/your-repo" 
  title="View on GitHub" 
  description="Check out the source code and contribute to the project."
  icon="external"
>}}

### File Icon Example

{{< ref-card 
  url="/docs/api/reference/" 
  title="API Reference" 
  description="Complete API documentation and reference guide."
  icon="file"
>}}

## Multiple Cards in a Grid

Use the `ref-cards-grid` shortcode to display multiple cards in a responsive grid:

```markdown
{{</* ref-cards-grid */>}}

{{</* ref-card 
  url="/docs/getting-started/installation/" 
  title="Installation" 
  description="Install and configure the project."
  icon="book"
*/>}}

{{</* ref-card 
  url="/docs/getting-started/quickstart/" 
  title="Quick Start" 
  description="Get started in minutes."
  icon="arrow-right"
*/>}}

{{</* ref-card 
  url="/docs/advanced/deployment/" 
  title="Deployment" 
  description="Deploy your application to production."
  icon="external"
*/>}}

{{</* /ref-cards-grid */>}}
```

{{< ref-cards-grid >}}

{{< ref-card 
  url="/docs/getting-started/installation/" 
  title="Installation" 
  description="Install and configure the project."
  icon="book"
>}}

{{< ref-card 
  url="/docs/getting-started/quickstart/" 
  title="Quick Start" 
  description="Get started in minutes."
  icon="arrow-right"
>}}

{{< ref-card 
  url="/docs/advanced/deployment/" 
  title="Deployment" 
  description="Deploy your application to production."
  icon="external"
>}}

{{< /ref-cards-grid >}}

## Without Description

You can omit the description for a more compact look:

{{< ref-card 
  url="/docs/concepts/" 
  title="Core Concepts"
>}}

## Features

- **Hover Effects**: Cards lift and change color on hover
- **Responsive**: Grid layout adapts to different screen sizes
- **Icons**: Multiple icon options to match your content
- **Dark Mode**: Automatic dark mode support
- **Accessible**: Semantic HTML with proper link structure

