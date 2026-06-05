# Project 1 Blueprint — White Snake

## 1. Page Identity

Project Name:
White Snake

Subtitle:
A Cantonese Opera Rhythm Game

Positioning:
This is a project case study inside Joy Li's personal portfolio.

It should not feel like a standalone game website or cultural exhibition page.

It should present White Snake as a design project exploring how games can reconnect traditional culture with younger audiences.

Core message:
```text
Using interactive storytelling to reconnect traditional culture with a new generation.
```

---

## 2. Visual Direction

Framework:
Modern international portfolio design

Project-specific visual language:
Chinese ink wash

Mood:
- elegant
- minimal
- narrative
- cultural
- clear
- admissions-friendly

Avoid:
- heavy Chinese ornamentation
- scroll-style ancient layout
- museum exhibition feeling
- long poetic writing
- overly decorative typography

---

## 3. Color System for This Project

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

Do not use it as a large background color.

---

## 4. Page Structure

```text
Hero Video

↓
Overview

↓
Design Goal

↓
Visual Break I — Act I: West Lake Encounter

↓
Gameplay Design: Act I

↓
Visual Break II — Act II: Flooding Jinshan Temple

↓
Gameplay Design: Act II

↓
Artistic Direction

↓
Building Systems for Storytelling

↓
Challenges & Solutions

↓
Reflection

↓
Next Steps

↓
Next Project
```

---

## 5. Section 01 — Hero Video

Height:
```css
100vh
```

Background:
Full-screen edited gameplay trailer created by Joy.

Video rules:
- muted
- autoplay
- loop
- object-fit: cover
- dark overlay for readability

Suggested trailer sequence:
```text
Logo
↓
West Lake Encounter
↓
Rhythm Gameplay
↓
Character Interaction
↓
Flooding Jinshan Temple
↓
Boss Battle
↓
Logo
```

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
White Snake is a narrative rhythm game inspired by Cantonese Opera. Through rhythm gameplay and interactive storytelling, the project explores how traditional performing arts can connect with younger audiences in the digital age.
```

Meta information:
```text
Role
Game Design / Programming / Art Direction

Engine
Unity

Platform
PC

Duration
[To be filled]
```

Scroll indicator:
Bottom right, small and minimal.

---

## 6. Section 02 — Overview

Layout:
Two-column editorial layout.

Container:
```css
max-width: 1200px;
padding-top/bottom: 160px;
```

Left column:
Project Summary

Right column:
Project Information

Suggested content:

```text
Project Summary

White Snake is a narrative rhythm game based on the Chinese folk legend of White Snake and inspired by Cantonese Opera. The game follows Bai Suzhen and Xu Xian from their first encounter at West Lake to the conflict at Jinshan Temple.

The project combines rhythm gameplay, ink-wash visual design, and interactive storytelling to introduce traditional performing arts through a contemporary game format.
```

Project Info:
```text
Genre: Narrative Rhythm Game
Role: Game Design / Programming / Art Direction
Engine: Unity
Platform: PC
Team Size: Solo Project
Duration: [To be filled]
```

Visual:
One selected gameplay screenshot below the two-column section.

---

## 7. Section 03 — Design Goal

Section title:
```text
Design Goal
```

Subtitle:
```text
How can traditional culture remain meaningful in a digital generation?
```

Layout:
Three cards in one row on desktop, stacked on mobile.

Cards:

```text
Challenge
Young audiences rarely encounter traditional opera in their daily media environment.
```

```text
Question
Could gameplay become a new entry point for cultural storytelling?
```

```text
Approach
Combine rhythm mechanics, narrative progression, and Cantonese Opera aesthetics into one interactive experience.
```

Keep this section concise.

---

## 8. Visual Break I — Act I: West Lake Encounter

Full-width or full-screen image.

Asset:
West Lake Encounter scene.

Text overlay:
```text
Act I
West Lake Encounter

Connection Through Rhythm
```

Purpose:
This is the first emotional visual break.

No long explanation.

---

## 9. Section 04 — Gameplay Design: Act I

Section title:
```text
Gameplay Design
```

Subtitle:
```text
Designing Emotion Through Rhythm
```

Act title:
```text
Act I — West Lake Encounter
```

Layout:
Two-column layout.

Left:
Design explanation

Right:
Gameplay GIF or short video

Structure:

```text
Design Goal
Express the emotional development between Bai Suzhen and Xu Xian.

Core Mechanic
Notes emerge from both characters and converge toward the center of the bridge.

Player Experience
Players participate in the gradual formation of connection through rhythm.

Outcome
The rhythm system becomes a narrative device rather than a separate gameplay layer.
```

Additional visual:
Mechanic diagram showing two-direction note convergence.

Diagram concept:
```text
Bai Suzhen → → → Judgement Area ← ← ← Xu Xian
```

---

## 10. Visual Break II — Act II: Flooding Jinshan Temple

Full-width or full-screen image.

Asset:
Flooding Jinshan Temple Boss Battle scene.

Text overlay:
```text
Act II
Flooding Jinshan Temple

Conflict Through Rhythm
```

Purpose:
This is the second major visual climax.

No long explanation.

---

## 11. Section 05 — Gameplay Design: Act II

Act title:
```text
Act II — Flooding Jinshan Temple
```

Layout:
Two-column layout.

Left:
Design explanation

Right:
Boss battle GIF or short video

Structure:

```text
Design Goal
Transform the story's emotional conflict into an active gameplay challenge.

Core Mechanic
The rhythm system is combined with a boss battle. Perfect and Good hits damage Fahai's shield and health, while Miss breaks the player's rhythm.

Player Experience
Players are no longer only following the story; they actively participate in the confrontation.

Outcome
The conflict between love, fate, and authority becomes playable through rhythm-based combat.
```

---

## 12. Section 06 — Artistic Direction

Section title:
```text
Artistic Direction
```

Subtitle:
```text
Translating Cantonese Opera into a playable visual language.
```

Structure:
Design Thinking → References → Final Result

Do not make this a pure image gallery.

Subsection 1:
```text
Why Ink Wash?
The ink-wash style creates a restrained visual atmosphere that echoes the mist, water, and emotional ambiguity of the White Snake legend.
```

Subsection 2:
```text
Why Cantonese Opera?
The project references Cantonese Opera costumes, stage aesthetics, and musical expression to preserve the cultural identity of the source material.
```

Suggested visuals:
- ink-wash background image
- character/costume reference
- final in-game character or scene screenshot
- UI screenshot

---

## 13. Section 07 — Building Systems for Storytelling

Use this title instead of “Technical Development”.

Section title:
```text
Building Systems for Storytelling
```

Subtitle:
```text
Technical systems were designed to support rhythm, narrative, and visual clarity.
```

Show four systems.

Each system uses:
Challenge → Solution → Impact

System 1:
```text
Timeline Judgement System

Challenge
Position-based judgement became inaccurate when notes had to follow animated characters.

Solution
I redesigned the judgement logic around a timeline-based system that compares player input with each note's expected arrival time.

Impact
This improved rhythm accuracy and kept music, animation, and narrative timing synchronized.
```

System 2:
```text
CSV Level Loader

Challenge
Manually adjusting note timing inside the engine was slow and error-prone.

Solution
I stored note timing, ownership, and level data in CSV files, then built a LevelData Loader to convert the data into playable note sequences.

Impact
This made iteration faster and reduced repetitive manual adjustment.
```

System 3:
```text
Boss Battle System

Challenge
The second act needed stronger conflict than a traditional rhythm stage.

Solution
I gave Fahai a shield and health system connected to rhythm judgement results.

Impact
The story climax became an interactive confrontation rather than a passive cutscene.
```

System 4:
```text
Note Rendering Camera

Challenge
Notes were sometimes hidden behind background effects, subtitles, characters, or UI elements.

Solution
I created a dedicated camera to render the note layer above other visual elements.

Impact
The rhythm interface remained clear during visually complex scenes.
```

Suggested visuals:
- timeline diagram
- CSV screenshot
- boss health/shield diagram
- camera layer diagram

---

## 14. Section 08 — Challenges & Solutions

Layout:
Card grid.

Cards should be short and scannable.

Card 1:
```text
Ghost Notes
Problem: Player inputs were counted as Miss even when no visible note was present.
Solution: Add an activation window so keys are only detected when a note enters the judgement zone.
```

Card 2:
```text
Layer Conflict
Problem: Notes were visually blocked by background effects and UI layers.
Solution: Use a dedicated note-rendering camera.
```

Card 3:
```text
Rhythm Synchronization
Problem: Character movement made position-based judgement unreliable.
Solution: Move to a timeline-based judgement system.
```

---

## 15. Section 09 — Reflection

Section title:
```text
Reflection
```

Suggested structure:

```text
What worked?
The strongest part of this project was the connection between gameplay and narrative. The two-direction note movement in West Lake Encounter and the boss battle in Flooding Jinshan Temple allowed the mechanics to express story emotions directly.

What surprised me?
I initially thought the main challenge would be adapting Cantonese Opera into a game. During development, I realized the deeper challenge was preserving the emotional meaning of the source material while still making the game readable and engaging for new players.

What would I improve next?
If I continue developing this project, I would refine the rhythm feedback, add more playable chapters, and create stronger transitions between music, animation, and player input.
```

Keep this section thoughtful but concise.

---

## 16. Section 10 — Next Steps

Keep short.

```text
Next Steps

Expand the story with additional chapters such as Stealing the Immortal Herb, Broken Bridge Reunion, and Leifeng Pagoda.

Add more Cantonese Opera music segments.

Develop a cultural archive system with costumes, character notes, and opera knowledge.

Optimize the game for PC and mobile platforms.
```

---

## 17. Ending

Do not use a heavy footer.

End with one quiet sentence:

```text
Traditional stories do not disappear. They simply wait for new ways to be told.
```

Below it:

```text
Next Project →
```

---

## 18. Required Assets

Hero:
- edited gameplay trailer

Overview:
- selected gameplay screenshot

Visual Break I:
- West Lake Encounter full-width image

Act I Gameplay:
- gameplay GIF or short video
- note convergence diagram

Visual Break II:
- Flooding Jinshan Temple full-width image

Act II Gameplay:
- boss battle GIF or short video
- boss system diagram

Artistic Direction:
- ink-wash background image
- Cantonese Opera costume reference
- final character/scene screenshots

Technical:
- timeline judgement diagram
- CSV level data screenshot
- boss shield/health diagram
- note rendering camera diagram
