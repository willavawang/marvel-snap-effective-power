# Formula v0.6 — decisions for next six-cost run (2026-10-21)

Status: **methodology decision, provisional**, not empirical card ratings.

## Target

Estimate each card's *effective board-power-equivalent contribution on occasions it is played*, not its average cube outcome, deck inclusion rate, draw consistency, or power of alternate cards that might have been played. The six-cost baseline Hulk is **6/14** unmodified. Use asterisks for wide conditional distributions; attach a measured 10th–90th percentile range only if samples support it.

## Simplified common formula

```
EP(c) = printed_cost(c) × E[
    (location-adjusted direct power-equivalent change
     + attributed interaction bonus
     − realized future-slot obstruction)
    / (actual energy for c + incremental wasted energy forced by c's prerequisite)
    | c actually played
]
```

Do **not** subtract the hypothetical power of the best alternative play. The reference state removes card c and its direct effect but does not replace it with a hypothetical competing card. Where other actual future additions were impossible because c occupied a space, charge only the incremental obstruction not already accounted for in the direct power change (no double deduction). Fixed per-slot charges are prohibited.

## (1) Board space — accept constrained addition and true obstruction; reject universal slot fee

- Respect 4-card limits and location-specific limits when determining whether tokens/resurrections can be added; Doom 6/5 creates at most 5+5+5 ordinarily, but only 10 if one other location full, only 5 if both full.
- A filled square on the final normal turn usually has no future opportunity cost. Earlier turns or extended games may have genuine obstruction of future additions; charge measured/estimated *lost marginal power* only then.
- Potential positive interactions from board bodies are not a blanket body premium. Credit specific bonus outputs (e.g. Dazzler +2 if a new body completes a lane; Patriot +2 on ability-less DoomBot), and split the **extra** interaction bonus between participating cards at first approximation. Credit Doom himself with his normal DoomBot bodies. Do not award synergy bonus independently to both.
- **Important rules correction:** Elsa Bloodstone's text is 'Each card you play to fill your side of a location gains +2 Power'; DoomBots are **added** and not **played**, so they do not trigger Elsa.

## (2) Locations — accept scoring/effect modifications; reject an arbitrary location popularity multiplier

- For every play state, compute actual power changes using the three revealed locations (plus any relevant evolving location effects), slot restrictions, destruction/prevention and bonuses. Source locations from game states when available, otherwise a documented frequency-weighted set of illustrative archetypes.
- Examples: Space Throne restricts additions; Sanctum Sanctorum prevents play but not all ability-based adds; Sewer System reduces the added card's power; Shuri's Lab doubles cards played there; Nexus can propagate location power to other lanes; Bar With No Name rewards **less** power and needs signed/flagged treatment.
- Sample locations **conditional on the card being played**, not uniform over the full catalog. Location frequency, current featured/hot conditions, decks, board crowding and turn of play correlate.
- Preserve distinction between 'more displayed power' and 'more valuable power for winning'. No general overkill deduction or contested-lane weight at this stage. If an exceptional objective reverses the meaning of power, flag and sign as appropriate rather than silently scoring as ordinary +power.
- Doctor Doom should no longer be listed as universally 6/15; the prior 6/13 assumes arbitrary 85%/75% placement success and is not an evidence-based estimate.

## (3) Combo cost — recalibrate actual played outcomes; reject blanket combo tax

- Hela is 6/6. Current text: 'For each different Cost among them, resurrect a card you discarded to a random location.' A Hela-played sample must tally actually discarded **different-cost** cards, power returned, random placement, space availability, and location modifications. Formula: 6 + E[successful resurrected effective Power | Hela played] minus legitimate incremental setup waste and obstruction, if present.
- **A 6/22 Hela requires an average 16 restored power in the games where she was actually played. This is conceivable; neither verified nor ruled out.** Do not reduce to 6/14 solely because Hela's deck has 1.4% popularity; inclusion/draw/setup success affect deck viability, not the conditional average.
- A discard enabler's *entire energy* is not inherently wasted if that enabler supplies its own useful body/power. Do not charge Blade and Lady Sif wholesale to Hela. Charge **incremental foregone energy/power** only if forced by the combo beyond independently useful plays. Distinguish rarity of setup from sacrificed resources.
- Interactions that produce *extra* power beyond Hela's own resurrection mechanics should not be counted twice. For the quick pass, credit resurrection to Hela, and ability contributions of the discard enablers to those cards; flag any shared incremental boosts.
- Knull, Infinaut, Jubilee, She-Hulk, Sasquatch should all use the same resource accounting principle (only real wasted energy incurred to realize the card), avoiding special-case multipliers.

## Next implementation

1. For all 6-cost candidates, record printed card text/current stats, simple conditionally expected direct effects, board-space success and obstruction, location score adjustments, and incremental forced wasted energy.
2. Output one estimate `6/X`, an asterisk for highly variable cards, and explicit assumption/estimated percentile if backed by data.
3. Compare to usage. Treat biggest anomalies first as possible model failures, then investigate enabler costs, playable conditions, meta mismatch, and only finally true missed market opportunity.

## Sources

- https://snap.untapped.gg/en/meta/cards/dr-doom
- https://snap.untapped.gg/en/meta/cards/hela
- https://snap.untapped.gg/en/meta/cards/elsa-bloodstone
- https://snap.untapped.gg/en/meta/cards/patriot
- https://snap.untapped.gg/en/meta/cards/dazzler
- https://marvelsnap.helpshift.com/hc/en/3-marvel-snap/faq/42-what-are-the-differences-between-play-add-put-and-move-on-a-card-location-ability/
- https://marvelsnap.helpshift.com/hc/en/3-marvel-snap/faq/94-how-many-cards-can-i-play-in-each-location/
- https://marvelsnapcards.com/locations/
