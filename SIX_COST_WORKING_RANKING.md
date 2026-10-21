# Six-cost Effective Power — working estimates v0.1

**2026-10-21. Model estimates, not observed match statistics.** Card pool and patch state are still being audited; this is an initial ranking of identified six-cost cards, **not yet certified exhaustive**. Cards with changed printed costs or unreleased variants must be corrected before the final all-card table.

## Uniform scoring rule

EP = printed power + expected direct power-equivalent effect when played, adjusted by printed cost / effective energy investment **only where extra required energy/turn sacrifice or discount can be estimated**. Do not penalize for better alternative cards, overall deck competitiveness, opponent retreats, card-draw frequency, or hypothetical resource allocations across unrelated cards. Summons add their power; direct enemy power reduction adds equivalent power swing; ongoing boosts count incremental resulting power. Card combos are credited provisionally to the payoff card, pending synergy attribution. `*` means outcome varies strongly by game. **Every decimal below is an explicit subjective working assumption, not an empirical mean.** No invented percentile ranges.

## Working six-cost ranking

| Card | EP (6 / X) | Reason / assumed scenario |
|---|---:|---|
| Hela* | 6/24 | 6 printed + assumed 18 net resurrection power after board-space constraints; high variance |
| Knull* | 6/22 | Assumed 22 total destroyed power at time of play; highly skewed |
| Ultron* | 6/20 | Assumed 12 incremental drone power plus body and common capacity/boost effects; verify current card text |
| Arnim Zola* | 6/20 | Assumed copied bodies add ~20 after original destroyed; high variance, support-dependent |
| The Living Tribunal* | 6/18 | Illustrative 18 power-equivalent contribution from distribution effect; *not physically created power*, methodological exception |
| Doctor Doom | 6/15 | 5 body + two 5-power bots, if both slots open; may be lower with congestion |
| Anti-Polar Magneto* | 6/14 | 8 body + 6 attributed power from summoning two 3/4-cost cards, with shared credit unresolved |
| Apocalypse* | 6/14 | 10 body + one assumed discard (+4) |
| Gorr the God Butcher* | 6/13 | 1 + 2×6 assumed On Reveals in play |
| Magneto* | 6/13 | Provisional: printed body + positional effect; requires current stat check |
| Red Hulk* | 6/13 | Provisional: body plus typical gained power; requires current stat check |
| Hulk | 6/14 | Verified current printed-power baseline (buffed Dec 19, 2025) |
| Sasquatch* | 6/11 | 11 printed; discounted energy does not automatically create power |
| She-Hulk* | 6/10 | 10 printed; discount affects energy efficiency, not physical power; current stat needs verification |
| Onslaught* | 6/10 | 8 body + modest assumed incremental Ongoing power; often much higher in synergy decks |
| Odin* | 6/10 | 9 body + 1 conservative incremental On Reveal credit; ability highly deck-dependent |
| Infinaut* | 6/10.9 | 20×6/(6+5), assuming all five T5 energy equivalents sacrificed; deliberately conservative and likely underestimates actual EP |
| Heimdall* | 6/10 | Provisional printed body plus small movement contribution; positional benefit not directly power |
| Spectrum* | 6/10 | Provisional body + boosted Ongoing cards; verify current printed stats |
| Galactus* | 6/10 | Provisional body + board destruction swing, highly dependent on location/conditions; not yet stable |
| Destroyer* | 6/10 | Provisional body minus friendly destroyed power; may improve when destruction is beneficial |
| Leader* | 6/9 | Provisional body + copied opposing play; needs current text/stats and observed opponent plays |
| Khonshu* | 6/10 | Phase-conditional resurrection; model not yet calibrated |
| Aurora* | 6/9 | 5 body + modest ability triggers, needs synergy data |
| Scorpion — Brand New Day* | 6/8 | 6 body + assumed doubled enemy debuffs |
| Vampire Enchantress* | 6/9 | 7 body + ~2 transferred power-equivalent; each steal swings two points if both sides count |
| Doctor Doom — Doomsday* | 6/8 | 6 body + conservative 2 copied-effect credit; release status to confirm |
| Hulk — Avengers* | 6/13 | 11 body + assumed 1 other Avenger here ×2 |
| Sinister Six* | 6/12 | 12 body; game-start requirement makes deployment exceptional, not yet quantified |
| Sir Percy Black Knight* | 6/9 | 9 body; discounts not yet normalized |
| The Grand Design* | 6/10 | 0 body + two +5 boosts, conditional on targets; release status to confirm |

**Warning:** Several rows are provisional and may reflect cards not in the currently released standard playable pool. They are *candidate rows*, not final verified current cards. Likewise, this is not a claim that all six-cost cards have been enumerated. Verify source card texts and playable status before using as a published ranking.

## Immediate lessons

- A high EP is not automatically a high win rate or inclusion rate.
- The simple approach handles Hulk, Doom and many additive power abilities.
- Knull and Hela need real played-game samples for defensible means and 10th–90th percentiles.
- Effects such as Living Tribunal and Galactus are not straightforward physical power; leave an asterisk rather than pretending precision.
- Infinaut's 10.9 is entirely driven by a strong skip-cost assumption. Revisit after comparing realistic skipped-turn output.
- The pilot's temporary full-credit treatment of summons/copies can overattribute power to payoffs; revisit only when rankings look implausible.

## Sources for checking patch/card definitions

- https://snap.fan/cards/history/2026/
- https://snap.fan/changelog/
- https://snap.fan/cards/

## Correction — October 21, 2026

Hulk is **6/14**, not 6/12, confirmed by Marvel Snap Zone (last changed December 19, 2025): https://marvelsnapzone.com/cards/hulk/ . Treat 6/14 as the current vanilla benchmark. The earlier six-cost pilot and research log use the outdated 6/12 figure and should be read with this correction. Doctor Doom's 6/15 is a maximum in ordinary open locations, not an average; provisional location-adjusted estimate 6/13 assumes bot placement probabilities of 85% and 75%, **not measured**.
