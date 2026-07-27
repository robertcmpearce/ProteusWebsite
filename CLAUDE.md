# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Overview

Marketing website for **Proteus Dynamics** — a single-page, static site presenting
the company's smart-handcuff technology for law enforcement. There is no build
step, framework, or backend: it is plain HTML and CSS with a few image assets.

## Structure

- `index.html` — the entire site (HTML + inline `<style>` block). All markup and
  styling live in this one file.
- `logo.png` — Proteus wordmark, shown in the top brand bar.
- `hero.png` — product hero image. Currently **not referenced** by the page (the
  hero image was removed) but retained as the `og:image` social-share preview.
- `favicon.png` — browser tab / apple-touch icon.

## Conventions

- **Single file.** Keep all CSS in the inline `<style>` block in `index.html`;
  do not add external stylesheets or JS files unless asked.
- **Design tokens** live in the `:root` CSS variables at the top of the style
  block. Reuse them (`--green` `#94FF00` accent, `--bg` `#000`, `--muted`, etc.)
  rather than hard-coding new colors.
- **Typography:** display font is `Rajdhani` (uppercase headings), body font is
  `IBM Plex Mono`, both loaded from Google Fonts. Everything else falls back to
  system fonts.
- **Responsive:** a single `@media (max-width:600px)` block holds the mobile
  overrides. Keep mobile adjustments there.
- **Motion:** entrance animations use the `.fx` class and respect
  `prefers-reduced-motion`.
- When removing an element, also remove its now-unused CSS rules (desktop and
  mobile) to keep the file clean.

## Content notes

- Company: Proteus Dynamics — Calgary, Alberta, Canada.
- Contact: Robert Pearce, CEO — rpearce@proteusdynamics.ca.
- Keep the tone factual and understated; this is a B2B/government-facing page.

## Viewing locally

No server required — open the file directly:

```
open index.html
```
