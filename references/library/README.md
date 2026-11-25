# Music Director reference library

## Purpose and scope

`references/library/` is a local, organized collection of musical reference knowledge. Music Director modules consult it when needed.

It is not an instruction module. The files in `references/instructions/` remain responsible for rules, decisions, checklists and delivery formats. The library provides reference knowledge: definitions, criteria and examples that modules may consult to avoid generic choices and ground decisions. It informs module rules without replacing or overriding them.

Entries are reference knowledge, not mandatory recipes. Genres, techniques, patterns, characteristics, references, best practices and examples describe possibilities, not obligations. No entry should be interpreted as a required structure, arrangement or development. See `references/instructions/orchestration.md`, "Core principles", specifically "Fundamental principle: musical knowledge without creative formulas".

The library is platform-independent. It provides musical knowledge, not output instructions for specific tools. Entries must not contain tool-specific directives; Suno-ready tags, for example, are neither required nor a default field.

## Difference between library and instruction modules

- Instruction modules (`references/instructions/style.md`, `references/instructions/arrangement.md`, `references/instructions/lyrics.md`, `references/instructions/performance.md`): rules, orchestration, coherence, anti-generic checks, output formats.
- Library (`references/library/`): reference knowledge covering what a term means, when to use or avoid it, audible effect, combinations, limitations and sources.

## Organization

```
references/library/
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
├── production/
│   └── production-foundations.md
├── harmony/
│   └── harmony-foundations.md
└── lyrics/
    └── lyrics-foundations.md
```

These directories are reference areas in the library: Performance, Arrangement, Rhythm, Production, Harmony and Lyrics. This is not an architectural reclassification: the specialized modules are Style, Arrangement, Lyrics, Performance and Analysis, and the transversal domains are Creative Direction, Harmony, Rhythm and Production. Reference knowledge in each area follows the same convention under `references/library/<domain>/`. Future areas, such as instrumentation, follow that convention and are created only when needed.

## Naming and contribution standards

- One canonical term per entry; synonyms point to it via `Aliases`.
- Each entry follows the standardized model (see "Article template" below).
- File names use lowercase kebab-case.
- Anchors are derived from the canonical term heading.
- Update `references/library/index.md` whenever entries are added, removed or renamed.

## Article template

Each entry follows this template. Fields are concise: 1 to 4 sentences each.

### Required fields

- Term: canonical term (one per entry).
- Aliases: synonyms (comma-separated; use "none" if none).
- Category: domain subcategory.
- Definition: concise musical definition. This field absorbs the former "Concept" field, so a single concise definition is sufficient. Do not duplicate Concept and Definition.
- Audible effect: what is heard.
- When to use: contexts where it may be useful (possibilities, not obligations).
- When to avoid / limitations: conditions where it is unsuitable or risky.
- Source: verifiable bibliographic reference, or an explicit unverified label (see "Source and verification policy").

### Optional fields (include only when they add value)

- Functioning: how it works, when the mechanism is not obvious from the definition.
- Compatible combinations: techniques/concepts that work well with it.
- Conflicts: techniques/concepts it clashes with.
- Relation to other concepts: links, contrasts, dependencies.
- Knowledge type: `consolidated`, `interpretation`, or `convention`. Recommended when the claim's epistemic status matters.
- Variation across traditions/sources: include when sources or traditions diverge; document the variation instead of imposing one definition.
- Example: a musical illustration using lacunae only (e.g., `[<section> - <audible change>]`), and only when it genuinely clarifies the concept. Must be platform-neutral. Omit otherwise.

### Template notes

- One canonical term per entry; synonyms point via `Aliases`.
- Anchors derived from the canonical term heading.
- Entries are reference knowledge, not recipes: "when to use" describes conditions, never obligations.
- No filled Style lines, tags, lyrics, or arcs anywhere in entries.

## Source and verification policy

### Knowledge types

- Verified knowledge: supported by identifiable, verifiable sources (bibliographic references). Presented as established within the scope of those sources.
- Stylistic conventions: supported by identifiable musical contexts or sources (genre/tradition practice documented in sources). Labeled as convention, not as universal fact.
- Unverified knowledge: no identifiable source. Must be labeled explicitly (`Unverified: ...`) and must not be presented as established fact.

### Key rules

- An "Unverified" label is a disclosure of uncertainty, not a bibliographic source. It does not substitute for a reference; it signals that no verifiable source was confirmed.
- Source authority is evaluated according to the claim being supported. Do not impose a universal ranking in which one source type is automatically superior for every subject; the appropriate authority depends on the specific claim.
- Important technical claims should have directly supporting references where practical. Where no source can be verified, label the entry unverified rather than fabricating support.
- Do not fabricate sources or citations. If a source cannot be verified, label the entry unverified. This is non-negotiable.
- Document variation: when sources or traditions diverge, record the variation rather than imposing a single universal definition.
- Do not copy long excerpts from copyrighted material; write original definitions grounded in sources.
- Internet may be used in curation/verification, never during musical generation. Sources are bibliographic references, not links to open.

## Domain boundaries

- Rhythm (`references/library/rhythm/`): metric and rhythmic theory; groove phenomena and their definitions; audible effects. Does not decide how they are materialized in form/layers (Arrangement), global identity (Style), timing interpretation (Performance), or prosodic fit (Lyrics).
- Arrangement (`references/library/arrangement/`): formal architecture; how rhythmic concepts are materialized within form and layers; compositional distribution of layers (entries/exits, density per section). Does not redefine rhythmic theory, production mechanisms, global sonic identity, vocal interpretation, or lyric content.
- Production (`references/library/production/`): production mechanisms and audible characteristics of texture. Does not decide global production direction (Style), per-section distribution (Arrangement), or vocal-local application (Performance).
- Harmony (`references/library/harmony/`): harmonic and tonal reference knowledge (tonal center, scales and modes, consonance/dissonance and color, function and cadence, harmonic rhythm, modulation, non-functional/static harmony, expectation, and limits of Western tonal concepts). Does not decide global harmonic identity (Style), per-section harmonic changes (Arrangement), prosodic alignment (Lyrics), or expressive interpretation (Performance).
- Lyrics (`references/library/lyrics/`): semantic and literary reference knowledge for sung text (layered meaning, metaphor, imagery, ambiguity, contextual meaning through repetition, lexical precision, lyrics as musical material). Does not redefine lyric content, prosody, singability, cliché, title, hook or tag rules (Lyrics module), vocal execution (Performance), section structure (Arrangement), or global sonic identity (Style).
- Style (module, not library): global sonic identity and production direction. Does not own per-section layer distribution or formal architecture.
- Performance (`references/library/performance/`): vocal technique and interpretive evolution/local execution. Does not own formal architecture, rhythmic theory, or production globals.

Library entries must not restate module rules.

## Utilization policy

### When to consult
- Consult the library whenever Performance is in scope (generation or review of interpretive directions).
- Arrangement consults `references/library/arrangement/` when formal decisions are material to the task (creating/changing/reviewing form, sections, order, durations, transitions, climax, repetition/variation, non-conventional forms).
- Pure layer, density, counterpoint, or transition revisions without formal change do not automatically require the Arrangement library.
- Lyrics may consult `references/library/lyrics/` on an optional, targeted basis when the brief calls for greater lyrical depth, subtext or layered meaning, stronger imagery or metaphor, emotional complexity, more distinctive word choices, interpretive ambiguity or coherent recurring motifs. It is not required for every lyric-writing task.
- Consultation is mandatory only where `references/instructions/orchestration.md` or the relevant module instructions explicitly require it, as with the mandatory Performance consultation. Otherwise, follow the module's optional and targeted consultation policy, as with Lyrics. Applying a retrieved technique is never mandatory; it depends on musical adequacy and user intent.

### How the index directs retrieval
- Always start at `references/library/index.md`.
- Search by term, alias, category, or musical intent.
- Open only the relevant category file and section.
- Never load the whole library or all category files at once.

### Avoiding unnecessary loads
- Retrieve only what the musical context requires.
- Reuse already-loaded files within the same session (deduplicate by file).
- Do not consult the Performance library for Style-only, Lyrics-only, Arrangement-only, or Analysis-only tasks.

### Absent terms
- If a term is not in the index/library, do not invent a definition or source.
- Label as assumption (if safe general knowledge) or ask the user.

### Local and internet-independent
- The library is local and versioned. No external research during musical generation.
- Sources are bibliographic references, not links to open.

### Knowledge, not decisions
- Decisions remain with the modules and the user's explicit choices; an explicit user
  request prevails over a library suggestion.
- Application is defined canonically in `orchestration.md`, section "Knowledge library": a
  consulted entry is applied only when it yields an identifiable decision in the output.
  See also "Output and presentation" there for usage reports.

### Maintenance
- Grow incrementally: prefer quality over quantity.
- Keep the index compact and grep-friendly.
