# Six-cost EP v0.8 — transparent assumption rerun (October 21, 2026)

> **An assumption stress test, NOT a measured EP study.** All values remain constructed from explicit, unmeasured play-conditioned scenarios. Popularity is an external observational comparison, not an input for forcing EP into an expected range. A **6/12–19** typical range is a prior for flagging anomalies, **not** a clamp; results outside it are retained. Supersedes earlier pilot estimates as the latest *illustrative* scenario calculation, not as statistically validated averages.

**Status and scope:** 39 previously identified printed-six-cost candidates, inherited from the prior pool audit; not independently guaranteed exhaustive. Historical matched Untapped popularity (last 30 days, ranks 10–79, Pool 3+, snapshots ~Oct 18–21 2026) shown for context; play percentages are not conditional played-card frequencies. As-of card statistics may differ if a newer patch subsequently changed a card: in particular, Anti-Polar Magneto appears **6/8** in Oct 18 last-30-days snapshot but later crawled pages reflect **6/9**; this analysis freezes at the historically matched snapshot **6/8** and marks that source drift. Independently verified current snapshots for Hulk, Hela, She-Hulk, Ultron, Orka, Doom. Other inherited printed stats and card pool membership remain subject to verification.

## Model

```
EP(card) = printed cost × mean(attributed power on occasions played) /
                          mean(attributed effective energy on occasions played)
```
All cards on this sheet have printed cost six. **No popularity inputs enter the computation.** "Average" values are **assumptions** until measured. Power includes a card's inherent body, realistically resolved ability outcome (space and location, where approximated), and allocated genuinely *joint* effects. Energy includes energy actually paid plus a Shapley-attributed share of useful resources truly sacrificed to realize its conditions. Do not penalize Hulk because an alternative six-energy play could add more power. A zero-energy play is permitted; division occurs only after averaging cost. We have not calculated true multiparty Shapley values from coalition game states; shares such as 50%, 55%, 60%, 65% are **scenario proxies**, not mathematical deductions. Do not share independent body power between cards without justification.

## Full ranking with explicit numerical assumptions

**Reading the table:** `P̄` = assumed mean power attributed to the card. `Ē` = assumed mean effective energy. The headline score is exactly `6 × P̄ / Ē` rounded to 0.1. `*` marks uncertain or conditional ratings. Risk labels `high`, `medium`, `low`, `structural` refer to **input/model confidence** (structural means total board power cannot adequately describe effect), *not* measured match-to-match variability. No percentiles or empirical confidence intervals were calculated.

| Rank | Card | Printed | EP estimate | Usage | P̄ | Ē | Numerical decomposition | Unmeasured assumptions / weakness | Risk |
|---:|---|---:|---:|---:|---:|---:|---|---|---|
| 1 | Ultron | 6/8 | **6/17*** | 1.9% | 17 | 6 | 8 body + 4.0 successful drones ×2 =8 + 1 allocated support bonus | Drones 4.0/play rather than 5.5; support bonus 1 rather than 2; both unmeasured | high |
| 2 | The Infinaut | 6/20 | **6/16.4*** | 3.9% | 20 | 7.3 | 20 body / 6 paid + 1.3 genuinely forgone-energy equivalents | T5 sacrificed-energy share guessed at 1.3; alternative cheats can differ | high |
| 3 | Giganto | 6/16 | **6/16*** | 3.1% | 16 | 6 | 16 body when successfully played left | Location restrictions reduce possibility of play; no verified conditional power reduction | medium |
| 4 | Orka | 6/11 | **6/15.6*** | 0.3% | 15.6 | 6 | 11 + 7×0.65 lone-lane trigger | 65% alone on actual plays, not 85%; unmeasured cost of leaving a lane unused not deducted | high |
| 5 | Sasquatch | 6/11 | **6/15.5*** | 10.9% | 11 | 4.3 | 11 body / 4.15 paid + 0.10 support-cost allocation | Discount cost distribution and Shapley support share unmeasured | high |
| 6 | Anti-Polar Magneto | 6/8 | **6/15.2*** | 5.5% | 15.2 | 6 | 8 body + 0.65 × 11 mean raw power from successfully summoned 3/4-cost cards | 11 successful added power is guessed, and 65% credited to Magneto is a Shapley *proxy*, not exact coalition value | high |
| 7 | Blob | 6/0 | **6/15*** | 1.6% | 15 | 6 | Assumed 15 combined absorbed power after effect | Mean merge output not observed; board modifiers and counters omitted | high |
| 8 | Hela | 6/6 | **6/14.1*** | 1.4% | 14.8 | 6.3 | 6 body + 0.55×16 successful restored power | 16 realized resurrected power and 55% Shapley allocation hypothetical; 0.3 useful sacrificed energy | high |
| 9 | She-Hulk | 6/10 | **6/14.1*** | 1.2% | 10 | 4.3 | 10 body / 3.85 mean energy paid + 0.40 attributed sacrifice | Paid-energy histogram and foregone-useful-energy distribution unmeasured | high |
| 10 | Destroyer | 6/18 | **6/14*** | 1.4% | 14 | 6 | 18 body minus 4 actual friendly power lost | Mean destroy-loss assumed; destroyed friendly effects may compensate | high |
| 11 | Emperor Hulkling | 6/12 | **6/14*** | 0.2% | 14 | 6 | 12 body + guessed +2 net from random six-cost effect | Random copied effect distribution unmeasured; ability may harm | high |
| 12 | Hulk | 6/14 | **6/14** | 5.4% | 14 | 6 | 14 printed body; no built-in ability | Verified baseline, excluding exceptional locations or external buffs | low |
| 13 | Mockingbird | 6/9 | **6/13.5*** | 2.1% | 9 | 4 | 9 body / 3.6 paid + 0.4 incremental creation setup | Mean discount and setup allocation guessed, including hand/deck constraints | high |
| 14 | Knull | 6/0 | **6/13.2*** | 9.0% | 13.2 | 6 | 0 body + 0.55 × 24 destroyed-power pool | 24 conditional destroyed Power and 55% Shapley credit both unmeasured; heavy tail | high |
| 15 | Leader | 6/5 | **6/13*** | 0.8% | 13 | 6 | 5 body + assumed 8 power of copied opponent plays | Opponent play-value distribution and copy success unmeasured | high |
| 16 | Odin | 6/10 | **6/13*** | 5.6% | 13 | 6 | 10 body + assumed half of 6 power gained by allied replay effects | Replay effectiveness and Shapley share unmeasured | high |
| 17 | Red Hulk | 6/10 | **6/13*** | 1.1% | 13 | 6 | 10 body plus single +3 accumulated trigger | Trigger count conditional on actual plays guessed | medium |
| 18 | Doctor Doom | 6/5 | **6/12.5*** | 2.9% | 12.5 | 6 | 5 body + 5×1.5 mean successful DoomBots | Illustration: 55% two /40% one /5% zero; not observed; location effect omissions | high |
| 19 | Galactus First Steps | 6/11 | **6/12.5*** | 1.2% | 12.5 | 6 | 11 body + assumed 1.5 attributed +2 interactions | Number/timing of gains and allocation uncertain | high |
| 20 | Apocalypse | 6/10 | **6/12.1*** | 3.1% | 12.5 | 6.2 | 10 body + 0.50×5.8 assumed discard growth | Average discard growth and half-credit modeled; 0.2 useful setup energy | high |
| 21 | Agatha Harkness | 6/12 | **6/12*** | 0.3% | 12 | 6 | 12 body; auto-play impairment omitted by stated EP target | Selection on being played and automation outside scope | structural |
| 22 | Helicarrier | 6/12 | **6/12*** | 0.3% | 12 | 6 | 12 body when played; discard benefit occurs in other games | Conditional-on-play may exclude primary use case | structural |
| 23 | Magneto | 6/12 | **6/12*** | 2.1% | 12 | 6 | 12 body, no extra total board power from relocation | Positional value not captured | structural |
| 24 | Sinister Six | 6/12 | **6/12*** | 0.7% | 12 | 6 | 12 added body; printed-cost normalization placeholder | Automatically added rather than normally played—conditional definition mismatch | structural |
| 25 | Thanos | 6/12 | **6/12*** | 2.2% | 12 | 6 | 12 body without game-start stone credit | Stones create independent game-start synergies, not captured here | structural |
| 26 | Vampire Enchantress | 6/7 | **6/12*** | 0.8% | 12 | 6 | 7 body + 2.5 successful steals ×2 swing | Steal count unmeasured | high |
| 27 | Eson | 6/10 | **6/11.5*** | 0.9% | 11.5 | 6 | 10 body + 0.5×3 added created-card power | On-turn addition probability and attribution guessed | high |
| 28 | Onslaught | 6/8 | **6/11*** | 3.6% | 11 | 6 | 8 body + half of estimated 6 ongoing bonus power | Existing ongoing buffs/location modifiers and coalition values unmeasured | high |
| 29 | Heimdall | 6/10 | **6/10*** | 1.2% | 10 | 6 | 10 body; repositions cards without adding total power | Metric undervalues positional shifts | structural |
| 30 | Spectrum | 6/7 | **6/10*** | 2.7% | 10 | 6 | 7 body + half of 6 power from 3 Ongoing allies | On-board Ongoing counts and shared credit guessed | high |
| 31 | Alioth | 6/7 | **6/9*** | 1.4% | 9 | 6 | 7 body + arbitrary 2 power-equivalent denied to opponent | Text denial rarely reducible to additive current board power; 2 guessed | structural |
| 32 | Aurora | 6/5 | **6/9*** | 0.7% | 9 | 6 | 5 body + half of 8 allied-trigger power | Trigger counts and allocations guessed | high |
| 33 | Gorr the God Butcher | 6/1 | **6/9*** | 4.8% | 9 | 6 | 1 body + two-thirds of +12 from 6 On Reveal allies | 6 active On Reveal cards and two-thirds attribution assumed; effect might have independent value | high |
| 34 | The Living Tribunal | 6/9 | **6/9*** | 1.7% | 9 | 6 | 9 body; total power conserved by split across lanes | Winning two lanes not captured by sum of all board power | structural |
| 35 | Scorpion Brand New Day | 6/6 | **6/8.5*** | 1.6% | 8.5 | 6 | 6 body + half of assumed 5 stacked earlier debuff power | Earlier debuffs and sharing unsupported | high |
| 36 | Arnim Zola | 6/0 | **6/8.4*** | 9.6% | 8.4 | 6 | 0 body + 60% of +14 net copied Power from 2 additions minus destroyed target | Target availability, locations, copied abilities and Shapley share guessed | high |
| 37 | Taskmaster | 6/0 | **6/7.8*** | 2.2% | 7.8 | 6 | 0 body + 60% of assumed 13 last-card copied Power | Previous-card strength, ability success and synergy credit guessed | high |
| 38 | Khonshu | 6/5 | **6/7.5*** | 1.3% | 7.5 | 6 | 5 body + 0.5×5 resurrected value | Phase-dependent action and resurrected value unmeasured | high |
| 39 | Galactus | 6/6 | **6/6*** | 2.9% | 6 | 6 | 6 body; destroyed locations not translated into power swing | Cannot compare fairly using total-power metric | structural |

## High-impact assumption audits

### Ultron: the old score was probably too optimistic

Earlier `P̄=8 + 5.5×2 + 2 =21`. This run uses `8 + 4×2 + 1 = 17`: **6/17**. These are not observed numbers. The number of drones actually fitting in the two other locations is constrained by the existing support bodies; the amount of bonus power from buffs may be correlated *negatively* with space available. With the same 1-point allocated bonus, **3 / 4 / 5 successful drones** yield **6/15 / 6/17 / 6/19**. What is needed: distribution of actual successful drones on Ultron plays, the rest of board's occupied spaces, and buff outcomes.

### Orka: activation likelihood is not the whole setup cost

Earlier probability of being alone was 85%, giving `11+7×0.85≈17`. This run uses 65%: `11+7×0.65=15.55`, rounded to **6/15.6**. Probability is **still guessed**. With 40%, 65%, 85%, results are **6/13.8**, **6/15.6**, **6/17** respectively. We have **not assigned a numerical opportunity cost to leaving a lane empty**; a principled Shapley analysis may include that lost option or other cards’ delayed play in attributed effective resource costs, but it cannot be equated to universally wasted energy.

### Anti-Polar Magneto: the previous assumed summons and mechanical 50/50 split were dubious

Use printed 6/8 in matched Oct 18 snapshot (flag source drift). We suppose the **successfully added** 3/4-cost cards together contribute **11 average resolved power** across plays, and assign **65%** of it to Magneto as a *temporary coalition approximation*: `8 + 0.65×11 = 15.15` -> **6/15.2**. At only 7 average summoned power the same approach yields 6/12.6; with 14 it yields 6/17.1. These aren't observed frequencies. Without Magneto, end-turn cards remaining in hand may never enter play; true Shapley credit could exceed this share. He can add 0, 1 or 2 cards depending on hand and slots. **Energy corresponding to the summoned cards is not magically created**, but their printed costs aren't automatically paid when they are added; this payoff must be reflected consistently in both power and energy attribution rather than automatically counting an extra 6–8 energy payment.

### Doom: placements, not a generic board-space tax

Current estimate 6/12.5 from `5 + 5×1.5 successful DoomBots`. One illustrative distribution is 55% both successful, 40% one successful, 5% neither. Earlier assumed 65%/30%/5% and 6/13. We have **no measured probabilities**. Under ordinary successful triggers a maximum of 6/15; location modifiers can change results.

### Hela, Knull and Arnim Zola: attribution still very uncertain

- Hela **6/14.1** approximately: `6×(6 + 55%×16) / 6.3`. Both *16 average resurrected power on actual plays* and the **55% Shapley proxy** are unmeasured. The actual Hela resurrection uses one discarded card for each **different cost**; available slots and random locations matter.
- Knull **6/13.2**: assume 24 destroyed power in games where played, credit 55% to Knull. Assumed mean power and credit fraction both unmeasured. High usage may reflect an effective destroy package or a mistaken coalition allocation, not necessarily stronger EP.
- Arnim Zola **6/8.4**: assume 14 net power from copies after target destruction, credit 60% to Zola. This implausibly low score versus prior ~9.6% observed popularity is a major **Shapley-proxy failure candidate**; splitting copied board bodies without considering that the target would otherwise remain on board is questionable. Do not accept the number as a credible measured EP.

### She-Hulk and Infinaut: average attributed ENERGY assumptions are biggest uncertainty

- She-Hulk **6/14.1**: mean paid cost 3.85 plus 0.40 incremental useful-energy sacrifice. The amount of preceding-turn unspent energy does not by itself equal sacrificed energy; Sunspot or no alternative play may reduce genuine sacrifice. Distribution is not observed.
- Infinaut **6/16.4**: 20 body / (6 actually paid + 1.3 attributable useful-energy sacrifice). The number is illustrative. Actual turn-5 available actions, Sunspot/She-Hulk coexistence and cheat-outs all shift cost.

## Explicit calibration discipline

1. Verify printed stats/text and recency (do **not** silently apply mismatched current- and past-patch card data).
2. Replace assumed scenario frequencies with **observed conditional-on-play distributions**: successful summons, open spaces, solo triggers, eligible discarded cards, energy paid, location modifiers.
3. Calculate real Shapley coalition power and energy if the interaction is a serious source of error. Arbitrary percentage shares are clearly labeled proxies.
4. Only then compare to independent popularity, ask whether lower-EP setup cards, delayed plays, meta constraints, selection effects or access account for discrepancies.
5. Retain warranted 6/12–19 outliers; no fake percentile ranges. Our intervals are sensitivity analyses only.
6. Structural failures (Galactus, Living Tribunal, Magneto, Heimdall, Sinister Six as an **added** card) remain flagged rather than given a falsely comparable board-power EP.

## Data sources

- https://snap.untapped.gg/en/meta/cards-tier-list
- https://snap.untapped.gg/en/meta/cards/ultron
- https://snap.untapped.gg/en/meta/cards/orka
- https://snap.untapped.gg/en/meta/cards/hela
- https://snap.untapped.gg/en/meta/cards/she-hulk
- https://snap.untapped.gg/en/meta/cards/dr-doom
- https://snap.untapped.gg/en/meta/cards/anti-polar-magneto?collectionLevel=pool3p&rankRange=10-70&timeFrame=Last30Days
- https://snap.fan/cards/Orka/Orka/
- Prior version: [SIX_COST_SHAPLEY_RERUN_V08.md](./SIX_COST_SHAPLEY_RERUN_V08.md)
