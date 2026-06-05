# Project 1 Blueprint - White Snake

## 1. Page Identity

Project name:

```text
White Snake
```

Subtitle:

```text
A Cantonese Opera Rhythm Game
```

Positioning:

White Snake is a project case study inside Joy Li's graduate application portfolio.

It should present White Snake as a design project exploring how interactive storytelling can reconnect traditional culture with younger audiences.

It should not feel like:

- a standalone game website
- a cultural exhibition page
- a game marketing page
- a classroom assignment
- a UX case study template

Core message:

```text
Using interactive storytelling to reconnect traditional culture with a new generation.
```

## 2. Visual Direction

Framework:

```text
Modern international portfolio design
```

Project-specific visual language:

```text
Chinese ink wash
Cantonese Opera references
Restrained editorial composition
```

Mood:

- elegant
- minimal
- narrative
- cultural
- clear
- admissions-friendly
- design-focused

Avoid:

- heavy Chinese ornamentation
- scroll-style ancient layout
- museum exhibition feeling
- long poetic writing
- overly decorative typography
- big UX-template section headers

## 3. Color System

Primary:

```css
Paper White: #F8F6F2
Ink Black: #111111
Light Gray: #D8D3CC
```

Accent:

```css
Muted Vermilion: #9B3D3D
```

Usage ratio:

```text
95% black / white / gray
5% muted vermilion
```

Use muted vermilion for:

- current navigation state
- section numbers
- small highlights
- important quotes
- hover states
- interaction accents

Do not use muted vermilion as a large background color.

## 4. Final Page Structure

The White Snake page must follow this structure:

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

Do not revert to the older structure:

```text
Hero Video
Overview
Design Goal
Gameplay Design
Artistic Direction
Technical Development
Reflection
```

## 5. Hero Video

Height:

```css
100vh
```

Background:

Full-screen edited gameplay trailer created by Joy.

Current implementation may use a still image placeholder until the trailer is available.

Video rules:

- muted
- autoplay
- loop
- object-fit: cover
- dark overlay for readability

Overlay:

```css
background: rgba(0,0,0,0.35);
```

Main text:

```text
WHITE SNAKE
A Cantonese Opera Rhythm Game
```

Short description:

```text
White Snake is a narrative rhythm game inspired by Cantonese Opera. The project explores how rhythm, performance, and interactive storytelling can make traditional performing arts feel immediate for younger players.
```

Meta information:

```text
Role
Game Design / Programming / Art Direction

Engine
Unity

Platform
PC

Team
Solo Project
```

## 6. Project Overview

Purpose:

Summarize what the project is and how it works as a design case study.

Content direction:

```text
The game follows Bai Suzhen and Xu Xian from their first encounter at West Lake to the confrontation at Jinshan Temple.

Instead of treating opera as surface decoration, the project translates timing, gesture, musical tension, and stage emotion into playable systems.
```

Layout:

- two-column editorial layout
- selected gameplay screenshot below
- concise project information

## 7. Why This Project

Purpose:

Explain the design motivation.

Core question:

```text
How can traditional culture remain meaningful in a digital generation?
```

Cards:

```text
Problem
Young audiences rarely encounter traditional opera in their daily media environment.
```

```text
Question
Could gameplay become a new entry point for cultural storytelling?
```

```text
Approach
Use rhythm mechanics, narrative progression, and Cantonese Opera aesthetics as one connected experience.
```

Keep this section concise.

## 8. Inspiration

Purpose:

Show where the project came from and how cultural material became interactive.

Core idea:

```text
The project began from the tension between a classical legend and a contemporary controller.
```

Content direction:

```text
Cantonese Opera gave the project its emotional vocabulary: gesture, costume, rhythm, pause, and musical expression.

The controller reframed that vocabulary as action, timing, and player responsibility.
```

Suggested visuals:

- Cantonese Opera reference
- White Snake logo
- controller image
- collage showing opera plus gameplay thinking

## 9. Narrative Experience

Purpose:

Document the player journey.

The page must include a dedicated player journey section:

```text
Opening

Story Scene 01

Act I Gameplay

Story Scene 02

Act II Gameplay

Ending
```

Design logic:

Act I should communicate connection.

Act II should communicate conflict.

The journey should feel like a rhythm of story scenes and playable emotional beats.

## 10. Gameplay Design

Purpose:

Explain how rhythm mechanics express narrative emotion.

Act I:

```text
West Lake Encounter
Connection Through Rhythm
```

Core mechanic:

```text
Notes emerge from both characters and converge toward the center of the bridge.
```

Player experience:

```text
Players participate in the gradual formation of connection through rhythm.
```

Act II:

```text
Flooding Jinshan Temple
Conflict Through Rhythm
```

Core mechanic:

```text
The rhythm system becomes a boss battle. Perfect and Good hits damage Fahai's shield and health, while Miss breaks the player's rhythm.
```

Player experience:

```text
Players actively participate in the confrontation rather than only following the story.
```

Required visual:

```text
Bai Suzhen -> -> -> Judgement Area <- <- <- Xu Xian
```

## 11. Art Direction

Purpose:

Translate Cantonese Opera into a playable visual language.

This should not be a pure image gallery. It should explain production thinking.

Required production asset categories:

- Bai Suzhen character assets
- Fahai character assets
- environment assets
- ink wash assets
- UI assets

Current available asset references:

```text
images/project1-bg.png
images/white-snake-video-frame.png
images/project1-page2-opera.png
images/project1-page2-logo.png
images/project1-page2-controller.png
images/project1-page2-arrow.png
images/project1-page2-plus.png
images/project1-page2-tape.png
```

Content direction:

```text
The visual system uses ink wash atmosphere, opera costume references, character assets, environment assets, and sparse UI assets to keep the project cultural but not ornamental.
```

## 12. Development Process

Purpose:

Show how the project was built and iterated.

This section must exist both in the website and in the blueprint.

Required process evidence categories:

- prototype screenshots
- Unity screenshots
- implementation screenshots
- code screenshots

Current implementation can use structured placeholders until final screenshots are available.

Suggested content:

```text
Prototype Screenshots
Early rhythm tests for timing, note movement, and player input.

Unity Screenshots
Scene assembly, timeline setup, camera layers, and gameplay state testing.

Implementation Screenshots
Boss battle, judgement windows, UI feedback, and level iteration.

Code Screenshots
Timeline judgement, CSV level loading, note rendering, and combat logic.
```

## 13. Technical Challenges

Use this title instead of Technical Development.

The technical section should support the design story.

Show four systems using challenge / solution / impact:

### Timeline Judgement System

Challenge:

```text
Position-based judgement became inaccurate when notes had to follow animated characters.
```

Solution:

```text
Redesign the logic around expected arrival time instead of only screen position.
```

Impact:

```text
Music, animation, and narrative timing stayed synchronized.
```

### CSV Level Loader

Challenge:

```text
Manually adjusting note timing inside Unity was slow and error-prone.
```

Solution:

```text
Store note timing, ownership, and level data in CSV files.
```

Impact:

```text
Iteration became faster and less repetitive.
```

### Boss Battle System

Challenge:

```text
The second act needed stronger conflict than a traditional rhythm stage.
```

Solution:

```text
Connect Fahai's shield and health to rhythm judgement results.
```

Impact:

```text
The story climax became an interactive confrontation.
```

### Note Rendering Camera

Challenge:

```text
Notes were sometimes hidden behind background effects, subtitles, characters, or UI elements.
```

Solution:

```text
A dedicated camera renders the note layer above other visual elements.
```

Impact:

```text
The rhythm interface remained clear during visually complex scenes.
```

## 14. Notes From Development

This replaces the old Reflection section.

Do not use:

- Reflection as a giant heading
- old question-and-answer headings
- Q&A format
- school assignment tone

Use a smaller, quieter section title:

```text
09
Notes From Development
```

Tone:

- design journal
- project notes
- personal observations
- creative reflection
- conversational
- thoughtful

Current copy:

```text
One thing that worked particularly well was connecting gameplay directly to narrative emotion. In West Lake Encounter, the converging note system allowed the rhythm mechanic itself to express the growing relationship between Bai Suzhen and Xu Xian.

During development, I realized the biggest challenge was not simply adapting Cantonese Opera into a game. The harder problem was preserving the emotional meaning of the original work while still creating an experience that felt readable and playable for new audiences.

If I continue this project, I would focus on expanding the story, improving rhythm feedback, and creating stronger transitions between gameplay and performance. I want the next version to feel less like separated stages and more like a continuous performance shaped by player input.
```

## 15. Future Development

Use this title instead of Next Steps.

Future plans:

- additional story chapters
- opera archive system
- costume collection
- educational applications
- PC/mobile release

Current copy direction:

```text
Add additional story chapters, including Stealing the Immortal Herb, Broken Bridge Reunion, and Leifeng Pagoda.

Develop an opera archive system with character notes, music context, and performance knowledge.

Create a costume collection system that lets players learn through visual discovery.

Explore educational applications for cultural learning and classroom use.

Optimize the project for PC and mobile release.
```

## 16. Ending / Next Project

Do not use a heavy footer.

End with one quiet sentence:

```text
Traditional stories do not disappear. They simply wait for new ways to be told.
```

Below it:

```text
Next Project -> Project 2
```

## 17. Required Future Assets

When Joy provides additional project materials, add them without changing the page hierarchy.

Needed assets:

- edited gameplay trailer
- selected gameplay screenshot
- West Lake Encounter full-width image
- Act I gameplay GIF or short video
- Flooding Jinshan Temple full-width image
- Act II boss battle GIF or short video
- Bai Suzhen character assets
- Fahai character assets
- environment assets
- ink wash assets
- UI assets
- prototype screenshots
- Unity screenshots
- implementation screenshots
- code screenshots

Do not delete or modify existing files inside `images/`.
