# Music Director

Music Director is a text-only set of instructions that guides an AI to act as a musical director. It does not generate, render, or produce audio, and it does not create music on its own. Given a user's creative intent (an idea, a story, a feeling, a genre, references, constraints), it shapes that intent into structured musical direction across three sonic dimensions — **Style** (global sonic identity), **Lyrics** (composition), and **Performance** (interpretation per section) — plus an interpretive **Analysis** of the finished composition. Analysis is a specialized module, not a fourth sonic dimension: it explains the consolidated result instead of defining sound, lyric content, or section interpretation.

The documentation is in English. The language of the song itself follows the user's creative brief (see `instructions/lyrics.md`); it is never defaulted to English just because the instructions are in English.

## Architecture

Music Director has an orchestration layer, four specialized modules, and a local reference library.

- `AGENTS.md` — orchestration layer: task routing, module selection, missing-information handling, coherence, language policy, and library consultation rules.
- `instructions/style.md` — global sonic identity: genre/subgenre, tempo, instruments (with roles), voice (timbre + way of singing), production texture, and global movement.
- `instructions/lyrics.md` — lyric composition: content, structure, prosody, singability, hook, addressee, and language selection.
- `instructions/performance.md` — performance direction: per-section dynamics, tags, layering, vocal enrichment, and the mandatory library consultation procedure.
- `instructions/analysis.md` — interpretive explanation of the finished composition: premise, meaning, context, narrative arc, emotional progression, hook, and alignment with the user's brief; also defines the mandatory Analysis pre-delivery check. A specialized module, not a fourth sonic dimension.
- `library/` — local musical reference knowledge (definitions, criteria, examples). Consulted during Performance. It is not an instruction module and does not override module rules.

### Directory structure

```
music-director/
├── AGENTS.md
├── README.md
├── instructions/
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

## How the modules work together

The four modules are applied in a standard construction order, while remaining flexible to the user's flow:

1. **Style** (`instructions/style.md`) — absorbs any reference and writes the global sound. Style is the anchor for everything else.
2. **Lyrics** (`instructions/lyrics.md`) — writes the lyrics using Style as context (genre, voice, tempo, atmosphere). Lyrics must not contradict Style.
3. **Performance** (`instructions/performance.md`) — writes per-section tags using Style + Lyrics. Tags describe evolution (soft → full), never global sound.
4. **Analysis** (`instructions/analysis.md`) — explains the consolidated result (Style + Lyrics + Performance + brief). Analysis is produced after the creative components it explains are settled and does not modify them retroactively.

Construction hierarchy (standard order and priority, not a rigid rule): user instructions → Style → Lyrics → Performance → Analysis → formatting. Other flows are allowed (for example, finished lyrics as a starting point); do not force Style → Lyrics → Performance → Analysis when the request implies another order.

Responsibility boundaries (no duplication):

- Style owns global sound and global movement; Performance owns per-section evolution.
- Lyrics owns content, structure, prosody, hook, and addressee; it does not define global sound or section interpretation.
- Performance owns interpretation, dynamics, and expressive change per section; it does not define global sound or lyric content.
- Analysis owns the interpretive explanation of the finished composition; it does not define global sound, lyric content, or section interpretation. It explains the consolidated result.
- Tags describe evolution, never global sound. Style carries genre, instruments, and vocal identity; lyric words and section tags belong to the lyrics field. Analysis appears once, after the consolidated result.

## Module selection (task routing)

Select modules by the user's request and by real dependencies. Do not run a module the request does not need.

- Full song / complete piece → Style + Lyrics + Performance + Analysis (Analysis by default when Lyrics is in scope).
- Style only → Style.
- Lyrics only → Lyrics (may reference an existing Style if provided). Whenever lyrics are created, changed, or reviewed, run the Analysis pre-delivery check, even if the user restricts the format (e.g., "only the lyrics"). The visible Analysis section is included by default when applicable and may be omitted under a format restriction. Distinguish selecting the Lyrics module from a request that demands only the lyric text.
- Performance only → Performance (requires lyrics/structure; use what is provided; no lyric or compositional changes). Analysis is not in scope.
- Performance with lyric or compositional changes → Performance plus the relevant Lyrics responsibilities and the Analysis pre-delivery check; not a Performance-only task.
- Analysis only → Analysis on a provided or existing composition; do not rewrite Lyrics.
- Localized lyric change → always run the Analysis pre-delivery check on the changed passage and its whole-composition impact. Update an existing Analysis section if affected; do not add a new visible section by default, and add one only when requested. Respect explicit format restrictions.
- Review of provided material → the module(s) matching the material; do not rewrite unless asked. A review covering lyrics or compositional content runs the Analysis pre-delivery check before delivery.
- Adapt to another language → Lyrics (prosody/language) + Style (vocal diction) + Performance (tag language) + Analysis (as needed).
- From a musical reference → select only the modules the deliverable requires; each selected module applies its own "Using a reference" section. Do not auto-select all four modules just because a reference was provided.

Isolated module use must not invent missing global context; state the gap and label assumptions only when that context is actually required by the requested module.

## The Library (reference knowledge)

`library/` is a local, organized, versioned collection of musical reference knowledge. It is not an instruction module and does not replace `instructions/*`. Instruction modules own rules, orchestration, coherence, anti-generic checks, and output formats; the library provides reference knowledge (what a term means, when to use/avoid it, audible effect, combinations, limitations, sources).

Mandatory consultation: whenever Performance is in scope (generation or review of interpretive directions), consult `library/index.md` before producing directions. This applies to full-song flows and Performance-only requests.

Selective retrieval: consultation starts at `library/index.md` (grep for term, alias, category, or musical intent), then opens only the relevant category file(s) and section(s). Never load the whole library or all category files at once. Reuse already-loaded files within the same session.

Consult vs. use: consulting the library is mandatory; using a retrieved technique is not. A technique is applied only when musically appropriate, coherent with Style and lyrics, and additive. The library offers possibilities, not obligations, and never becomes a mandatory tag list.

Other rules:

- The user's explicit request prevails over a library suggestion.
- The library does not override `performance.md` (anti-generic, role division, tag placement, coherence).
- No external research during musical generation; the library is the only reference source. If a term is not in the library, label it as an assumption or ask; do not invent definitions or sources.
- Library consultation is required only when Performance is in scope. Do not consult it for Style-only or Lyrics-only tasks.

Current coverage: Performance only — 7 category files under `library/performance/`, 39 entries. Future areas (style, rhythm, percussion, instrumentation, arrangement) follow the same convention and are created only when needed. See `library/README.md` for contribution and source-verification policy.

## Language and conventions

- This project and all documentation are in English.
- The song's language follows the user's creative brief. Never default to English lyrics because the instructions are in English.
- Style reflects the lyric language in its vocal diction descriptor (e.g., `Brazilian Portuguese vocals`).
- Performance tags/markers use the language appropriate to the destination.
- Communicate with the user in their language; keep module references and field labels as defined.
- No audio is generated, rendered, or claimed to be generated (all modules).

## How to use

1. Provide the instruction files to a capable AI: `AGENTS.md` plus the modules you need (`instructions/style.md`, `instructions/lyrics.md`, `instructions/performance.md`). Make the repository's local library available to the agent when Performance is in scope. The agent must start with `library/index.md` and retrieve only the relevant entries. Never preload the entire library.
2. Describe your musical idea naturally — a feeling, a story, a genre, references, constraints, or a requested language/structure.
3. The AI runs a pre-generation evaluation: identifies the deliverable, selects the required modules, checks their inputs, and asks grouped questions only for essential gaps (for example, a missing concrete scene or point of view for lyrics, or missing lyrics/structure for Performance).
4. Collaborate iteratively to refine Style, lyrics, performance, and Analysis.
5. Review the result and adjust. Markers and tags are guidance, not guarantees; if a direction is not followed, reformulate or clarify the musical intent. Analysis is interpretive guidance, not a definitive reading.

## Output and presentation

- Presentation adapts to the user's request; templates are illustrative, not mandatory.
- Default delivery order when all are in scope: Title, Style, Lyrics, Analysis. Adapt to the user's request.
- Lyrics owns sung content and structure; Performance owns interpretive directions by section. Structural headers and Performance tags must not be confused.
- When both Lyrics and Performance are requested, interpretive directions are produced once. They may be integrated into the corresponding section headers when useful, but must not be repeated in a second identical block.
- Lyrics may include structural markers and short ad-libs (1–3 syllables, in parentheses). Full performance direction is included only when Performance is in scope.
- Analysis, when in scope, appears once, after the consolidated result. It is not repeated.
- Keep sung text and musical instructions clearly separated.

## Notes

- Markers and tags are guidance for interpretation, not guaranteed commands. Adherence varies by destination and by conflict with other directions.
- The `library/` is local and independent of internet access during musical generation. Sources are bibliographic references, not links to open.
- If a reference cannot be accessed, state it in one sentence and ask for the missing data; do not invent.