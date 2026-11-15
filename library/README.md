# Music Director — Reference Library

## Purpose and scope

`library/` is a **local, organized collection of musical reference knowledge** consulted by the Music Director modules when needed.

It is **not** an instruction module. The files in `instructions/` remain responsible for rules, decisions, checklists and delivery formats. The library provides **reference knowledge** (definitions, criteria, examples) that modules may consult to avoid generic choices and to ground Performance directions.

## Difference between library and instruction modules

- **Instruction modules** (`instructions/style.md`, `lyrics.md`, `performance.md`): rules, orchestration, coherence, anti-generic checks, output formats.
- **Library** (`library/`): reference knowledge — what a term means, when to use/avoid it, audible effect, combinations, limitations, sources.

The library does not replace or override module rules. It informs them.

Entries are reference knowledge, not mandatory recipes: genres, techniques,
patterns, characteristics, references, best practices and examples describe
possibilities, not obligations. No entry should be interpreted as a required
structure, arrangement or development. See `instructions/orchestration.md`,
"Core principles" — "Fundamental principle: musical knowledge without creative
formulas".

## Organization

```
library/
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

Only Performance is implemented in this first version. Future areas (style, rhythm, percussion, instrumentation, arrangement) will follow the same convention, created only when needed.

## Naming and contribution standards

- One canonical term per entry; synonyms point to it via `Aliases`.
- Each entry follows the standardized model (see category files).
- File names use lowercase kebab-case.
- Anchors are derived from the canonical term heading.
- Update `library/index.md` whenever entries are added, removed or renamed.

## Source and verification policy

- Every entry must have a `Source` field.
- A source may be a verifiable bibliographic reference or an explicit label "Unverified — general performance practice; no identifiable bibliographic source confirmed."
- Unverified entries must be labeled explicitly, not presented as confirmed.
- Do not invent authors, titles, dates or publications.
- When terminology diverges across methods, record the distinction instead of presenting one definition as universal.
- Do not copy long excerpts from copyrighted material; write original definitions grounded in sources.

## Utilization policy

### When to consult
- Consult the library whenever Performance is in scope (generation or review of interpretive directions).
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
