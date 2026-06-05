# Joy Li Portfolio — Global Website Blueprint

## 1. Website Purpose

This is a personal portfolio website for Joy Li, primarily targeting CMU ETC and secondarily USC Games.

The website should present Joy as a designer who creates interactive experiences through storytelling, culture, and play.

The portfolio should feel modern, international, clean, design-driven, and easy for admissions reviewers to scan.

It should not feel like a corporate website, game studio website, traditional Chinese cultural exhibition, blog, or resume-only page.

---

## 2. Overall Site Structure

The website contains one landing page and four main content pages.

```text
Landing Page
│
├── Project 1: White Snake
├── Project 2: [Project Name]
├── Project 3: [Project Name]
└── Design Philosophy
```

Each project should have its own independent page.

The user enters the website through the landing page, then clicks into each project page.

Each project page should be a long vertical scrolling case study.

---

## 3. Navigation

Use a simple fixed top navigation bar.

```text
JOY LI

White Snake
Project 2
Project 3
Design Philosophy

EN | 中文
```

Rules:
- Do not hide the projects under a “Projects” dropdown.
- Each project should be directly visible in the navigation.
- Replace “Project 2” and “Project 3” with final project names later.
- The current page should be highlighted.
- For White Snake, use muted vermilion as the active color.

---

## 4. Landing Page

The landing page should be minimal and direct.

Purpose:
- introduce Joy Li
- show the three projects immediately
- allow quick navigation

Suggested hero text:

```text
JOY LI

Designing Interactive Experiences
Through Storytelling, Culture, and Play.
```

Below the hero, show three large project cards:

```text
White Snake
A Cantonese Opera Rhythm Game

Project 2
[Short description]

Project 3
[Short description]
```

Each project card should include:
- project title
- one-sentence description
- thumbnail image or short looping preview
- click interaction leading to that project page

---

## 5. Design Philosophy Page

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

Do not make it a long biography.

---

## 6. Global Visual Language

The overall website framework should use a modern international design language.

Project-specific visual identities can change per project.

For example:

White Snake:
- ink wash
- black and white
- muted vermilion accent
- paper-like background

Future projects may use different visual systems while sharing the same global layout rules.

---

## 7. Typography System

English:
- Titles: Cormorant Garamond
- Body text: Inter

Chinese:
- Titles: Source Han Serif / 思源宋体
- Body text: Source Han Sans / 思源黑体

Use large, elegant titles and clean readable body text.

Avoid decorative calligraphy fonts for the main interface.

---

## 8. Spacing System

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
Title → Subtitle: 16px
Subtitle → Body: 24px
Body → Image: 48px
Internal module spacing: 96px
Section-to-section spacing: 160px
Before/after full-screen visual breaks: 240px
```

The website should feel spacious, calm, and editorial.

---

## 9. Layout System

Use a hybrid layout.

For emotional or cinematic moments:
- full-width / centered / Apple-like

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

---

## 10. Image and Video Rules

Use visuals as the main storytelling tool.

Recommended ratio:
- 70% visuals
- 30% text

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

---

## 11. Bilingual System

The website should support English and Chinese switching.

Default language:
English

Chinese version should not be a literal word-by-word translation. It should preserve the same design logic and tone.

Language switch:
```text
EN | 中文
```

Should appear in the main navigation.

---

## 12. Development Notes for Codex

Build the website as multiple pages/routes:

```text
/
 /white-snake
 /project-2
 /project-3
 /design-philosophy
```

Each page should have:
- fixed navigation
- responsive layout
- English/Chinese content support
- smooth scrolling behavior
- image/video asset placeholders

The project pages should use reusable components:
- HeroVideo
- ProjectOverview
- SectionHeader
- VisualBreak
- TwoColumnBlock
- ChallengeSolutionImpactCard
- ProjectNavigation
