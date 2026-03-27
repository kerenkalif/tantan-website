# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A static Hebrew (RTL) website for "תאן תאן" (TanTan), hosted on GitHub Pages at **tantan.co.il**. The site showcases YouTube content, Scratch projects, and game-related series (סאן תאן, Suntan PVP, Township).

## Architecture

- **Pure static site** — plain HTML/CSS, no build tools, no JavaScript, no frameworks
- **No build/test/lint commands** — open HTML files directly in a browser to preview
- **Deployment** — pushed to `main` branch, served via GitHub Pages (CNAME: `tantan.co.il`)

## Site Structure

- [index.html](index.html) — Homepage with links to series, YouTube, and Scratch profile
- [style.css](style.css) — Shared stylesheet (fixed left sidebar navigation)
- Series subpages: [suntan.html](suntan.html) → [suntan_s1.html](suntan_s1.html) → character pages; [tantan_tv.HTML](tantan_tv.HTML); [suntanpvp.HTML](suntanpvp.HTML); [township.html](township.html)
- Images stored in root and [images/](images/) folder

## Key Conventions

- **RTL layout**: All pages use `text-align:right` on `<body>`, content is in Hebrew
- **Navigation**: Shared sidebar pattern using `<ul>` styled via `style.css` (fixed position, orange background). Each page manually includes its own nav links — there is no templating
- **Inline styles**: Pages mix inline `<style>` blocks with the shared CSS file
- **File naming**: Inconsistent casing (`.html` vs `.HTML`) — maintain existing casing when editing existing files
- **Favicon**: All pages use `tantanush.png` as the icon
- **Image sizing**: Images use `width="10%"` inline attribute consistently
