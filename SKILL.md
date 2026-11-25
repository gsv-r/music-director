---
name: music-director
description: >-
  Turns a creative brief into structured, text-only musical direction: Style
  (global sonic identity), Arrangement (form, layers, entries, exits, density,
  texture, and instrumental development), Lyrics, section-by-section Performance
  tags, and an interpretive Analysis. Use when the user wants to write a song,
  draft or review lyrics, build a sound/style prompt (e.g. for Suno or a
  producer brief), direct vocal performance per section, arrange a composition,
  analyze existing lyrics, adapt a song to another language, or work from a
  musical reference. Never generates, renders, or produces audio.
---

# Music Director

Music Director is a text-only skill. Given a creative brief, it produces structured
musical direction — Style, Arrangement, Lyrics, Performance and an interpretive
Analysis — and never generates, renders or produces audio. It supplies criteria,
vocabulary, methods, questions and checks, not ready-made lyrics, Style lines,
structures or development arcs. The base always comes from the user's context.

## Read and use this skill

1. Read this file for activation, module selection and navigation.
2. Read `references/instructions/orchestration.md`. It is the single canonical source
   of operational rules; routing, gates, workflows, coherence, validation,
   termination, output, library consultation, Creative Direction and reference
   handling are defined there, not here.
3. Open only the selected module files and the library sections the context requires.
4. Find technical knowledge through `references/library/index.md`, including its
   "Intent → Category/File" route, and open only the pointed file and section.
5. Consider, consult and apply knowledge as distinguished below. If this entry point
   and the canonical source seem to disagree, the canonical source governs.

## Canonical source: orchestration.md

`references/instructions/orchestration.md` is the authority for:

- Core principles and the fundamental principle (musical knowledge without creative formulas).
- Task routing and the complete route list.
- Pre-generation evaluation and missing-information gates.
- Orchestration workflows (full song, style only, arrangement only, instrumental,
  lyrics only, performance only, review, adapt to another language, from musical references).
- Language policy; coherence and responsibility boundaries.
- Validation and termination, including the Analysis pre-delivery check.
- Output and presentation.
- Knowledge library policy, including mandatory and conditional consultation.
- Creative Direction (transversal layer) and the Musical reference protocol.
- Compatibility and path resolution.

Open the relevant section there for rules. This file does not reproduce the universal
operational rules; it provides activation, navigation and knowledge-discovery guidance.

## Modules

| File | Open when | Owns |
|---|---|---|
| `references/instructions/orchestration.md` | Always, for the applicable sections | Canonical universal rules; routing; workflows; gates; validation; Creative Direction; reference protocol |
| `references/instructions/style.md` | Global sonic identity is in scope | Genre, tempo, instruments with function, voice, audible production texture, global movement |
| `references/instructions/arrangement.md` | Form or layers are in scope | Sections, order, relative durations, entries, exits, density, texture, transitions, counterpoints, instrumental development |
| `references/instructions/lyrics.md` | Sung text is created, changed or reviewed | Content, structure, singability, prosody, hook, addressee; mode-aware input gate |
| `references/instructions/performance.md` | Per-section interpretation is in scope | Tags, dynamics, expressive change, local execution, vocal enrichment criteria |
| `references/instructions/analysis.md` | Analysis is in scope or a pre-delivery check applies | Interpretive explanation and the canonical detailed Analysis pre-delivery check |

Creative Direction is a transversal section of `orchestration.md`, not a module and
not a sixth delivery dimension. Each module owns its specialized rules, checklists
and delivery formats; universal rules stay canonical in `orchestration.md`.

## Knowledge library

`references/library/` is local technical reference knowledge: definitions, audible
effects, when to use or avoid, compatible combinations, limitations and sources. It
informs the modules and never overrides them. The library is platform-independent
and local; the rule on external research is canonical in `orchestration.md`,
section "Knowledge library".

| Area | Files | Covers |
|---|---|---|
| Navigation | `references/library/index.md`, `references/library/README.md` | Term/alias/category/intent lookup; article template; source and verification policy |
| Performance | `references/library/performance/vocal-articulation.md`, `references/library/performance/vocal-delivery.md`, `references/library/performance/vocal-dynamics.md`, `references/library/performance/vocal-registers.md`, `references/library/performance/vocal-ornaments-effects.md`, `references/library/performance/phrasing-timing.md`, `references/library/performance/section-development.md` | Vocal technique, delivery modes, dynamics, registers, ornaments, phrasing/timing, interpretive and local section development |
| Arrangement (Form & Structure) | `references/library/arrangement/form-structure.md` | Transitions as formal events, climax preparation and release, delayed resolution, formal contrast, repetition with variation, non-conventional forms |
| Rhythm & Groove | `references/library/rhythm/rhythm-foundations.md` | Simple/compound meter, swing and straight feel, shuffle, backbeat, syncopation, groove, rhythmic density |
| Production & Texture | `references/library/production/production-foundations.md` | Ambience, spatiality, saturation, reverb, delay/echo, compression |
| Harmony & Tonality | `references/library/harmony/harmony-foundations.md` | Tonal center and ambiguity, scales and modes, consonance/dissonance and chord color, function and cadence, harmonic rhythm, modulation, static harmony, expectation, cross-tradition caution |

Instrumentation and a dedicated `references/library/analysis/` have no implemented
library yet; do not assume entries exist there.

## Finding knowledge

Always start at `references/library/index.md`:

- **Domains** lists the implemented areas.
- **Term → File** maps canonical terms and aliases to a file and an anchor.
- **Intent → Category/File** is the search route by natural-language musical intent —
  for example "airy voice", "transition that changes the form", "wet large space".
  Use it when the brief describes an effect rather than naming a technique.
- **Sources registry** records bibliographic support and explicit unverified labels.

Open only the file and section the index points to; retrieve one entry at a time.
Whether a consultation is mandatory, conditional or absent is decided by
`orchestration.md`, section "Knowledge library", and by the selected module — not by
this file. For instrumental Performance, consultation remains mandatory, but only
entries whose audible effect fits instruments apply: vocal registers, delivery modes
and vocal ornaments are not instructions for instruments.

## Selecting modules

Choose modules by the request and its real dependencies; do not run a module the
request does not need. The complete route list, its conditions and gates are in
`orchestration.md`, sections "Task routing" and "Pre-generation evaluation"; the
procedures are in "Orchestration workflows". A brief selection aid:

| Request | Modules to consider |
|---|---|
| Full song / complete piece | Style, Lyrics, Arrangement, Performance, Analysis |
| Style only | Style |
| Arrangement only | Arrangement |
| Lyrics only | Lyrics, plus Analysis check per canonical rules |
| Performance only | Performance |
| Instrumental (no lyrics/voice) | Style, Arrangement, Performance |
| Analysis only | Analysis |
| Review | Modules matching the reviewed material |
| Adapt to another language | Lyrics, Style, Performance, Analysis as needed |
| From a musical reference | Only the modules the deliverable requires |

For vocal writing, identify the lyric mode before deciding what information is
essential: `references/instructions/lyrics.md`, "Input gate and outline", is the
specialized gate for narrative, abstract, hook/chant, hypnotic, minimalist and
texture-based modes. See also `orchestration.md`, "Missing information and questions".

Any use of a musical reference follows the canonical "Musical reference protocol" in
`orchestration.md`; modules add only a short application note.

## Consider, consult, apply

- **CONSIDER.** Recognize which domains and techniques may be pertinent
  to this composition: Style, Arrangement, Lyrics, Performance, Analysis, Creative
  Direction, Rhythm & Groove, Production & Texture, Harmony & Tonality and the
  Musical reference protocol. Pertinence comes from the brief, the intended sound,
  the form, the voice (or its absence) and the user's constraints. Considering does
  not mean loading everything: do not preload the library.

- **CONSULT.** When a domain is pertinent and the canonical rules call
  for it, use `index.md` by term, alias, category or the "Intent → Category/File"
  route, then open the pointed file and the relevant section. Preserve the mandatory
  and conditional triggers defined in `orchestration.md` and in the modules.
  Consultation is not application: retrieve only what the context requires.

- **APPLY.** Use a consulted technique only when it is musically adequate,
  coherent with Style, Lyrics, Arrangement and the user's intent, and additive.
  The existence of knowledge never creates an obligation to apply it; an explicit
  user request prevails over a library suggestion, and the library never overrides
  module rules. If a direction is not followed, reformulate or clarify the musical
  intent.

## Complete rules

`references/instructions/orchestration.md` holds the complete orchestration layer and
is the single canonical source. Follow the selected modules for specialized rules,
checklists and delivery formats; open the library only for technical reference.
