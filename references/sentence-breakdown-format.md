# Sentence Breakdown Format — Full Reference

This is the detailed spec for Step 2 of SKILL.md. Read this before producing any breakdown.

**Bridge language: English.** All translation, gloss, and explanation text is in English, not the
learner's native language — this is a deliberate choice (see SKILL.md rationale), not a default.

## The six-part template (full form)

```markdown
## N. [French sentence]

**English**: [translation]
**IPA**: [transcription in brackets]

**Word-by-word gloss**
1. **word1** — [part of speech / role]: [gloss]
2. **word2** — [conjugation info if verb, e.g. "être, present tense, vous form"]
...

**Sentence structure**
`[abstract skeleton, e.g. "si + subject + passé composé, [main clause]"]`

**Grammar notes**
[1–3 grammar points worth teaching. This is the actual payload of the exercise — spend the most
effort here. For each point, tag it explicitly:]
- **[Converges with English]** — structure maps over cleanly onto the English equivalent. Note
  briefly; this is exactly why the bridge works here, but doesn't need much space.
- **[Diverges from English]** — this is where calquing errors come from. Slow down here. Prioritize:
  - Points the learner has visibly gotten wrong elsewhere (check their own writing/journal if
    available) — call this out explicitly ("this is the same pattern from your journal entry...")
  - Points where spoken French diverges from what a textbook/teaching podcast would show (elision,
    dropped ne, liaison, colloquial register)
  - Points that recur across the text (flag recurrence — "echoes sentence X")
  - Genuine traps: des→de before a preceding adjective, qui/que, y/en, aller+infinitive requiring
    the infinitive (not a second conjugated verb), partitive articles, subject/object reversal verbs
    like *plaire à* / *manquer à*, passive-voice restructuring (*ma demande a été refusée* vs. a
    literal "I was refused")

**Extension examples**
- [example sentence 1 using the same structure, with English gloss]
- [example sentence 2]
```

## Two running threads (not per-sentence — track across the whole document)

### French-only restatement checkpoints

After each natural chunk (a themed section, or every 5–8 sentences of continuous prose), insert:

```markdown
> **Restatement checkpoint**: Close the English column. Retell this passage in French only, in
> your own words. Then check yourself against the text — did you keep the tense choices? The
> pronouns? Don't just re-read; actually produce it first.
```

This is not decoration. The entire risk of an English bridge is that it becomes a permanent
translation step the learner never sheds. This checkpoint is the mechanism that converts a
comprehension gain into direct French processing. Do not omit it, and do not make it optional
filler — phrase it as an instruction to actually do, not a suggestion to skim past.

### Faux-amis (false friends) log

Maintain one running table across the whole document, appended to as items come up, not scattered
as isolated inline asides only:

```markdown
## Faux amis encountered

| French | Looks like | Actually means | Note |
| --- | --- | --- | --- |
| actuellement | actually | currently, right now | actually = en fait / en réalité |
| assister à | to assist | to attend | aider = to assist/help |
| librairie | library | bookshop | bibliothèque = library |
| concurrence | concurrence (agreement) | competition | very strong trap — nothing to do with simultaneity |
| roman | Roman (adjective/Empire) | novel | visual overlap only |
| expérience | experience | experience OR experiment | French doesn't distinguish; context decides |
| chargé | charged (electrical/emotional) | busy (schedule); ornate/busy (decor, style) | two common non-English senses depending on context |
| demander | to demand | to ask (for); to require/take (time, effort) | much weaker/neutral than English "demand" |
| défi | to defy | a challenge (noun) | milder than English "defiance" |
| or | English "or" | now/well/but (logical-pivot connector) | completely different word from *ou* ("or") — a serious trap at the start of a sentence |
| comprendre | to understand | (also) to comprise/include | context-dependent secondary sense, common in formal lists |
| important | important (mattering) | (also) significant/large (in size/degree) | secondary sense, common in statistics/analysis |
| bien | well | (also) an intensifier: "indeed/really" | position/context-dependent, distinct from the adverb-of-manner sense |
| fétiche (couleur fétiche) | fetish | favorite/signature/lucky | much broader, everyday sense than the narrow English word |
| occasion (d'occasion) | occasion (event) | secondhand/used; a bargain | *une bonne occasion* = a good deal |
| assister à | to assist | to attend/be present at | *aider* = to assist/help |
| appréhender | to apprehend (arrest) | to dread/be apprehensive about | can also mean "to apprehend" formally, but the "dread" sense is more common in everyday speech |
| chaud (quartier chaud) | hot (temperature) | rough/dangerous (idiomatic) | context-dependent — don't assume literal temperature |
```

Every time a lookalike-but-different word appears in the transcript, add a row here in addition to
whatever's said inline at that sentence. By the end of a long document this becomes the single most
reusable study artifact — it's the thing worth reviewing on its own later.

## Tying grammar notes back to the learner's tense-progression roadmap

If the learner has a stated tense-learning order (e.g. présent → imparfait → futur simple →
conditionnel présent → subjonctif présent), actively flag when material previews a **tense further
along that roadmap than they've formally studied yet** — this is genuinely useful context, not just
trivia. For example: a real, natural `si + imparfait + conditionnel présent` sentence encountered in
authentic material is worth bookmarking explicitly as "a preview of your next tense" rather than
just explaining it in isolation, since the learner will get more value revisiting that exact
real-world sentence once they reach that point in their curriculum than from a textbook example
built for the occasion. Do this for passé composé auxiliary choice (avoir vs. être) and agreement
rules too, since these are usually flagged as a current priority — give them extra weight and
cross-reference every new occurrence back to earlier ones rather than re-deriving the rule from
scratch each time.

## Compression rules

**The word-by-word gloss and English translation are never skipped, for any sentence, regardless
of length or repetition.** This is the one non-negotiable part of the template. A learner with a
limited vocabulary (e.g. ~1,000 words) can fail to know individual words even inside a sentence
whose *grammar* is a repeat — compressing away the gloss on the assumption that "this structure was
already covered" silently drops vocabulary coverage, which is a real gap, not a convenience. What
compresses is everything *else*:

- **Full six-part treatment**: sentences that introduce a new grammar point, a trap, an idiom, or
  a structure not yet covered — especially anything tagged [Diverges from English]. Full IPA,
  sentence structure, grammar notes, and extension examples.
- **Compressed**: sentences that repeat a structure already fully explained a few sentences
  earlier. Still give the **full translation + word-by-word gloss**. Drop or shorten: IPA (optional
  for simple/short sentences), the sentence-structure skeleton, and the grammar notes (a one-line
  cross-reference like "same *qui* pattern as sentence 14" is enough), and skip fresh extension
  examples.
- **One-liner-with-gloss**: short interjections/fillers ("Incroyable.", "Trop bon.", "Ça va") still
  get translation + a quick word gloss if any word is non-trivial; pure discourse fillers with no
  real lexical content ("euh," "donc," repeated as a standalone filler) can be noted without a full
  entry.
- **Exact verbatim repeats** (the identical phrase said twice in a row for emphasis/pronunciation
  drilling) are glossed once, with a note that it repeats — this is not the same as compressing a
  *new* sentence, since there's no new vocabulary to cover in a literal duplicate.

A useful ratio for how much *supporting apparatus* (IPA/structure/grammar notes/extensions) to
spend per sentence on a ~60–80 sentence authentic transcript: roughly 60% full treatment, 30%
compressed-apparatus, 10% one-liner-apparatus — but the gloss itself stays at 100% coverage
throughout. A teaching-podcast transcript (Simply French style) will skew much more compressed on
apparatus since it deliberately repeats the same 3–4 grammar structures dozens of times — don't
re-explain the grammar of "je voudrais" fifteen times — but if fifteen different nouns follow "je
voudrais," gloss all fifteen nouns.

**When a transcript is extremely vocabulary-repetitive with minimal grammar variety** (e.g. a
themed vocabulary-drill episode — seasons, food, clothing), consider organizing by **theme/
vocabulary group** instead of strict sequential numbering — see SKILL.md Step 2 for when this
applies. Every distinct word still needs its English gloss; only the organizing structure changes.

## The recurring-structures analysis (for longer/authentic texts)

At the end of a long breakdown, add a section like this — it is often more valuable to the learner
than the sentence-by-sentence detail, because it tells them where to spend limited time:

```markdown
## Master review: structures that recur throughout

| Structure | Occurrences | Example | English relationship |
| --- | --- | --- | --- |
| Dislocation (noun + c'est / pronoun) | 5+ | Montpellier, c'est une ville... | diverges — no English equivalent, purely French discourse habit |
| Near future (aller + infinitive) | 6+ | on va flâner | converges — like "going to" |
...

> Recommendation: master the high-frequency structures first — they're worth more listening/
> speaking practice right now than low-frequency, "advanced-looking" structures (subjonctif, futur
> antérieur), which for now only need to be recognizable, not producible.
```

Rank by frequency, not by textbook prestige. A structure that appears 6 times in real speech (e.g.
dropped `ne`, `il y a`/`il fait`, `qui`/`que`) is worth more practice time right now than a
grammatically "advanced" structure that appears once, even though the latter looks more impressive
on paper.

## Grammar review table (end of each session/part)

```markdown
| Grammar point | Sentence(s) | English relationship | Takeaway |
| --- | --- | --- | --- |
| aller + infinitive | 6, 10, 19 | converges | main spoken future tense |
| des → de (adjective before noun) | 47 | diverges | de très hautes attentes |
...
```

Keep this cumulative if breaking a long text into multiple parts — carry the table forward and
append rather than starting fresh each time, so the user has one running reference by the end. Close
the full document with the accumulated faux-amis table too, so both running threads land as single
consolidated references rather than scattered footnotes.

## Worked example (short, for calibration)

Input sentence: *"Mais si vous avez écouté jusqu'à la fin, vous savez la réponse."*

```markdown
## 1. Mais si vous avez écouté jusqu'à la fin, vous savez la réponse.

**English**: But if you've listened to the end, you know the answer.
**IPA**: [mɛ si vu ave ekute ʒyska la fɛ̃ vu save la ʁepɔ̃s]

**Word-by-word gloss**
1. **mais** — conjunction: but
2. **si** — conjunction, introduces a conditional clause: if
3. **vous** — subject pronoun: you (plural/formal)
4. **avez écouté** — passé composé (avoir, present, vous form + écouter past participle): have listened
5. **jusqu'à** — jusque + à contracted: until
6. **la fin** — feminine noun: the end
7. **vous savez** — savoir, present, vous form: you know
8. **la réponse** — feminine noun: the answer

**Sentence structure**
`mais + si [conditional clause: subject + passé composé], [main clause: subject + present tense]`

**Grammar notes**
1. **[Converges with English]** si + passé composé → main clause present tense: this maps onto the
   English "if you've listened..., you know..." almost word for word — a rare case where the French
   conditional-perfect-to-present pattern lines up cleanly with English, unlike the classic
   si + present → future pattern.
2. **[Diverges from English]** écouter vs. entendre: English "to hear" covers both meanings, but
   French splits them — écouter is active, attentive listening; entendre is passively hearing a
   sound. English speakers often default to entendre by false analogy with "hear," when écouter is
   what's meant here.
3. jusqu'à + noun = until: jusqu'à demain (until tomorrow), jusqu'à midi (until noon).

**Extension examples**
- Si tu as fini, tu peux partir. — If you've finished, you can leave.
- J'ai travaillé jusqu'à minuit. — I worked until midnight.
```

Match this depth for any sentence that teaches something new.
