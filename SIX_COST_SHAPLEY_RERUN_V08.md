# Six-cost Effective Power — v0.8 Shapley power AND energy rerun (2026-10-21)

**Status: 39-card provisional back-of-the-envelope scenario estimates, not measurements.** This file supersedes the modeling assumptions of `SIX_COST_QUICK_PASS_2026-10-21.md`. It is intentionally a rough *stress test* of the proposed uniform statistic; no game-level played-card logs or actual Shapley coalition values have been obtained. `*` means estimation/variation concerns; no percentile ranges are asserted without observations.

**Current formula v0.8:**
```
EP(card) = printed_cost(card) × mean(Shapley-attributed realized power | played)
                               / mean(Shapley-attributed effective energy cost | played)
```
For every entry below printed cost=6, so `EP = 6 × P̄ / Ē`. Mean energy is taken **before dividing**, handling occasional zero-cost deployments. Mean power includes real lane success/fail and location effects only to extent a concrete card-specific assumption is available; we do not assign a universal location or slot penalty. This pilot does **not** simulate complete location distributions. Do not present the figures as empirical conditional averages.

### How allocation was approximated

For a two-contributor interaction, genuine **incremental cooperative power** was split 50/50 in accordance with the two-player Shapley value. E.g., if Hela contributes 6 on her own, discard setup has other independent effects, and their interaction yields 18 extra resurrected Power, Hela gets `6 + 18/2=15`. This is **not** a full multi-card Shapley computation and may be dramatically wrong when a synergy requires three+ components, has independent backup routes, or has high-order interactions. Baseline printed independent Power remains assigned to its source, not split mechanically. For Knull, hypothetical 22 destroyed-Power pool is allocated 11 to Knull and 11 to destroy-enabling actions. For a genuine synergy-independent body/token generated directly by one card (Doom or Ultron), the maker gets the body/token Power; we split only *additional* synergistic buffs contributed with other cards.

For energy, assign *energy physically paid for the card* to it unless joint enablement changes that accounting, then split only **incremental genuinely forgone useful energy**, rather than charging the entire energy of enablers who made independently useful plays. This is a simplified Shapley-inspired proxy, not a computed Shapley energy characteristic function. Energy already wasted for lack of useful plays is zero sacrifice. Avoid crediting the same Sunspot gain as both She-Hulk's discount and Sunspot's power.

**Usage comparator:** Untapped.gg observed *card popularity* (share of ranked matches in its tracked sample), last 30 days / Pool 3+ / roughly ranks 10–79, mostly October 18–21, 2026. Popularity is not conditional play rate, collection ownership-adjusted demand or win rate. Source: https://snap.untapped.gg/en/meta/cards-tier-list ; individual card pages such as https://snap.untapped.gg/en/meta/cards/hela and https://snap.untapped.gg/en/meta/cards/she-hulk . Inputs rounded and occasionally from prior crawl, so interpret ~ not precise.

## Results (sorted by v0.8 EP)

| Rank | Card | Printed | v0.8 EP | v0.7 quick pass | Usage | Allocated P̄ | Allocated Ē | Main assumption |
|---:|---|---:|---:|---:|---:|---:|---:|---|
| 1 | Ultron | 6/8 | **6/21*** | 6/19 | 1.9% | 21 | 6 | 8 body + 5.5 successfully added 2-Power drones (11) + half of ~4 support-buff power (2) |
| 2 | Orka | 6/11 | **6/17*** | 6/17 | 0.3% | 17 | 6 | 11 + 7×85% probability of being alone in its location after play; estimate, not measured |
| 3 | The Infinaut | 6/20 | **6/16.4*** | 6/13.3 | 3.9% | 20 | 7.3 | 20 direct body; pay 6 Energy plus 1.3 mean attributed useful-energy sacrifice from turn-5 skip |
| 4 | Giganto | 6/16 | **6/16*** | 6/16 | 3.1% | 16 | 6 | 16 when successfully played left; location restriction affects chance to play, not physical body |
| 5 | Sasquatch | 6/11 | **6/15.5*** | 6/16.5 | 10.9% | 11 | 4.3 | Mean 4.15 Energy paid after last-turn card-count discount + 0.10 joint setup cost |
| 6 | Blob | 6/0 | **6/15*** | 6/15 | 1.6% | 15 | 6 | Assume merged deck cards produce 15 power in aggregate; direct ability, not a required teammate combo |
| 7 | Leader | 6/5 | **6/15*** | 6/15 | 0.8% | 15 | 6 | 5 body + expected 10 Power from copied enemy cards when played; opponent isn't a cooperative Shapley partner |
| 8 | Hela | 6/6 | **6/14.3*** | 6/24 | 1.4% | 15 | 6.3 | 6 body + half of assumed 18 resurrected power; 0.3 attributable incremental setup energy |
| 9 | She-Hulk | 6/10 | **6/14.1*** | 6/12 | 1.2% | 10 | 4.3 | Illustrative mean paid 3.85 Energy + 0.40 Shapley share of truly forgone useful Energy |
| 10 | Destroyer | 6/18 | **6/14*** | 6/14 | 1.4% | 14 | 6 | 18 body - 4 net friendly power destroyed; may create offsetting effects in destroy decks |
| 11 | Emperor Hulkling | 6/12 | **6/14*** | 6/14 | 0.2% | 14 | 6 | 12 body + assumed net 2 from random copied six-cost ability; huge variance |
| 12 | Hulk | 6/14 | **6/14** | 6/14 | 5.4% | 14 | 6 | Printed body, no inherent synergies; unchanged anchor |
| 13 | Mockingbird | 6/9 | **6/13.5*** | 6/18 | 2.1% | 9 | 4 | Mean 3.6 Energy paid + 0.4 Shapley-allocated opportunity energy for creation setup |
| 14 | Doctor Doom | 6/5 | **6/13*** | 6/13 | 2.9% | 13 | 6 | 5 body + 5×(2×65%+1×30%) = 13 total; 5% fail both, illustrative slot mix |
| 15 | Odin | 6/10 | **6/13*** | 6/14 | 5.6% | 13 | 6 | 10 body + half of estimated 6 power from replaying prior allied On Reveals |
| 16 | Red Hulk | 6/10 | **6/13*** | 6/13 | 1.1% | 13 | 6 | 10 body + assumed single +3 end-of-turn trigger during hand/play |
| 17 | Apocalypse | 6/10 | **6/12.6*** | 6/14 | 3.1% | 13 | 6.2 | 10 body + half of 1.5×4 discard growth (3), 0.2 incremental attributed setup cost |
| 18 | Galactus First Steps | 6/11 | **6/12.5*** | 6/13 | 1.2% | 12.5 | 6 | 11 body + half of assumed 3 Power accumulated through Herald-dependent +2 triggers |
| 19 | Agatha Harkness | 6/12 | **6/12** | 6/12 | 0.3% | 12 | 6 | 12 Power; automation's strategic damage excluded by design |
| 20 | Helicarrier | 6/12 | **6/12** | 6/12 | 0.3% | 12 | 6 | 12 Power when played; its discard-trigger benefit is excluded from played-conditioned figure |
| 21 | Magneto | 6/12 | **6/12*** | 6/12 | 2.1% | 12 | 6 | 12 Power, movement redistributes enemy cards but adds no global board Power |
| 22 | Sinister Six | 6/12 | **6/12*** | 6/12 | 0.7% | 12 | 6 | 12 body, but normally ADDED after six EVIL plays, not played; denominator/condition fails here |
| 23 | Thanos | 6/12 | **6/12*** | 6/12 | 2.2% | 12 | 6 | 12 when played; six stones are pre-game setup, attributed effect not fully captured |
| 24 | Vampire Enchantress | 6/7 | **6/12*** | 6/12 | 0.8% | 12 | 6 | 7 body + assumed 2.5 Power steals ×2 Power swing each (our loss/opponent gain) |
| 25 | Anti-Polar Magneto | 6/8 | **6/11.5*** | 6/15 | 5.5% | 11.5 | 6 | 8 body + half of ~7 Power from hand cards jointly added without being played; coarse two-bundle attribution |
| 26 | Eson | 6/10 | **6/11.5*** | 6/13 | 0.9% | 11.5 | 6 | 10 body + half of assumed 3 Power generated through added created-hand card |
| 27 | Knull | 6/0 | **6/11*** | 6/22 | 9.0% | 11 | 6 | Half of assumed 22 destroyed-power pool credited to payoff, half to destroy engine |
| 28 | Onslaught | 6/8 | **6/11*** | 6/14 | 3.6% | 11 | 6 | 8 body + half of estimated 6 additional ongoing power made with other cards |
| 29 | Heimdall | 6/10 | **6/10*** | 6/10 | 1.2% | 10 | 6 | Movement changes distribution and potential win, not global raw Power |
| 30 | Spectrum | 6/7 | **6/10*** | 6/13 | 2.7% | 10 | 6 | 7 body + half of +6 from boosting three existing Ongoing cards |
| 31 | Alioth | 6/7 | **6/9*** | 6/7 | 1.4% | 9 | 6 | 7 body + assumed ~2 points of future enemy Power denied by text removal; many denial effects not convertible |
| 32 | Aurora | 6/5 | **6/9*** | 6/13 | 0.7% | 9 | 6 | 5 body + half of estimated 8 power in allied category-specific boosts |
| 33 | The Living Tribunal | 6/9 | **6/9*** | 6/9 | 1.7% | 9 | 6 | 9 body; global Power conserved by splitting; benefit across lanes invisible to this metric |
| 34 | Scorpion Brand New Day | 6/6 | **6/8.5*** | 6/11 | 1.6% | 8.5 | 6 | 6 body + half of ~5 additional enemy Power reduced with earlier allied debuffs |
| 35 | Khonshu | 6/5 | **6/7.5*** | 6/10 | 1.3% | 7.5 | 6 | 5 body + half of a single revived 5-Power discard combo; phase effects excluded |
| 36 | Arnim Zola | 6/0 | **6/7*** | 6/14 | 9.6% | 7 | 6 | Assume copied card has ~14 power: destroying one and adding two gains net +14; split marginal synergy with target |
| 37 | Gorr the God Butcher | 6/1 | **6/7*** | 6/13 | 4.8% | 7 | 6 | 1 body + half of +12 from 6 allied On Reveal cards (each interaction shared) |
| 38 | Taskmaster | 6/0 | **6/6.5*** | 6/13 | 2.2% | 6.5 | 6 | Assume previous allied card 13 Power; half of copied-output synergy allocated to Taskmaster |
| 39 | Galactus | 6/6 | **6/6*** | 6/6 | 2.9% | 6 | 6 | 6 body; destroying locations changes the game objective, not representable by global added Power |

## Largest changes from previous quick pass

- **Knull**: 6/22 → **6/11** (-11 EP): Half of assumed 22 destroyed-power pool credited to payoff, half to destroy engine
- **Hela**: 6/24 → **6/14.3** (-9.7 EP): 6 body + half of assumed 18 resurrected power; 0.3 attributable incremental setup energy
- **Arnim Zola**: 6/14 → **6/7** (-7 EP): Assume copied card has ~14 power: destroying one and adding two gains net +14; split marginal synergy with target
- **Taskmaster**: 6/13 → **6/6.5** (-6.5 EP): Assume previous allied card 13 Power; half of copied-output synergy allocated to Taskmaster
- **Gorr the God Butcher**: 6/13 → **6/7** (-6 EP): 1 body + half of +12 from 6 allied On Reveal cards (each interaction shared)
- **Mockingbird**: 6/18 → **6/13.5** (-4.5 EP): Mean 3.6 Energy paid + 0.4 Shapley-allocated opportunity energy for creation setup
- **Aurora**: 6/13 → **6/9** (-4 EP): 5 body + half of estimated 8 power in allied category-specific boosts
- **Anti-Polar Magneto**: 6/15 → **6/11.5** (-3.5 EP): 8 body + half of ~7 Power from hand cards jointly added without being played; coarse two-bundle attribution
- **The Infinaut**: 6/13.3 → **6/16.4** (3.1 EP): 20 direct body; pay 6 Energy plus 1.3 mean attributed useful-energy sacrifice from turn-5 skip
- **Onslaught**: 6/14 → **6/11** (-3 EP): 8 body + half of estimated 6 additional ongoing power made with other cards
- **Spectrum**: 6/13 → **6/10** (-3 EP): 7 body + half of +6 from boosting three existing Ongoing cards
- **Scorpion Brand New Day**: 6/11 → **6/8.5** (-2.5 EP): 6 body + half of ~5 additional enemy Power reduced with earlier allied debuffs

## Cases that test the new model, rather than confirm it

1. **Hulk 6/14** is unchanged and fully auditable (before incidental location modifications). **Doctor Doom 6/13** assumes 65%/30%/5% probability of 2/1/0 successful DoomBots; this is **hypothetical**; location and board crowding must be measured.
2. **Hela 6/14.3**, **Knull 6/11**, **Arnim Zola 6/7**, and **Gorr 6/7** now receive substantially less EP because the combo bonus is shared with contributors. These large downward changes illustrate the dangers of a blanket 50/50 split—especially when the other component would have happened anyway. Their observed usage (1.4%, 9.0%, 9.6%, 4.8%) is a useful falsification target. Do **not** lower observed figures, change card inclusion assumptions, or silently waive sharing just to fit popularity.
3. **She-Hulk 6/14.1** uses hypothetical paid-energy mixture averaging **3.85** plus a Shapley-style **0.40** truly sacrificed-energy charge. Energy may cost 0 when no alternative useful play existed. **Sasquatch 6/15.5** and **Mockingbird 6/13.5** get analogous (unmeasured) normalized discounts.
4. **Infinaut 6/16.4** assumes 1.3 useful energy-equivalents truly sacrificed on turn 5, not all 5 idle energy; Sunspot and She-Hulk can absorb opportunity cost. This assumption is especially influential.
5. **Ultron 6/21** assumes 5.5 2-Power drones successfully added (11 Power), and *half* of 4 additional buff Power from cooperative support. **Orka 6/17** assumes 85% lone-lane success. Both may be rare in deckbuilding for reasons outside EP.
6. **Galactus, Living Tribunal, Heimdall, Magneto, Alioth** demonstrate **structural failure** of raw global board-power scoring: changing lane selection, removing lanes, or denying text is strategically important without creating measurable additive Power. Their ratings are **not** comparable as strategic values even if accurately measured.
7. **Sinister Six** normally enters play by being **added**, not played. Rating it as if played for 6 is a placeholder that violates the stated conditioning rule.
8. **Shapley logic needs a consistent characteristic function**, i.e., specify which board state and energy are evaluated with *subsets of the enabler cards removed*, keeping the same plausible baseline. Counterfactuals must not arbitrarily replace absent cards with best alternatives. Detailed exact allocation is therefore *not yet implemented*, only a 2-contributor share proxy.
9. **Percentile ranges** are not provided because no game-level power sample is available. An asterisk is not a measured interval; confidence is low for nearly all non-vanilla ratings.

## Next data collection priority

Capture per-play records with: card, current printed stats, energy paid, preceding-turn unused energy, genuinely useful plays foregone (or estimate), allies that enabled effect, location board slots, local modifiers, effect-added cards, power gained/lost, and game result separately. Then calculate power/cost coalition values for Hela, Knull, Arnim Zola and She-Hulk. Explicitly contrast **(A) full triggered payoff** vs **(B) Shapley-attributed payoff**, instead of assuming either fits usage better.

## Sources

- Untapped (card texts, popularity): https://snap.untapped.gg/en/meta/cards-tier-list
- Hela: https://snap.untapped.gg/en/meta/cards/hela
- She-Hulk: https://snap.untapped.gg/en/meta/cards/she-hulk
- Ultron: https://snap.untapped.gg/en/meta/cards/ultron
- Hulk: https://snap.untapped.gg/en/meta/cards/hulk
- Orka: https://snap.untapped.gg/en/meta/cards/orka
- October 2026 changes: https://snap.fan/cards/history/2026/
- Official April 2026 Hela resolver note: https://marvelsnap.com/balance-update-april-16-2026/
- Past work: `SIX_COST_QUICK_PASS_2026-10-21.md`, `FORMULA_V06_DECISIONS.md`, `RESEARCH_LOG.md`
