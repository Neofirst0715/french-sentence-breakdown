# Transcript Cleaning — Reference

Use this when the input is a raw/auto-generated transcript (ASR output), not already clean.

## Signs a transcript needs cleaning

- No punctuation, or wrong punctuation
- No speaker labels even though multiple people are clearly talking
- Missing accents (e.g. `aprè` for `après`, `refuse` for `refusée`)
- Homophone errors (e.g. `une huile` for `une ville`, `Paul Valérie` for `Paul Valéry`)
- Dropped grammatical words, especially partitive articles (`je voudrais poisson` instead of
  `je voudrais du poisson`) and the negative `ne` (already normal in speech, but ASR sometimes also
  drops words that speakers *did* say)
- Stray non-speech tokens: `[musique]`, sound-effect transliterations (nonsense syllables that were
  actually a jingle or sound effect), stage directions accidentally transcribed as dialogue
- English asides mixed into French speech (a bilingual speaker glossing a word) — keep or cut
  depending on whether it's pedagogically useful; if kept, mark it as translation, not dialogue
- **Copyrighted song lyrics bleeding into the transcript** from background/outro music (common in
  vlogs) — never reproduce or quote these, even partially. Cut them from the cleaned transcript
  entirely and note in the corrections table that a fragment of song lyrics was removed and not
  reproduced, per copyright limits. Do not paraphrase them either; just note the removal.
- **Speaker-attribution inconsistencies in scripted dialogue** (e.g. a teaching-podcast script
  where a question is clearly meant for one host but a stray label or context makes it look like
  they asked and answered themselves) — reassign the turn to whichever speaker the *content* logic
  requires, and flag the specific spot in the corrections table as a script/editing inconsistency
  rather than silently fixing it without a note.

## Process

1. **Segment thematically.** Read through once, identify natural topic breaks, add numbered French
   headers (`## 1. Introduction`, `## 2. Dire son nom`, etc.).
2. **Attribute speakers** if there are multiple. If the raw file has no labels, infer from content
   and **say explicitly that attribution was reconstructed** — don't silently present a guess as
   fact. Flag it in a note at the end.
3. **Fix errors**, but track every fix in a corrections table so nothing is silently altered without
   a paper trail:

   ```markdown
   | Sous-titre automatique | Correction | Type |
   | --- | --- | --- |
   | je voudrait du poulet | je voudra**is** du poulet | conjugaison (muet) |
   | je voudrais poisson | je voudrais **du** poisson | article partitif manquant |
   | une table fort de s'il vous plaît | une table **pour deux**, s'il vous plaît | mots mal reconnus |
   ```

   Type categories to use: `orthographe`, `accord (muet)`, `article partitif manquant`, `mot mal
   reconnu`, `nom propre`, `phrase tronquée`, `hors-texte (musique/régie)`, `inaudible`,
   `incohérence de script` (attribution/logic mismatch in a scripted dialogue), `incertain`
   (a plausible reconstruction offered, but genuinely not confident — say so rather than presenting
   a guess as fact).

   For proper nouns badly mangled by ASR (real people, places, books, brands), cross-check against
   context before committing to a correction — a name mentioned once ambiguously is often confirmed
   by a second, clearer mention elsewhere in the same transcript (e.g. a garbled author name
   confirmed by a correctly-transcribed book title later in the same passage). When genuinely
   uncertain even after checking context, offer the best-guess reconstruction but mark it
   `incertain` rather than asserting it.

4. **Cut, don't guess, for genuinely unrecoverable content.** If a phrase is nonsense syllables from
   a sound effect or truly inaudible, remove it from the clean transcript and note it was removed —
   do not invent plausible-sounding French to fill the gap.
5. **Preserve register.** If the raw speech has colloquialisms (`ouais`, `sympa`, dropped `ne`,
   dropped partitive articles in truly casual speech), don't over-correct into textbook French —
   only fix genuine transcription *errors*, not authentic colloquial usage. Flag colloquial-but-
   correct usage separately from actual errors so the learner doesn't confuse "the ASR heard it
   wrong" with "the speaker said it informally on purpose." Sentence breakdown (Step 2 of SKILL.md)
   is the right place to explain *why* a colloquial form is fine and shouldn't be imitated in formal
   writing.

## Note to append at the end of the clean transcript

Always close a cleaned transcript with a brief note like:

> Note : l'attribution des tours de parole a été reconstruite ; quelques répliques pourraient être
> inversées. Le fichier audio reste la référence finale.

This keeps the user's trust calibrated correctly — the transcript is a study aid, not a certified
verbatim record.
