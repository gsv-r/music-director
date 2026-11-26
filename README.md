# Music Director

Music Director turns a brief into musical direction written as text. It produces
three copyable fields: lyrics, a style line and a title. A short analysis explains
the result to you. The skill makes no audio and does not operate a
music-generation platform.

## What it helps with

- Developing a vocal or instrumental piece from a brief.
- Writing a one-line style description, or reviewing one you already have.
- Writing or reviewing lyrics: prosody, imagery, singability, hook, structure.
- Planning section order, layers and transitions. This stays internal, folded
  into lyrics and style.
- Writing audible performance indications into the lyric sections.
- Analyzing a finished piece or adapting lyrics into another language.
- Translating a musical reference into generic descriptors, without copying it.

## How it works

The brief supplies the material. The agent decides what the piece needs, writes
the three fields and explains the result. Anything that leaves those four
outputs unchanged is left out of the answer.

`references/instructions/best-practices.md` is the short guide to the criteria
that matter. `references/instructions/orchestration.md` holds the universal
rules. Each module owns one deliverable. The local library supplies vocabulary
when a term needs grounding.

## Delivery format

The answer has three fenced code blocks in a fixed order: lyrics, style, title.
A short analysis follows as ordinary prose. The blocks contain only the generated
text, with no labels above or inside them, so copying a block gives clean
material. Field identifiers never appear in the answer. The full definition is
in `references/instructions/orchestration.md`, "Final delivery format
(mandatory)".

## Getting started

Put this folder where your agent looks for skills and give it a brief. Say what
the music should communicate, how it should sound, what must survive, what to
avoid and how finished the result should be. Keep the folder intact. The
documentation is in English. The language of the song follows the brief.

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

`AGENTS.md` is a pointer for tools that load that file automatically. It holds
no separate rules.
