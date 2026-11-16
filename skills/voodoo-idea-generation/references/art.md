# Mobile art and game feel

Use [Execution: Art, Gamefeel & Animations](https://app.notion.com/p/Execution-Art-Gamefeel-Animations-bc6fe94c74608317a6e001042f76d2bb) as the main visual benchmark and the [Puzzle Prototype Playbook](https://claude.ai/artifact/YMNU5BTiJHZVDWS6fJ6dRS) for prototype context.

## Art that explains the rules

- Target first-glance recognition of the board and actionable object, then a roughly 1–3 second read of the action and its outcome. Give the playfield the prime screen area. Keep UI secondary, touch areas generous and negative space deliberate. Use size, placement, value and silhouette to show hierarchy. Avoid numbers on pieces, dense labels and visual clutter. If information is essential, surface it plainly in the scene or HUD.
- Use a controlled, vibrant palette with a dark or neutral field. Give neighboring roles distinct colors and values; use complementary pairings where they help. Use up to eight gameplay colors per level. Keep light purple, white and black off playable pieces. Check grayscale screenshots for separation of piece, target, board, blocked state and important UI. Use shape or another cue for gameplay distinctions that would otherwise rely on hue alone.
- Prefer a coherent soft, rounded shape language and symbols players already recognize. A container suggests collection, a lock signals blocked, and a bomb signals destruction or pressure. Make selectable, selected, preview, blocked and resolved states visually distinct. Use controlled depth or gloss only where it guides attention. Default to 2D where it reads and loads cleanly. When spatial mechanics warrant 3D, use low-poly assets, simple materials and lightweight lighting.
- Establish one real visual reference and label what to learn from each benchmark. For example, study Pixel Flow for movement and input, Car Match for easing, Block Blast for reward scale, and Royal Kingdom for FX. Respect the project's art pipeline. Use a cited art direction, owned assets, hand-built geometric blockouts or approved packs. The team playbook uses in-house final art. AI may assist execution studies and iteration with approved references. Require matching silhouettes, materials, palette and perspective across revisions. Reject generic plastic gloss, gradient-heavy pieces, noisy generated textures, fake lettering, inconsistent renders, unsupported spectacle and placeholder visuals in a test-ready build. Art should be recognizably about this puzzle.

## Feedback spec

For each critical event define cue, start/travel/settle, priority, audio/haptic and what the board communicates. Include select, move, place, illegal or blocked input, score or goal progress, combo or payoff, win, near-loss and revive.

1. Start visible response on touch. Match movement to the gesture, and give an invalid move a brief rejection cue.
2. Give each success a readable payoff. Scale move, success and combo with distinct intensity. Repeated events should still feel satisfying.
3. Let nearby objects or the environment respond when it reinforces cause and effect.
4. Use contrast, highlights, depth and clear affordances to guide the next choice.
5. Specify short input audio and differentiated haptics on supported devices, with stronger cues for important actions and a rising pitch for a streak. Check on a phone with audio and haptics enabled and muted.
6. Celebrate a win promptly. Show remaining progress and the revive benefit on a loss.

Animate purposeful starts, travel and stops with easing, selective overshoot and settling. Use brisk small moves and greater weight for larger events. Align particles with the action's direction and reward scale. Keep the next playable state visible and responsive. Inspect phone-size screenshots, grayscale and a frame-by-frame clip. Compare a raw iteration and a polished one with the same rules. Identify the top three gaps and prioritize the feedback the player experiences every move.
