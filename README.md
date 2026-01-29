# AliceBaw.com

A modern, fast blog built with Astro and powered by Markdown. Optimized for GitHub Pages deployment.

## Features

- ⚡ **Lightning Fast**: Built with Astro for optimal performance
- 📝 **Markdown Powered**: All blog posts written in Markdown
- 🎨 **Modern Design**: Clean, responsive design
- 🚀 **SSG**: Static Site Generation for best performance
- 📱 **Responsive**: Works perfectly on all devices
- 🔍 **SEO Friendly**: Built-in sitemap and metadata

## Getting Started

### Prerequisites

- Node.js 18 or higher
- npm or your preferred package manager

### Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/alicebaw.com.git
cd alicebaw.com
```

2. Install dependencies:

```bash
npm install
```

3. Start the development server:

```bash
npm run dev
```

4. Open your browser and visit `http://localhost:4321`

## Project Structure

```
/
├── public/              # Static assets
├── src/
│   ├── content/
│   │   ├── blog/       # Blog posts (Markdown files)
│   │   └── config.ts   # Content collections config
│   ├── layouts/
│   │   └── Layout.astro # Base layout
│   └── pages/
│       ├── index.astro         # Landing page
│       └── blog/
│           ├── index.astro     # Blog listing
│           └── [...slug].astro # Blog post template
├── astro.config.mjs    # Astro configuration
└── package.json
```

## Writing Blog Posts

Blog posts are stored in `src/content/blog/` as Markdown files.

Create a new post:

```markdown
---
title: "Your Post Title"
description: "A brief description of your post"
pubDate: 2026-01-29
author: "AliceBaw"
---

## Your Content Here

Write your blog post using Markdown...
```

## Available Commands

| Command           | Action                               |
| ----------------- | ------------------------------------ |
| `npm install`     | Install dependencies                 |
| `npm run dev`     | Start dev server at `localhost:4321` |
| `npm run build`   | Build production site to `./dist/`   |
| `npm run preview` | Preview production build locally     |

## Deploying to GitHub Pages

### Setup

1. **Update Configuration**: Edit `astro.config.mjs`:

   ```javascript
   export default defineConfig({
     site: "https://yourusername.github.io",
     base: "/alicebaw.com", // or '/' if using custom domain
   });
   ```

2. **Enable GitHub Pages**:
   - Go to your repository Settings
   - Navigate to Pages
   - Set Source to "GitHub Actions"

3. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

The GitHub Actions workflow will automatically build and deploy your site!

### Custom Domain (Optional)

To use a custom domain:

1. Update `site` in `astro.config.mjs` to your domain
2. Add a `CNAME` file in the `public/` directory with your domain
3. Configure DNS settings with your domain provider

## Customization

### Styling

The site uses CSS custom properties defined in [src/layouts/Layout.astro](src/layouts/Layout.astro). Modify these to change colors:

```css
:root {
  --primary: #6366f1;
  --text: #1f2937;
  --bg: #ffffff;
}
```

### Adding Pages

Create new `.astro` files in `src/pages/` to add pages. They'll automatically become routes.

### Navigation

Update the navigation in [src/layouts/Layout.astro](src/layouts/Layout.astro).

## Technologies Used

- [Astro](https://astro.build) - Web framework
- [MDX](https://mdxjs.com/) - Markdown with JSX
- GitHub Actions - CI/CD
- GitHub Pages - Hosting

## License

MIT License - feel free to use this project as a template!

## Contributing

Issues and pull requests are welcome!

---

Built with ❤️ using Astro
