# Study System — Reference

Use this for Mode 2 (study plans, progress checks, "what should I practice"). Always establish
these five numbers first — ask once, briefly, if missing:

1. Current vocabulary size (rough word count)
2. Current CEFR level (self-assessed or estimated from samples)
3. Target CEFR level
4. Deadline
5. Realistic daily time budget

Everything below scales against these five numbers. Don't give generic advice without them.

## Reality-check math

Rule of thumb: reaching the next full CEFR level from a stable starting point takes on the order of
150-250 hours of dedicated study (varies by source/method; treat as an order-of-magnitude estimate,
not a guarantee). Two levels (e.g. A2→B2) is roughly double that. Divide by the number of days until
the deadline to get the required daily hours. If that number is unrealistic given the stated time
budget, **say so plainly** and offer the honest trade-off (extend the deadline, lower the target
level, or accept the tight schedule with no slack) rather than producing an aspirational plan the
learner can't sustain. A correct discouraging answer is more useful than an encouraging wrong one.

## The Three Listen Rule — correct scope

The rule: listen to the same short audio **three times**, each pass with a different job:
1. Pass 1 — no text, get the gist
2. Pass 2 — no text, catch detail, mark exactly where comprehension breaks down
3. Pass 3 — with text, reconcile sound to spelling
(Optionally a 4th pass: shadow/read aloud to convert input into output.)

**This is an intensive-listening technique, not an extensive-listening one.** Two failure modes to
actively prevent:

- **Applying it to too-long material.** If a learner tries to run this on a 20+ minute episode,
  the technique either gets abandoned (too much effort) or done superficially (not really three full
  passes). Recommend short segments — **2-4 minutes** for a beginner-intermediate learner — so the
  full three-pass cycle fits in about 15 minutes. Long material should be *trimmed* to a segment, not
  processed whole.
- **Letting it eat the extensive-listening time budget.** A learner who needs to build up total
  listening-minutes-per-day (a distinct, volume-based goal) will not get there by only doing
  intensive 3x-repeat listening — the same minutes covers 1/3 the material. Keep the two goals on
  separate time allocations (see Daily Engine below); don't let one crowd out the other.

**Difficulty gate**: only run this on material where the learner can already understand roughly
70-90% on a first pass (i+1). If first-pass comprehension is well below that, the technique won't
rescue it — recommend easier material instead of more repetition.

**Frequency vs. depth trade-off**: if the learner feels a low session count (e.g. "1-2 long pieces a
month") is too infrequent, the fix is almost always to **shrink the segment length**, not to increase
how fast a helper (human or AI) can produce deep breakdowns. A daily 2-4 minute micro-segment,
self-processed with a lightweight breakdown (see below), scales to daily practice in a way that
outsourcing full 60-80-sentence breakdowns to someone else never will.

## The Daily Engine

A fixed daily rotation, budget-scaled. Example for a ~2.5 hr/day budget (scale proportionally for
other budgets, but never drop vocabulary or micro-listening below a functional minimum — see the
triage order at the end):

| Block | Time | What |
| --- | --- | --- |
| ① Vocabulary SRS | ~40 min | Spaced repetition (Anki or similar). New cards drawn first from that day's listening material (has context), then from a frequency list, then from words the learner needed while writing but didn't have. **Cards should be full sentences, not isolated words** — isolated words train recognition only, not production. |
| ② Micro-listening | ~15 min | One 2-4 min segment, full Three Listen Rule cycle. The comprehension breakdowns marked in Pass 2 are the most valuable data point — log them in a running breakdown log; review weekly. They usually cluster into: dropped `ne`, liaison/elision, or genuine vocabulary gaps (→ feed straight into the SRS deck). If a learner is using English as a bridge, do the French-only restatement checkpoint here too, before moving on. |
| ③ Self-breakdown | ~15 min | After Pass 3, the learner picks the 2-3 hardest sentences in the segment and answers 5 fixed questions themselves (see below) rather than waiting for an external breakdown. Any lookalike-but-different French/English word pairs go straight into the running faux-amis log. |
| ④ Extensive listening | 30-45 min | Different material, understood at ~70-80% on first pass, listened once or twice, no dissection. Purely for volume and ear training. Can be semi-passive (background) but should include focused listening several times a week too. |
| ⑤ Output (speak + write) | ~30 min | Shadow-read the day's segment aloud; free retell it *in French only* without the text (this is the restatement checkpoint applied at day-scale); then write (journal or similar), deliberately reusing 1-2 structures learned that day. Self-check against the learner's known recurring error types before finishing. |

### The 5 self-breakdown questions (Block ③)

Give the learner this fixed checklist instead of a full six-part breakdown, so they can process
material daily without waiting on an external source:

1. Any unknown words? → look them up, add the full sentence to the SRS deck.
2. What tense is the verb, and why that one?
3. Any pronouns (le/la/lui/y/en)? What do they replace?
4. What preposition follows the verb (+à / +de / none)?
5. Why this article (le/du/de/des)?
6. Does anything here look like an English word but mean something different? → add to the
   faux-amis log.

Tune the fixed list to the learner's own known recurring errors if those are known (e.g. from past
writing corrections) — the point is that the questions target their specific gaps, not a generic
checklist.

## Back-translation (listening → writing bridge)

A high-leverage technique when time is tight, because it converts listening material directly into
measured writing practice. Uses English as the intermediate language, consistent with this learner's
bridge — this also doubles as calque-detection, since translating into English and back tends to
surface exactly the places where the learner would copy English structure onto French (see the
divergence-flagging in `sentence-breakdown-format.md`):

1. Day 1: take that day's (or a recent) listening segment's French transcript, translate it into
   English, keep only the English.
2. A few days later (spacing matters — not the same day): translate the English back into French
   without looking at the original.
3. Compare against the original French line by line. The differences are the learner's *actual*,
   measured capability gap — not a guess. Simpler-than-original phrasing = correct but clunky (fluency
   gap); wrong phrasing = a real grammar/vocabulary gap; **English sentence structure copied wholesale
   into the French** = a calque error, and the highest-priority category to flag, since it's the
   specific failure mode this bridge method risks. Feed all three into the SRS deck, tagging calque
   errors distinctly so they can be reviewed as their own category.

Cadence: 1-2x per week, ~20 min each, is enough — don't let it crowd out the daily engine.

## Grammar: two tracks, not one

Extraction-based grammar notes (from Mode 1 breakdowns) are necessarily **random** — whatever the
material happens to contain. That's fine for depth but insufficient for coverage. Run a **systematic
track in parallel**:

Ordered curriculum (adjust pacing to the deadline math above; this is priority order, not a fixed
week count):
1. Passé composé vs. imparfait (the single highest-value pair for narrating anything)
2. Object pronouns (le/la/les/lui/leur) and their ordering
3. Pronominal adverbs y / en
4. Futur simple + the three conditional-sentence types (si + present, si + imparfait, si +
   plus-que-parfait) — flag the common error of using futur after si
5. Relative pronouns qui/que/dont/où
6. Conditionnel (present and past) — hypotheticals and regret
7. Subjonctif — trigger list first (falloir que, vouloir que, bien que, avant que...), production
   later
8. Passive voice + impersonal constructions (il faut, il y a, il fait)
9. Review and gap-filling

Require the learner to **actively use** each newly-studied point in that week's writing output
(Block ⑤) — passive recognition from grammar study alone doesn't transfer to production.

## Material tiers (extensive listening, Block ④)

| Tier | What | Purpose |
| --- | --- | --- |
| Staple | Didactic podcasts at or just above current level (slow, repetitive, built for learners) | Bulk of listening-minutes; should be comfortable at 70-90% first-pass comprehension |
| Bridge | Content deliberately slowed/simplified for learners but using natural vocabulary and topics (e.g. "authentic-adjacent" learner podcasts) | Closes the gap before jumping to fully authentic material |
| Stretch | Fully authentic native content (vlogs, native podcasts, interviews), ideally with full transcripts available | Where real-speed comprehension, elision, and register actually get trained; used sparingly and always with a transcript as scaffolding until upgrade |

**Upgrade test**: take a *new* (never-heard) piece at the current tier; if first-pass comprehension
(no transcript) is reliably ≥70%, move up a tier. Don't upgrade based on comprehension of material
already heard multiple times — that measures memory, not improved listening ability.

## Weekly rhythm

- Mon-Fri: full daily engine
- Saturday: one longer intensive session (8-10 min segment, full pipeline including
  back-translation)
- Sunday: review — go back through the week's breakdown log and faux-amis log, rewrite one of the
  week's journal entries incorporating corrections, top up the SRS deck with any backlog

## Monthly checkpoint

Concrete, falsifiable thresholds beat vague progress checks. Example structure (calibrate numbers
to the specific deadline math):

| Check | Threshold |
| --- | --- |
| Vocabulary size | target number by this date |
| First-pass comprehension on new same-tier material | ≥ 70% |
| Unassisted writing (~150 words) | error rate below X per 100 words, specifically on the learner's known recurring error types |

If any metric misses, **reallocate time toward it and away from others** rather than spreading effort
evenly — evenly-spread effort under a hard deadline usually means every metric arrives slightly short.

## Triage order when time is short

State this explicitly to the learner so they have a fallback on bad days:

```
Never skip: ① Vocabulary SRS + ② Micro-listening (the irreplaceable, cumulative pair)
Skip first: ④ Extensive listening, ③ Self-breakdown
```

Vocabulary is cumulative and spaced-repetition-dependent — missing a day breaks the review schedule
in a way that's hard to recover from. Extensive listening and self-breakdown are both recoverable
later without the same cost.
