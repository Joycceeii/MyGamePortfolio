# Joy Li Portfolio - Global Website Blueprint

## 1. Website Purpose

This is Joy Li's personal portfolio website for graduate school applications.

Primary audience:

```text
CMU Entertainment Technology Center
```

Secondary audience:

```text
USC Games
```

The website should present Joy as a designer who creates interactive experiences through storytelling, culture, and play.

The portfolio should feel:

- modern
- international
- clean
- design-driven
- intellectually curious
- easy for admissions reviewers to scan

It should not feel like:

- a corporate website
- a game studio website
- a traditional Chinese cultural exhibition
- a blog
- a resume-only page
- an influencer portfolio
- a freelancer landing page
- a personal branding site

## 2. Core Design Principles

The homepage should introduce the designer's ideas before introducing the designer.

Projects are the main characters of the portfolio. The designer is the narrator.

The homepage should function as an introduction to the work, not an introduction to the person.

Admissions reviewers should first understand:

- what problems Joy explores
- what kind of experiences Joy designs
- what themes connect the work

Only afterwards should they learn Joy's name.

The portfolio should communicate:

```text
Joy Li designs interactive experiences through storytelling, culture, and play.
```

Priority order:

1. Design thinking
2. Storytelling
3. Interactive experience
4. Technical execution

Technology supports the experience. Technology is not the main focus.

## 3. Overall Site Structure

The website contains one landing page and four content pages.

```text
Landing Page
|-- Project 1: White Snake
|-- Project 2: [Project Name]
|-- Project 3: [Project Name]
`-- Design Philosophy
```

Each project should have its own independent page.

The user enters through the landing page, then clicks directly into each project page.

Each project page should be a long vertical scrolling case study.

GitHub Pages route structure:

```text
/
/whitesnake/
/project2/
/project3/
/designphilosophy/
```

Use relative links so the site works under:

```text
https://joycceeii.github.io/MyGamePortfolio/
```

Do not use root-relative links such as `/whitesnake/`.

## 4. Navigation

Use a simple fixed top navigation bar.

```text
JOY LI

White Snake
Project 2
Project 3
Design Philosophy

EN | Chinese
```

Rules:

- Do not hide projects under a Projects dropdown.
- Each project should be directly visible in the navigation.
- No desktop hamburger menu.
- Replace Project 2 and Project 3 with final project names later.
- The current page should be highlighted.
- For White Snake, muted vermilion may be used as the active color.
- The language switch should stay visible.

The nav can contain Joy's name as a small orientation marker, but the homepage hero must not make JOY LI the dominant visual element.

## 5. Landing Page

The landing page should be minimal, direct, and ETC-oriented.

Purpose:

- introduce Joy's design ideas
- communicate the themes connecting the work
- show the three featured projects immediately
- allow quick navigation into case studies

The landing page should feel like:

```text
Here is how I think.
```

Not:

```text
Here is who I am.
```

New landing page structure:

```text
Hero Statement

↓

Three Featured Projects

↓

Small Designer Signature
```

### Hero Statement

The hero should center around a design philosophy statement.

Do not use a giant JOY LI hero.

Do not place Joy's name as the largest visual element on the page.

Recommended structure:

```text
[small label]
INTERACTIVE EXPERIENCE DESIGN

[main statement]
Designing Interactive Experiences
Through Storytelling, Culture, and Play.

[supporting text]
I create games and interactive experiences that explore culture, emotion, and human connection through play.
```

The main statement is the primary visual element.

### Three Featured Projects

After the hero statement, immediately present:

```text
White Snake
Project 2
Project 3
```

Use large editorial project cards.

Project previews should be more visually dominant than Joy's name.

Each project card should include:

- project title
- one-sentence description
- thumbnail image or short looping preview
- click interaction leading to that project page

### Small Designer Signature

Joy's identity should appear as a tertiary element after the work direction is clear.

Suggested signature:

```text
Joy Li
Interactive Experience Designer
```

The signature should be small and quiet. It should never compete with the project previews or the hero design statement.

## 6. Design Philosophy Page

This replaces a traditional About page.

It should be short, thoughtful, and ETC-oriented.

It should answer:

- What kind of designer is Joy?
- What does Joy care about?
- Why does Joy make games?

Suggested structure:

```text
Design Philosophy

I believe games are not only systems of play, but systems of communication.

Story
Games can make stories participatory.

Culture
Games can connect people with traditions that might otherwise feel distant.

Experience
Games create emotional understanding through interaction.
```

Keep this page within one screen or slightly longer.

Do not make it a biography page.

## 7. Global Visual Language

The overall website framework should use a modern international design language.

Project-specific visual identities can change per project.

White Snake:

- ink wash
- black and white
- muted vermilion accent
- paper-like background

Future projects may use different visual systems while sharing the same global layout rules.

Avoid:

- heavy Chinese ornamentation
- scroll-style ancient layout
- excessive decoration
- overly promotional copy
- resume-first presentation

## 8. Typography System

English:

```text
Titles: Cormorant Garamond
Body text: Inter
```

Chinese:

```text
Titles: Source Han Serif / Noto Serif SC fallback
Body text: Source Han Sans / Noto Sans SC fallback
```

Use large, elegant titles and clean readable body text.

Avoid decorative calligraphy fonts for the main interface.

## 9. Color System

Global colors:

```css
Paper White: #F8F6F2
Ink Black: #111111
Light Gray: #D8D3CC
Muted Vermilion: #9B3D3D
```

Use muted vermilion sparingly for:

- current navigation state
- section numbers
- small highlights
- important quotes
- hover states
- interaction accents

Do not use muted vermilion as a large background color.

## 10. Spacing System

Use an 8px-based spacing system.

```css
XS = 8px
S  = 16px
M  = 24px
L  = 48px
XL = 96px
2XL = 160px
3XL = 240px
```

Recommended usage:

```text
Title to subtitle: 16px
Subtitle to body: 24px
Body to image: 48px
Internal module spacing: 96px
Section-to-section spacing: 160px
Before/after full-screen visual breaks: 240px
```

The website should feel spacious, calm, and editorial.

## 11. Layout System

Use a hybrid layout.

For emotional or cinematic moments:

- full-width
- centered
- cinematic

For detailed design explanation:

- two-column editorial layout

For technical breakdown:

- cards or structured grids

General container:

```css
max-width: 1200px;
margin: 0 auto;
padding-left/right: responsive;
```

Body text width:

```css
max-width: 650px;
```

## 12. Image and Video Rules

Use visuals as the main storytelling tool.

Recommended ratio:

```text
70% visuals
30% text
```

Do not overuse rounded corners.

Preferred:

```css
border-radius: 0;
```

Avoid:

- heavy shadows
- glossy cards
- gradients
- overdecorated frames
- purely decorative visuals that do not explain the work

## 13. Bilingual System

The website should support English and Chinese switching.

Default language:

```text
English
```

Chinese version should not be a literal word-by-word translation. It should preserve the same design logic and tone.

Language switch:

```text
EN | Chinese
```

The language switch should appear in the main navigation.

## 14. Development Notes for Codex

Build and maintain the website as multiple static pages/routes:

```text
/
/whitesnake/
/project2/
/project3/
/designphilosophy/
```

Each page should have:

- fixed navigation
- responsive layout
- English/Chinese content support
- smooth scrolling behavior
- image/video asset placeholders

Reusable page patterns:

- Hero Statement
- Hero Video
- Project Overview
- Why This Project
- Inspiration
- Narrative Experience
- Section Header
- Visual Break
- Two Column Block
- Challenge/Solution/Impact Card
- Development Process
- Project Navigation

Future implementations must preserve the homepage hierarchy:

```text
Ideas first
Projects second
Designer identity third
```

The homepage should direct attention toward the work.

## 15. White Snake Page Structure

White Snake is the first fully developed project case study.

Its structure is:

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

Do not use the older structure:

```text
Hero Video
Overview
Design Goal
Gameplay Design
Artistic Direction
Technical Development
Reflection
```

White Snake should include a dedicated Narrative Experience section documenting the player journey:

```text
Opening
Story Scene 01
Act I Gameplay
Story Scene 02
Act II Gameplay
Ending
```

White Snake should include a dedicated Development Process section documenting:

- prototype screenshots
- Unity screenshots
- implementation screenshots
- code screenshots

White Snake should include Art Direction production asset categories:

- Bai Suzhen character assets
- Fahai character assets
- environment assets
- ink wash assets
- UI assets

The old case-study Reflection structure should not be used.

Replace it with:

```text
Notes From Development
```

This section should feel like a designer's notebook, not a school assignment or UX template.

Future Development should include:

- additional story chapters
- opera archive system
- costume collection
- educational applications
- PC/mobile release
