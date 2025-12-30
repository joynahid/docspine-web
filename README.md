# Kontext Landing Page

> CI/CD Friendly API Documentation Generator

This is the marketing landing page for [Kontext](https://github.com/kontext-ai/kontext), an automated API documentation generator for FastAPI applications.

## 🚀 Features

- Beautiful, modern design with dark theme
- Responsive layout
- Single-page marketing site
- Built with Hugo static site generator

## 🛠️ Development

### Prerequisites

- [Hugo](https://gohugo.io/) v0.152.2 or higher

### Local Development

```bash
# Clone the repository
git clone https://github.com/joynahid/docspine-web.git
cd docspine-web

# Run local development server
hugo server -D

# Build for production
hugo --gc --minify
```

The site will be available at `http://localhost:1313`

## 📦 Deployment

### Netlify

This site is configured for one-click deployment on Netlify:

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/joynahid/docspine-web)

The `netlify.toml` file includes all necessary build configuration.

### Vercel

Deploy to Vercel with Hugo framework preset:

```bash
vercel --prod
```

### Manual Deployment

```bash
hugo --gc --minify
# Upload the public/ folder to your hosting service
```

## 📁 Project Structure

```
.
├── config.toml          # Hugo configuration
├── layouts/
│   └── index.html      # Landing page template
├── static/             # Static assets (images, etc.)
└── netlify.toml        # Netlify deployment config
```

## 🎨 Customization

Edit `layouts/index.html` to modify the landing page content and styling.

## 📄 License

MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Links

- [Kontext GitHub Repository](https://github.com/kontext-ai/kontext)
- [Documentation](#)
- [Report Issues](https://github.com/kontext-ai/kontext/issues)

