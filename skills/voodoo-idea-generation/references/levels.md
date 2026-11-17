# Levels, fairness and economy

Use the user's brief and *Game Ideation Guide (1).pdf*, pp. 2 and 5, for the 20-level core. Use the playbook for difficulty and economy examples. [Puzzle Prototype Playbook](https://claude.ai/artifact/YMNU5BTiJHZVDWS6fJ6dRS)

## First 20 levels

- L1 teaches one action with a guaranteed payoff. L2 demonstrates why order matters and delivers the signature payoff. L3 demonstrates failure pressure safely. For each step, define the allowed input and exact board targets, then show the required tap, drag or swipe with an animated hand. Enforce the restriction in game input as well as visually. Block off-target or out-of-step input before it changes the board, spends a move or advances the lesson. Advance the hand and lesson after the expected action resolves. Keep L1–3 finishable and shield them from terminal loss and forced restarts. L4 is the first level that can trigger Game Over.
- Give each level a personality and a purpose. Use quick wins, memorable shapes, crowded boards, longer setups and very hard squeezes. Target difficulty peaks at L9, L14 and L19. Follow them with easy L10, L15 and L20. Tune layout, order, occupancy, piece count, target and budget within the same rules.
- For each level specify ID, personality, learning or decision objective, layout/preset, starting quantities, goal, fail budget, difficulty and replay check. Map gameplay from any requested promo to L1–3. For representative boards include reproducible configurations with two distinct winning paths. After the L20 Win panel, proceed to a validated non-tutorial board around L6, using L6 by default. Keep the player's economy and validate the repeated sequence and seeded variants.

## Retry variation and validation

- Vary at least one meaningful opening choice per retry where compatible with tutorial clarity. Use seeded, bounded permutations or a curated pool, with visible changes and deterministic resolution. Log level ID, seed and actions. Generate only from allowed ranges and use known-good fallbacks. Prove each shipping variant has meaningful solutions and a fair difficulty band via solver, replay or curated QA. A global color rename alone is cosmetic unless it changes decisions.
- For depth, show how board families, dimensions, targets and budgets combine within validated bounds and screen out duplicates, unsolvable variants, one-path boards and difficulty outliers.
- Define `loss_progress` using an observable goal fraction or puzzle-specific progress proxy. Target a majority of failures at or above 80% progress. Track early deadlocks, progress by difficulty and whether the continue can finish the attempt. Move burn alone can overstate progress. Use deterministic replay sweeps for the board logic and playtests to learn when players would continue instead of restarting.

## Economy

- Start at 1,000 coins and award +50 per win as playbook defaults. Revive costs 900 coins and adds +5 moves in a moves-based level or +30 seconds in a timed level. Offer it from Game Over when the grant restores a playable attempt. Show the price and grant up front. Charge once on acceptance, retain the current board and objective progress, and return the player to that level. Retry starts the level over without a revive charge. Keep Retry available when the balance is under 900 coins. The revive uses coins only.
