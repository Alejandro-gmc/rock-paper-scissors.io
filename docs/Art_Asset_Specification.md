# Document 4 — Art & Asset Specification

## 1. Art and Asset Overview

This document defines the artwork required for the **Rock, Paper, Scissors** game.

The assets should be created specifically for the animated gameplay sequence and should be suitable for use on desktop, tablet and mobile screens.

All artwork should follow a consistent visual style and should be prepared so that individual elements can be animated when required.

## 2. Human Fist

A human closed-fist asset is required for the countdown and preparation sequence.

The asset should:

- Show a closed fist.
- Face towards the centre of the screen.
- Match the proportions of the human Rock, Paper and Scissors hands.
- Use a clean and recognisable silhouette.
- Have a transparent background.

The fist should be suitable for repeated movement during the countdown animation.

## 3. Robot Fist

A robot closed-fist asset is required.

The asset should:

- Clearly look mechanical.
- Face towards the centre of the screen.
- Match the proportions of the robot Rock, Paper and Scissors hands.
- Maintain the same visual style as the other robot artwork.
- Have a transparent background.

## 4. Human Rock, Paper and Scissors Hands

Three human hand assets are required:

- Human Rock.
- Human Paper.
- Human Scissors.

The three assets should use the same hand, perspective, lighting and visual style.

The hands should maintain a consistent wrist position and scale so that the reveal animation can change from the fist to the selected hand without obvious visual displacement.

Each asset should have a transparent background.

## 5. Robot Rock, Paper and Scissors Hands

Three robot hand assets are required:

- Robot Rock.
- Robot Paper.
- Robot Scissors.

These assets should match the robot fist and share the same proportions, perspective and visual language.

Each hand should face towards the centre of the screen and use a transparent background.

The robot versions should clearly represent the same three game choices as the human versions while remaining visually distinct.

## 6. Rock Asset

A standalone Rock object is required for the object movement and collision sequence.

The Rock should:

- Have a clear silhouette.
- Be recognisable at smaller sizes.
- Support the wrapping interaction with Paper.
- Work correctly as a moving object.
- Have a transparent background.

## 7. Paper Asset

A standalone Paper object is required.

The Paper should:

- Have a clear paper shape.
- Be suitable for movement and deformation.
- Support the Paper wrapping Rock interaction.
- Support the tearing interaction.
- Have a transparent background.

The artwork should be designed so that separate pieces can be used when required for animation.

## 8. Scissors Asset

A standalone Scissors object is required.

The Scissors should:

- Be immediately recognisable.
- Have a strong and readable silhouette.
- Be suitable for movement and collision.
- Support the breaking animation.
- Have a transparent background.

## 9. Broken Scissors

A broken Scissors asset is required for the Rock vs Scissors interaction.

The asset should provide either:

- A finished broken Scissors state.
- Or separate animation-ready pieces.

Where separate pieces are supplied, they should be independently movable.

The broken state should make it visually obvious that the Scissors have been defeated by Rock.

## 10. Torn Paper

A torn Paper asset is required for the Paper vs Scissors interaction.

The asset should provide:

- A torn or cut Paper state.
- Optional separate torn pieces.
- Shapes that can be animated independently.

The result should clearly communicate that Scissors defeated Paper.

## 11. Wrapped Rock

A wrapped Rock state is required for the Rock vs Paper interaction.

The artwork should show Paper wrapping around the Rock.

The Rock should remain recognisable while appearing partially or completely covered by Paper.

The wrapping state should be suitable for a short animation rather than only a static image.

## 12. Result Graphics

Result graphics should be created for the three possible outcomes:

- YOU WIN.
- YOU LOSE.
- DRAW.

Additional visual effects may also be created for:

- Celebration.
- Impact.
- Victory.
- Defeat.
- Draw feedback.

Result graphics should remain readable on both large and small screens.

## 13. Animation Requirements

Assets should be prepared for the following animation types:

- Translation.
- Rotation.
- Scaling.
- Fading.
- Deformation.
- Splitting.
- Wrapping.
- Breaking.
- Impact effects.

Whenever an object must move as separate parts, those parts should be exported separately.

For example, broken Scissors should ideally be delivered as multiple pieces rather than as one flattened image.

The artwork should avoid unnecessary details that would make animation difficult.

## 14. File Formats

Preferred file formats are:

- **PNG** for raster assets that require transparency.
- **SVG** for suitable vector graphics and simple result graphics.
- **WebP** for optimised raster assets where transparency and browser compatibility are confirmed.

Editable source files should also be retained when possible.

## 15. Dimensions

Recommended export dimensions are:

| Asset | Recommended Size |
|---|---:|
| Human fist | 512 × 512 px |
| Robot fist | 512 × 512 px |
| Human hands | 512 × 512 px |
| Robot hands | 512 × 512 px |
| Rock | 512 × 512 px |
| Paper | 512 × 512 px |
| Scissors | 512 × 512 px |
| Broken Scissors pieces | 256–512 px each |
| Torn Paper pieces | 256–512 px each |
| Result graphics | 1024 × 512 px |
| Large effects | 1024 × 1024 px |

These dimensions may be adjusted during implementation when necessary, provided that the artwork remains sharp and consistent.

## 16. Transparent Backgrounds

Gameplay artwork should use transparent backgrounds.

Assets should not include:

- White rectangular backgrounds.
- Unnecessary coloured backgrounds.
- Environmental scenery.
- Permanent shadows that prevent independent animation.

Transparency is required so that the assets can be placed directly over the game interface.

## 17. Naming Conventions

Asset filenames should use lowercase kebab-case.

Examples:

```text
human-fist.png
human-rock.png
human-paper.png
human-scissors.png

robot-fist.png
robot-rock.png
robot-paper.png
robot-scissors.png

rock.png
paper.png
scissors.png

scissors-broken.png
paper-torn.png
rock-wrapped.png

result-win.svg
result-lose.svg
result-draw.svg
```

For animation pieces, use numbered filenames:

```text
scissors-broken-piece-01.png
scissors-broken-piece-02.png
paper-torn-piece-01.png
paper-torn-piece-02.png
```

## 18. Asset Organisation

The final assets should be organised into logical folders.

Recommended structure:

```text
assets/
├── characters/
│   ├── human/
│   └── robot/
├── objects/
│   ├── rock/
│   ├── paper/
│   └── scissors/
├── results/
└── effects/
```

This structure should make the assets easy for both designers and developers to locate.

## 19. Consistency Requirements

All assets should be checked for:

- Consistent proportions.
- Consistent orientation.
- Consistent perspective.
- Consistent lighting.
- Consistent visual quality.
- Correct transparency.
- Correct dimensions.
- Correct naming.

The human and robot assets should look like parts of the same game while remaining visually distinct.

## 20. Delivery Requirements

The final asset package should contain:

- All required human assets.
- All required robot assets.
- Rock, Paper and Scissors objects.
- Broken Scissors.
- Torn Paper.
- Wrapped Rock.
- Result graphics.
- Animation-specific pieces.
- Editable source files where available.
- Final exported assets.
- The agreed folder structure.

Every asset should be tested inside the game before it is considered final.
