# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Hexo 8.1.1 static blog using the Volantis theme (v6). Content is written in Markdown (Chinese), stored in `source/_posts/` with post asset folders for images.

## Commands

| Command | Description |
|---------|-------------|
| `pnpm run server` | Start local dev server |
| `pnpm run build` | Generate static site to `public/` |
| `pnpm run clean` | Delete `public/` |
| `pnpm run deploy` | Deploy the site |

## Configuration

- **`_config.yml`** — Main Hexo config: site metadata, URL (`http://blog.brianeee.cloud`), permalink format, syntax highlighting (highlight.js), pagination, theme selection (`volantis`).
- **`_config.volantis.yml`** — Volantis theme config: cover page, navbar, sidebar widgets, analytics, comments, and all visual settings.

## Content structure

- `source/_posts/` — Blog posts (Markdown). Each post can have a same-named asset folder for images (e.g., `source/_posts/Openrouter大模型平台/` holds images for that post).
- `source/about/` — About page.
- `source/images/` — Legacy/referenced images. Prefer post asset folders for new content.
- `source/tags/` — Tags index page.
- `scaffolds/` — Post templates used by `hexo new`.

## Creating a new post

Run `npx hexo new "Post Title"` to create a post from the scaffold. The post will be created as `source/_posts/Post Title.md` with an associated asset folder at `source/_posts/Post Title/` (because `post_asset_folder: true` is set).

Insert images in posts with standard Markdown: `![](Post Title/image.png)`.

## Theme notes

The theme (`themes/`) is managed as an npm package (`hexo-theme-volantis`), so the theme directory will be empty in the repo. Theme source lives in `node_modules/hexo-theme-volantis/` — avoid editing files there directly. Override theme behavior via `_config.volantis.yml` instead.

## Package manager

Uses pnpm with a lockfile (`pnpm-lock.yaml`). Run `pnpm install` to restore dependencies after a fresh clone.
