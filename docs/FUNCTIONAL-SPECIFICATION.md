# Functional Specification --- Rock, Paper, Scissors

## 1. Purpose

This document defines the functional behaviour of the Rock, Paper,
Scissors web application.

It translates the project's overall vision from the Project Brief into
precise functional requirements. It describes what the application must
do and how a round should behave, without prescribing the specific
programming language structures, animation technology or
asset-production software used to implement it.

## 2. Functional Scope

The application shall provide a single-player Rock, Paper, Scissors game
in which:

-   The human player competes against a computer-controlled opponent.
-   The player selects Rock, Paper or Scissors.
-   The computer independently selects one of the same three choices.
-   The application determines the winner using the standard game rules.
-   The round is presented through a predefined sequence of visual
    states and animations.
-   The result is clearly communicated.
-   The score is updated after every completed round.
-   The player can begin another round without reloading the
    application.

## 3. Game Rules

The application shall use the standard Rock, Paper, Scissors rules:

  Player Choice   Beats
  --------------- ----------
  Rock            Scissors
  Paper           Rock
  Scissors        Paper

If both players select the same option, the round is a draw.

The result calculation must be independent of the visual animation used
to represent the round.

## 4. Game State and Round Lifecycle

The application shall conceptually progress through the following
states:

**IDLE → PLAYER_CHOICE → PREPARING → REVEAL → BATTLE → RESULT →
SCORE_UPDATE → READY_FOR_NEXT_ROUND**

### 4.1 IDLE

The application displays the initial game interface and waits for the
player to select one of the three choices.

### 4.2 PLAYER_CHOICE

The player has selected an option.

The selected choice is stored for the current round and further
player-choice input is temporarily disabled until the round reaches an
appropriate state.

The computer generates its choice for the same round.

### 4.3 PREPARING

The player's human fist and the computer's robot fist appear.

Both fists perform the preparation animation simultaneously.

The preparation sequence consists of exactly three shakes.

Neither choice is revealed during the preparation sequence.

### 4.4 REVEAL

After the third shake, both choices are revealed.

The player's human hand displays the player's selected sign.

The computer's robot hand displays the computer's selected sign.

The two choices must become identifiable to the player before the battle
sequence begins.

### 4.5 BATTLE

The corresponding physical Rock, Paper or Scissors objects appear
beneath the respective hands.

The player's object begins on the player's side.

The computer's object begins on the computer's side.

The two objects move towards one another.

The movement and appearance of each object depend on its type:

-   Rock moves by rolling.
-   Paper moves by flying or travelling through the air.
-   Scissors advances while opening and closing.

The objects meet approximately in the centre of the play area.

### 4.6 RESULT

When the objects meet, a visual interaction represents the relationship
between the two choices.

The interaction must correspond to the actual game result.

After the interaction, the objects continue their movement towards the
opposite side of the screen and eventually fade from view, where
applicable.

A prominent result animation then communicates:

-   **YOU WIN!**
-   **YOU LOSE!**
-   **IT'S A DRAW!**

### 4.7 SCORE_UPDATE

Once the round result has been established, the score is updated.

The score update must correspond to the actual result and must occur
only once per completed round.

### 4.8 READY_FOR_NEXT_ROUND

After the result sequence has completed, the application returns to a
state in which the player can select another choice and start a new
round.

The accumulated score remains available.

## 5. Initial Interface

The initial interface shall provide:

-   A clear game title.
-   Three large player-choice controls.
-   A visual representation of Rock, Paper and Scissors on those
    controls.
-   A visible score area.
-   Appropriate instructions or contextual information where necessary.
-   A mechanism for controlling sound if sound is enabled.

The three primary choices must be visually distinct and sufficiently
large for comfortable interaction on both desktop and touch devices.

## 6. Player Choice

The player shall be able to select exactly one of:

-   Rock
-   Paper
-   Scissors

A choice shall begin a round.

Once a choice has been made:

-   The selected choice shall be stored.
-   The computer shall select its choice.
-   The three player-choice controls shall no longer trigger additional
    choices during the current round.
-   The application shall proceed to the preparation state.

The player must not be able to accidentally start multiple rounds by
repeatedly activating a control during the same round.

## 7. Computer Choice

The computer shall select Rock, Paper or Scissors automatically.

The selection shall be made independently of the player's choice.

Each of the three choices must be capable of being selected.

The computer's choice shall be determined before the reveal and retained
for the remainder of the round.

The computer must not change its choice after the reveal has begun.

## 8. Preparation Sequence

After both choices have been established:

1.  The human fist appears on the player's side.
2.  The robot fist appears on the computer's side.
3.  Both fists perform the preparation movement simultaneously.
4.  The fists shake exactly three times.
5.  The actual choices remain hidden during these three shakes.
6.  After the third shake, the reveal sequence begins.

The preparation animation must not alter the underlying game result.

## 9. Choice Reveal

Following the preparation sequence:

-   The player's fist changes to the appropriate human-hand sign.
-   The computer's fist changes to the appropriate robot-hand sign.
-   Both choices are revealed as part of the same stage of the round.

The application must ensure that the visual choice shown corresponds
exactly to the choice stored in the game state.

## 10. Battle Objects

Each choice shall have a corresponding physical object:

  Choice     Battle Object    Movement
  ---------- ---------------- ------------------------------------
  Rock       Rock             Rolls across the screen
  Paper      Sheet of paper   Flies/glides across the screen
  Scissors   Scissors         Advances while opening and closing

The player's object starts from the player's side.

The computer's object starts from the computer's side.

The objects then travel towards the centre.

The battle animation must visually distinguish the three object types.

## 11. Battle Outcomes

The visual battle must represent the actual Rock, Paper, Scissors
relationship.

### 11.1 Rock vs Scissors

Rock defeats Scissors.

The battle animation should communicate that the rock damages or breaks
the scissors.

The scissors may visually break as part of the result.

The rock continues its movement after the interaction.

### 11.2 Scissors vs Paper

Scissors defeats Paper.

The scissors should visually cut the paper.

The paper should separate into two pieces as part of the interaction.

The scissors continues moving after the interaction.

### 11.3 Paper vs Rock

Paper defeats Rock.

The paper should visually wrap around the rock.

The rock should become contained by the paper.

The wrapped rock and paper continue their movement after the
interaction.

### 11.4 Draws

If both choices are identical:

-   The objects meet.
-   No object defeats the other.
-   No winning/losing transformation occurs.
-   Both objects continue their movement appropriately.
-   The round is classified as a draw.

The exact visual treatment of a draw will be defined in the UI/UX &
Animation Specification.

## 12. Post-Collision Movement

After the central interaction:

-   The objects continue travelling towards the opposite sides of the
    screen.
-   Appropriate result states remain visible during this movement where
    required.
-   Objects eventually fade or otherwise transition out of the active
    play area.
-   The application must not allow the objects from a completed round to
    interfere with the next round.

The precise timing, movement curves, fading and visual effects will be
defined separately.

## 13. Round Result

After the battle sequence, the application shall display a prominent
result message.

Possible results are:

-   **YOU WIN!**
-   **YOU LOSE!**
-   **IT'S A DRAW!**

The result must correspond to the game logic.

The result presentation should be visually prominent and understandable
without relying exclusively on colour or sound.

The result animation must not modify the underlying result.

## 14. Score

The application shall maintain at least two scores:

-   Player score.
-   Computer score.

A draw shall not increase either score.

For each completed round:

-   Player win → player score increases by one.
-   Computer win → computer score increases by one.
-   Draw → neither score increases.

The score must be updated only once for each completed round.

The score must persist while the current page/session remains active.

A future version may introduce additional statistics, but these are
outside the initial functional scope.

## 15. Starting a New Round

After a round has finished:

-   The player shall be able to start another round.
-   The previous round's temporary visual elements shall be cleared or
    reset.
-   The accumulated score shall remain.
-   The player shall again be able to choose Rock, Paper or Scissors.

The player should not need to refresh the browser to play another round.

## 16. Input Protection and Invalid Actions

The application shall prevent invalid actions caused by the player
interacting at inappropriate times.

Examples include:

-   Selecting multiple choices during one round.
-   Starting another round while the current battle is still running.
-   Triggering the result multiple times.
-   Updating the score more than once.
-   Activating controls that are temporarily unavailable.

The application should fail safely if an unexpected state occurs.

## 17. Sound

The application may provide sound effects associated with important
events, including:

-   Player selection.
-   Fist shaking.
-   Choice reveal.
-   Rock movement.
-   Paper movement.
-   Scissors movement.
-   Collision.
-   Paper tearing.
-   Scissors breaking.
-   Win.
-   Loss.
-   Draw.

Sound must be supplementary rather than essential to understanding the
game.

The application should provide a clear way to disable or enable sound.

If sound is disabled, all essential game information and interaction
must remain available visually.

## 18. Responsive Behaviour

The application shall support the intended desktop, tablet and mobile
layouts.

The functional experience must remain intact when the available screen
space changes.

In particular:

-   The three player-choice controls must remain usable.
-   The player and computer areas must remain distinguishable.
-   The central battle must remain understandable.
-   Important result information must remain visible.
-   Interactive elements must remain appropriately sized for touch
    input.
-   Animations must not make essential controls inaccessible.

The exact responsive layouts will be specified in the UI/UX
Specification.

## 19. Accessibility Requirements

The application shall consider accessibility as a functional
requirement.

At minimum:

-   Interactive controls must have meaningful accessible names.
-   The game must not depend solely on colour to communicate the result.
-   The game must not depend solely on sound to communicate important
    information.
-   Keyboard users should be able to reach and operate the primary
    controls.
-   Focus states should remain visible.
-   Text and controls should maintain appropriate readability.
-   Motion should be considered for users who prefer reduced motion.
-   Important result information should be available in an appropriate
    non-animated form as well.

The precise accessibility implementation will be defined in the UI/UX
and Technical Specifications.

## 20. Animation Timing and Synchronisation

The different parts of a round must occur in a controlled sequence.

The application must ensure that:

1.  The player selects a choice.
2.  The computer selects its choice.
3.  The preparation sequence begins.
4.  Exactly three fist shakes occur.
5.  Both choices are revealed.
6.  Both battle objects appear.
7.  Both objects move towards the centre.
8.  The collision/result interaction occurs.
9.  The objects continue away from the centre.
10. The result is displayed.
11. The score is updated.
12. The application becomes ready for another round.

The player must not be able to skip or accidentally duplicate critical
stages through repeated input.

The exact durations and transition timings are not defined here and will
be established during animation design and implementation.

## 21. Separation of Functional Logic and Assets

The game shall be designed so that externally created artwork and audio
can be changed without requiring changes to the underlying Rock, Paper,
Scissors rules.

The following should remain conceptually separate:

-   Game rules.
-   Game state.
-   Player and computer choices.
-   Score management.
-   Interface controls.
-   Animation behaviour.
-   Visual assets.
-   Audio assets.

This requirement is intended to support maintainability and allow
artwork or animation to evolve independently from the core game.

## 22. Functional Error Handling

The application should handle unexpected situations gracefully.

Examples include:

-   Missing visual assets.
-   Missing optional sound assets.
-   Animation failure.
-   An invalid or unavailable game state.
-   An interaction occurring while the application is not ready for
    input.

A failure in a non-essential visual or audio element should not prevent
the core game from functioning wherever reasonably possible.

## 23. Round Completion Criteria

A round is considered complete when:

-   Both choices have been determined.
-   The winner has been calculated.
-   The battle sequence has completed sufficiently to communicate the
    result.
-   The result has been presented.
-   The score has been updated exactly once.
-   The application is ready to accept the next player choice.

## 24. Functional Acceptance Criteria

The initial implementation shall be considered functionally acceptable
when all of the following are true:

### Player Interaction

-   [ ] The player can select Rock.
-   [ ] The player can select Paper.
-   [ ] The player can select Scissors.
-   [ ] A player selection starts exactly one round.
-   [ ] Additional selections are prevented while a round is in
    progress.

### Computer

-   [ ] The computer selects one of the three choices.
-   [ ] The computer's selection is random.
-   [ ] The computer's selection remains fixed throughout the round.

### Preparation and Reveal

-   [ ] A human fist appears on the player's side.
-   [ ] A robot fist appears on the computer's side.
-   [ ] Both fists shake three times.
-   [ ] Neither choice is revealed before the preparation sequence
    finishes.
-   [ ] The player's selected hand sign is displayed correctly.
-   [ ] The computer's selected hand sign is displayed correctly.

### Battle

-   [ ] Rock uses the intended rolling behaviour.
-   [ ] Paper uses the intended flying/gliding behaviour.
-   [ ] Scissors uses the intended opening/closing movement.
-   [ ] The two objects travel towards the centre.
-   [ ] The battle outcome corresponds to the actual game rules.
-   [ ] Rock defeats Scissors visually.
-   [ ] Scissors defeats Paper visually.
-   [ ] Paper defeats Rock visually.
-   [ ] Draws do not produce a winner.
-   [ ] Objects leave the active battle area after the interaction.

### Result and Score

-   [ ] A player win displays the appropriate result.
-   [ ] A computer win displays the appropriate result.
-   [ ] A draw displays the appropriate result.
-   [ ] The player score increases only after a player win.
-   [ ] The computer score increases only after a computer win.
-   [ ] A draw does not increase either score.
-   [ ] Each round updates the score exactly once.

### Replay

-   [ ] A new round can be started without refreshing the page.
-   [ ] Previous-round temporary elements are cleared/reset.
-   [ ] The score is retained between rounds.

### Accessibility and Responsiveness

-   [ ] The primary controls are keyboard accessible.
-   [ ] Controls have meaningful accessible names.
-   [ ] Results are understandable without sound.
-   [ ] Results are not communicated by colour alone.
-   [ ] The game remains usable on supported mobile, tablet and desktop
    layouts.
-   [ ] A reduced-motion experience can be supported where required.

## 25. Relationship to Other Project Documents

This document defines **what the application must do**.

It does not define the complete visual design, exact animation
implementation, asset-production workflow or code architecture.

Those decisions belong to the following documents:

-   **UI/UX & Animation Specification** --- defines how the experience
    should look and behave visually.
-   **Art & Asset Specification** --- defines the artwork, animation and
    audio assets required.
-   **Technical Specification** --- defines how the application will be
    implemented.
-   **Development Plan** --- defines how the work will be divided and
    implemented.
-   **Testing Plan** --- defines how the functional requirements will be
    verified.

------------------------------------------------------------------------

**Document status:** Initial Functional Specification\
**Project:** Rock, Paper, Scissors\
**Purpose:** Define the required functional behaviour before
implementation begins.
