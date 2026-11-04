# EV Advisory brand intro: scorecard, 2026-11-04

Five build rounds. After each round an independent reviewer, who had not built it and had not read the builder's notes, scored fresh frames from both cuts (16x9 master, 9x16 variant, plus a 390 px phone crop). Scores run 1 to 10, strict: 8 is shippable and distinctive, a generic consultancy intro is 5. AI slop is scored so that 10 means no slop.

## Final verdict: round 5 ships, every score is 8 or higher

| Axis | Round 1 | Round 2 | Round 3 | Round 4 | Round 5 (final) |
|---|---|---|---|---|---|
| Hierarchy | 6 | 7 | 8 | 8 | 8 |
| Type | 5 | 7 | 7 | 7 | 8 |
| Colour | 7 | 7 | 8 | 8 | 8 |
| Motion timing | 5 | 7 | 7 | 8 | 8 |
| Brand fit | 6 | 7 | 8 | 8 | 8 |
| AI slop (10 = none) | 6 | 6 | 7 | 8 | 8 |
| Mean | 5.83 | 6.83 | 7.50 | 7.83 | 8.00 |

The starting point (the intro as it stood before this work) scored a mean of 5.2 on a single reviewer's pass, so it is shown here for context only and is not on the same footing as the five independent rounds.

## What moved the scores

- Round 1 to 2: removed a stray dot, the empty placeholder circle and the looping ring. Cut the dead hold and fixed a leftover mark on the last frame. Set the wordmark and byline in Geist only.
- Round 3: kept the terracotta wave at full strength through the hold so the before-to-after step is the idea. Rebalanced both ratios and kept the 9x16 rule inside the platform safe width.
- Round 4: one wave settle, a single crisp end dot (the doubled dot came from motion blur on the tip), only the baseline hairline left, and the glow banding removed.
- Round 5: "EV" set heavier than "Advisory" with a softer ink on "Advisory", measured at stem width (1.53 times, up from 1.23 times) so it reads on a phone. The 9x16 wordmark now sits on the riser. The closing settle is twice as large and lands on the same beat as the end dot.

## Accepted tradeoff

In 9x16 the wave is about 19 percent of the width, not 30 percent. A 30 percent wave would shrink the name to about 86 px, which costs more on a phone feed than it gains. The reviewer accepted this.

## Known minor defects (none block the ship verdict)

1. 9x16 side margins are unequal and the byline sits about 25 px right of the "EV" edge.
2. 16x9 text starts a little right of the riser.
3. A lone grey "EV" shows for about 0.2 s before "Advisory" starts, between 1.2 and 1.8 s.

## Checks

- Frame check: PASS on both cuts (no blank frames, no dead stretch, no teleport, margins clear). 4.8 s, 60 fps master.
- Frame score (engine script, Geist font): PASS on all six metrics, both cuts.
- Engine tests: 572 of 572 pass.
- Design detector: exit 0 on the scene and the engine files (it only pattern matches source text, so it can undercount).

## Files in this folder

- intro.mp4 (1920 x 1080 master)
- intro-9x16.mp4 (1080 x 1920 variant)
- contact-sheet.png
- before-after.png (top row: before, bottom row: final)
- scorecard.md
