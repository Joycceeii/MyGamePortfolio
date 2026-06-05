# Agent Guide for Joy Li Portfolio

This repository is Joy Li's personal interactive experience design portfolio for graduate school applications, primarily CMU Entertainment Technology Center and secondarily USC Games.

The current website is a complete redesign. Do not restore the old single-page architecture, old layouts, old CSS system, old pagination system, hamburger menu, decorative hand-drawn style, or previous portfolio structure.

## Read First

Before making design or content changes, read these files in this order:

1. `joy_li_portfolio_global_blueprint.md`
2. `white_snake_project_blueprint.md`
3. `agent.md`
4. The page file you are editing
5. `style.css`

The two blueprint files are the source of truth. If existing code conflicts with a blueprint, follow the blueprint unless the user gives a newer instruction in the conversation.

## Current Published Site

The site is intended to publish through GitHub Pages as a project site:

```text
https://joycceeii.github.io/MyGamePortfolio/
```

Use relative links so the site works under `/MyGamePortfolio/`.

Required URL structure:

```text
/MyGamePortfolio/
/MyGamePortfolio/whitesnake/
/MyGamePortfolio/project2/
/MyGamePortfolio/project3/
/MyGamePortfolio/designphilosophy/
```

Do not use root-relative links like `/whitesnake/`, because those can break on GitHub Pages project sites.

Use these link patterns:

From `index.html`:

```html
<a href="whitesnake/">White Snake</a>
```

From project subpages:

```html
<a href="../whitesnake/">White Snake</a>
```

## Current File Structure

```text
index.html
style.css
.nojekyll
agent.md
joy_li_portfolio_global_blueprint.md
white_snake_project_blueprint.md

whitesnake/index.html
project2/index.html
project3/index.html
designphilosophy/index.html

images/
```

`index.html` is the landing page.

Each folder route contains an `index.html` so GitHub Pages can serve clean URLs such as `/whitesnake/`.

`.nojekyll` should stay in the repository so GitHub Pages serves the static folders directly.

## Asset Rule

`images/` is the master asset library.

Do not delete, rename, move, compress, overwrite, or modify files inside `images/` unless the user explicitly asks for that exact asset operation.

It is okay to reference existing images from HTML or CSS.

If the user adds new images, treat them as user-owned assets. Add them to Git only when they are used by the site or the user asks to track them.

Current image assets include:

```text
images/project1-bg.png
images/white-snake-video-frame.png
images/project1-page2-arrow.png
images/project1-page2-controller.png
images/project1-page2-logo.png
images/project1-page2-opera.png
images/project1-page2-plus.png
images/project1-page2-tape.png
```

## Design Direction

The portfolio should feel like a professional graduate application portfolio, not a student assignment, game studio site, museum exhibition, culture-promotion page, or resume page.

The site should communicate:

```text
Designing interactive experiences through storytelling, culture, and play.
```

Homepage hierarchy:

```text
Ideas first
Projects second
Designer identity third
```

The homepage should introduce Joy's ideas before introducing Joy as a person.

Projects are the main characters of the portfolio. Joy is the narrator.

Priority order:

1. Design thinking
2. Storytelling
3. Interactive experience
4. Technical execution

Technology supports the experience. Do not make technology the main narrative focus.

## Visual Language

Use a modern international portfolio style:

- editorial
- minimal
- elegant
- contemporary
- design-focused
- admissions-friendly

Avoid:

- heavy Chinese decoration
- ancient scroll aesthetics
- excessive animation
- visual clutter
- corporate styling
- glossy cards
- long poetic writing
- decorative calligraphy fonts for interface text

White Snake may use ink-wash atmosphere, but the page must still feel like an international design case study.

## Typography

English:

```text
Titles: Cormorant Garamond
Body: Inter
```

Chinese:

```text
Titles: Source Han Serif / Noto Serif SC fallback
Body: Source Han Sans / Noto Sans SC fallback
```

Do not reintroduce old decorative fonts such as handwritten or playful display fonts for the main interface.

## Color System

Global colors:

```css
Paper White: #F8F6F2
Ink Black: #111111
Light Gray: #D8D3CC
Muted Vermilion: #9B3D3D
```

Use muted vermilion sparingly for:

- active navigation state
- section numbers
- small highlights
- hover states
- important quotes
- interaction accents

Do not use muted vermilion as a large background color.

## Spacing System

Use the 8px-based spacing tokens already defined in `style.css`:

```css
--xs: 8px;
--s: 16px;
--m: 24px;
--l: 48px;
--xl: 96px;
--2xl: 160px;
--3xl: 240px;
```

Keep the site spacious and calm. Favor readability and visual hierarchy over dense content.

## Layout System

Use the existing shared CSS system in `style.css`.

Key layout patterns:

- `.container`: max-width 1200px
- `.measure`: readable body text width, max-width 650px
- `.two-column`: editorial explanation layout
- `.card-grid`: structured cards
- `.system-grid`: technical system cards
- `.visual-break`: full-screen emotional/cinematic break
- `.project-hero`: full-screen project hero

Do not add a framework or build step unless the user explicitly asks. This is a static HTML/CSS site.

## Navigation Rules

Fixed top navigation should stay visible:

```text
JOY LI
White Snake
Project 2
Project 3
Design Philosophy
EN | Chinese
```

Rules:

- No dropdown menu
- No desktop hamburger menu
- Current page highlighted with `aria-current="page"`
- Language switch visible at all times
- Use relative links for GitHub Pages compatibility

## Bilingual System

The site uses `.en` and `.zh` spans plus a small JavaScript language switcher on each page.

Default language: English.

Chinese copy should match the same design intent and tone. It does not need to be word-for-word literal.

If adding visible content, add both English and Chinese unless the user asks otherwise.

## Landing Page

File:

```text
index.html
```

Purpose:

- Introduce Joy's design ideas before Joy's identity
- Communicate the themes connecting the work
- Immediately show the three project cards
- Let admissions reviewers navigate quickly

Required landing page structure:

```text
Hero Statement
Three Featured Projects
Small Designer Signature
```

Hero statement:

```text
INTERACTIVE EXPERIENCE DESIGN
Designing Interactive Experiences Through Storytelling, Culture, and Play.
I create games and interactive experiences that explore culture, emotion, and human connection through play.
```

Do not use a giant `JOY LI` hero.

Joy's name should never be the largest visual element on the homepage.

Keep the landing page minimal and intellectually curious. Do not turn it into an about page, resume page, personal branding site, or long project list.

Project cards should link directly to:

```text
whitesnake/
project2/
project3/
```

Designer signature should appear quietly after the featured projects:

```text
Joy Li
Interactive Experience Designer
```

## White Snake Page

File:

```text
whitesnake/index.html
```

Follow `white_snake_project_blueprint.md`.

Required section order:

```text
Hero Video
Project Overview
Why This Project
Inspiration
Narrative Experience
Gameplay Design
Art Direction
Development Process
Technical Challenges
Notes From Development
Future Development
Next Project
```

Do not remove or reorder these sections unless the user gives a new direction.

The current implementation uses available still images as placeholders where the blueprint asks for video/GIF/specific screenshots. If the user later provides actual videos, GIFs, or screenshots, replace the placeholders while preserving the same section structure.

Narrative Experience must document this player journey:

```text
Opening
Story Scene 01
Act I Gameplay
Story Scene 02
Act II Gameplay
Ending
```

Development Process must include placeholders or final materials for:

- prototype screenshots
- Unity screenshots
- implementation screenshots
- code screenshots

Art Direction must account for:

- Bai Suzhen character assets
- Fahai character assets
- environment assets
- ink wash assets
- UI assets

Notes From Development replaces the old Reflection section. Do not use old question-and-answer headings.

Important White Snake positioning:

```text
Using interactive storytelling to reconnect traditional culture with a new generation.
```

White Snake should read as a design case study. It should not read as a standalone game marketing site or cultural exhibition page.

## Project 2 and Project 3

Files:

```text
project2/index.html
project3/index.html
```

These are placeholder case-study routes until the user provides final project names, content, and assets.

Do not invent detailed project claims. Keep placeholders restrained and professional.

When the user provides new project details, turn each page into a long vertical case study using the same global layout logic:

1. Project hero
2. Overview
3. Design goal
4. Gameplay or interaction design
5. Visual/process evidence
6. Systems or technical support
7. Challenges and solutions
8. Notes From Development
9. Next project link

Update navigation labels when final project names are known.

## Design Philosophy Page

File:

```text
designphilosophy/index.html
```

This replaces a traditional About page.

It should be short, thoughtful, and ETC-oriented.

It should answer:

- What kind of designer is Joy?
- What does Joy care about?
- Why does Joy make games?

Current structure:

```text
Design Philosophy
Story
Culture
Experience
```

Do not turn this page into a biography, resume, or long personal essay.

## CSS Maintenance

File:

```text
style.css
```

Keep all shared visual systems here.

Before adding new CSS:

1. Check whether an existing class already fits.
2. Reuse spacing/color/type variables.
3. Avoid one-off visual hacks.
4. Keep cards, images, and sections responsive.

Avoid:

- heavy shadows
- large gradients
- decorative blobs
- excessive border radius
- dense visual noise
- viewport-width font scaling

## Local Preview

Because the site uses folder routes, preview it with a local server instead of opening nested HTML files directly.

Recommended command:

```powershell
python -m http.server 4173 --bind 127.0.0.1
```

Then open:

```text
http://127.0.0.1:4173/
http://127.0.0.1:4173/whitesnake/
http://127.0.0.1:4173/project2/
http://127.0.0.1:4173/project3/
http://127.0.0.1:4173/designphilosophy/
```

## Verification Checklist

Before committing changes:

1. Check `git status --short`.
2. Confirm no unintended edits inside `images/`.
3. Confirm no root-relative page links like `href="/whitesnake/"`.
4. Confirm required routes load locally:
   - `/`
   - `/whitesnake/`
   - `/project2/`
   - `/project3/`
   - `/designphilosophy/`
5. Confirm navigation current state uses `aria-current="page"`.
6. Confirm language switch still appears in the top nav.
7. Confirm English and Chinese spans are present for new visible content.
8. Confirm the page still feels calm, editorial, and admissions-friendly.

Useful checks:

```powershell
rg -n 'href="/|src="/' index.html whitesnake project2 project3 designphilosophy
git status --short
git diff --stat
```

## Git Workflow

The main remote is:

```text
origin https://github.com/Joycceeii/MyGamePortfolio.git
```

Default branch:

```text
main
```

Normal publish flow:

```powershell
git status
git add <changed files>
git commit -m "Clear commit message"
git push origin main
```

Do not commit unrelated user changes unless the user asks.

If `agent.md` or blueprint files are updated, it is okay to commit them when the user explicitly asks to update project documentation.

## Current Documentation Files

The blueprint files are now part of the project folder:

```text
joy_li_portfolio_global_blueprint.md
white_snake_project_blueprint.md
```

Future AI agents should use these local files instead of reading copies from Downloads.

Older Chinese guide files may still exist in the repo from the previous website era. They are not the current source of truth for the redesign.

## Non-Goals

Do not:

- rebuild the old single-page portfolio
- restore old section pagination
- add a Projects landing page
- hide project links inside a dropdown
- use `/white-snake/`, `/project-2/`, or `/project-3/` as final URLs
- make White Snake a cultural exhibition page
- make the site look like a game studio marketing site
- delete or modify assets in `images/`
- introduce a build system unless requested

The current goal is a clean, static, GitHub Pages-friendly portfolio that presents Joy Li as a thoughtful designer of interactive experiences.
