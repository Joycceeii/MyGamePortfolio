# Agent Guide

This repository is a single-page personal game design portfolio website for graduate school applications, especially for a game designer applying to programs in the United States.

## Must Read First

When starting a new AI conversation for this project, read these files before making changes:

- `agent.md`
- `index.html`
- `填空指南.md`
- `Figma网页排版完全指南.md`
- `README.md`

Then inspect the current folder tree and run:

```powershell
git status --short
```

Do not begin editing until you understand the current HTML structure and the user's intended Figma-based workflow.

## Current Project Shape

- Main website file: `index.html`
- The website is intentionally a single HTML file with embedded `<style>` and `<script>`.
- `style.css` is legacy/unused by the current `index.html`; do not rely on it unless the user asks to restore external CSS.
- No build system is configured.
- The site should work by opening `index.html` directly in a browser.
- Supporting documentation:
  - `填空指南.md`: detailed fill-in guide for replacing text, images, navigation, project content, styles, testing, and GitHub Pages publishing.
  - `Figma网页排版完全指南.md`: detailed beginner Figma workflow for designing project layouts and pasting exported content into `.section-content`.

## Website Structure

The current `index.html` contains:

- Full-screen welcome section: `#welcome`, `.welcome-section`
- Fixed top navigation: `.site-nav`
- Language switching: `.zh` and `.en` elements, controlled by JavaScript
- Project 1: `#project1.project-shuimo`, intended for the user's `《白蛇传》` project with ink-wash styling
- Project 2: `#project2.project-handdrawn`
- Project 3: `#project3.project-handdrawn`
- About section: `#about.section-about`
- Empty project content containers: `.section-content`
- Mobile hamburger navigation
- Active nav highlighting via `IntersectionObserver`
- Back-to-top buttons: `.btn-top`
- A large HTML comment at the end with image replacement, text replacement, and Figma workflow notes

## User Workflow Assumption

The user wants to build layouts visually, like collage work, rather than hand-code coordinates.

Preferred workflow:

1. Design a 900px-wide project section in Figma.
2. Export HTML/CSS or export a full section image as a fallback.
3. Place exported images in an `images/` folder.
4. Paste project layout HTML into the matching `.section-content`.
5. Update image paths to local paths such as `images/project1-main.png`.
6. Preview `index.html` in a browser.

If Figma export code is messy, recommend the simple screenshot/image fallback before over-engineering.

## Replacement Conventions

The project uses visible comments for replacement points:

```html
<!-- 🔧 替换：说明 -->
```

When adding new replaceable content, keep this convention.

Recommended image folder:

```text
images/
```

Recommended image names:

- `logo-small.png`
- `welcome-bg.jpg`
- `welcome-logo.png`
- `project1-bg.jpg`
- `project2-bg.jpg`
- `project3-bg.jpg`
- `avatar.jpg`
- `divider.png`

Use forward slashes in HTML paths:

```html
<img src="images/avatar.jpg" alt="头像">
```

## Design Direction

The site is for graduate admissions reviewers, so it should be visually expressive but easy to scan.

Priorities:

- Clear project storytelling
- Visible design process and iteration
- Strong screenshots or visual artifacts
- Easy reading in English
- Mobile-friendly layout
- Polished, gentle, hand-drawn portfolio aesthetic

Current global visual direction:

- Cream background: `--bg-cream`
- Soft pastel accents
- Rounded paper-like containers
- Handwritten title fonts
- Ink-wash style for project 1
- Playful hand-drawn style for projects 2 and 3

## Editing Rules

- Keep `index.html` as the single source of truth unless the user asks to split files.
- Keep encoding as UTF-8.
- Preserve Chinese comments and replacement markers.
- Do not remove bilingual `.zh` / `.en` structure when editing visible text.
- When adding text, provide both Chinese and English versions where appropriate.
- Keep project `.section-content` areas flexible for user/Figma content.
- Avoid introducing frameworks or build tools unless explicitly requested.
- Do not overwrite user-filled portfolio content.
- If generated Figma code includes a full `<!DOCTYPE html>`, `<html>`, `<head>`, or `<body>`, do not paste those wrappers into `.section-content`; only paste the relevant inner content and merge CSS into the existing `<style>`.

## Verification

After edits:

- Read the edited area back with UTF-8.
- Check that `index.html` still contains one valid document structure.
- Confirm key anchors still exist: `#welcome`, `#project1`, `#project2`, `#project3`, `#about`.
- Confirm language switching still uses `.zh`, `.en`, and `body.lang-en`.
- Confirm navigation links have matching `href="#..."` and `data-target="..."`.
- Confirm image paths use local `images/...` paths when possible.
- Preview `index.html` in a browser when feasible.
- Check desktop and mobile widths, especially the hamburger menu and timeline.
- Run `git status --short` and report changed files.

## Known Notes

- Earlier mojibake in `index.html` and `style.css` was repaired. If乱码 reappears, fix encoding/content as UTF-8.
- `style.css` may still show as modified in Git history, but the current website does not import it.
- The user prefers every assistant answer to end with `水蓝蓝`.
