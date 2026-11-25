# Music Director

Music Director is a text-only set of instructions that guides an AI to act as a
musical director. It does not generate, render, or produce audio, and it does not
create music on its own. Given a user's creative intent (an idea, a story, a
feeling, a genre, references, constraints), it shapes that intent into structured
musical direction across the musical dimensions — **Style** (global sonic
identity), **Arrangement** (form, layers, entries, exits, density, texture, and
instrumental development), **Lyrics** (composition), and **Performance**
(interpretation per section) — plus an interpretive **Analysis** of the finished
composition. Analysis is a specialized module, not a sonic dimension: it explains
the consolidated result instead of defining sound, form, lyric content, layers,
or section interpretation.

Music Director also applies a transversal layer of **textual humanization and
singability**: text is judged not only on the page but on how it sounds when
performed. Lyrics in particular are shaped for natural, singable phrasing —
respecting fluency, prosody, articulation, and the artist's identity — without
simplifying indiscriminately or erasing poetic devices. This is an editorial
sense, not a visible process: "Humanize the expression, never invent the
intention." The universal guardrails live canonically in
`references/instructions/orchestration.md`; each module applies them to its own output.

The repository is packaged as a portable skill in the open skill format: the
repository root is the skill directory, and the entry point is `SKILL.md`. The
documentation is in English. The language of the song itself follows the user's
creative brief; it is never defaulted to English just because the instructions are
in English.

## Package structure

```text
music-director/
├── SKILL.md                     # skill entry point: frontmatter, routing, gates
├── AGENTS.md                    # compatibility pointer for AGENTS-aware tools
├── README.md                    # this human-facing documentation
├── references/instructions/
│   ├── orchestration.md         # full orchestration rules and workflows
│   ├── style.md
│   ├── arrangement.md
│   ├── lyrics.md
│   ├── performance.md
│   └── analysis.md
└── references/library/
    ├── README.md
    ├── index.md
    ├── performance/
    │   ├── vocal-articulation.md
    │   ├── vocal-delivery.md
    │   ├── vocal-dynamics.md
    │   ├── vocal-registers.md
    │   ├── vocal-ornaments-effects.md
    │   ├── phrasing-timing.md
    │   └── section-development.md
    ├── arrangement/
    │   └── form-structure.md
    ├── rhythm/
    │   └── rhythm-foundations.md
    └── production/
        └── production-foundations.md
    └── harmony/
        └── harmony-foundations.md
```

Role of each part:

- `SKILL.md` — portable entry point. It declares the skill (`name`, `description`)
  and dispatches to the files below. Load it first.
- `references/instructions/` — rules. `references/instructions/orchestration.md` is the canonical location for universal
  rules, routing, language policy, missing-information gates, workflows, coherence,
  validation, termination, output rules, library consultation policy, and the
  universal guardrails for textual humanization and singability. The module
  files own their specialized rules, checklists, and delivery formats and reference
  the universal rules instead of repeating them.
- `references/library/` — local musical reference knowledge, consulted during Performance
  starting at `references/library/index.md`. It is not an instruction module and does not
  override module rules.
- `README.md` — packaging, installation, and usage documentation for humans.
- `AGENTS.md` — short compatibility pointer for tools that auto-load `AGENTS.md`.
  It is not a second rule source.

The operational rules are not repeated here. They live in `references/instructions/`, with the
complete orchestration layer in `references/instructions/orchestration.md`.

## Connecting the skill to an agent

The open skill format uses a folder containing a `SKILL.md` file whose YAML
frontmatter declares a `name` and a `description`. Music Director follows that
format, so any agent that supports it can use this folder as a skill.

Typical steps:

1. Put this repository — or a copy or symbolic link of it — where the agent looks
   for skills, or register the folder with the agent. The folder name and the
   frontmatter `name` are both `music-director`.
2. Keep the folder together. `SKILL.md`, `references/instructions/`, and `references/library/` are all
   required: without `references/library/`, Performance directions cannot follow the mandatory
   consultation procedure.
3. Make sure the agent reads files with relative paths from the skill root, not
   from its current working directory.
4. Ask for a full song, a style prompt, lyrics, performance direction, or an
   analysis.

Discovery and installation differ between agents and versions: some load skills
from a personal or project-level skills directory, some require an explicit
registration or a plugin, and some do not support the skill format at all. Check
your agent's documentation before assuming automatic discovery. `AGENTS.md` exists
only as a compatibility pointer for tools that auto-load it.

## Using the skill

1. Describe the musical idea naturally — a feeling, a story, a genre, references,
   constraints, or a requested language or structure.
2. The agent runs the pre-generation evaluation described in
   `references/instructions/orchestration.md`, selects the required modules, verifies their
   inputs, and asks grouped questions only for essential gaps.
3. Collaborate iteratively on Style, Arrangement, lyrics, performance, and Analysis.
4. Review the result and adjust. Markers and tags are guidance, not guarantees, and
   Analysis is interpretive guidance rather than a definitive reading.

No audio is generated, rendered, or claimed to be generated. Descriptors and
library entries are text references for AI collaboration, music production, and
work with human musicians.

Design principle: Music Director supplies tools (criteria, vocabulary, methods,
questions, checks), not ready-made bases. No lyrics, full Style line, structure,
or development arc is provided as a default to copy. Examples are limited to
isolated terms or lacuna formats (e.g., `[<section> - <audible change from this
song>]`); no filled tag, Style line, lyric, or arc is provided. The musical base
comes from the user's context.

## Textual humanization and singability

Music Director writes as someone who understands music and composition. Beyond
musical accuracy, its text is shaped to sound natural when performed:

- **Singability:** prefer words and expressions that are natural to sing; avoid
  terms that are hard to articulate or constructions that stall vocal delivery.
- **Naturalness and fluency:** avoid artificial phrasing, needlessly ornate
  words, and expressions chosen only to complete a rhyme; consider the sound of
  words, natural stress, phrase rhythm, and ease of vocal interpretation.
- **Simplicity when equivalent:** when two constructions communicate the same
  intent, prefer the more natural and singable one, without impoverishing the
  text.
- **Artistic identity:** preserve the language, poetry, vocabulary, and
  genre-specific character of the work. Poetry, metaphors, repetition, and
  intentional rhyme are kept when they serve the composition.
- **Fidelity:** do not change meaning, narrative, or emotional intent solely to
  make the text simpler or more elaborate, and never add information absent from
  the brief or the composition.
- **No obligation:** if a text is already natural, clear, expressive, and suited
  to its context, it is not rewritten.

Lyrics receives the most attention: it considers not only the quality of the
lyric as text, but how it sounds when sung — fluency, prosody, articulation, and
artistic identity. Style, Performance, and Analysis apply the same editorial
sense to their own output (descriptions, vocal directions, and interpretive
observations, respectively).

Humanization is integrated into orchestration and the modules; it is not an
independent skill or module, and it never overrides musical rules or the user's
intent.

## Library

`references/library/` is a local, organized, versioned collection of musical reference
knowledge. Performance consultation is mandatory when Performance is in scope.
Arrangement consults `references/library/arrangement/` when formal decisions are material,
`references/library/rhythm/` when rhythmic decisions are material, `references/library/production/`
when texture mechanisms are material, and `references/library/harmony/` when harmonic
changes, modulation, or harmonic rhythm are material. Style consults
`references/library/rhythm/` when groove and rhythmic identity decisions are material,
`references/library/production/` when production-texture descriptors are material, and
`references/library/harmony/` when harmonic identity decisions are material. Lyrics and
Performance may consult `references/library/harmony/` when harmonic theory is material.
Consultation always starts at `references/library/index.md`, and only the relevant entries
are retrieved. It is independent of internet access during musical generation;
sources are bibliographic references, not links to open. See `references/library/README.md`
for the contribution and source-verification policy.
