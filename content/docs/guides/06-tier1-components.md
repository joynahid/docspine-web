---
title: "Tier 1 Components"
description: "Keyboard shortcuts, terminal, figures, and diagrams"
weight: 6
---

# Tier 1 Components

Essential components for technical documentation: keyboard shortcuts, terminal output, figures with captions, and Mermaid diagrams.

## Keyboard Shortcuts (kbd)

Display keyboard shortcuts beautifully.

### Basic Usage

Press {{< kbd "Cmd" />}}+{{< kbd "K" />}} to open the command palette.

Use {{< kbd "Ctrl" />}}+{{< kbd "C" />}} to copy and {{< kbd "Ctrl" />}}+{{< kbd "V" />}} to paste.

Press {{< kbd "Esc" />}} to cancel or {{< kbd "Enter" />}} to confirm.

### Common Shortcuts

| Action | Mac | Windows/Linux |
|--------|-----|---------------|
| Save | {{< kbd "Cmd" />}}+{{< kbd "S" />}} | {{< kbd "Ctrl" />}}+{{< kbd "S" />}} |
| Find | {{< kbd "Cmd" />}}+{{< kbd "F" />}} | {{< kbd "Ctrl" />}}+{{< kbd "F" />}} |
| Undo | {{< kbd "Cmd" />}}+{{< kbd "Z" />}} | {{< kbd "Ctrl" />}}+{{< kbd "Z" />}} |
| New Tab | {{< kbd "Cmd" />}}+{{< kbd "T" />}} | {{< kbd "Ctrl" />}}+{{< kbd "T" />}} |

### Arrow Keys and Special Keys

Navigate with {{< kbd "↑" />}} {{< kbd "↓" />}} {{< kbd "←" />}} {{< kbd "→" />}}

Press {{< kbd "Tab" />}} to indent or {{< kbd "Shift" />}}+{{< kbd "Tab" />}} to outdent.

Use {{< kbd "Space" />}} to toggle or {{< kbd "Delete" />}} to remove.

---

## Terminal Component

Show command-line interactions with a beautiful terminal window.

### Basic Terminal

{{< terminal >}}
$ npm install docspine
✓ Installing dependencies...
✓ Package installed successfully!
{{< /terminal >}}

### Git Commands

{{< terminal title="Git" >}}
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

$ git checkout -b feature/new-component
Switched to a new branch 'feature/new-component'
{{< /terminal >}}

### Build Output

{{< terminal title="Build" >}}
$ npm run build

> docspine@1.0.0 build
> hugo --minify

Start building sites … 
hugo v0.115.0

                   | EN  
-------------------+-----
  Pages            |  47
  Paginator pages  |   0
  Non-page files   |   0
  Static files     |  23
  Processed images |   0
  Aliases          |   0
  Sitemaps         |   1
  Cleaned          |   0

Total in 234 ms
{{< /terminal >}}

### Multi-line Commands

{{< terminal >}}
$ docker run -d \
  --name my-container \
  --restart unless-stopped \
  -p 3000:3000 \
  -v $(pwd):/app \
  my-image:latest

Container started: abc123def456
{{< /terminal >}}

### Error Output

{{< terminal >}}
$ npm test
FAIL tests/component.test.js
  ● Component › renders correctly
  
    expect(received).toBe(expected)
    
    Expected: "Hello World"
    Received: "Hello"
    
      12 |   const { getByText } = render(<Component />);
      13 |   const element = getByText(/hello/i);
    > 14 |   expect(element.textContent).toBe('Hello World');
         |                                ^
      15 | });

Tests: 1 failed, 5 passed, 6 total
{{< /terminal >}}

---

## Figure Component

Images with captions and optional links.

### Basic Figure

{{< figure 
  src="https://via.placeholder.com/800x400/4a5ae8/ffffff?text=Dashboard+Overview" 
  alt="Dashboard screenshot" 
  caption="The main dashboard showing analytics and metrics" 
>}}

### Figure with Link

{{< figure 
  src="https://via.placeholder.com/600x400/10b981/ffffff?text=Architecture+Diagram" 
  alt="System architecture" 
  caption="Click to view full-size architecture diagram"
  link="https://via.placeholder.com/1200x800"
>}}

### Figure with Custom Width

{{< figure 
  src="https://via.placeholder.com/400x300/8b5cf6/ffffff?text=Logo" 
  alt="Company logo" 
  caption="Our new logo design"
  width="400"
>}}

### Multiple Figures in Grid

{{< embed-grid cols="2" >}}

{{< figure 
  src="https://via.placeholder.com/400x300/ef4444/ffffff?text=Before" 
  alt="Before optimization" 
  caption="Performance before optimization: 3.2s load time" 
>}}

{{< figure 
  src="https://via.placeholder.com/400x300/22c55e/ffffff?text=After" 
  alt="After optimization" 
  caption="Performance after optimization: 0.8s load time" 
>}}

{{< /embed-grid >}}

---

## Mermaid Diagrams

Create flowcharts, sequence diagrams, and more using Mermaid.

### Flowchart

{{< mermaid >}}
graph TD
    A[Start] --> B{Is it working?}
    B -->|Yes| C[Great!]
    B -->|No| D[Debug]
    D --> E[Fix issue]
    E --> B
    C --> F[Deploy]
    F --> G[End]
{{< /mermaid >}}

### Sequence Diagram

{{< mermaid >}}
sequenceDiagram
    participant User
    participant Browser
    participant Server
    participant Database
    
    User->>Browser: Enter URL
    Browser->>Server: HTTP Request
    Server->>Database: Query Data
    Database-->>Server: Return Data
    Server-->>Browser: HTTP Response
    Browser-->>User: Display Page
{{< /mermaid >}}

### Class Diagram

{{< mermaid >}}
classDiagram
    class Animal {
        +String name
        +int age
        +makeSound()
    }
    class Dog {
        +String breed
        +bark()
    }
    class Cat {
        +Boolean indoor
        +meow()
    }
    
    Animal <|-- Dog
    Animal <|-- Cat
{{< /mermaid >}}

### State Diagram

{{< mermaid >}}
stateDiagram-v2
    [*] --> Idle
    Idle --> Processing: Start
    Processing --> Success: Complete
    Processing --> Error: Fail
    Success --> [*]
    Error --> Retry: Retry
    Retry --> Processing
    Error --> [*]: Give Up
{{< /mermaid >}}

### Entity Relationship Diagram

{{< mermaid >}}
erDiagram
    USER ||--o{ ORDER : places
    USER {
        int id
        string name
        string email
    }
    ORDER ||--|{ ORDER_ITEM : contains
    ORDER {
        int id
        date created_at
        string status
    }
    PRODUCT ||--o{ ORDER_ITEM : "ordered in"
    PRODUCT {
        int id
        string name
        float price
    }
    ORDER_ITEM {
        int quantity
        float price
    }
{{< /mermaid >}}

### Gantt Chart

{{< mermaid >}}
gantt
    title Project Timeline
    dateFormat  YYYY-MM-DD
    section Planning
    Requirements    :a1, 2024-01-01, 14d
    Design         :a2, after a1, 21d
    section Development
    Backend        :b1, 2024-02-01, 30d
    Frontend       :b2, after b1, 28d
    section Testing
    QA Testing     :c1, after b2, 14d
    Bug Fixes      :c2, after c1, 7d
    section Deployment
    Release        :d1, after c2, 3d
{{< /mermaid >}}

### Pie Chart

{{< mermaid >}}
pie title Technology Stack Usage
    "JavaScript" : 35
    "TypeScript" : 25
    "Python" : 20
    "Go" : 12
    "Rust" : 8
{{< /mermaid >}}

---

## Combined Examples

### Installation Guide with All Components

{{< tabs >}}

{{< tab "Quick Start" >}}

Follow these steps to install:

{{< terminal >}}
$ npm install -g docspine
✓ Installation complete!
{{< /terminal >}}

{{< callout type="tip" >}}
Press {{< kbd "Ctrl" />}}+{{< kbd "C" />}} to cancel installation at any time.
{{< /callout >}}

{{< /tab >}}

{{< tab "Architecture" >}}

{{< mermaid >}}
graph LR
    A[User] --> B[CLI]
    B --> C[Core]
    C --> D[Templates]
    C --> E[Components]
    C --> F[Assets]
    D --> G[Output]
    E --> G
    F --> G
{{< /mermaid >}}

{{< /tab >}}

{{< tab "Screenshots" >}}

{{< figure 
  src="https://via.placeholder.com/700x400/6366f1/ffffff?text=CLI+Output" 
  alt="CLI in action" 
  caption="DocSpine CLI generating documentation" 
>}}

{{< /tab >}}

{{< /tabs >}}

### Workflow Documentation

{{< steps >}}

{{< step >}}

### Initialize Project

{{< terminal >}}
$ docspine init my-docs
Creating project structure...
✓ Project created!
{{< /terminal >}}

Press {{< kbd "Enter" />}} to use defaults or customize options.

{{< /step >}}

{{< step >}}

### Configure

Edit the configuration file:

{{< terminal >}}
$ cd my-docs
$ nano config.toml
{{< /terminal >}}

{{< figure 
  src="https://via.placeholder.com/600x300/f59e0b/ffffff?text=Config+File" 
  alt="Configuration" 
  caption="Example configuration file" 
>}}

{{< /step >}}

{{< step >}}

### Build & Deploy

{{< terminal >}}
$ docspine build
Building documentation...
✓ Build complete!

$ docspine deploy
Deploying to production...
✓ Deployed successfully!
{{< /terminal >}}

{{< callout type="success" >}}
Your documentation is now live!
{{< /callout >}}

{{< /step >}}

{{< /steps >}}

---

## Component Features

### Keyboard Shortcuts (kbd)
- {{< icon "check" >}} Platform-specific shortcuts
- {{< icon "check" >}} Inline usage
- {{< icon "check" >}} Styled like real keys
- {{< icon "check" >}} Dark mode support

### Terminal
- {{< icon "check" >}} macOS-style window
- {{< icon "check" >}} Custom titles
- {{< icon "check" >}} Monospace font
- {{< icon "check" >}} Syntax preservation
- {{< icon "check" >}} Copy-paste friendly

### Figure
- {{< icon "check" >}} Responsive images
- {{< icon "check" >}} Captions with markdown
- {{< icon "check" >}} Optional linking
- {{< icon "check" >}} Custom dimensions
- {{< icon "check" >}} Lazy loading

### Mermaid
- {{< icon "check" >}} 8+ diagram types
- {{< icon "check" >}} Interactive (zoom/pan)
- {{< icon "check" >}} Theme-aware
- {{< icon "check" >}} Responsive
- {{< icon "check" >}} Auto-rendering

---

## Summary

You now have the most essential documentation components:

1. {{< kbd "kbd" />}} **Keyboard Shortcuts** - Show key combinations
2. {{< icon "terminal" >}} **Terminal** - Command-line examples
3. {{< icon "file" >}} **Figure** - Images with captions
4. {{< icon "code" >}} **Mermaid** - Diagrams and charts

{{< callout type="success" >}}
These 4 components cover 80% of technical documentation needs!
{{< /callout >}}

