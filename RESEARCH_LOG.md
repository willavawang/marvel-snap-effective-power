# Marvel Snap Effective Power — Research Log

**Started:** 2026-10-20  
**Status:** Methodology draft; not yet statistically calibrated.  
**Goal:** Rank every currently playable card by one Effective Power (EP) number, grouped by printed energy cost, with a concise rationale. No website required.

## Core principles

1. Display one headline rating: printed cost / EP (e.g. Hulk 6/12).
2. Evaluate conditional on the card actually being played in plausible competent decks; weight actual play timing, rather than discounting every card for not being drawn.
3. Prefer observed frequencies; label simulations and assumptions. Pin a date/patch for card text and stats.
4. Share synergy through Shapley-style marginal contributions with a consistent counterfactual replacement-card baseline. Never count the same generated power twice.
5. Model competent, strategically adaptive opponents under imperfect information, including retreat/snap and best responses to visible signals.
6. Normalize effective energy investment back to printed energy cost. Account for discounts, turn skips, energy sinks, cost reducers and cheat-outs without double counting. Free summons require an allocation convention rather than division by zero.
7. Distinguish realized board power from power-equivalent strategic value, calibrated against winning locations and games.
8. Account for board slots, lane distribution, location restrictions and bonuses, matchup/counter prevalence, protection, timing, consistency, draw/play decisions, and opportunity costs.

## Provisional formula (v0.4; not validated)

EP(c) = C(c) × E_s[ φ_c(V(s)) / E_eff(c,s) | c played ]

- C(c): printed energy cost.
- s: deck, draws, turn, locations, opponent, strategies and observed information.
- φ_c: Shapley-style allocated marginal power-equivalent value.
- E_eff: positive allocated energy-equivalent investment, including relevant opportunity costs.
- Expectation weights scenarios by frequency under competent play.

**Unresolved mathematical issue:** The numerator and denominator need a coherent shared counterfactual baseline; otherwise opportunity cost may be double counted. Dividing by an energy allocation also risks inflating free-cheated cards. A benchmark energy-to-power exchange rate or counterfactual comparison may be preferable. This is a testable proposal, not an established final estimator.

## Infinaut: first stress test

- Straightforward line: skip turn 5, spend 6 on turn 6. Naively treating all 5 skipped energy as lost yields 20×6/11≈10.9 EP, but this is only an illustrative approximation.
- Skipped energy is not automatically wasted: Sunspot, She-Hulk and other mechanics can turn it into power or discounts. Calculate the net opportunity cost.
- Alternative deployment: Jubilee, other summons, discounts and extended games (e.g. Magik). Attribute the enabling benefit jointly.
- **Signaling / information leakage:** skipping turn 5 changes the opponent's posterior beliefs about Infinaut, She-Hulk and other plays. A competent opponent may abandon a lane, preserve a counter, or retreat. Model P(opponent action | public history), not a fixed signaling penalty.
- Bluffing and ambiguity can make the same skip less informative. Opponent adaptation affects both realized power and the value of the card.
- Retreats introduce selection bias: observed games where Infinaut reaches the board are not representative of all attempted Infinaut lines. Record the chosen conditional scoring convention.

## Attribution examples

- Elsa + Kitty: hypothetical isolated contributions Elsa=2, Kitty=4, together=8. Shapley allocation gives Elsa=3 and Kitty=5, not an arbitrary 50/50 total split.
- Silver Surfer and its supporting three-cost cards should use the same marginal-contribution rule.
- Sentinel's replacement card is not automatically three free power: additional plays consume energy and turns. Value the improved future options.
- Doctor Doom's distributed power is not equivalent in game value to the same total concentrated in one lane.

## Proposed first batch (printed stats must be verified at calculation time)

Hulk; Infinaut; She-Hulk; Death; Doctor Doom; Apocalypse. Expand to other six-cost cards after resolving timing, energy allocation, counterplay and location effects.

## Data needed

- Versioned full playable card definitions, including ability and current costs/power.
- Location pool, appearance probabilities and effects.
- Archetype/deck prevalence, card pairings, play rates, timing, and turn-by-turn game logs where obtainable.
- Counter frequencies and conditional opponent responses, including retreats.
- Rules for cost reduction, summoned cards, transforms, energy carryover, lane occupancy and final power.
- Empirical calibration/holdout comparisons; distinguish measured values from simulated assumptions.

## Reporting protocol

One row per card: name | printed cost/power | EP | short explanation | data confidence/assumptions in accompanying notes. Sort by printed energy, then descending EP. Preserve each formula revision and reasons for changes. Never present speculative EP estimates as measured facts.

## Open research questions

1. Exact value function V: board-power delta vs win-equivalent power, especially for retreats and disruption.
2. How to assign energy cost to free summons and joint enablers.
3. How to weight plausible decks without making the rating entirely dependent on meta prevalence.
4. How to approximate strategic equilibrium without assuming opponents know hidden cards.
5. Whether energy-ratio normalization survives stress tests, or needs replacement with a marginal reference-power conversion.
