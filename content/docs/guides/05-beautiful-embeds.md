---
title: "Beautiful Embeds"
description: "Tweet, YouTube, GitHub Gist, CodePen embeds with grid layouts"
weight: 5
---

# Beautiful Embeds

Embed rich content from various platforms with beautiful, responsive layouts.

## Tweet Embeds

Embed tweets with a clean, card-style design.

### Basic Tweet

{{< tweet user="vercel" id="1234567890" >}}
Check out our latest feature release! 🚀

New capabilities:
- Edge Functions
- Instant Rollbacks
- Advanced Analytics

Learn more at vercel.com
{{< /tweet >}}

### Tweet with URL

{{< tweet url="https://twitter.com/github/status/1234567890" >}}
GitHub Actions now supports reusable workflows! Build once, use everywhere. 💪
{{< /tweet >}}

---

## YouTube Videos

Embed YouTube videos with responsive 16:9 ratio.

### Basic Video

{{< youtube id="dQw4w9WgXcQ" >}}

### Video with Custom Title

{{< youtube id="jNQXAC9IVRw" title="Me at the zoo" >}}

### Video Starting at Specific Time

Start at 1:30 (90 seconds):

{{< youtube id="dQw4w9WgXcQ" start="90" >}}

---

## GitHub Gists

Embed GitHub Gists with syntax highlighting.

### Full Gist

{{< gist user="mojombo" id="1" >}}

### Specific File from Gist

{{< gist user="example" id="abc123" file="example.js" >}}

### With URL

{{< gist url="https://gist.github.com/username/1234567890abcdef" >}}

---

## CodePen Embeds

Embed interactive CodePen demos.

### Basic CodePen

{{< codepen user="chriscoyier" id="myBvwd" >}}

### Custom Height and Tab

{{< codepen user="chriscoyier" id="myBvwd" height="500" tab="css" >}}

### Dark Theme

{{< codepen user="example" id="xyz123" theme="dark" >}}

---

## Embed Grids

Organize multiple embeds in responsive grid layouts.

### 2-Column Grid

{{< embed-grid cols="2" >}}

{{< youtube id="dQw4w9WgXcQ" >}}

{{< tweet user="vercel" id="123" >}}
Amazing new features! 🎉
{{< /tweet >}}

{{< /embed-grid >}}

### 3-Column Grid

{{< embed-grid cols="3" gap="lg" >}}

{{< tweet user="github" id="1" >}}
GitHub Actions ⚡
{{< /tweet >}}

{{< tweet user="vercel" id="2" >}}
Edge Functions 🚀
{{< /tweet >}}

{{< tweet user="nodejs" id="3" >}}
Node.js v20 📦
{{< /tweet >}}

{{< /embed-grid >}}

### Mixed Content Grid

{{< embed-grid cols="2" gap="md" >}}

{{< youtube id="jNQXAC9IVRw" >}}

{{< codepen user="chriscoyier" id="myBvwd" height="300" >}}

{{< tweet user="example" id="123" >}}
Check out this amazing demo! 🎨
{{< /tweet >}}

{{< gist user="mojombo" id="1" >}}

{{< /embed-grid >}}

---

## Gallery Layout (4 Columns)

Perfect for showcasing multiple tweets or small embeds:

{{< embed-grid cols="4" gap="sm" >}}

{{< tweet user="vercel" id="1" >}}
Feature 1 ✨
{{< /tweet >}}

{{< tweet user="vercel" id="2" >}}
Feature 2 🚀
{{< /tweet >}}

{{< tweet user="vercel" id="3" >}}
Feature 3 💎
{{< /tweet >}}

{{< tweet user="vercel" id="4" >}}
Feature 4 ⚡
{{< /tweet >}}

{{< /embed-grid >}}

---

## Advanced Examples

### Combined with Other Components

{{< tabs >}}

{{< tab "Video Tutorial" >}}

{{< youtube id="dQw4w9WgXcQ" >}}

{{< callout type="tip" >}}
Watch the video above for a complete walkthrough!
{{< /callout >}}

{{< /tab >}}

{{< tab "Code Example" >}}

{{< codepen user="chriscoyier" id="myBvwd" >}}

{{< details title="View Source Code" >}}

You can also view the source on CodePen or check out the embedded version above.

{{< /details >}}

{{< /tab >}}

{{< tab "Social Proof" >}}

{{< embed-grid cols="2" >}}

{{< tweet user="user1" id="1" >}}
This is amazing! Best docs ever 🎉
{{< /tweet >}}

{{< tweet user="user2" id="2" >}}
Love the embed support! So clean 💎
{{< /tweet >}}

{{< /embed-grid >}}

{{< /tab >}}

{{< /tabs >}}

---

## Responsive Behavior

All embeds are fully responsive:

- **Desktop (>1024px)**: Full grid layout as specified
- **Tablet (640-1024px)**: 4-col → 2-col, 3-col → 2-col
- **Mobile (<640px)**: All embeds stack to single column

{{< callout type="info" >}}
Grid layouts automatically adapt to screen size for the best viewing experience!
{{< /callout >}}

---

## Features

### Tweet Embeds
- {{< icon "check" >}} Clean card design
- {{< icon "check" >}} Dark mode support
- {{< icon "check" >}} External link to original tweet
- {{< icon "check" >}} Custom content or placeholder

### Video Embeds
- {{< icon "check" >}} 16:9 responsive ratio
- {{< icon "check" >}} YouTube support
- {{< icon "check" >}} Autoplay option
- {{< icon "check" >}} Start time control
- {{< icon "check" >}} Loading animation

### Gist Embeds
- {{< icon "check" >}} GitHub integration
- {{< icon "check" >}} Syntax highlighting
- {{< icon "check" >}} Single file selection
- {{< icon "check" >}} Theme integration

### CodePen Embeds
- {{< icon "check" >}} Live preview
- {{< icon "check" >}} Custom height
- {{< icon "check" >}} Tab selection (HTML/CSS/JS/Result)
- {{< icon "check" >}} Theme options

### Grid Layouts
- {{< icon "check" >}} 1-4 column support
- {{< icon "check" >}} Responsive breakpoints
- {{< icon "check" >}} Customizable gaps
- {{< icon "check" >}} Mixed content support

---

## Usage Tips

{{< details title="Best Practices" >}}

1. **Performance**: Use embed grids to organize multiple embeds efficiently
2. **Loading**: Videos and CodePens have loading animations
3. **Accessibility**: All embeds include proper titles and fallbacks
4. **Dark Mode**: Embeds automatically adapt to theme
5. **Mobile**: Always test embeds on mobile devices

{{< /details >}}

{{< details title="When to Use Each Embed Type" >}}

- **Tweets**: Social proof, announcements, community highlights
- **YouTube**: Tutorials, demos, presentations
- **Gists**: Code snippets, configuration examples
- **CodePen**: Interactive demos, live examples
- **Grids**: Multiple items, galleries, comparisons

{{< /details >}}

---

## Summary

You now have beautiful embed components for:

1. {{< icon "external" >}} **Tweets** - Social media integration
2. {{< icon "external" >}} **YouTube** - Video content
3. {{< icon "code" >}} **GitHub Gists** - Code snippets
4. {{< icon "code" >}} **CodePen** - Interactive demos
5. {{< icon "folder" >}} **Embed Grids** - Flexible layouts

{{< callout type="success" >}}
All embeds are fully responsive, support dark mode, and include beautiful animations!
{{< /callout >}}

