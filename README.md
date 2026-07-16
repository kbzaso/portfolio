# saez.me

Personal journal for Alejandro Sáez, live at [saez.me](https://saez.me/).

Built with [Astro](https://astro.build/) and [Tailwind CSS](https://tailwindcss.com/), deployed on [Vercel](https://vercel.com/) as a static site.

## Pages

- `/` — home: hero, experience, projects, about me
- `/quotes` — a collection of quotes
- `/books` — books read/recommended
- `/components` — component showcase

## Stack

- **Astro** — static site generation
- **Tailwind CSS v4** — styling, wired in via `@tailwindcss/vite` (no `tailwind.config.js` — theme lives in `src/styles/global.css`)
- **TypeScript**
- **astro-robots-txt** — generates `robots.txt` at build time

## Getting started

Requires Node ≥22.12 (see `.nvmrc`) and [pnpm](https://pnpm.io/).

```bash
pnpm install
pnpm dev       # start the dev server
```

## Scripts

| Script              | What it does                                         |
| ------------------- | ---------------------------------------------------- |
| `pnpm dev`          | Start the local dev server                           |
| `pnpm build`        | Type-check (`astro check`) then build for production |
| `pnpm preview`      | Preview the production build locally                 |
| `pnpm format`       | Format the codebase with Prettier                    |
| `pnpm format:check` | Check formatting without writing (used in CI)        |

## CI

`.github/workflows/format.yml` checks formatting on every push to `main` and on all pull requests.

## Project structure

```
src/
  components/   Astro components, including icons/
  layouts/      Page layouts (Layout.astro is the one actually used by pages)
  pages/        Route files
  styles/       global.css — Tailwind entry point + global CSS
public/         Static assets served as-is
```
