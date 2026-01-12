# My Blog

This is a Gatsby-based blog for GitHub Pages. It has been stripped of all original content and set up as a basic framework for your own blog.

## Quick Start

1. **Update site metadata:**
   - Edit `gatsby-config.mjs` with your title, description, URL, and social links
   - Update `src/mdx/about.mdx` with your bio and contact info

2. **Add your content:**
   - Blog posts in `src/mdx/` as `.mdx` files
   - Microblog posts in `src/microblog_md/` as `.md` files
   - Link posts in `src/links_quotes_markdown/` as `.md` files

3. **Deploy:**
   - Push to the `dev` branch to automatically deploy via GitHub Actions

## Content Types

The blog supports four types of content, each displayed differently:

### Blog Posts (`src/mdx/`)
- **Format:** MDX files (Markdown with JSX support)
- **Display:** Listed on the homepage with category filtering
- **Use for:** Full articles, tutorials, in-depth posts
- **Frontmatter:**
  ```yaml
  ---
  title: Post Title
  description: Brief description
  post_date: 2024-01-12
  post_category: blog_post  # or custom category
  ---
  ```

### Microblog Posts (`src/microblog_md/`)
- **Format:** Markdown files
- **Display:** Short posts with tag-based filtering
- **Use for:** Quick thoughts, updates, short insights
- **Frontmatter:**
  ```yaml
  ---
  title: Short Title
  description: Brief description
  date: 2024-01-12
  type: microblog
  author: Your Name
  tags: [tag1, tag2]
  ---
  ```

### Linkblog Posts (`src/links_quotes_markdown/`)
- **Format:** Markdown files
- **Display:** Dedicated `/quotes-links/` page with type and tag filtering
- **Use for:** Sharing links, quotes, or external content
- **Frontmatter:**
  ```yaml
  ---
  title: Link Title
  description: Brief description
  date: 2024-01-12
  type: link  # or "quote"
  author: Source Author
  url: https://example.com
  tags: [tag1, tag2]
  ---
  ```

### Definitions (`src/definitions_markdown/`)
- **Format:** Markdown files
- **Display:** Tooltips in blog posts when terms are referenced
- **Use for:** Glossary terms, explanations
- **Frontmatter:**
  ```yaml
  ---
  title: Term Name
  ---
  ```

## Publishing & Updates

The site uses GitHub Actions for automatic deployment:

- **Automatic:** Push to the `dev` branch triggers a build and deploy to the `master` branch
- **Manual:** Run `npm run build` locally to test, then push changes
- **GitHub Pages:** Served from the `master` branch

New content is automatically included when you add files to the appropriate directories and push to `dev`.

## Development

```bash
npm run develop  # Start development server at http://localhost:8000
npm run build    # Build for production
```

## Customization

- **Styles:** `tailwind.config.js`, `src/styles/`
- **Components:** `src/components/`
- **Navigation:** Update `src/components/Header.jsx`
- **Layout:** `src/components/Layout.jsx`

## Notes

- The site is configured for GitHub Pages at `thomashudsonuk.github.io`
- Update the CNAME file if using a custom domain
- Remove or update Google Analytics tracking if desired
