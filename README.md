# Project
COM-437 project

# Mobile Coin Flip Application
---

## I. Project Description

### A. Overview
A simple, mobile application that simulates a coin flip. The app provides an unbiased, digital version of a traditional coin toss with visual coin graphics.

### B. Goal
To provide a fun, interactive tool for users to make quick, random binary decisions (Heads/Tails) with realistic coin flip visuals.

### C. Target Audience
- General smartphone users needing quick decision-making tools
- Students learning mobile development fundamentals
- Anyone needing a fair method to choose between two options

---

## II. Problem Addressing

### A. Problem Statement
People often struggle to make quick, arbitrary decisions or need a fair method for choosing between two options. Physical coins may not always be available, and mental coin flips are inherently biased.

### B. Proposed Solution
A digital coin flip application that is:
- **Unbiased**: Uses true random number generation
- **Always available**: Lives on the user's phone
- **Visually satisfying**: Shows actual coin images
- **Simple**: Two-screen interface for ease of use

### C. Use Cases
1. Deciding who goes first in a board game or sports match
2. Resolving simple disputes ("Heads I win, Tails you lose")
3. Randomizing daily choices (e.g., which restaurant to visit)
4. Teaching probability concepts to students
5. Making quick decisions when both options are equally valid

---

## III. Platform

| Category | Choice | Justification |
|----------|--------|----------------|
| Operating System | Android (Minimum API 24 / Android 7.0) | Wide market reach, accessible development tools |
| IDE | Android Studio | Industry standard, excellent debugging tools |
| Programming Language | Kotlin | Modern, concise, official Android language |
| Build System | Gradle DSL (Kotlin DSL) | Standard for Android projects |
| Version Control | Git / GitHub | Industry standard for source control |
| Testing Devices | Pixel 3 Emulator (API 33) | Stable graphics rendering |

---

## IV. Front/Back End Support

### A. Front-End (Client-Side)

**Languages:**
- XML for user interface layouts
- Kotlin for application logic

**Components:**
- `MainActivity`: Welcome screen logic and navigation
- `FlipActivity`: Core coin flip game logic
- `activity_main.xml`: Welcome screen layout
- `activity_flip.xml`: Game screen layout
- `ImageView`: Displays coin graphics (heads.png / tails.png)
- `Button`: User interaction (Start, Flip)
- `TextView`: Displays textual results (HEADS/TAILS)

**UI Styling:**
- Background: White for clean appearance
- Text: Black for contrast
- Buttons: Material Design blue
- Layout: Center-gravity for focused user experience

### B. Back-End (Local)

**Architecture:**
- **No external server or database** - fully self-contained
- **No network dependencies** - works offline
- **No user data collection** - respects privacy

**Local Logic:**
- `kotlin.random.Random` for statistically unbiased result generation
- Random.nextInt(2) produces 0 (Heads) or 1 (Tails) with equal probability

**State Management:**
- Simple in-memory variables
- No persistent storage required
- Each flip is independent with no memory of previous flips

---

## V. Functionality

### A. Core Features

**Navigation:**
- Intent-based transition between screens
- Simple forward-only navigation flow

**Randomization:**
- True random number generation on each flip
- 50% probability for Heads
- 50% probability for Tails
- No pattern or sequence prediction possible

**Replayability:**
- Users can flip the coin unlimited times
- No cooldown or restrictions
- Instant results with each tap

### VI. Wireframe Diagrams

**Welcome Screen Layout:**
**Screen 1: Welcome Screen**
- Displays app title prominently
- Provides "Start Game" button
- Serves as clean entry point
  
├──────────────────────────────────────┤
│ │
│ │
│ WELCOME TO COIN FLIP │
│ │
│ │
│ ┌─────────────────┐ │
│ │ │ │
│ │ START GAME │ │
│ │ │ │
│ └─────────────────┘ │
│ │
│ │
│ │
└──────────────────────────────────────┘

**Screen 2: Coin Flip Screen**
- Shows current coin image (heads or tails)
- Displays result text ("HEADS!" or "TAILS!")
- Provides "Flip Coin" button for repeated use
- Updates both image and text simultaneously

├──────────────────────────────────────┤
│ │
│ ┌───────┐ │
│ │ │ │
│ │ 🪙 │ │
│ │ │ │
│ └───────┘ │
│ │
│ Tap Flip to Start │
└──────────────────────────────────────┘
