# Music Director reference library

`references/library/` is local reference knowledge: what a musical term means,
its audible effect, when it fits and when it does not. It informs the modules
in `references/instructions/` but never replaces or overrides them. Rules,
checks and delivery formats live in the modules.

Entries are possibilities, not recipes. A convention describes common practice;
it does not require a particular composition to follow it. See
`references/instructions/orchestration.md`, "Fundamental principle: musical
knowledge without creative formulas".

Entries are platform-independent. They contain no tool-specific directives,
tool-ready tags or parameter values.

## Organization

```text
references/library/
├── README.md
├── index.md
├── performance/     vocal delivery, dynamics, registers, articulation,
│                    ornaments, phrasing and section development
├── arrangement/     form and structure
├── rhythm/          meter, groove and rhythmic density
├── production/      ambience, space, saturation, reverb, delay, compression
├── harmony/         tonal center, mode, color, function, harmonic rhythm
└── lyrics/          imagery, contextual meaning, words as musical material
```

## Entry format

Each entry has one canonical term with a heading, aliases, a short definition,
the audible effect, when to use it and when to avoid it. Optional lines cover
compatible combinations and conflicts. Keep each field to one or two sentences.
Anchors come from the canonical heading. Update `index.md` when entries change.

Entries use lacunae in examples, never filled style lines, lyrics or tags.
Knowledge is labeled `consolidated`, `convention`, `interpretation` or
`unverified` when that status matters. Do not fabricate sources: if no source
can be verified, say so. A source is a bibliographic reference, not a link to
open. Where sources or traditions diverge, record the variation.

## How to use it

Always start at `index.md`: search by term, alias, category or intent, then
open only the pointed file and section. Never load the whole library.
Consultation is used when Performance needs execution vocabulary or when a
Style, Arrangement or Lyrics decision needs a precise definition. Consulting is
not applying: use an entry only when it fits the composition and the brief.
Explicit user requests prevail. No external research during generation.

## Maintenance

Prefer quality over quantity. Keep the index compact and grep-friendly. Add a
new area only when a real need appears.
