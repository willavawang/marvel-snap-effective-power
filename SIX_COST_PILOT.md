# Six-cost pilot — 2026-10-21

**Status: first analytical run; NOT an empirical million-game estimate.** Card text checked against October 2026 Marvel Snap sources. Numbers labeled exact are conditional on stated board conditions; formulas are not estimated means.

## Agreed scope

EP describes expected attributable **board power on occasions a card is played**, not relative deck win rate or best alternative use of energy. Hulk stays 6/12 even if two other cards could add 14. Ignore card-draw opportunity, deck-level strategic fit, and retreat selection for now. Note large variability with an asterisk and eventual 10th–90th percentile range, based on real samples. Do not invent percentiles.

## First run

| Card | Printed stats | First-pass EP | Calculation and caveat |
|---|---|---|---|
| Hulk | 6/12 | **6/12** | Exact baseline absent modifiers |
| Doctor Doom | 6/5 | **6/15** in fully open board | 5 + 5 + 5; less if other locations full, blocked, or On Reveal prevented |
| Infinaut | 6/20 | **6/10.9** in a conventional T5 skip/T6 play under *full-energy opportunity-cost assumption* | 20×6/(6+5); not yet a measured average. If T5 opportunity cost is 0, EP=20; with 2, EP=15. Alternative deployments change denominator |
| She-Hulk | 6/10 | **6/10** as board-power output; energy efficiency unresolved | Unspent prior-turn energy reduces cost. Do not multiply 10 by 6/(discounted cost) without allocating foregone energy |
| Apocalypse | 6/10 | **6/(10+4d)** | d is number of times discarded while in hand. A distribution of d is required |
| Knull | 6/0 | **6/D*** | D is total power of destroyed cards, as counted by ongoing ability. Needs actual played-game distribution, not a made-up 10–90 range |
| Hela | 6/6 | **6/(6+R)*** | R is summed power of revived cards; resurrection is restricted to different costs and space. Joint credit with discard enablers unresolved |
| Onslaught | 6/8 | **6/(8+B)*** | B is the allocated incremental board-power contribution from reapplying other ongoing effects here; some effects are not directly power-valued |

## Infinaut opportunity-cost sensitivity (illustrative, not measured)

Effective cost E=6+s where s is **actual opportunity value of the skipped turn in energy equivalents**.

| s | EP |
|---:|---:|
| 0 | 20.0 |
| 1 | 17.1 |
| 2 | 15.0 |
| 3 | 13.3 |
| 4 | 12.0 |
| 5 | 10.9 |

Important: s need not be 5; unused energy is not the same as lost achievable board power. This table exposes how sensitive the old formula is to an assumption, not a calibrated Infinaut rating.

## Findings

1. The raw-power calculation is reliable for Hulk and conditionally for Doctor Doom.
2. Infinaut shows that a full 5-energy turn skip is a very strong, often unjustified penalty. Need estimate of actual foregone turn-5 output, and separate skip cases from summon/cheat cases.
3. She-Hulk shows the opposite trap: a low paid energy cost may have required prior unspent energy. Discounted cost alone is misleading.
4. Knull, Hela, Apocalypse need observed play-conditioned distributions before a meaningful single EP and 10–90 percentile can be claimed.
5. Onslaught demonstrates that not every Ongoing effect maps straightforwardly to additive power.
6. Shapley attribution of support interactions remains an open issue. For this pilot, ability-created power is temporarily credited to the named payoff card, clearly labeled provisional.

## Sources

- https://marvelsnap.com/balance-update-october-15-2026/
- https://snap.fan/cards/DrDoom/
- https://snap.fan/cards/Infinaut/
- https://snap.fan/cards/SheHulk/
- https://snap.fan/cards/Knull/
- https://snap.fan/cards/Onslaught/
- https://snap.untapped.gg/en/meta/cards/hela

## Next step

Obtain turn-by-turn gameplay or defensible empirical estimates of conditional outcomes for 6-cost cards. Compute actual means, quantiles, and sample sizes; avoid fabricating precise rankings.
