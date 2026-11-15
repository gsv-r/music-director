# Music Director

Music Director is a text-only set of instructions that guides an AI to act as a
musical director. It does not generate, render, or produce audio, and it does not
create music on its own. Given a user's creative intent (an idea, a story, a
feeling, a genre, references, constraints), it shapes that intent into structured
musical direction across three sonic dimensions — **Style** (global sonic
identity), **Lyrics** (composition), and **Performance** (interpretation per
section) — plus an interpretive **Analysis** of the finished composition. Analysis
is a specialized module, not a fourth sonic dimension: it explains the consolidated
result instead of defining sound, lyric content, or section interpretation.

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
├── instructions/
│   ├── orchestration.md         # full orchestration rules and workflows
│   ├── style.md
│   ├── lyrics.md
│   ├── performance.md
│   └── analysis.md
└── library/
    ├── README.md
    ├── index.md
    └── performance/
        ├── vocal-articulation.md
        ├── vocal-delivery.md
        ├── vocal-dynamics.md
        ├── vocal-registers.md
        ├── vocal-ornaments-effects.md
        ├── phrasing-timing.md
        └── section-development.md
```

Role of each part:

- `SKILL.md` — portable entry point. It declares the skill (`name`, `description`)
  and dispatches to the files below. Load it first.
- `instructions/` — rules. `orchestration.md` is the canonical location for universal
  rules, routing, language policy, missing-information gates, workflows, coherence,
  validation, termination, output rules, and library consultation policy. The four
  module files own their specialized rules, checklists, and delivery formats and
  reference the universal rules instead of repeating them.
- `library/` — local musical reference knowledge, consulted during Performance
  starting at `library/index.md`. It is not an instruction module and does not
  override module rules.
- `README.md` — packaging, installation, and usage documentation for humans.
- `AGENTS.md` — short compatibility pointer for tools that auto-load `AGENTS.md`.
  It is not a second rule source.

The operational rules are not repeated here. They live in `instructions/`, with the
complete orchestration layer in `instructions/orchestration.md`.

## Connecting the skill to an agent

The open skill format uses a folder containing a `SKILL.md` file whose YAML
frontmatter declares a `name` and a `description`. Music Director follows that
format, so any agent that supports it can use this folder as a skill.

Typical steps:

1. Put this repository — or a copy or symbolic link of it — where the agent looks
   for skills, or register the folder with the agent. The folder name and the
   frontmatter `name` are both `music-director`.
2. Keep the folder together. `SKILL.md`, `instructions/`, and `library/` are all
   required: without `library/`, Performance directions cannot follow the mandatory
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
   `instructions/orchestration.md`, selects the required modules, verifies their
   inputs, and asks grouped questions only for essential gaps.
3. Collaborate iteratively on Style, lyrics, performance, and Analysis.
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

## Library

`library/` is a local, organized, versioned collection of musical reference
knowledge. It is consulted only when Performance is in scope, always starting at
`library/index.md`, and only the relevant entries are retrieved. It is independent
of internet access during musical generation; sources are bibliographic references,
not links to open. See `library/README.md` for the contribution and
source-verification policy.
