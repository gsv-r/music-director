# Music Director

A text-only skill for AI-assisted songwriting and musical direction. It turns a
brief into three copyable fields, lyrics, style and title, plus a short analysis
written for the user. It does not generate audio and does not operate a
music-generation platform.

## What it helps with

- Developing a vocal or instrumental piece from a brief.
- Writing a one-line style description, or reviewing one you already have.
- Writing or reviewing lyrics: prosody, imagery, singability, hook, structure.
- Planning section order, layers and transitions (internal, folded into the output).
- Writing audible performance indications inside the lyric sections.
- Analyzing a finished piece or adapting lyrics to another language.
- Translating a musical reference into generic descriptors, without copying it.

## How it works

The brief is the starting material. The agent decides what the piece needs,
writes the three fields and explains the result briefly. Anything that does not
change one of those four things stays out of the final answer.

`references/instructions/best-practices.md` is the short guide to the criteria
that matter. `references/instructions/orchestration.md` holds the universal
rules. Each module owns one deliverable; the local library supplies vocabulary
when a term needs grounding.

## Delivery format

The final answer has exactly three fenced code blocks, in order, lyrics, style,
title, followed by the analysis as ordinary prose. The blocks contain only the
generated text and no labels, so copying a block gives clean material. Field
identifiers are never written in the answer. The canonical definition is in
`references/instructions/orchestration.md`, "Final delivery format (mandatory)".

## Getting started

Put this folder where your agent looks for skills, then give the agent a brief:
what the music should communicate, how it should sound, what must survive, what
to avoid and how finished the result should be. Keep the folder intact. The
documentation is in English; the language of the song follows the brief.

## Repository structure

```text
music-director/
├── AGENTS.md
├── README.md
├── SKILL.md
└── references/
    ├── instructions/
    │   ├── analysis.md
    │   ├── arrangement.md
    │   ├── best-practices.md
    │   ├── lyrics.md
    │   ├── orchestration.md
    │   ├── performance.md
    │   └── style.md
    └── library/
        ├── README.md
        ├── index.md
        ├── arrangement/
        ├── harmony/
        ├── lyrics/
        ├── performance/
        ├── production/
        └── rhythm/
```

`AGENTS.md` is a compatibility pointer, not a second set of rules.
