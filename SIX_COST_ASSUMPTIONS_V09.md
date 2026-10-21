# Marvel Snap six-cost EP — v0.9 assumption-first rerun
**As of 2026-10-21. All 39 values are SCENARIO ESTIMATES, not observed card-on-play EP.** Older v0.8 comparison is historical. No complete match logs or full Shapley games have been computed. Cards flagged 'structural' are fundamentally underrepresented by raw board Power. This is **not a statistical empirical study**.

## Formula (unchanged from v0.8)

```text
EP(card) = printed cost × mean(Shapley-attributed realized Power | card played)
                           / mean(Shapley-attributed effective Energy | card played)
```

Every card here has printed cost 6, so EP = 6 × P_mean / E_mean. This is **ratio of means**, not mean of ratios. On any individual zero-cost play, the aggregate mean energy denominator remains valid. For ordinary cards, E_mean=6. Actual paid energy and *genuinely useful sacrificed* energy are allocated fairly among the combo participants. Energy that would have been unused anyway is not a sacrifice. Do not count the same energy gain or same shared incremental Power twice. Locations and lane capacity enter the card's *actual successful outcome frequency*, not a universal subtraction.

## Assumption discipline

- **Checked facts:** printed card numbers and text can be checked against current SNAP.FAN changelog / Untapped card pages, but the **39-card candidate pool is not claimed independently exhaustive**.
- **Observed comparator:** previous pass's Untapped *deck/card popularity*, approximate **last 30 days, ranks 10–79, Pool 3+**, mainly Oct 18–21, 2026; estimates of inclusion, NOT power when played. Data can shift as windows advance. Those percentages are **not used to calculate EP**.
- **Assumed conditional frequencies:** slot occupancy, unique combo pieces available, successful activations, mean discounts, destroyed/resurrected Power, location modifiers. Every such numerical assumption is printed by each row; none is based on game-level samples.
- **Assumed coalition attribution:** numbers like “50%, 72%, 75%, 80%” are sensitivity parameters, **NOT computed Shapley values**. True Shapley is a weighted average of a card's incremental contribution across combinations with and without other cards. Splitting every combo 50/50 is not a general Shapley solution.
- **Calibration prior:** We expect many competitive 6-costs roughly **6/12–19**, but this is neither a mathematical rule nor a tuning target. Ratings outside this interval are retained if assumptions make them plausible. Likewise, popularity disagreements are **investigation prompts**, not fitting targets.
- **Ranges:** Asterisks flag volatile or assumption-sensitive scores. We **cannot claim observed percentile ranges** without sampled power/energy distributions. Any sensitivity range below is an alternative scenario range, not a sampling interval.

## Full 39-card table — assumptions exposed

| Rank | Card | Printed | EP v0.9 | v0.8 | Observed popularity | Mean allocated Power P | Mean allocated Energy E | Card-specific assumption (not measured) |
|---:|---|---:|---:|---:|---:|---:|---:|---|
| 1 | The Infinaut | 6/20 | **6/16.4*** | 6/16.4 | 3.9% | 20 | 7.3 | 20 body; 6 paid + 1.3 useful Energy sacrificed in turn-5 skip, after other uses; **1.3 assumed**. |
| 2 | Giganto | 6/16 | **6/16*** | 6/16 | 3.1% | 16 | 6 | 16 body on successful left-lane play; location restriction affects plays possible, not conditional body. |
| 3 | Ultron | 6/8 | **6/16*** | 6/21 | 1.9% | 16 | 6 | 8 body + 3.5 successfully placed 2-Power drones (=7) + 1 shared support Power; **3.5 slots assumed**, not measured. |
| 4 | Orka | 6/11 | **6/15.6*** | 6/17 | 0.3% | 15.6 | 6 | 11 body + 7×65% lone-lane activation. **65% assumed**; positional sacrifice is unmeasured and not deducted. |
| 5 | Sasquatch | 6/11 | **6/15.5*** | 6/15.5 | 10.9% | 11 | 4.3 | 11 body; **4.15 mean paid** after prior-turn card-count reduction + **0.10 genuinely sacrificed** setup Energy, both assumed. |
| 6 | Anti-Polar Magneto | 6/8 | **6/15.4*** | 6/11.5 | 5.5% | 15.4 | 6 | 8 body + **1.65** expected successful summons × **6** mean Power each × **75%** payoff attribution ≈15.4; 1.65, 6, 75% all UNMEASURED; hand/slot restrictions matter. |
| 7 | Blob | 6/0 | **6/15*** | 6/15 | 1.6% | 15 | 6 | Assume 15 accumulated deck-absorption Power by the time played; not measured. |
| 8 | Leader | 6/5 | **6/15*** | 6/15 | 0.8% | 15 | 6 | 5 body + assumed 10 copied opposing Power; opponent is not Shapley ally, and copy success varies. |
| 9 | Hela | 6/6 | **6/14.6*** | 6/14.3 | 1.4% | 15.4 | 6.3 | 6 body + **17** successfully revived Power × **55%** Shapley payoff attribution; 0.3 genuine setup-cost Energy, all assumed. |
| 10 | Knull | 6/0 | **6/14.4*** | 6/11 | 9.0% | 14.4 | 6 | **20** destroyed-power pool × **72%** attributed to Knull rather than destroy engine. Both pool and fraction unmeasured. |
| 11 | She-Hulk | 6/10 | **6/14.1*** | 6/14.1 | 1.2% | 10 | 4.3 | 10 body; assumed 3.85 mean paid +0.40 Shapley-allocated meaningful earlier wasted Energy; no divide-by-zero. |
| 12 | Destroyer | 6/18 | **6/14*** | 6/14 | 1.4% | 14 | 6 | 18 body − assumed net 4 friendly Power loss; destroy triggers could reduce loss or benefit. |
| 13 | Emperor Hulkling | 6/12 | **6/14*** | 6/14 | 0.2% | 14 | 6 | 12 body + assumed 2 net Power from random copied text; very uncertain. |
| 14 | Hulk | 6/14 | **6/14** | 6/14 | 5.4% | 14 | 6 | 14 unmodified body, anchor; location changes ignored only in this baseline. |
| 15 | Mockingbird | 6/9 | **6/13.5*** | 6/13.5 | 2.1% | 9 | 4 | 9 body; assumed 3.6 paid +0.4 co-attributed setup resource due to created cards. |
| 16 | Doctor Doom | 6/5 | **6/13*** | 6/13 | 2.9% | 13 | 6 | 5 body; assume 2/1/0 successful 5-Power bots in **65%/30%/5%** of played cases; needs observed slot data. |
| 17 | Odin | 6/10 | **6/13*** | 6/13 | 5.6% | 13 | 6 | 10 body + 6 assumed total allied On Reveal extra Power ×50% Shapley allocation. |
| 18 | Red Hulk | 6/10 | **6/13*** | 6/13 | 1.1% | 13 | 6 | 10 body + one assumed +3 trigger before play. |
| 19 | Galactus First Steps | 6/11 | **6/12.5*** | 6/12.5 | 1.2% | 12.5 | 6 | 11 body + 3 estimated Herald-synergy Power ×50% split. |
| 20 | Apocalypse | 6/10 | **6/12.2*** | 6/12.6 | 3.1% | 12.6 | 6.2 | 10 body + (1.5 discard triggers×4 boost)×50% payoff attribution; +0.2 incremental setup Energy. |
| 21 | Agatha Harkness | 6/12 | **6/12*** | 6/12 | 0.3% | 12 | 6 | 12 body; strategic autopilot cost lies outside board-Power EP. |
| 22 | Arnim Zola | 6/0 | **6/12*** | 6/7 | 9.6% | 12 | 6 | Assumed net +15 Power from one destroyed source and two copies after slots, ×80% marginal attribution to Zola. 15 and 80% unmeasured. |
| 23 | Helicarrier | 6/12 | **6/12*** | 6/12 | 0.3% | 12 | 6 | 12 body when played; discard-hand benefit happens when discarded, excluded under played-only convention. |
| 24 | Magneto | 6/12 | **6/12*** | 6/12 | 2.1% | 12 | 6 | 12 body; enemy repositioning changes lane outcomes, not global additive Power. |
| 25 | Sinister Six | 6/12 | **6/12*** | 6/12 | 0.7% | 12 | 6 | 12 body, but usually added by marked-card condition, not played; 6-energy normalization is only a placeholder. |
| 26 | Thanos | 6/12 | **6/12*** | 6/12 | 2.2% | 12 | 6 | 12 body; stones/game-start effect not Shapley-valued under narrow 'played' condition. |
| 27 | Vampire Enchantress | 6/7 | **6/12*** | 6/12 | 0.8% | 12 | 6 | 7 body + assumed 2.5 Power stolen, ×2 for two-sided relative Power swing. |
| 28 | Eson | 6/10 | **6/11.5*** | 6/11.5 | 0.9% | 11.5 | 6 | 10 body + 3 expected created-card Power ×50% joint attribution. |
| 29 | Onslaught | 6/8 | **6/11*** | 6/11 | 3.6% | 11 | 6 | 8 body + 6 incremental allied Ongoing Power ×50% joint split; independent contributions need coalition test. |
| 30 | Taskmaster | 6/0 | **6/10.4*** | 6/6.5 | 2.2% | 10.4 | 6 | Assume 13 copied Power ×80% attribution to copying mechanism; prior card body retains its independent value. |
| 31 | Heimdall | 6/10 | **6/10*** | 6/10 | 1.2% | 10 | 6 | 10 body; shifting existing Power among lanes is not additive board Power. |
| 32 | Spectrum | 6/7 | **6/10*** | 6/10 | 2.7% | 10 | 6 | 7 body + 6 Ongoing buffs ×50% synergy allocation. |
| 33 | Alioth | 6/7 | **6/9*** | 6/9 | 1.4% | 9 | 6 | 7 body + 2 assumed directly preventable opposing Power; preventing card text often non-additive. |
| 34 | Aurora | 6/5 | **6/9*** | 6/9 | 0.7% | 9 | 6 | 5 body + assumed 8 synergistic trigger Power ×50% attribution. |
| 35 | Gorr the God Butcher | 6/1 | **6/9*** | 6/7 | 4.8% | 9 | 6 | 1 body + 12 boost from six allied On Reveal cards × 2/3 payoff attribution; 6 and split unmeasured. |
| 36 | The Living Tribunal | 6/9 | **6/9*** | 6/9 | 1.7% | 9 | 6 | 9 body; redistribution not additive Power; EP intentionally misses strategic value. |
| 37 | Scorpion Brand New Day | 6/6 | **6/8.5*** | 6/8.5 | 1.6% | 8.5 | 6 | 6 body + assumed 5 extra opponent reductions ×50% Shapley sharing with debuff enablers. |
| 38 | Khonshu | 6/5 | **6/7.5*** | 6/7.5 | 1.3% | 7.5 | 6 | 5 body + 5 revived Power ×50% pairing; other phase cases not modeled. |
| 39 | Galactus | 6/6 | **6/6*** | 6/6 | 2.9% | 6 | 6 | 6 body. Eliminating locations fundamentally changes win condition; ranking not strategically comparable. |

## Major updates and how the estimates were constructed

### Ultron — revise 6/21 to 6/16
Direct 8 Power plus the assumed average of **3.5 actually placed** 2-Power Drones (=7), plus **1** Shapley-allocated extra support Power = **16**. We formerly assumed **5.5 drones** and **2** support Power. Both drone counts are guesses. A support-heavy deck simultaneously supplies buffs *and occupies drone slots*; outcome averages should model those jointly. At 2/3.5/5 placed drones, holding the 1 extra synergy Power fixed, he would be 6/13, 6/16, 6/19. **These are not confidence intervals.** Need actual open-slot distribution of Ultron games.

### Orka — revise 6/17 to 6/15.6
11 printed plus 7 bonus times **65%** success (previously 85%). This probability is illustrative; the cost of keeping an entire lane free remains **unmeasured**, and could warrant attribution to Orka through the same resource framework used for She-Hulk. At 40% / 65% / 85% success, EP is 6/13.8 / 6/15.6 / 6/17, excluding any placement cost.

### Anti-Polar Magneto — revise 6/11.5 to 6/15.4
8 body + **1.65** successfully added cards per play × **6 Power** per successful added card × **75%** of the incremental effect attributed to Magneto = 15.425. This explicitly counts **only the incremental summons that actually happen**, not all two automatically. Unlike the previous pass, the model no longer automatically halves an arbitrarily tiny 7-power total. These numbers are **assumed**, not observed. Outcomes with zero/one/two summons, availability of 3/4-cost cards in hand, other-lane open slots and triggered abilities must be measured. Note the 6–8 **printed Energy cost** of two 3/4-cost cards is NOT itself six to eight Power: saved Energy has to be reflected consistently in attribution, not added as phantom Power. With 1.0/1.65/2.0 successful summons, all else equal, EP would be 6/12.5 / 6/15.4 / 6/17.

### Hela — 6/14.6 (formerly 6/14.3)
6 printed + 17 assumed successfully revived Power ×55% hypothetical payoff share = 15.35 attributed Power; 6.3 allocated Energy. Full-Shapley shares are uncomputed. **The estimate is uncertain, not evidence that Hela actually revives 17 Power.**

### Knull — 6/14.4 (formerly 6/11)
Assume 20 destroyed Power available when played, 72% credited to Knull rather than destroy enablers. We increased the notional share because a card that converts ordinary destruction into a large body may have high marginal contribution even when destruction occurs independently. Both assumptions need coalition analysis. With the same 20 pool, 50%/72%/90% allocation gives **6/10 / 6/14.4 / 6/18**, before location changes.

### Arnim Zola — 6/12 (formerly 6/7)
Assume ~15 net Power from destroying one ally and successfully creating up to two copies after board restrictions. Attribute 80% of that incremental outcome to Zola, rather than mechanically splitting it in half; the copied source's independent preexisting board Power stays credited to itself. **Important:** whether 80% is consistent with the true Shapley characteristic function is unresolved. If target Power, copy slots and other card effects differ, the score changes substantially.

### She-Hulk — 6/14.1, no numerical change
10 Power, **3.85 average actual Energy paid** plus **0.40** Shapley-attributed useful Energy forgone on previous turn, producing 6×10/4.25 = 14.1. Explicitly a scenario; no measured cost histogram.

## Most informative discrepancies remaining

- **Ultron (6/16; ~1.9% use)**: conditional Power no longer wildly above 6/19, but no direct gameplay-slot evidence yet; weak inclusion can result from board design and enabler cards' efficiency.
- **Orka (6/15.6; ~0.3%)**: score now assumes less reliable lone-lane play; placement costs could lower score, but rare inclusion does not automatically disprove conditional EP.
- **Anti-Polar Magneto (6/15.4; ~5.5%)**: now looks more coherent, but estimated summoned-card Power/attribution remains weakly sourced.
- **Knull (6/14.4; ~9.0%) and Arnim Zola (6/12; ~9.6%)**: observed usage suggests taking their joint-effect modeling seriously. It is **not proof** the new allocation percentages are correct.
- **Galactus (6/6), Living Tribunal (6/9), Magneto (6/12), Heimdall (6/10)**: these are structural counterexamples to *global raw Power as a complete measure of strategic worth*; do not force-fit them to 6/12–19.
- **Hela (6/14.6; ~1.4%)**: combo setup and conditional power sampling remain unmeasured; poor inclusion cannot alone settle the Shapley output.

## Data that would actually improve the scores

For each *played instance*, capture real Power before/after effects, actual energy paid, useful foregone Energy (or documented proxy), location state and open slots, other enabling cards, targets summoned/destroyed/revived, and canceled/blocked effects. Report **sample size** and **measured 10th–90th percentile range** only when available. For interaction-heavy examples, evaluate meaningful coalitions (e.g. M alone, individual 3/4-cost card alone, combined, all together), not arbitrary percentage allocations.

### Sources
- https://snap.fan/changelog/ (as of October 15, 2026 balance changes)
- https://snap.untapped.gg/en/meta/cards/ultron (current 6/8 with 2-Power Drones; usage ~2.0%)
- https://snap.untapped.gg/en/meta/cards/orka (6/11, +7 when alone; usage ~0.3%)
- https://snap.untapped.gg/en/meta/cards/anti-polar-magneto (6/8, summon effect; ~5.7% usage)
- https://snap.fan/cards/AntiPolarMagneto/
- Earlier provisional tables: [v0.8](./SIX_COST_SHAPLEY_RERUN_V08.md), [original quick pass](./SIX_COST_QUICK_PASS_2026-10-21.md)

**Reminder:** this is an assumption-transparent thought experiment, not a statistically inferred ranking or an independently complete census of printed six-cost cards.