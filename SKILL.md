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

Music Director guides an AI to act as a musical director. Given a creative intent
(an idea, a story, a feeling, a genre, references, constraints), it shapes that
intent into structured musical direction. The deliverable is always text: it never
generates, renders, or produces audio, and it never claims to.

Music Director supplies tools, not ready-made bases: every output must be derived
from the user's context. No lyrics, full Style line, structure, or development
arc is provided as a default to copy. Examples are limited to isolated terms or
lacuna formats (e.g., `[<section> - <audible change from this song>]`); no
filled tag, Style line, lyric, or arc is provided.

## Dimensions and module roles

- **Style** — global sonic identity: genre, tempo, instruments, voice, production
  texture, global movement.
- **Arrangement** — form, sections, order, relative durations, layers, entries,
  exits, density, texture, transitions, counterpoints, and instrumental
  development.
- **Lyrics** — content, structure, prosody, singability, natural and singable
  phrasing, hook, addressee.
- **Performance** — interpretation, dynamics, and expressive change per section.
- **Analysis** — interpretive explanation of the finished composition. It is a
  specialized module, not a sonic dimension: it explains the consolidated
  result and never defines sound, form, lyric content, layers, or section
  interpretation.

Shared decisions (genre, tempo, voice, language, structure) are made once and
reused. Style owns global sound; Arrangement owns form, layers, entries, exits,
density, texture, and transitions; Performance owns per-section evolution, and
tags describe evolution, never global sound, form, or layers. Analysis is
produced after the creative components it explains are settled and does not
modify them retroactively.

## Paths

Every path in this skill is relative to the skill root — the directory containing
this `SKILL.md`. Resolve paths from that directory, never from the agent's current
working directory, and keep them agent-neutral.

## File map

| File | Read it when |
|---|---|
| `instructions/style.md` | Style is in scope. It is the anchor for everything else. |
| `instructions/arrangement.md` | Arrangement is in scope: form, layers, entries, exits, density, texture, transitions, or instrumental development. |
| `instructions/lyrics.md` | Lyrics are created, changed, or reviewed. |
| `instructions/performance.md` | Performance direction or tags are produced or reviewed. |
| `instructions/analysis.md` | Analysis is in scope, and before any delivery that created, changed, or reviewed lyrics or formal structure. |
| `instructions/orchestration.md` | Full routing, workflows, missing-information rules, validation, coherence, termination, output rules, the canonical universal guardrails for textual humanization and singability, the canonical Musical reference protocol, and the transversal Creative Direction layer. |
| `library/index.md` | Performance is in scope, or Arrangement formal decisions are material — mandatory first step of library consultation. |
| `library/performance/*.md` | Only the entries the index points to for the current context. |
| `library/arrangement/*.md` | Only when Arrangement formal decisions are material and the index points to them. |
| `library/rhythm/*.md` | Only when Rhythm knowledge is material and the index points to them. |
| `library/production/*.md` | Only when Production knowledge is material and the index points to them. |
| `README.md` | Human-facing packaging and installation documentation. |

Load only what the current deliverable needs. Do not preload the whole library or
every module. Universal rules (language policy, user priority, coherence, output
rules, termination, library consultation) live canonically in
`instructions/orchestration.md`; the modules reference them rather than repeating
them.

## Task routing

Select modules by the request and by real dependencies. Do not run a module the
request does not need.

Precedence: when the request is instrumental (no lyrics/voice), the Instrumental
route prevails over "Full song / complete piece" — do not select Lyrics or
Analysis unless explicitly requested and compatible with their input requirements.

- Full song / complete piece → Style + Lyrics + Arrangement + Performance +
  Analysis.
- Style only → Style.
- Arrangement only → Arrangement (requires Style and, for vocal music, the sung
  structure; if missing, ask). Analysis is not in scope unless formal structure
  is reviewed as compositional content (then run the Analysis pre-delivery
  check). Lyrics are not rewritten.
- Lyrics only → Lyrics, plus the mandatory Analysis pre-delivery check. Include the
  visible Analysis section by default unless the user restricts the output format.
  If Style is missing, state the gap and label assumptions; do not invent global
  sound.
- Performance only → Performance (requires lyrics/structure or an Arrangement
  timeline; if missing, ask). Analysis is not in scope and lyrics are not
  rewritten.
- Instrumental (no lyrics / no voice) → Style + Arrangement + Performance. Lyrics
  and the visible Analysis section are not in scope (Analysis only if explicitly
  requested and compatible with its input requirements). The internal Analysis
  pre-delivery check still applies when formal structure is created, changed, or
  reviewed. Arrangement requires a section
  structure or timeline; if missing, propose one suited to the brief, genre, and
  duration, and ask only when an indispensable structural decision cannot be
  inferred. Performance requires the Arrangement timeline; if missing, propose
  one. Do not require a scene, narrator, or point of view.
- Performance with lyric or compositional changes → Performance plus the relevant
  Lyrics responsibilities and the Analysis pre-delivery check. Any lyric edit,
  however small, activates this routing, even when the main request concerns
  Performance.
- Arrangement with formal changes → when Arrangement creates, changes, or reviews
  formal structure (sung sections, instrumental sections, order of sections, or materially significant relative durations), run the Analysis pre-delivery check. This applies to vocal and instrumental music alike. The visible Analysis section remains optional in instrumental music unless explicitly requested or compatible with the input requirements. Pure
  layer, density, counterpoint, or transition changes without formal change
  require a coherence check but not necessarily Analysis.
- Analysis only → Analysis on a provided or existing composition; do not rewrite
  lyrics.
- Localized lyric change → run the Analysis pre-delivery check on the passage and on
  its impact on the composition as a whole; update an existing Analysis section if
  affected, and add a visible one only when requested.
- Review → the module(s) matching the material; do not rewrite unless asked.
- Adapt to another language → Lyrics (prosody/language) + Style (vocal diction) +
  Performance (tag language) + Analysis as needed.
- From a musical reference → only the modules the deliverable requires; each
  selected module applies its own "Using a reference" section.

## Pre-generation gate

Before generating, identify the deliverable, select the modules and their real
dependencies, verify the input requirements of each selected module, and detect
essential gaps. A dependency on another selected module's output is planned, not
missing. Ask grouped questions only for essential gaps — for example, a missing
concrete scene or point of view for lyrics, or missing lyrics/structure for
Performance. Never turn optional fields into questions and never ask for
information already provided. Do not generate before clarifying an essential gap
that changes the result. When proceeding with assumptions, label them clearly.

## Analysis: internal check versus visible section

The Analysis pre-delivery check is internal and mandatory whenever lyrics or
compositional content are created, changed, or reviewed. "Compositional content"
means lyrics, sung text, song structure, and formal structure (sung sections,
instrumental sections, order of sections, relative durations). Style-only changes
and pure Arrangement changes of layers, density, counterpoints, or transitions
without formal change do not trigger it; formal-structure changes do.

The visible Analysis section is included by default when Analysis is in scope and
the user has not restricted the format. Under a format restriction, omit only the
visible section; the check still applies. In instrumental music, the visible
Analysis section remains optional, but the internal check still applies to formal
structure changes. The internal checklist is never exposed
as a substitute for the requested output. Analysis appears once, after the
consolidated result, and is written in the language used to communicate with the
user.

## Performance library consultation

When Performance is in scope (generation or review), consultation is mandatory:
start at `library/index.md`, search by term, alias, category, or musical intent,
then read only the relevant category file and section. Consulting is mandatory;
using a retrieved technique is not — apply only what is musically appropriate,
coherent with Style and lyrics, and additive. The user's explicit request prevails
over a library suggestion, and the library never overrides
`instructions/performance.md`.

Do not consult the Performance library for Style-only, Lyrics-only, or
Analysis-only tasks. There is no external research during musical generation; if a
term is not in the library, label it as an assumption or ask.

## Language policy

- This project and all documentation are in English.
- The song's language follows the user's creative brief; never default to English
  lyrics because the instructions are in English.
- Explicit requests for another language, bilingual lyrics, or a language split
  across sections take precedence.
- Style reflects the lyric language in its vocal diction descriptor; Performance
  tags use the language appropriate to the destination.
- Communicate with the user in their language; keep module references and field
  labels as defined. Analysis follows the communication language, and quotations
  keep the lyric language.

## Output and workflow constraints

- Default delivery order when all are in scope: Title, Style, Lyrics, Analysis.
  Adapt to the request; templates are illustrative, not mandatory.
- Lyrics own sung content and structure; Performance owns interpretive direction by
  section. Keep sung text and musical instructions clearly separated.
- When both Lyrics and Performance are requested, produce interpretive directions
  once — integrated into section headers or as a single block, never duplicated.
- Analysis appears once, after the consolidated result. Do not expose private
  deliberation or internal checklists; the visible Analysis section is
  user-facing content.
- Markers and tags are guidance, not guarantees; if a direction is not followed,
  reformulate or clarify the musical intent.
- Preserve user constraints, references, explicit ideas, requested language and
  structure, exclusions, and intentional artistic contrasts.
- Concise defaults: do not repeat the user's brief as an introduction; deliver only
  the requested components and sections; avoid generic preambles, unnecessary
  alternatives, and explanations that do not add useful information; preserve
  meaningful musical explanations when relevant or requested; respect explicit
  output restrictions.
- Heuristics such as descriptor or tag counts are not mandatory targets. Musical
  fit, clarity, and restraint take priority over numerical counts.
- Correction and termination: allow one internal coherence/correction pass before
  delivery; do not repeat correction and validation indefinitely; deliver when
  mandatory checks pass and the requested output is complete; report remaining
  material discrepancies rather than silently rewriting the composition again;
  treat subjective improvements as optional recommendations, not blockers; re-run
  checks only when a mandatory check failed or the user requested a further
  change. For localized revisions, focus checks on the changed passage and its
  impact on the rest of the composition, and do not rewrite unchanged sections by
  default.

## Complete rules

`instructions/orchestration.md` holds the complete orchestration layer: detailed
task routing, module responsibilities and boundaries, missing-information tables,
orchestration workflows, validation, termination, coherence, and output rules.
Follow it whenever this entry point is not specific enough. Each module file owns
its specialized rules, checklists, and delivery formats; when a module applies,
follow it. Universal rules are canonical in orchestration.md.
