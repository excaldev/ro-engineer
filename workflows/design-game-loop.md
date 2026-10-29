# Workflow: design-game-loop (game designer role)

Design what the player does and why they keep doing it, before any systems.
Load `references/game-loops.md` and `references/player-incentives.md`; load
`references/progression-economy.md` for step 6.

## Phases

1. **Fantasy and audience.** One or two sentences: who the player is in this
   game, what they get to feel, and the target age range and platform mix
   (assume mobile-heavy unless told otherwise).
2. **Core loop.** Four steps: action, reward, progression, reinvestment. Each
   step gets a concrete example from this game.
3. **Loops at three time scales.**
   - **Micro** (seconds): the moment-to-moment action and feedback. Describe
     the feel (sound, VFX, camera) that makes it satisfying with no rewards.
   - **Session** (minutes): a satisfying round, run or shift with a clear end
     and a "one more" pull.
   - **Meta** (days and weeks): goals that span sessions, such as
     collections, ranks and prestige.
4. **First-session path.** With rough timestamps: when the first reward lands
   (target: within the first minute), when the first choice appears, when the
   first goal is visible, when the first session naturally ends.
5. **Hooks per time scale** with the player-facing reason each works and the
   motivation it serves (competence, autonomy, relatedness, discovery).
6. **Economy overview.** Currencies, sources, sinks, expected pacing to the
   first few milestones.
7. **Risks.** Grind walls, dead ends, exploits, pressure patterns that could
   feel manipulative, policy checks needed (paid random items, trading,
   time-limited offers).
8. **Systems required,** each mapped to the loop step it serves. These feed
   `design-system`.
9. **Output** using `templates/game-loop-template.md`.

**Stop and ask for approval.** Do not design systems or write code until the
loop is approved.

## In studio / rotex mode

For an existing game, inspect what is actually there (scripts, config,
existing systems) and design from the current loop, marking what is new vs.
changed.
