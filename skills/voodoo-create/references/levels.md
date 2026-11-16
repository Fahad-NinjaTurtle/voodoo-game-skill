# Levels, fairness and economy

Sources [Puzzle Prototype Playbook](https://claude.ai/artifact/YMNU5BTiJHZVDWS6fJ6dRS) (Level design, Targets), the user's brief and *Game Ideation Guide (1).pdf*, pp. 2 and 5. The example curve below is a playbook starting point. The brief and PDF's 20-level core-only requirement govern V1. Put the playbook's suggested feature introductions in V2. V1 can introduce examples of decisions and consequences already in the rules.

## First 20 levels

- L1 teaches one action with a guaranteed payoff. L2 demonstrates why order matters and delivers the signature payoff. L3 demonstrates failure pressure safely. L1–3 must always remain finishable. Test inefficient moves, depleted budgets, timeouts and blocked states. Use guidance, constrained choices or free recovery to keep the tutorial playable. L4 is the first level allowed to trigger Game Over. Check the opening levels with new players on a portrait phone.
- Give each level a personality and a purpose. Use quick wins, memorable shapes, crowded boards, longer setups and very hard squeezes. Target difficulty peaks at L9, L14 and L19. Follow them with easy L10, L15 and L20. Tune layout, order, occupancy, piece count, target and budget within the same rules.
- For each level specify ID, personality, learning or decision objective, layout/preset, starting quantities, goal, fail budget, difficulty and replay check. Map ad moments to L1–3. For representative boards include reproducible configurations with two distinct winning paths. After the L20 Win panel, go straight into a validated non-tutorial board around L6, using L6 by default. Keep the player's economy and validate the repeated sequence and seeded variants. The loop reuses authored boards.

## Retry variation and validation

- Vary at least one meaningful opening choice per retry where compatible with tutorial clarity. Use seeded, bounded permutations or a curated pool, with visible changes and deterministic resolution. Log level ID, seed and actions. Generate only from allowed ranges and use known-good fallbacks. Prove each shipping variant has meaningful solutions and a fair difficulty band via solver, replay or curated QA. A global color rename alone is cosmetic unless it changes decisions.
- For depth, show how board families, dimensions, targets and budgets combine within validated bounds and screen out duplicates, unsolvable variants, one-path boards and difficulty outliers. Explain how this workflow can reach 50 authored levels and credibly scale toward 1,000.
- Define `loss_progress` using an observable goal fraction or puzzle-specific progress proxy. Target a majority of failures at or above 80% progress. Track early deadlocks, progress by difficulty and whether the continue can finish the attempt. Move burn alone can overstate progress. Use deterministic replay sweeps for the board logic and playtests to learn when players would continue instead of restarting.

## Economy for publisher-style prototypes

- Playbook V1 defaults are 1,000 starting coins and +50 per win. A revive costs 900 coins and adds +5 moves in a moves-based level or +30 seconds in a timed level. Offer it from Game Over when it can restore a playable attempt. Show the price and grant up front. Charge once on acceptance, keep the current board and objective progress, and return the player to that level. Verify Retry and the insufficient-coins state.
- Playbook V2 targets 50 complete levels after a good D1 signal. Introduce one feature at a time with its own forgiving teaching level. Playbook defaults include three boosters at 600 coins each and roughly 1.4 ads per session. Treat these as test settings for that publishing context. Specify revive and reward behavior on retries or repeated actions when implementation is requested.
