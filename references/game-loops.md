# Game loops

## Loop anatomy

```
action -> reward -> progression -> reinvestment -> (action, now better)
```

- **Action:** the verb the player performs (mine, fight, build, jump, hatch).
- **Reward:** what the action produces (currency, item, XP, a reveal).
- **Progression:** visible change in the player's state (level, capacity,
  new zone, new tool).
- **Reinvestment:** the player spends the reward to get better at the action,
  which makes the next action more satisfying and restarts the loop.

If any step is missing, the loop leaks: rewards with nothing to spend on,
spending with no visible change, or progression that does not change how the
action feels.

## Time scales

**Micro loop (seconds).** The verb and its feedback. Must feel good with zero
rewards attached: movement, hit feel, sound, VFX, camera response, number
pops. If the micro loop is dull, no reward structure saves it.

**Session loop (minutes).** A run, round, shift or hatch cycle with a clear
start, peak and end. End on a visible gain and a visible next goal, so
stopping feels satisfying and returning feels obvious.

**Meta loop (days and weeks).** Collections, ranks, rebirth/prestige,
seasons, social standing. Gives a reason to come back that is bigger than one
session.

Each larger loop is made of repetitions of the smaller one. Design them
together: the meta loop should change how the micro loop feels (new tools,
new abilities, new places), not just multiply numbers.

## Genre loop examples

Adapt, do not copy. Each is a starting skeleton.

| Genre | Micro | Session | Meta |
|---|---|---|---|
| Simulator | Click/swing to collect | Fill bag, sell, upgrade capacity, unlock zone | Rebirth for permanent multipliers, pet collection |
| Tycoon | Collect drops, buy next button | Buy producers, earn faster, unlock tier | Complete the base, rebirth, new themes |
| Obby | Jump, fail fast, retry | Reach checkpoints, finish stage | Stage completion, speedrun times, cosmetics |
| RPG | Fight with abilities | Clear area/dungeon, loot, level | Gear sets, harder content, classes |
| Round-based / horror | Hide, run, solve | Survive the round, escape | Unlock cosmetics, lore, ranks |
| Social / roleplay | Interact, express | Play a role, complete a scenario | Housing, outfits, relationships |

## Loop quality checks

- Can a new player describe the loop after two minutes?
- Does the micro loop feel good with rewards turned off?
- Is each step's duration right? Does any step feel like waiting?
- Is there a meaningful choice in reinvestment, or only one obvious upgrade?
- What is the long-term goal, and can the player see it from the start?
- Where does a session naturally end, and what does the player see at that
  moment?
- Does progression unlock *new* things to do, or only bigger numbers?
- What does a player with 10 hours do differently from one with 10 minutes?

## Common failures

- **Grind wall:** the next unlock takes far longer than the previous one with
  nothing new in between. Add intermediate goals or alternate routes.
- **Dead end:** finishing the content leaves nothing to pursue. Add a meta
  loop (prestige, collection, mastery) before players reach it.
- **Reward without reinvestment:** currency piles up with nothing worth
  buying. Add sinks that improve the action.
- **Reinvestment without feel:** upgrades change a number the player cannot
  perceive. Make every upgrade visible and audible.
- **Single dominant choice:** one upgrade path is always correct. Create
  trade-offs or situational value.

## Writing a loop down

Use `templates/game-loop-template.md`. For each step, give a concrete
example from the game, the expected duration, and the system that implements
it.
