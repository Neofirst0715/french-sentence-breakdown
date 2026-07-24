# French Sentence Breakdown & Study System

A [Claude Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) that turns
any French audio transcript, article, or piece of writing into a full bilingual study package —
using **English as the bridge language** — and runs an ongoing listening/writing training system
built around the **Three Listen Rule**.

English is used deliberately, not by default: French and English share grammatical categories
(tense marking, agreement, relative pronouns) that make translation-as-bridge preserve grammar
structure in a way a non-Indo-European L1 often can't. That convenience brings its own risks —
translation-mediated reaction speed, French/English false friends, copying English sentence
structure where the two diverge — so the skill builds in three explicit countermeasures: a
French-only restatement checkpoint after every chunk, a running faux-amis log, and grammar notes
that flag convergence *and* divergence rather than just similarity.

## What it does

**Give it French content, get back:**
- A cleaned, speaker-labeled, thematically segmented transcript (with a corrections table showing
  every fix made to the raw auto-generated version)
- A sentence-by-sentence breakdown: English translation, IPA, word-by-word gloss, sentence
  structure, grammar notes flagging English/French convergence and divergence, and 2 extension
  examples — per sentence
- A running grammar-review table and a "recurring structures" analysis so you know what to actually
  prioritize
- A practical note on how to use that specific piece of material given its difficulty

**Give it your own French writing, get back:**
- A corrected version, an error table, explanations of the real grammar gaps (not just typos), and
  an explicit list of what you already did well

**Ask it for a study plan, get back:**
- A daily engine (vocab SRS / micro-listening / self-breakdown / extensive listening / output)
  scaled to your actual deadline math
- A back-translation routine to convert listening material into measured writing practice
- A systematic grammar curriculum to run alongside the material-driven notes
- Material tiers (staple / bridge / stretch) with an honest upgrade test

## Why it exists

Full sentence-by-sentence breakdowns of long transcripts are expensive to produce on demand, which
tempts you into "one long piece a month." That's the wrong lever. This skill scales the **Three
Listen Rule** down to short daily segments (2-4 minutes) so depth and frequency stop trading off
against each other — and it explicitly separates *intensive* listening practice (this technique)
from *extensive* listening practice (volume/minutes), which are easy to conflate but train
different things.

## Website

`index.html` is a self-contained showcase page for this skill. To publish it with GitHub Pages:
Settings → Pages → Deploy from a branch → `main` / root → Save. It'll be live at
`https://neofirst0715.github.io/french-sentence-breakdown/` a minute or two later.

## Install

Drop the `french-sentence-breakdown/` folder into your Claude Skills directory (or upload the
`.skill` file if you packaged one), or reference `SKILL.md` directly if you're using it as a system
prompt / instruction set elsewhere.

## Structure

```
french-sentence-breakdown/
├── SKILL.md                              — entry point, always loaded when the skill triggers
├── README.md                             — this file
└── references/
    ├── sentence-breakdown-format.md       — the six-part breakdown template + calibration rules
    ├── transcript-cleaning.md             — how to clean raw/auto-generated transcripts
    ├── writing-correction.md              — how to correct the learner's own writing
    └── study-system.md                    — the full daily/weekly/monthly training system
```

## Notes

- Designed for a learner going from A1/A2 toward B1/B2, using English as the bridge language, but
  the format generalizes to other level ranges and other bridge languages with light editing (see
  the rationale in `SKILL.md` for how to decide whether a given bridge language is a good fit before
  swapping it in).
- Respects copyright: transcript cleaning is a functional transformation in service of instruction,
  not redistribution. The skill never reproduces song lyrics verbatim.
- Not affiliated with Anthropic beyond using the standard Skill format.
