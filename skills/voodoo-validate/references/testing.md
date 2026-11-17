# Prototype acceptance and loss logging

Plan and deliver one finished playable prototype in the selected engine. Use the project's normal entry point and a build or URL the user can run. Check the complete player flow and report any device behavior that still needs a real phone. The playbook provides suggested tests for comprehension and feel. [Puzzle Prototype Playbook](https://claude.ai/artifact/YMNU5BTiJHZVDWS6fJ6dRS)

## Acceptance checks

- Launch into the Main Menu. Start a new game with Play and resume saved progression with Continue. Verify all screens fit portrait safe areas on short and tall phones. Check that rotating a device preserves portrait play.
- For each step in L1–3, try off-target taps, drags, fast repeats and out-of-order actions. Confirm blocked input changes neither the board nor the move budget, the animated hand shows the current action and stops or moves at the right time, and the tutorial stays finishable. Exercise the first real loss in L4. Have new players try the tutorials on-device where possible.
- Verify 20 authored levels, core rules, distinct level personalities, hard-to-easy transitions around L9–10, L14–15 and L19–20, and L20 looping to about L6. Replay representative winning paths, mistakes, seeds and retries.
- Verify the Win panel, single coin reward and Next Level action. Confirm that Game Over blocks board input, displays the loss snapshot, offers Retry and handles 899 and 900 coins correctly. An accepted revive debits 900 once, adds exactly +5 moves or +30 seconds and preserves progress. A subsequent genuine loss generates a fresh record. Check that the prototype contains zero ad code, including disabled ad stubs, SDKs, placements and ad-gated actions.
- On a phone, check particles, brief screen shake, sound and vibration for small actions, blocked inputs and larger payoffs. Inspect the board after feedback and during repeated input. Record phone vibration as unverified if only desktop evidence is available.
- For any requested promotional footage, validate the opening in 3–5 seconds and show where its gameplay appears in L1–3. Keep footage outside the playable build.

## Loss event

Choose a progress metric that represents the objective, such as collected items divided by the target. Normalize it to a fraction from 0 to 1. For a puzzle with no countable goal, define a board-specific progress measure before implementing logging. Move or time consumption can explain the cause and should be recorded separately from objective progress.

On every genuine transition to loss, capture objective progress before showing Game Over or changing the board. Write one `level_lost` event with a unique loss ID, level ID, attempt ID, seed when applicable, loss cause, completed and required objectives or the progress proxy, `loss_progress`, and the relevant moves or time left. Reuse the snapshot in Game Over to tell the player how close they got. Use an inspectable local log or the project's existing instrumentation. Verify that redraws and repeated button taps produce no duplicates. Record a new loss ID if the player revives and genuinely loses again. Review the share of failures at or above 80% objective progress and tune earlier failures where feasible.
