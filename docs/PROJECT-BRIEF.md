# Project Brief --- Rock, Paper, Scissors

## 1. Project Overview

**Rock, Paper, Scissors** is an interactive web game that reimagines the
classic hand game as a visually engaging and animated experience.

The player chooses Rock, Paper, or Scissors and competes against a
computer-controlled opponent. Rather than simply displaying the result,
the application presents each round as a short visual sequence: the
player's and computer's fists prepare and reveal their choices, the
corresponding objects battle across the screen, the winning interaction
is visually represented, and the final result and score are displayed.

The project is intended to combine straightforward game logic with
custom artwork, animation, sound and responsive interface design.

## 2. Project Purpose

The primary purpose of the project is to create a fun, polished and
memorable browser-based Rock, Paper, Scissors game.

The project also provides an opportunity to practise and demonstrate:

-   Frontend development.
-   Interactive user interfaces.
-   Game logic and state management.
-   Animation integration.
-   Working with externally created visual and audio assets.
-   Responsive and accessible web design.
-   Separation of presentation, assets and application logic.
-   Testing and maintainable project organisation.

## 3. Project Objectives

The project should:

-   Provide an intuitive way for the player to select Rock, Paper or
    Scissors.
-   Create an engaging animated sequence for every round.
-   Make the outcome visually understandable.
-   Allow the player to play repeatedly and track the score.
-   Use custom artwork and animations created separately from the
    application code.
-   Incorporate sound effects where appropriate.
-   Work effectively across desktop, tablet and mobile devices.
-   Consider accessibility from the beginning.
-   Keep the game logic independent from the visual assets and animation
    implementation.
-   Remain simple enough to understand, maintain and extend.

## 4. Game Concept

Each round follows the general sequence:

**Choose → Prepare → Reveal → Battle → Result → Score → Replay**

1.  The player chooses one of the three available options.
2.  A human fist appears on the player's side and a robot fist appears
    on the computer's side.
3.  Both fists shake three times.
4.  The fists reveal the player's and computer's choices.
5.  The corresponding Rock, Paper or Scissors objects appear.
6.  Both objects move towards the centre of the screen.
7.  When they meet, a visual interaction represents the winning
    relationship between the two choices.
8.  The objects continue moving away and fade from view, with
    appropriate consequences for the losing object.
9.  A large result animation communicates whether the player won, lost
    or drew.
10. The score is updated.
11. The player can begin another round.

## 5. Target User

The game is intended for anyone who wants to play a quick and
entertaining game of Rock, Paper, Scissors in a web browser.

The experience should be understandable without instructions or
technical knowledge.

## 6. Core User Experience

The game should provide:

-   **Immediate understanding:** The player should quickly recognise the
    three available choices.
-   **Simple interaction:** Selecting an option should require only one
    clear action.
-   **Anticipation:** The three fist shakes should create suspense
    before the choices are revealed.
-   **Visual feedback:** The battle animation should make the
    relationship between the two choices clear.
-   **Clear results:** The player should immediately understand whether
    they won, lost or drew.
-   **Replayability:** Starting another round should be quick and
    obvious.
-   **Entertainment:** Animation, artwork and sound should make the game
    feel more engaging than a basic text-based implementation.

## 7. Project Scope

### 7.1 In Scope

The initial version will include:

-   Player versus computer gameplay.
-   Rock, Paper and Scissors.
-   Random computer choice.
-   Standard Rock, Paper, Scissors rules.
-   Score tracking.
-   Three large player-selection buttons.
-   Custom human-hand artwork.
-   Custom robot-hand artwork.
-   Fist preparation and reveal sequence.
-   Animated Rock, Paper and Scissors objects.
-   Visual battle/collision sequences.
-   Different visual consequences for winning and losing objects.
-   Win, lose and draw result animations.
-   Sound effects, where practical.
-   Responsive interface.
-   Accessibility considerations.
-   Separation of game logic, interface, animation and external assets.

### 7.2 Out of Scope for the Initial Version

The following features are not required for the initial release:

-   Online multiplayer.
-   Real-time player-versus-player matches.
-   User accounts.
-   User profiles.
-   Online leaderboards.
-   Persistent player statistics.
-   Social features.
-   A backend or database unless a later requirement makes one
    necessary.
-   Unnecessary third-party services.

These features may be considered in future versions if they provide a
meaningful benefit to the project.

## 8. Design Principles

### Simplicity

The rules and controls should remain immediately understandable despite
the richness of the visual presentation.

### Visual Storytelling

The animation should communicate what happens during the round rather
than relying exclusively on text.

### Separation of Concerns

Game rules, application state, interface elements, animation behaviour
and external assets should be kept appropriately separate.

### Accessibility

Important information should not depend exclusively on colour, sound or
animation. Controls should be usable with appropriate input methods, and
motion and audio should be considered carefully.

### Responsive Design

The experience should adapt to different screen sizes and input methods,
with particular attention to mobile devices.

### Performance

Animations and assets should provide a rich experience without
unnecessarily compromising loading time, responsiveness or device
performance.

### Maintainability

The project should favour clear, understandable solutions over
unnecessary complexity.

### Extensibility

The structure should allow additional visual assets, sound effects or
game features to be introduced later without requiring the entire
application to be redesigned.

## 9. Technology --- High Level

The application will be developed as a modern web application using the
technologies appropriate for the project.

The initial implementation is expected to use:

-   HTML
-   CSS
-   JavaScript

Additional technologies or libraries may be introduced if they provide a
clear and justified benefit, particularly for animation or asset
integration.

The exact animation technology should be determined during the Technical
Specification phase rather than being fixed in this Project Brief.

## 10. Artwork and Audio

The project's visual identity will rely heavily on custom-created
artwork and animations.

Artwork and animation assets should therefore be produced separately
from the application's core code using appropriate creative software.

The project may include:

-   Human hand illustrations.
-   Robot hand illustrations.
-   Rock, paper and scissors artwork.
-   Damaged or transformed objects.
-   Result graphics and animations.
-   Supporting visual effects.
-   Sound effects for important game events.

The exact assets, formats, dimensions, naming conventions and animation
requirements will be defined separately in the **Art & Asset
Specification** and **UI/UX & Animation Specification**.

## 11. Definition of Success

The project will be considered successful when a user can:

1.  Understand the three available choices immediately.
2.  Select Rock, Paper or Scissors easily.
3.  Experience the complete preparation and reveal sequence.
4.  Clearly understand both choices.
5.  Follow the animated battle between the two objects.
6.  Understand the outcome of the round.
7.  See the score updated correctly.
8.  Start another round without unnecessary interaction.
9.  Use the application comfortably across supported screen sizes.
10. Experience the game without accessibility barriers caused by
    animation, sound or colour alone.

The final application should feel like a **polished interactive game**,
rather than simply a programming exercise that happens to implement the
Rock, Paper, Scissors rules.

## 12. Future Documentation

The following documents will define the project in greater detail:

1.  **PROJECT-BRIEF.md** --- Overall purpose, scope and vision.
2.  **FUNCTIONAL-SPECIFICATION.md** --- Detailed application behaviour
    and game rules.
3.  **UI-UX-ANIMATION-SPECIFICATION.md** --- Screens, interactions,
    transitions and animation sequences.
4.  **ART-ASSET-SPECIFICATION.md** --- Artwork, animation assets, audio
    and production requirements.
5.  **TECHNICAL-SPECIFICATION.md** --- Architecture, technologies,
    project structure and implementation approach.
6.  **DEVELOPMENT-PLAN.md** --- Development tasks, milestones and
    implementation order.
7.  **TESTING-PLAN.md** --- Functional, visual, responsive,
    accessibility and performance testing.

------------------------------------------------------------------------

**Document status:** Initial Project Brief\
**Project:** Rock, Paper, Scissors\
**Purpose:** Establish the project's vision and scope before
implementation begins.
