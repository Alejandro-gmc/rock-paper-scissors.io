# Document 3 — UI/UX & Animation Specification

## 1. UI/UX Overview

The **Rock, Paper, Scissors** game should provide a clear, responsive and visually engaging interface that supports the animated sequence of every round.

The interface should make it immediately clear what the player can do, what stage of the round is currently taking place, and what the final result is.

The visual design should remain consistent with the main project brief and should support the use of custom artwork, animation and sound.

## 2. Screen Layout

The main game screen should contain:

- Game title and basic game information.
- Current score for the player and the computer.
- Main gameplay area.
- Human player area.
- Robot opponent area.
- Central interaction area.
- Rock, Paper and Scissors selection controls.
- Round result area.
- Sound and optional settings controls.

On desktop screens, the human player should be positioned on the left and the robot opponent on the right.

The central area should provide enough space for the selected objects to move towards each other and visually interact.

On smaller screens, the layout may become more vertical while keeping the two opponents visually distinct.

## 3. Buttons and Player Controls

The player should select one of three options:

- Rock.
- Paper.
- Scissors.

Each option should be clearly visible and easy to understand.

Buttons should support:

- Default state.
- Hover state.
- Focus state.
- Pressed state.
- Selected state.
- Disabled state.

The selected option should receive clear visual feedback.

After the player makes a selection, the other choices should become temporarily unavailable until the round finishes.

A **Play Again** or equivalent control should be available after the result has been displayed.

## 4. Hand Positions

The human and robot hands should begin in a neutral closed-fist position.

The human hand should appear on the left side of the gameplay area.

The robot hand should appear on the right side of the gameplay area.

Both hands should face towards the centre of the screen.

The positions of the hands should remain consistent between rounds so that the animation feels predictable and polished.

The hands should not overlap before the reveal stage.

## 5. Fist Animation

Each round should begin with both characters displaying their closed fists.

The fist animation should follow a repeated rhythmic movement:

1. Both fists move slightly upward.
2. Both fists move slightly downward.
3. The movement repeats during the countdown.
4. The fists stop on the final beat.
5. The selected hand is revealed.

The movement should use smooth easing rather than abrupt changes.

The human and robot animations should remain visually synchronized.

## 6. Reveal Animation

The reveal animation should happen for both players at approximately the same time.

The sequence should be:

1. Final fist position.
2. Short pause.
3. Fist changes into the selected Rock, Paper or Scissors hand.
4. The selected hands become fully visible.
5. The objects begin moving towards the centre.
6. The collision or interaction begins.

The reveal should be fast enough to keep the game exciting while remaining easy to follow.

## 7. Object Movement

Once the choices have been revealed, the corresponding objects should move from the player positions towards the centre of the screen.

The movement should:

- Use smooth animation.
- Have a consistent duration.
- Use appropriate easing.
- Keep both objects visually balanced.
- Stop at a predictable interaction point.

Objects should not appear to teleport from one position to another.

## 8. Collision and Interaction

The selected objects should visually interact when they meet.

The result should depend on the normal Rock, Paper, Scissors rules.

### Rock vs Paper

Paper should wrap around the Rock.

The Paper should become the visually dominant object while the Rock is partially or completely covered.

### Paper vs Scissors

The Scissors should cut the Paper.

The Paper should become torn or separated to communicate that Scissors defeated it.

### Scissors vs Rock

The Rock should defeat and break the Scissors.

The Scissors should visually separate into broken pieces.

### Matching Objects

When both players choose the same object:

- Both objects should remain visible.
- No object should be shown as the winner.
- A neutral draw animation should be displayed.

## 9. Winning and Losing Object Behaviour

The winning object should receive visual emphasis after the interaction.

The winning object may:

- Move slightly forward.
- Scale up slightly.
- Receive a glow or emphasis effect.
- Remain visible for the result sequence.

The losing object should:

- Move away from the centre.
- Become visually reduced.
- Fade or move downward where appropriate.
- Complete its losing interaction animation.

The purpose of these effects is to make the result understandable without relying only on text.

## 10. Result Animation

After the object interaction, the game should clearly display the final result.

Possible results are:

- YOU WIN.
- YOU LOSE.
- DRAW.

The result should appear using a short, noticeable animation.

A winning result may use a scale-up or celebration effect.

A losing result may use a restrained movement or fade effect.

A draw result should use a neutral animation that gives both players equal visual treatment.

The result should remain visible long enough for the player to understand it before the next round begins.

## 11. Transitions

Transitions should be used between the main stages of the round:

- Game start.
- Player selection.
- Countdown.
- Fist animation.
- Reveal.
- Object movement.
- Collision.
- Result.
- Next round.

Transitions should be short and purposeful.

Animations should not create unnecessary delays between rounds.

## 12. Responsive Behaviour

The interface should support:

- Desktop screens.
- Tablet screens.
- Mobile screens.

### Desktop

The human and robot should appear side by side.

The gameplay area should make full use of the available horizontal space.

### Tablet

The same general layout should be preserved with reduced spacing and appropriately scaled artwork.

### Mobile

The layout may become vertical.

Controls should remain large enough for touch interaction.

The main animation should remain visible without horizontal scrolling.

Important text and result graphics should remain readable at smaller sizes.

## 13. Accessibility

All interactive controls should be usable with a keyboard.

Interactive elements should provide:

- Visible focus states.
- Meaningful labels.
- Appropriate semantic elements.
- Sufficient colour contrast.
- Clear selected and disabled states.

The game should not rely only on colour to communicate the result.

The result should always be available as readable text such as **YOU WIN**, **YOU LOSE** or **DRAW**.

Animations should respect reduced-motion preferences where supported.

## 14. Sound Behaviour

Sound should support the visual sequence without being required to understand the game.

Sound effects may be used for:

- Button selection.
- Countdown.
- Fist movement.
- Reveal.
- Collision.
- Winning result.
- Losing result.
- Draw result.

A visible mute or sound control should be provided.

The game should continue to function correctly when sound is disabled.

## 15. Performance and Timing

Animations should remain smooth on supported devices.

The visual sequence and game logic must remain synchronized.

The application should avoid unnecessary rendering during animations.

Animation durations should be consistent enough that the result always occurs at the expected point in the round.

## 16. UI/UX Principles

The interface should follow these principles:

- The player should always understand the current game state.
- The next available action should always be clear.
- Animations should communicate gameplay events.
- Human and robot interactions should remain visually balanced.
- Important results should receive the strongest visual emphasis.
- The interface should remain usable on different screen sizes.
- Accessibility should be considered as part of the design rather than added later.
