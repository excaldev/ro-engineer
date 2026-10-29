# Workflow: retention-audit

Review an existing game's loops and hooks against player incentives. Load
`references/game-loops.md` and `references/player-incentives.md`.

## Phases

1. **Reconstruct the loop.** From the game (playtest, scripts and config in
   `studio` mode) or the user's description: core loop steps, session loop,
   meta loop.
2. **First session walk-through,** with timestamps:
   - when the first reward lands
   - when the first choice appears
   - when the first goal is visible
   - where a new player is likely to hesitate or get lost
3. **Stall points.** Where pacing slows sharply, where progression stops
   unlocking new things, where content runs out.
4. **Hook inventory** per time scale (first minute, session, days, long term,
   social). For each: the motivation it serves, the player-facing reason, and
   whether it is purely pressure (guilt, fake urgency, punishing absence).
5. **Data.** What analytics are tracked (funnels, D1/D7/D30, session length,
   progression). If none, recommend the minimum set.
6. **Ethics and policy check** on hooks involving paid randomness,
   time-limited purchases, or streaks.

## Output

A ranked list of fixes, highest expected impact first. Each fix: the
problem, the evidence, the change, the loop step or time scale it affects,
and how to measure whether it worked.
