# Music Director — Reference Library

## Purpose and scope

`library/` is a **local, organized collection of musical reference knowledge** consulted by the Music Director modules when needed.

It is **not** an instruction module. The files in `instructions/` remain responsible for rules, decisions, checklists and delivery formats. The library provides **reference knowledge** (definitions, criteria, examples) that modules may consult to avoid generic choices and to ground decisions.

The library does not replace or override module rules. It informs them.

Entries are reference knowledge, not mandatory recipes: genres, techniques,
patterns, characteristics, references, best practices and examples describe
possibilities, not obligations. No entry should be interpreted as a required
structure, arrangement or development. See `instructions/orchestration.md`,
"Core principles" — "Fundamental principle: musical knowledge without creative
formulas".

The library is **platform-independent**. It provides musical knowledge, not
output instructions for specific tools. Entries must not contain tool-specific
directives (for example, Suno-ready tags are not a required or default field).

## Difference between library and instruction modules

- **Instruction modules** (`instructions/style.md`, `instructions/arrangement.md`, `instructions/lyrics.md`, `instructions/performance.md`): rules, orchestration, coherence, anti-generic checks, output formats.
- **Library** (`library/`): reference knowledge — what a term means, when to use/avoid it, audible effect, combinations, limitations, sources.

The library does not replace or override module rules. It informs them.

## Organization

```
library/
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
└── arrangement/
    └── form-structure.md
└── rhythm/
    └── rhythm-foundations.md
└── production/
    └── production-foundations.md
└── harmony/
    └── harmony-foundations.md
```

Performance, Arrangement, Rhythm, Production and Harmony are modules/domains. Arrangement
reference knowledge follows the convention under `library/arrangement/`; Rhythm reference
knowledge follows the convention under `library/rhythm/`; Production reference knowledge
follows the convention under `library/production/`; Harmony reference knowledge
follows the convention under `library/harmony/`. Future areas (instrumentation) will
follow the same convention, created only when needed.

## Naming and contribution standards

- One canonical term per entry; synonyms point to it via `Aliases`.
- Each entry follows the standardized model (see "Article template" below).
- File names use lowercase kebab-case.
- Anchors are derived from the canonical term heading.
- Update `library/index.md` whenever entries are added, removed or renamed.

## Article template

Each entry follows this template. Fields are concise (1–4 sentences each).

### Required fields

- **Term** — canonical term (one per entry).
- **Aliases** — synonyms (comma-separated; use "none" if none).
- **Category** — domain subcategory.
- **Definition** — concise musical definition. This field absorbs the former "Concept" field; a single concise definition is sufficient. Do not duplicate Concept and Definition.
- **Audible effect** — what is heard.
- **When to use** — contexts where it may be useful (possibilities, not obligations).
- **When to avoid / limitations** — conditions where it is unsuitable or risky.
- **Source** — verifiable bibliographic reference, or an explicit unverified label (see "Source and verification policy").

### Optional fields (include only when they add value)

- **Functioning** — how it works, when the mechanism is not obvious from the definition.
- **Compatible combinations** — techniques/concepts that work well with it.
- **Conflicts** — techniques/concepts it clashes with.
- **Relation to other concepts** — links, contrasts, dependencies.
- **Knowledge type** — `consolidated`, `interpretation`, or `convention`. Recommended when the claim's epistemic status matters.
- **Variation across traditions/sources** — include when sources or traditions diverge; document the variation instead of imposing one definition.
- **Example** — a musical illustration using lacunae only (e.g., `[<section> - <audible change>]`), and only when it genuinely clarifies the concept. Must be platform-neutral. Omit otherwise.

### Template notes

- One canonical term per entry; synonyms point via `Aliases`.
- Anchors derived from the canonical term heading.
- Entries are reference knowledge, not recipes: "when to use" describes conditions, never obligations.
- No filled Style lines, tags, lyrics, or arcs anywhere in entries.

## Source and verification policy

### Knowledge types

- **Verified knowledge:** supported by identifiable, verifiable sources (bibliographic references). Presented as established within the scope of those sources.
- **Stylistic conventions:** supported by identifiable musical contexts or sources (genre/tradition practice documented in sources). Labeled as convention, not as universal fact.
- **Unverified knowledge:** no identifiable source. Must be labeled explicitly (`Unverified — ...`) and must not be presented as established fact.

### Key rules

- An "Unverified" label is a disclosure of uncertainty, not a bibliographic source. It does not substitute for a reference; it signals that no verifiable source was confirmed.
- Source authority is evaluated according to the claim being supported. Do not impose a universal ranking in which one source type is automatically superior for every subject. The appropriate authority depends on the specific claim.
- Important technical claims should have directly supporting references where practical. Where no source can be verified, label the entry unverified rather than fabricating support.
- Do not fabricate sources or citations. If a source cannot be verified, label the entry unverified. This is non-negotiable.
- Document variation: when sources or traditions diverge, record the variation rather than imposing a single universal definition.
- Do not copy long excerpts from copyrighted material; write original definitions grounded in sources.
- Internet may be used in curation/verification, never during musical generation. Sources are bibliographic references, not links to open.

## Domain boundaries

- **Rhythm** (`library/rhythm/`): metric and rhythmic theory; groove phenomena and their definitions; audible effects. Does not decide how they are materialized in form/layers (Arrangement), global identity (Style), timing interpretation (Performance), or prosodic fit (Lyrics).
- **Arrangement** (`library/arrangement/`): formal architecture; how rhythmic concepts are materialized within form and layers; compositional distribution of layers (entries/exits, density per section). Does not redefine rhythmic theory, production mechanisms, global sonic identity, vocal interpretation, or lyric content.
- **Production** (`library/production/`): production mechanisms and audible characteristics of texture. Does not decide global production direction (Style), per-section distribution (Arrangement), or vocal-local application (Performance).
- **Harmony** (`library/harmony/`): harmonic and tonal reference knowledge (tonal center, scales and modes, consonance/dissonance and color, function and cadence, harmonic rhythm, modulation, non-functional/static harmony, expectation, and limits of Western tonal concepts). Does not decide global harmonic identity (Style), per-section harmonic changes (Arrangement), prosodic alignment (Lyrics), or expressive interpretation (Performance).
- **Style** (module, not library): global sonic identity and production direction. Does not own per-section layer distribution or formal architecture.
- **Performance** (`library/performance/`): vocal technique and interpretive evolution/local execution. Does not own formal architecture, rhythmic theory, or production globals.

The library provides reference knowledge; modules provide rules. Library entries must not restate module rules.

## Utilization policy

### When to consult
- Consult the library whenever Performance is in scope (generation or review of interpretive directions).
- Arrangement consults `library/arrangement/` when formal decisions are material to the task (creating/changing/reviewing form, sections, order, durations, transitions, climax, repetition/variation, non-conventional forms).
- Pure layer, density, counterpoint, or transition revisions without formal change do not automatically require the Arrangement library.
- Consultation is mandatory; using a retrieved technique is not (depends on musical adequacy).

### How the index directs retrieval
- Always start at `library/index.md`.
- Search by term, alias, category, or musical intent.
- Open only the relevant category file and section.
- Never load the whole library or all category files at once.

### Avoiding unnecessary loads
- Retrieve only what the musical context requires.
- Reuse already-loaded files within the same session (deduplicate by file).
- Do not consult the Performance library for Style-only or Lyrics-only tasks.
- Do not consult the Arrangement library for pure layer/density/counterpoint revisions without formal change.

### Absent terms
- If a term is not in the index/library, do not invent a definition or source.
- Label as assumption (if safe general knowledge) or ask the user.

### Local and internet-independent
- The library is local and versioned. No external research during musical generation.
- Sources are bibliographic references, not links to open.

### Knowledge, not decisions
- The library provides reference knowledge (definitions, criteria, examples).
- Decisions remain with the modules and the user's explicit choices.
- The user's explicit request prevails over a library suggestion.

- Grow incrementally: prefer quality over quantity.
- Preserve module responsibilities: the library provides reference knowledge; modules provide rules.
- Keep the index compact and grep-friendly.
- Internet may be used in curation/verification, never during musical generation. The library stores the knowledge needed so generation does not depend on external research.
- A term not found in the library must not receive an invented definition.
- The library is platform-independent: it provides musical knowledge, not output instructions for specific tools.
