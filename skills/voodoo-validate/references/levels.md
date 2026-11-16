# Levels, fairness and economy

Sources [Puzzle Prototype Playbook](https://claude.ai/artifact/YMNU5BTiJHZVDWS6fJ6dRS) (Level design, Targets), the user's brief and *Game Ideation Guide (1).pdf*, pp. 2 and 5. The example curve below is a playbook starting point. The brief and PDF's 20-level core-only requirement govern V1. Put the playbook's suggested feature introductions in V2. V1 can introduce examples of decisions and consequences already in the rules.

## First 20 levels

- L1 teaches one action with a guaranteed payoff. L2 demonstrates why order matters or shows the signature payoff. L3 demonstrates failure pressure safely. Use L4–5 for guided practice as needed. The first 3–5 are onboarding and must be clearable by new players. Use constrained scenarios, hint or recovery affordances as needed. Check with non-gamers on a real phone and record completions, confusion, retries and where help was needed.
- Start with small, clear boards and widening decision space. Use short confidence sprints, recognizable board silhouettes, crowded pressure boards, unfolding or longer boards, and squeeze levels. L9, L14 and L19 are example marked peaks with satisfying recovery at L10, L15 and L20. Justify another cadence if the game calls for it. The difficulty comes from layout, order, occupancy, piece count, target or resource budget within the same rules.
- For each level specify ID, learning or decision objective, layout/preset, mechanics already in use, starting quantities, goal, fail budget, difficulty and the replay check. For representative boards include reproducible configurations with two distinct winning paths. If V1 must loop past 20, rotate validated non-tutorial boards from around L6 with controlled variants. A loop does not count as additional complete levels.

## Retry variation and validation

- Vary at least one meaningful opening choice per retry where compatible with tutorial clarity. Use seeded, bounded permutations or a curated pool, with visible changes and deterministic resolution. Log level ID, seed and actions. Generate only from allowed ranges and use known-good fallbacks. Prove each shipping variant has meaningful solutions and a fair difficulty band via solver, replay or curated QA. A global color rename alone is cosmetic unless it changes decisions.
- For depth, show how board families, dimensions, targets and budgets combine within validated bounds and screen out duplicates, unsolvable variants, one-path boards and difficulty outliers. Explain how this workflow can reach 50 authored levels and credibly scale toward 1,000.
- Define `loss_progress` using an observable goal fraction or puzzle-specific progress proxy. Log it on failure and examine the share of losses at or above 80%, early deadlocks, progress by difficulty, and credible revive paths. Move burn alone can overstate progress. Keep tension and enough meaningful loss for continues while tuning away early irrecoverable states. Run deterministic bot or replay sweeps where available and verify what confused or satisfied humans on device.

## Economy for publisher-style prototypes

- Playbook V1 defaults are 1,000 starting coins, +50 per win, and a revive at 900. It normally grants +5 moves or +30 seconds when the relevant limit is moves or time. Choose a meaningful, bounded restoration for another limit. Preserve earned progress and check that the revived state is playable. Keep V1 focused on sequential levels, coins and revive. Reserve boosters, shop, lives and meta for later scope as applicable. Keep tutorial UI minimal and win transitions short.
- Playbook V2 targets 50 complete levels after a good D1 signal. Introduce one feature at a time with its own forgiving teaching level. Playbook defaults include three boosters at 600 coins each and roughly 1.4 ads per session. Treat these as test settings for that publishing context. Specify revive and reward behavior on retries or repeated actions when implementation is requested.
