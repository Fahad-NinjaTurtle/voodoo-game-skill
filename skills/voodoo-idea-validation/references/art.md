# Mobile art and game feel

Use [Execution: Art, Gamefeel & Animations](https://app.notion.com/p/Execution-Art-Gamefeel-Animations-bc6fe94c74608317a6e001042f76d2bb) as the main visual benchmark and the [Puzzle Prototype Playbook](https://claude.ai/artifact/YMNU5BTiJHZVDWS6fJ6dRS) for prototype context.

## Art that explains the rules

- Target first-glance recognition of the board and actionable object, then a roughly 1–3 second read of the action and its outcome. Give the playfield the prime screen area. Keep UI secondary, touch areas generous and negative space deliberate. Use size, placement, value and silhouette to show hierarchy. Avoid numbers on pieces, dense labels and visual clutter. If information is essential, surface it plainly in the scene or HUD.
- Use a controlled, vibrant palette with a dark or neutral field. Give neighboring roles distinct colors and values; use complementary pairings where they help. Use up to eight gameplay colors per level. Keep light purple, white and black off playable pieces. Check grayscale screenshots for separation of piece, target, board, blocked state and important UI. Use shape or another cue for gameplay distinctions that would otherwise rely on hue alone.
- Prefer a coherent soft, rounded shape language and symbols players already recognize. A container suggests collection, a lock signals blocked, and a bomb signals destruction or pressure. Make selectable, selected, preview, blocked and resolved states visually distinct. Use controlled depth or gloss only where it guides attention. Default to 2D where it reads and loads cleanly. When spatial mechanics warrant 3D, use low-poly assets, simple materials and lightweight lighting.
- Establish one real visual reference and label what to learn from each benchmark. For example, study Pixel Flow for movement and input, Car Match for easing, Block Blast for reward scale, and Royal Kingdom for FX. Respect the project's art pipeline. Use a cited art direction, owned assets, hand-built geometric blockouts or approved packs. The team playbook uses in-house final art. AI may assist execution studies and iteration with approved references. Require matching silhouettes, materials, palette and perspective across revisions. Reject generic plastic gloss, gradient-heavy pieces, noisy generated textures, fake lettering, inconsistent renders, unsupported spectacle and placeholder visuals in a test-ready build. Art should be recognizably about this puzzle.

## Portrait layout and panels

- Design every screen for portrait. Lock native builds to portrait and disable landscape autorotation. Where a web build cannot lock device orientation, keep the playable viewport in a centered portrait frame on wide screens. Check short and tall phones, safe areas and reachable primary controls.
- Main Menu. Open here on launch. Give Play a clear route to L1 for new players and Continue a route to the player's saved progression. Keep these controls distinct from the game board.
- Win. Show the result and coins earned. Credit the reward once. Next Level advances directly into the next board, including the loop after L20. Keep the celebration brief.
- Game Over. From L4 onward, show the progress reached and the remaining goal. Offer Retry and, when eligible, a 900-coin revive with its exact grant. Explain an insufficient balance. Keep board input blocked while a result panel is open.
- Tutorial hand. Animate a point and tap pulse for taps, or trace the actual path for a drag or swipe. Anchor the hand to the current target in portrait layouts. Keep it clear of the main action and let touches pass through it. Update or hide it when the step completes or the player leaves the tutorial.

## Feedback spec

Specify particles, screen shake, sound and phone vibration for each discrete gameplay action. Include selection, move, placement, blocked input, goal progress, combos and result actions. Give each action a visible response and a short sound and haptic cue on supported devices. Scale particles and screen shake to the event. Blocked or small actions use subtle cues and larger successes earn stronger effects. Avoid retriggering cues on every frame of a hold or drag. Keep the board readable and respect mute, haptics and reduced-motion settings where available.

1. Start visible response on touch. Match movement to the gesture, and give an invalid move a brief rejection cue.
2. Give each success a readable payoff. Scale move, success and combo with distinct intensity. Repeated events should still feel satisfying.
3. Let nearby objects or the environment respond when it reinforces cause and effect.
4. Use contrast, highlights, depth and clear affordances to guide the next choice.
5. Use a rising pitch for streaks when it fits the game. Check that the sound and vibration patterns are distinct on a real phone.
6. Reinforce each result with the corresponding panel, motion and audio cue.

Animate purposeful starts, travel and stops with easing, selective overshoot and settling. Use brisk small moves and greater weight for larger events. Align particles with the action's direction and reward scale. Keep the next playable state visible and responsive. Inspect phone-size screenshots, grayscale and a frame-by-frame clip. Compare a raw iteration and a polished one with the same rules. Identify the top three gaps and prioritize the feedback the player experiences every move.
