# Six-cost EP quick pass — 21 October 2026

**Provisional model calibration, not measured EP.** Estimated values are subjective back-of-envelope assumptions; usage figures are observed Untapped.gg *popularity* (% matches), last 30 days / ranks 10–79 / Pool 3+, mostly updated October 18–21 2026. Popularity is NOT the share of drawn cards played, and comparisons are ecological, not causal.

## Working uniform rule

For each card: estimated net board-Power-equivalent change attributable to its deployment, divided by energy-equivalent investment and multiplied by its 6 printed cost. Ordinary cards use 6 energy; for cost reductions use estimated paid energy plus any opportunity-energy foregone to obtain discount. Direct boosts/summons add; enemy power stolen counts twice (a two-sided swing); friendly power destroyed subtracts; movement, location destruction, on-card text denial are *not* fully represented. We condition on card being played, not deck inclusion or win rate. When cards have high variance, mark *. We have NOT measured means or quantiles.

| Card | Printed | Estimated EP | Untapped popularity | Quick assumption |
|---|---:|---:|---:|---|
| Hela | 6/6 | **6/24** | 1.3% | ~18 revived power after unique-cost and space limits; payoff credit provisional |
| Knull | 6/0 | **6/22*** | 9.0% | Assume 22 total destroyed Power in games where played; tail may be extreme |
| Ultron | 6/8 | **6/19** | 1.9% | ~5.5 of eight possible 2-Power drones reach open slots |
| Mockingbird | 6/9 | **6/18*** | 2.3% | Assume 3 created cards already in play; paid 3 Energy -> 9×6/3 |
| Orka | 6/11 | **6/17*** | 0.3% | +7 if alone; assume succeeds in ~86% of cases played |
| Sasquatch | 6/11 | **6/16.5*** | 10.9% | Assume two cards played previous turn, so paid 4 Energy; 11×6/4 |
| Giganto | 6/16 | **6/16** | 3.1% | Left-lane restriction affects play frequency and location distribution, not raw Power when played |
| Anti-Polar Magneto | 6/8 | **6/15*** | 5.5% | Assume ~7 Power of 3/4-cost hand cards added into free slots |
| Blob | 6/0 | **6/15*** | 1.6% | Merges deck cards to at least 13 Power; assumes overshoot to ~15 |
| Leader | 6/5 | **6/15** | 0.7% | Copies an estimated 10 Power of strongest opposing turn-play when ability succeeds |
| Apocalypse | 6/10 | **6/14*** | 3.1% | Assume one discard while in hand (+4); Dracula rather than play makes many cases conditional |
| Arnim Zola | 6/0 | **6/14** | 9.6% | Destroys target then creates copies at other locations; estimate net +14, not sum copies without lost target |
| Destroyer | 6/18 | **6/14*** | 1.4% | Assume 4 net friendly Power lost on reveal; shields/destroy synergies change this |
| Emperor Hulkling | 6/12 | **6/14*** | 0.2% | Assume +2 net from random copied six-cost text, high random-effect risk |
| Hulk | 6/14 | **6/14** | 5.4% | Unmodified reliable 14; verified October 2026 |
| Odin | 6/10 | **6/14*** | 5.6% | Assume +4 incremental replayed On Reveal Power |
| Onslaught | 6/8 | **6/14*** | 3.6% | Assume +6 from repeated local Ongoing effects |
| The Infinaut | 6/20 | **6/13.3*** | 3.9% | Assume effective 3 Energy-equivalents sacrificed by prior turn of no card play, 20×6/9; some cheat-outs differ |
| Aurora | 6/5 | **6/13*** | 0.8% | Assume four +2 triggers across card-ability types; depends on available targets |
| Doctor Doom | 6/5 | **6/13*** | 3.1% | Assume bots successfully add to other lanes 85% and 75% of plays |
| Eson | 6/10 | **6/13*** | 0.9% | End of turn adds a created card from hand; assume average ~3 Power, available space |
| Galactus First Steps | 6/11 | **6/13*** | 1.2% | Assume one +2 End of Turn trigger; some gains happen before he is played |
| Gorr the God Butcher | 6/1 | **6/13*** | 4.8% | Assume six On Reveal cards in play, 1 + 2×6 |
| Red Hulk | 6/10 | **6/13*** | 1.1% | Assume one unspent-energy trigger (+3) |
| Spectrum | 6/7 | **6/13*** | 2.7% | Assume three Ongoing cards receive +2 |
| Taskmaster | 6/0 | **6/13*** | 2.2% | Assume copied previous card has 13 Power on occasions Taskmaster played |
| Agatha Harkness | 6/12 | **6/12** | 0.3% | Automated even-turn play hurts decisions, not physical Power |
| Helicarrier | 6/12 | **6/12** | 0.3% | Hand refill happens when discarded, not when Helicarrier is played |
| Magneto | 6/12 | **6/12** | 2.1% | Moves 3/4-cost enemy cards; positional swing not counted as additional Power |
| She-Hulk | 6/10 | **6/12*** | 1.2% | Assume paid 4 plus 1 effective Energy-equivalent sacrificed the preceding turn; 10×6/5 |
| Sinister Six | 6/12 | **6/12** | 0.7% | Typically automatically added after playing six marked characters; play-conditioned formula awkward |
| Thanos | 6/12 | **6/12** | 2.2% | Game-start stones change deck, but their played Power is not automatically credited to Thanos body |
| Vampire Enchantress | 6/7 | **6/12** | 0.8% | ~2.5 successful Power steals, each worth 2 Power-equivalent across both sides |
| Scorpion Brand New Day | 6/6 | **6/11*** | 1.6% | Assume ~5 total prior enemy Power reductions doubled |
| Heimdall | 6/10 | **6/10** | — | Movement redistributes existing Power; our simple metric misses tactical relocation |
| Khonshu | 6/5 | **6/10*** | 1.4% | Assume resurrects a discarded card set to 5 Power; other phases add complexity |
| The Living Tribunal | 6/9 | **6/9** | 1.7% | Redistribution across lanes is worth far more strategically than 9 raw added Power in many games |
| Alioth | 6/7 | **6/7** | 1.4% | Text denial on unrevealed enemy cards is not direct immediate Power |
| Galactus | 6/6 | **6/6** | 2.9% | Location destruction/removal cannot be represented sensibly as simple board Power added |

## Observations to test

1. **Orka (6/17; ~0.3% use)** and **Leader (6/15; 0.7%)** are candidate underuse signals, but almost certainly owe some of the gap to lane/turn restrictions and prediction risk.
2. **Ultron (6/19; 1.9%)** illustrates the need for location congestion and board-slot credit, especially if his drones are amplified by Patriot/Blue Marvel.
3. **Hela (6/24; 1.3%)** looks anomalously high because her resurrection is scored as if all output belongs to her; discount the costs and interdependence of getting the right discards.
4. **Knull (6/22; 9.0%)** is a high-power, high-usage alignment, but the average and heavy upper tail have not been empirically measured.
5. **Sasquatch (6/16.5; 10.9%)** seems aligned once cost discount is included; **She-Hulk (6/12; 1.2%)** may expose arbitrary accounting for saved vs foregone energy.
6. **Alioth, Galactus, Magneto, Heimdall, Living Tribunal** have strategically consequential effects that do not *create* Power and are structurally underrated by this board-Power formulation.
7. **Hulk (6/14; 5.4%)** is a stable reference; current popularity is disproportionately tied to High Evolutionary archetypes and should not be interpreted as pure vanilla card demand.
8. **Emperor Hulkling (6/14; 0.2%)** shows that random, uncontrolled outcomes cannot be summarized reliably by a point estimate even when average copied effects may be positive.

## Grounding and exclusions

- Base collectible card pool cross-checked with https://www.marvelsnapcards.com/series/pool-1/ , /pool-2/ , /pool-3/ , /pool-4/ , /pool-5/ ; updated texts/current balance checked against https://snap.fan/changelog/ and individual snap.fan card pages.
- Popularity checks: https://snap.untapped.gg/en/meta/cards-tier-list and many individual https://snap.untapped.gg/en/meta/cards/NAME pages (e.g. https://snap.untapped.gg/en/meta/cards/orka and https://snap.untapped.gg/en/meta/cards/anti-polar-magneto ).
- October 20 patch introduced cards but **not all newly datamined cards are released/collectible yet**. Excluded unreleased Sir Percy Black Knight, Doctor Doom Doomsday, The Grand Design, and noncollectible Hulk Avengers; also exclude Death, Skaar, and Fin Fang Foom, whose printed costs are now 8/7/7 rather than 6.
- The source pool pages are incomplete for the most recent released season cards. We added Sinister Six, Anti-Polar Magneto, Scorpion Brand New Day, Vampire Enchantress from individually checked current Snap.Fan and Untapped sources.

## Methodological audit flags

- The Infinaut: E_eff=9 assumes 3 effective turn-5 energy equivalents wasted; no empirical basis yet, so rating is extremely provisional.
- She-Hulk: E_eff=5 assumes 4 energy spent, 1 foregone energy-equivalent; no empirical basis.
- Sasquatch: E_eff=4 assumes two cards played prior turn, which still contributed ordinary value.
- Mockingbird: E_eff=3 assumes 3 created cards in play, with those cards' own energy costs assigned to themselves.
- All calculated bonus effects except direct card-text guarantees are hypothetical conditional averages. Asterisks mean uncertain/variable, not measured 10–90 percentile ranges.

**Total rows: 39.**