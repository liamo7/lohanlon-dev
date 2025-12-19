# lohanlon.dev

This is my personal site / engineering notebook.

It exists primarily as a reference for myself: a place to write things down so I don’t have to
re-learn them later. If anything here is useful to someone else, that’s a bonus rather
than the goal.

The site is intentionally simple, static, and low-maintenance.

---

## Tech stack

- **Astro** – static site generation
- **Markdown / MDX** – content
- **Cloudflare Pages** – hosting and deployment
- **GitHub** – source control and CI

---

## Hosting & deployment

The site is hosted on **Cloudflare Pages**.

- This GitHub repository is connected to Cloudflare Pages
- Every push to the `main` branch automatically triggers a build and deployment

### Deploying the site

There is no manual deployment step.

```
git push origin main
```

---

## Running locally

Install dependencies once:

```
npm install
```

Start the local development server:

```
npm run dev
```

The site will be available at:

```
http://localhost:4321
```

---

## Project structure (high level)

```
public/
  Static files served as-is

src/
  assets/
    Images imported into components (hero images, etc.)

  content/
    Markdown / MDX content collections
    blog/
      Blog posts and notes

  components/
    Reusable components

  layouts/
    Page and post layouts

  pages/
    Top-level routes (about, index, etc.)
```

---

## Asset usage

Astro distinguishes between **build-time assets** and **runtime assets**.

- **Imported assets** → `src/assets/`
  - Example: blog post hero images imported into layouts
- **Assets referenced by URL** (`<img src="...">`) → `public/`
  - Example: icons, favicons, static images

---

## Writing new blog posts / notes

Posts live under:

```
src/content/blog/
```

To add a new post:

1. Create a new `.md` or `.mdx` file in `src/content/blog/`
2. Add frontmatter (title, description, publish date, etc.)
3. Write content in Markdown or MDX
4. Commit and push to `main`

---

## Building the site manually (optional)

To generate a production build locally:

```
npm run build
```

The output will be created in:

```
dist/
```

This is usually only needed for debugging build issues.

---
