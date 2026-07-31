---
name: french-sentence-breakdown
description: Turn any French audio transcript, article, or written text into a full deep-dive study package using English (not the learner's native language) as the bilingual bridge — clean transcript, sentence-by-sentence grammatical breakdown (English translation, IPA, word-by-word gloss, sentence structure, grammar notes flagging English/French convergence and divergence, extension examples), a running grammar-review table, a running faux-amis (false friend) log, and a Three-Listen-Rule listening plan. Use this whenever the user uploads or pastes French content (podcast transcript, subtitles, song, article, journal entry) and wants it broken down, explained, corrected, or turned into study material — even if they just say "break this down" or "整理一下" or "帮我看看这段法语". Also use when the user asks for a French listening/study plan, wants their own French writing corrected, or wants to track French grammar progress toward a level goal (A1–B2). Handle long transcripts (40–80+ sentences) in a single pass rather than defaulting to tiny chunks — the user explicitly wants longer sessions, not more frequent short ones.
---

# French Sentence Breakdown & Study System

A skill for converting raw French audio/text into structured bilingual study material — using
**English as the bridge language**, not the learner's native language — and for running an ongoing
French-acquisition system built on the **Three Listen Rule**.

**Why English as the bridge, not the learner's L1**: French and English are both Indo-European and
share grammatical categories (tense marking, agreement, relative pronouns, article systems) that a
non-Indo-European L1 often lacks. Translating French into English tends to preserve the grammatical
structure in a way translating into, say, Chinese does not — the L1 translation is often correct in
meaning but strips the grammar out entirely. Use this only when the learner is genuinely comfortable
in English at a level where it can serve as a reliable bridge — confirm this once rather than
assuming it.

This convenience comes with three real risks, so every breakdown must actively guard against them
(see Step 2):
1. **Translation-mediated reaction speed** — routing French through English on every sentence can
   become a crutch that slows real-time listening/speaking, where there's no time for a two-step
   conversion. Counter with a mandatory French-only restatement step.
2. **Faux amis (false friends)** — French and English look alike, which makes look-alike-but-wrong
   word pairs the single biggest failure mode of this method (*actuellement* ≠ actually,
   *assister à* ≠ assist, *librairie* ≠ library). Counter with a running false-friends log.
3. **Structure calquing** — copying English sentence structure into French where the two actually
   diverge (e.g. *plaire à qqn* reverses subject/object versus "to like"; passive constructions like
   "I was rejected for a visa" need restructuring in French, not word-for-word translation). Counter
   by explicitly flagging divergence points, not just convergence points.

This skill has two modes. Detect which one the input calls for:

1. **Material mode** — the user gives you French content (transcript, article, lyrics, their own
   journal entry) and wants it cleaned up, explained, corrected, or turned into study material.
2. **System mode** — the user wants a listening/study plan, a progress check, or help deciding what
   to practice next.

Most conversations start in Material mode and drift into System mode once several pieces of
material exist. Keep both available.

---

## Mode 1: Material Mode

### Step 0 — Classify the input

Before doing anything, identify:

- **Is it clean or raw?** Auto-generated transcripts are full of noise: missing punctuation, wrong
  homophones, dropped accents, stray `[musique]`/sound-effect tags, English asides, mis-heard
  proper nouns. If raw, clean it first (see `references/transcript-cleaning.md`).
- **What register/tier is it, and roughly what CEFR level?** These are genuinely different content
  types requiring different treatment, not just different difficulty:
  - **Teaching podcast** (e.g. Simply French Podcast style): slow, deliberately repetitive,
    drills the same 3–5 structures dozens of times, built-in Q&A/negation practice. Usually A1–A2.
  - **Semi-authentic, learner-directed vlog**: a real person narrating their own life, but
    consciously paced/simplified for learners ("je parle lentement," explicit vocabulary teaching
    asides). Usually A2/B1. This is the most common "sweet spot" tier for active intensive study.
  - **Fully authentic content** (vlogs/podcasts not aimed at learners, native-speed): heavy
    disfluency, self-corrections, idioms, cultural references, proper nouns badly mangled by ASR.
    Usually B1+ to C1. Treat as **stretch/aspirational** material relative to an A1–B2 learner —
    see the level-mismatch protocol below.
  - **Formal scripted narration** (documentaries, historical/political explainers, read-aloud
    written French): no disfluencies at all, dense passive voice, "historical present" tense for
    narrating past events, long subordinate-clause sentences. A completely different register from
    conversational French — usually B2/C1 regardless of topic simplicity, closer to how a native
    speaker would read a textbook aloud than to any spoken-French register above. Flag this
    register shift explicitly; grammar notes should highlight how it differs from the conversational
    material (density of the passive, historical present, formal connectors like *puisque, ainsi,
    lorsque, ainsi que* vs. their everyday equivalents).
  Say explicitly which tier the input is and roughly what CEFR level — the user needs this to
  calibrate expectations. Don't let them assume every piece of content is equally learnable at
  their current level, and don't assume a slow, simple-sounding topic (e.g. a fruit-and-vegetable
  podcast) is the same tier as a fast, idiom-dense one on a similar surface topic.
- **Is it the user's own writing?** If so, this is a correction task, not a transcript-cleaning
  task — go to `references/writing-correction.md` instead of the breakdown format below.

### Level-mismatch protocol (fully authentic / formal content far above the learner's level)

When Step 0 identifies content that's a large gap above the learner's current level (typically:
fully authentic native-speed vlogs, or formal scripted/documentary narration), **do not silently
force the full per-sentence treatment** — the ROI is poor and the output becomes enormous without
being usable study material. Instead:

1. Say so explicitly and give a concrete comparison ("this is closer to X tier than Y tier you've
   worked with before").
2. Still do the **full transcript cleaning + corrections table** — this is high value regardless of
   level, since a clean reference transcript is useful at any stage.
3. Give a **selective** breakdown instead of exhaustive per-sentence treatment: pull out the
   genuinely new/useful grammar points, idioms, faux amis, and cultural notes, organized thematically
   rather than sentence-by-sentence.
4. Offer, rather than force, a full six-part breakdown of one shorter, self-contained segment (e.g.
   "just the first 2 minutes" or "just the book-discussion section") as a more realistic study unit.
5. If the document is extremely long (well beyond anything done so far in the conversation, e.g. a
   long-form documentary transcript), **ask the user how they want to handle the scope** before
   committing to a huge multi-part output — options: full treatment split across multiple files,
   cleaned transcript + corrections table only, or a quick summary of topic/difficulty with no full
   processing. Don't assume; a mismatch here wastes a lot of effort in the wrong direction.

### Step 1 — Produce a clean, speaker-labeled, thematically segmented transcript

Only needed for raw/messy input. Standard for a clean transcript:

- Segment into numbered thematic sections with a short French header (e.g. `## 3. Le dessert`)
- Label speaker turns if multiple speakers (infer from content if the raw file has no labels —
  say so explicitly, e.g. "attribution reconstructed from content")
- Fix mis-transcribed words, missing accents, dropped partitive articles, etc.
- Append a **corrections table** at the end: `| Sous-titre automatique | Correction | Type |`
- If anything is genuinely inaudible or a musical/sound-effect artifact, cut it and note it in the
  table rather than guessing at content

Full template and worked example: `references/transcript-cleaning.md`

### Step 2 — Sentence-by-sentence breakdown

This is the core deliverable. For each sentence, produce the six-part format below. Full template,
worked examples, and calibration notes (when to compress a short/simple sentence) are in
`references/sentence-breakdown-format.md`. Read that file before producing breakdowns — it defines
exactly how much detail each part needs and when to abbreviate.

The six parts, in order, per sentence:
1. **English translation**
2. **IPA**
3. **Word-by-word gloss** (number every word/morpheme)
4. **Sentence structure** (skeleton, for anything beyond a simple SVO sentence)
5. **Grammar notes** (the grammar point(s) worth teaching from this sentence — the actual payload).
   Explicitly mark each point as either **converges with English** (structure maps over cleanly —
   worth noting briefly, since this is exactly why the bridge works) or **diverges from English**
   (worth slowing down on — this is where calquing errors come from). Don't only list convergences;
   divergences are the higher-value half of this section.
6. **Extension examples** (2 short examples using the same structure)

Two additions run alongside the six parts, not per-sentence but as running threads through the
whole breakdown:

- **French-only restatement.** After finishing a natural chunk of sentences (a themed section, or
  every 5-8 sentences in continuous prose), insert a short prompt telling the learner to close the
  English side and restate the passage in French only, in their own words. This is not optional
  decoration — it's the step that converts the English-bridge comprehension gain back into direct
  French processing, and skipping it is exactly how the bridge becomes a permanent crutch.
- **Faux-amis log.** Maintain a running table across the whole document of any French word that
  resembles an English word but means something different, or where the surface similarity could
  tempt a wrong guess. Append to it as they come up rather than scattering the warning inline only —
  a consolidated list is what the learner will actually review later.

**Word-by-word gloss is never optional, even when the rest of the template compresses.** If the
learner's vocabulary is limited (confirm their approximate word count — see System Mode), a
structurally-repeated sentence can still contain individual words they don't know yet. **Do not
skip the gloss just because a sentence repeats a grammar structure already covered.** What *can*
compress for a repeated structure is the IPA, the sentence-structure skeleton, the grammar notes
(a one-line cross-reference like "same structure as sentence 14" is fine), and the extension
examples — but every distinct sentence still gets its English translation and a full word-by-word
gloss. See the compression rules in `references/sentence-breakdown-format.md` for exactly what can
and can't be compressed.

**Exception — exact verbatim repeats.** If the *identical* phrase is repeated back-to-back for
emphasis or pronunciation drilling (e.g. "Un maillot de bain. Un maillot de bain." or a single word
echoed twice), gloss it once and note it was repeated, rather than duplicating the entry. This is
different from compressing a *new* sentence that merely shares a structure with an earlier one —
that always still gets its own gloss, since the words themselves are new even if the grammar isn't.

**Thematic organization for heavily repetitive drilling content.** Some teaching-podcast material
(vocabulary-drill episodes on a theme — seasons, food, colors, clothing) is so repetitive and
vocabulary-dense, with so little new grammar, that strict sequential sentence numbering is less
useful than organizing the breakdown **by vocabulary/theme group** (e.g. "months," "weather
expressions," "clothing") with a full gloss table for each group, plus grammar notes on whatever
genuine structures do appear (impersonal weather verbs, comparatives, question templates). Use
judgment: if a transcript is mostly building a vocabulary set with minimal new grammar, thematic
organization serves the learner better than 80 nearly-identical numbered entries. If it has real
grammatical variety and development, use sequential numbering instead.

**Handle long transcripts in one pass.** The user has explicitly asked for longer sessions rather
than many tiny ones — a 40–80 sentence transcript should normally be broken down as one continuous
document (or at most 2–3 large parts if length limits force a split), not chopped into many
short files. Don't default to 15–20 sentence chunks unless the user asks for that.

### Step 3 — Cross-cutting grammar review

At the end of each breakdown, add a **grammar review table**: every grammar point taught, which
sentence(s) it came from, whether it converges or diverges from English, and a one-line takeaway.
See the format and the "recurring structures" style analysis in
`references/sentence-breakdown-format.md` — for longer/authentic texts, explicitly call out which
structures *recur* across many sentences (these are the highest ROI to master) versus which appear
once (lower priority, recognition-only for now). Close with the accumulated **faux-amis log** table
so it reads as one reference list, not scattered footnotes.

### Step 4 — Practical use note

Close with a short, concrete note on how this specific piece of material should be used given its
difficulty level relative to the learner (intensive deep-dive vs. extensive/background listening
vs. skip-for-now). Don't let a B2 vlog get treated the same way as an A1 teaching podcast — say so.

---

## Mode 2: System Mode

When the user wants a study plan, a progress check, or help deciding what to do next, use
`references/study-system.md`. It defines:

- The **Three Listen Rule**, scaled correctly by learner level and by material type (teaching
  podcast vs. authentic content) — this is a listening *comprehension* technique and must not be
  conflated with extensive/volume listening
- A **daily engine** (vocabulary SRS, micro-listening, self-breakdown, extensive listening, output)
  that fits into a fixed daily time budget
- A **back-translation** method (French → English → French, spaced across days) for converting
  listening material directly into writing practice, plus the French-only restatement drill that
  keeps the English bridge from becoming a permanent crutch
- A **systematic grammar curriculum** (ordered list of grammar points to cover on a timeline) to
  run alongside the material-driven, extraction-based grammar notes from Mode 1
- Level-appropriate material tiers (staple / bridge / stretch) and the upgrade test for moving
  between them
- A weekly rhythm and a monthly checkpoint with concrete pass/fail thresholds

Always ask or infer: **current vocabulary size, current CEFR level, target level, deadline, daily
time budget.** These five numbers drive every recommendation — don't give generic advice without
them. If any are missing, ask once, briefly, rather than guessing.

---

## Formatting conventions (apply in both modes)

- All learner-facing explanatory text is in **English**; French sentences, IPA, and example
  sentences stay in French. (English was chosen deliberately as the bridge language — see the
  rationale above — not defaulted to as a generic choice. If the learner's preference changes, or if
  a specific phrase is genuinely clearer glossed in their L1, that's fine as an occasional aside, but
  it shouldn't become the default mode.)
- Bold the French target word/phrase inside English explanations rather than translating it away.
- Use `>` blockquotes for important warnings/exceptions the learner is likely to get wrong —
  divergence points and faux amis are the most common candidates for this treatment.
- Never present output only as a chat reply for anything long-form — create a markdown file so the
  user can save/reuse it (this is study material, not a one-off answer).
- Respect copyright: this skill produces **learner analysis and pedagogical restructuring** of the
  source, not a verbatim reproduction for its own sake. Never reproduce song lyrics. Transcript
  cleaning is fine because it's a functional transformation (fixing ASR errors) in service of
  language instruction, not redistribution of the work.
