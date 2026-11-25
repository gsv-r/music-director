# Guidelines for Musical Arrangement

This file is one of the musical dimensions of music creation: Style (global
sonic identity and global movement), Arrangement (form, layers, entries, exits,
density, texture, and instrumental development), Lyrics (composition, content,
narrative, and singability), and Performance (interpretation, dynamics, and
expressive change per section). This file focuses on musical arrangement. Title
is optional identification metadata, not a dimension or a substitute for any of
the others. This organization is one possible way to present the creation; adapt
the structure to what the user requests, preserving the musical intent.

## Task limit

Do not generate, render, or produce audio or music (see
`references/instructions/orchestration.md`, Core principles). The result of this file is
exclusively textual: form, sections, layers, entries and exits, density and
texture, transitions, counterpoints, and instrumental development. These
instructions support AI collaboration, music production, and work with human
musicians.

## Shared musical context

Universal coherence requirements, user-priority rules, and correction/termination
rules are canonical in `references/instructions/orchestration.md`. For Arrangement, verify
internally that form, sections, order, relative durations, layers, entries and
exits, density, texture, transitions, counterpoints, and instrumental
development combine with the global sound and global movement of Style, with the
sung structure of Lyrics when present, with the interpretive directions of
Performance, and with the transversal intent of Creative Direction. If something
does not combine, correct it in one internal pass before delivery; report any
remaining discrepancy rather than rewriting repeatedly. Do not show this internal
analysis to the user.

## Module role and boundaries

Arrangement owns:

- Form and musical architecture: sections (sung and instrumental), their order,
  and their relative durations.
- Introductions, endings, interludes, and instrumental-only sections.
- Passages and transitions as formal events when they alter form, balance, or
  development.
- Distribution of instrumental layers and the combination of layers per section.
- Entries and exits of instruments and other layers.
- Density and texture per section.
- Counterpoints and instrumental responses.
- Instrumental development across the composition.

Arrangement does not own:

- Global sound, genre, tempo, instruments' identity, voice, or production texture
  (Style).
- Lyric content, narrative, prosody, singability, or sung text (Lyrics).
- Section interpretation, dynamics of execution, articulation, or expressive tags
  (Performance).
- Interpretive explanation of the finished composition (Analysis).
- Artistic intent as such; it materializes intent into form and layers
  (Creative Direction).

Growth by adding or removing instruments belongs to Arrangement. Growth by
intensity of execution belongs to Performance. Breakdown by withdrawing layers
belongs to Arrangement. A more contained or more intense interpretation belongs
to Performance. Performance consumes Arrangement and does not redefine layers or
entries.

## Inputs and dependencies

- **Style** is the anchor for the global sound, the instrumental palette, and the
  global movement. If Style is missing, state the gap and label assumptions; do
  not invent global sound, BPM, instruments, or production texture.
- **Lyrics**, when in scope, supplies the sung structure (sung sections and
  their order). Arrangement consumes it. If Lyrics is missing, Arrangement does
  not invent sung content; it states the gap.
- **Creative Direction**, when present, supplies transversal intent (contrast,
  density target, emotional trajectory, high-level form decisions without
  templates). Arrangement materializes it into concrete form and layers.
- **Performance** is downstream: it consumes the Arrangement timeline and produces
  execution instructions per section.
- **Analysis** is downstream of formal changes: it evaluates the result.

When the composition is instrumental (no lyrics/voice), Arrangement may propose a
section structure or timeline suited to the brief, genre, and duration. Ask only
when an indispensable structural decision cannot be inferred. Do not require a
scene, narrator, or point of view.

## Duration and structure (context for the Arrangement)

- Duration and structure are compositional decisions, configurable according to
  the brief. Respect the duration and structure defined by the brief or by the
  composition planning.
- Arrangement defines the form: sections, their order, and their relative
  durations. Absolute durations are used only when the brief provides them.
- Arrangement may add instrumental sections (introductions, interludes, endings,
  instrumental passages) without requiring lyric content.
- Changes to the sequence of sung sections require coordination with Lyrics.
- There is no default structure. Structural templates are illustrative
  possibilities, not mandatory formulas.
- Introductions, endings, and interludes are optional and exist only when they
  serve the composition.
- Transitions (modulations, pauses, drops, fills, metric changes) are formal
  events when they materially alter form, balance, or development.

## Using a reference, if provided

Follow the canonical **Musical reference protocol** in
`references/instructions/orchestration.md`. Apply the identification checklist, classify
each claim individually by evidence source and degree of interpretation, and
resolve conflicts per the protocol's triggers. Do not redefine the protocol here.

Arrangement-specific application:

- Identify, when relevant and audible: form/structure, section order, approximate
  durations, dynamics, density, instrument entries and exits, transitions,
  counterpoints, and instrumental development.
- Translate every characteristic into generic descriptors; never use artist,
  band, singer, or song names as a substitute for musical description.
- Do not copy lyrics, melody, identifiable arrangement, or excerpts.
- If the reference cannot be accessed, say so in one sentence and ask for the
  missing data, without inventing.

## Form and architecture

- Name sections when useful (`[Intro]`, `[Verse]`, `[Chorus]`, `[Bridge]`,
  `[Outro]`, `[Fade Out]`, or instrumental-only labels), but naming and section
  types are possibilities, not requirements.
- Sung and instrumental sections may coexist; an instrumental-only section is
  valid and does not require lyric content.
- The order of sections follows the intent of the composition. Do not default
  to any standard order.
- Relative durations are expressed as proportions or as roles ("brief
  introduction", "extended development"), not as mandatory timings.
- A transition becomes a formal event when it changes the perceived form,
  balance, or trajectory of the composition. Label it as such.
- An ending has intent (natural conclusion, fade, dry cut, final image, or
  other), derived from the brief, not from a default.

## Layers and entries

- The global instrumental palette comes from Style. Arrangement decides which
  layers are active in each section, how they combine, and when they enter or
  leave.
- Give a function to each important sound: pulse carrier, groove anchor,
  harmonic bed, counterline, hook, impact layer, texture glue, contrast color.
- Layer entries and exits must have a musical reason. Do not add or remove layers
  mechanically.
- Growth by adding instruments or layers is an Arrangement decision.
- Breakdown by withdrawing layers is an Arrangement decision.
- Density and texture per section (sparse vs. dense, open vs. tight, dry vs.
  reverberant) are Arrangement decisions. There is no default density for any
  section type.
- Avoid instrument lists without function. Each layer must earn its place.

## Counterpoints and instrumental responses

- Counterlines, call-and-response between instruments, and instrumental responses
  to vocal phrases (when the composition is vocal) are Arrangement decisions.
- Use them when they serve the intent; silence and stability are equally valid.
- A counterpoint must not obscure the lead or the sung text.

## Instrumental development

Before writing the arrangement, build a short internal development map: for each
section, its role and what changes versus its previous appearance (or
"intentional repetition" when repetition is the effect). The map is planning,
not output.

- Axes of change (possibilities, not obligations): number of layers, register,
  rhythmic density, space and silence, texture, harmonic color, counterpoint
  activity.
- Lyric content and perspective are owned by Lyrics; Arrangement coordinates
  with them but does not define them.
- Exact repetition is a valid artistic decision and must not be "corrected."
- Variation, when present, must have a musical reason and land where the
  composition needs it.
- Development may be progressive, circular, episodic, stable, contrastive,
  transformative, or any other shape the intent justifies. Do not force a label.

## Coordination with other modules

- **Style:** Arrangement consumes the global sound, the instrumental palette, and
  the global movement. It does not redefine genre, tempo, instruments' identity,
  voice, or production texture. Global movement belongs to Style; local density,
  entries, and exits belong to Arrangement.
- **Lyrics:** Arrangement consumes the sung structure. It may add instrumental
  sections without lyric content. Changes to the sequence of sung sections require
  coordination with Lyrics, including any needed lyric adjustments. Arrangement
  does not rewrite lyrics or sung text.
- **Performance:** Performance consumes the Arrangement timeline and produces
  execution instructions per section. Performance does not redefine layers,
  entries, or exits. Arrangement does not produce tags or interpretive directions.
- **Creative Direction:** Arrangement materializes transversal intent (contrast,
  density target, emotional trajectory, high-level form) into concrete form and
  layers. Creative Direction does not decide concrete arrangement.
- **Analysis:** Formal changes trigger the Analysis pre-delivery check (see
  "Analysis trigger" below). Analysis evaluates alignment; it does not modify
  Arrangement retroactively.

## Growth by layers versus growth by intensity

Distinguish the two kinds of crescendo and their owners:

- Crescendo by **adding instruments or layers** belongs to Arrangement.
- Crescendo by **intensity of execution** (dynamics, articulation, register,
  phrasing) belongs to Performance.
- Breakdown by **withdrawing layers** belongs to Arrangement.
- A more **contained or more intense interpretation** belongs to Performance.

When both occur, state which kind of growth applies in each section so the
responsibility is unambiguous. A performance tag must not be used to imply a
layer entry that Arrangement did not decide, and an Arrangement layer decision
must not be expressed as an execution intensity.

## Instrumental music (no lyrics/voice)

Flow: Style → Arrangement → Performance.

- Arrangement produces the form and timeline (sections, order, relative
  durations, layers, entries, exits, density, texture, transitions).
- Performance produces execution instructions per section, associated with the
  Arrangement timeline, without depending on Lyrics.
- No scene, narrator, or point of view is required.
- Analysis is not in scope for instrumental music unless explicitly requested
  and compatible with its input requirements.

## Analysis trigger

The Analysis pre-delivery check occurs when lyrics or compositional content are
created, changed, or reviewed. For Arrangement, this means:

- Formal structure is compositional content. Formal structure comprises sung
  sections, instrumental sections, the order of sections, and relative
  durations.
- Changes to formal structure trigger the internal Analysis pre-delivery check in
  both vocal and instrumental music. Materially significant changes in relative
  durations are included among these triggers.
- Changes of duration trigger Analysis only when they materially modify the
  formal arc, the balance, or the rhythm of development of the composition.
- Pure changes of layers, density, counterpoints, or transitions, without any
  change to formal structure, require a coherence verification but do not
  necessarily trigger Analysis.

In instrumental music, the visible Analysis section remains optional unless
explicitly requested or compatible with its input requirements. The internal
Analysis pre-delivery check still applies to formal structure changes.

## Humanization of arrangement descriptions

Apply the universal guardrails in `references/instructions/orchestration.md` ("Textual
humanization and singability") to arrangement descriptions. This is an editorial
sense, not a restriction list.

- **Natural, specific, musical:** descriptions should read as natural, specific,
  and musically coherent; avoid generic sequences of adjectives and
  descriptions that could fit any composition.
- **Fluency:** vary phrasing and word choice so different arrangements do not
  follow the same mold; keep descriptions concise and purposeful.
- **No loss of precision:** humanization never relaxes musical specificity
  (section roles, layer functions, entries, density, transitions).
- **No obligation:** if an arrangement description is already natural, clear,
  specific, and coherent, do not rewrite it.
- **No invention:** never add a section, layer, entry, or transition absent from
  the brief or unjustified by the composition.

## Anti-generic and common mistakes

To avoid generic arrangements:

1. Do not default to any standard section order or structure. Derive form from
   the brief and the intent.
2. Do not assign a default density to any section type.
3. Do not add layers without function or remove layers without reason.
4. Do not describe entries/exits vaguely ("builds up", "gets bigger"); name the
   audible change.
5. Do not copy a reference's form or arrangement; translate into generic
   descriptors.
6. Do not duplicate global sound (Style) or execution intensity (Performance).
7. Do not use artist, band, singer, or song names as substitutes for musical
   description.
8. Do not introduce transitions that do not alter the result.
9. Do not force development where stability is intended.
10. Keep descriptions proportional to the composition's complexity.

## Coherence with the other parts

Coherence boundaries and responsibility division are canonical in
`references/instructions/orchestration.md`. Arrangement must be coherent with Style (global
sound, palette, global movement), with Lyrics (sung structure, when present),
with Performance (interpretation per section), with Creative Direction (intent),
and with the Analysis trigger rules. Formal changes are reported to Analysis
rather than silently applied. When a Title is used, it may be derived from the
hook or central idea, according to the user's intent, and should combine with
the arrangement.

## Output format

The final presentation is adaptable. The output may be:

- A form/timeline (sections in order, with relative durations and transition
  events).
- A layer map (which layers are active per section, with entries and exits).
- Density and texture notes per section.
- Counterpoint and response notes.
- Development notes.

A common presentation groups these by section, using bracketed markers and a
blank line between sections, adapting to the destination:

```
[<section> - <audible change from this song>]
```

Use lacuna formats only. No filled tag, Style line, lyric, or arc is provided.
Adapt the presentation to the user's request and destination; templates are
illustrative, not mandatory.

**Format validation (adaptable):**

- Clearly organize the parts of the composition.
- Differentiate arrangement decisions (form, layers, entries) from sung text and
  from performance instructions.
- Preserve the musical divisions.
- Adapt the presentation to the informed destination.
- Keep a structure that is easy to copy and reuse.

## Pre-delivery check (Arrangement)

Run before delivery when Arrangement is in scope:

- [ ] Form decisions (sections, order, relative durations) are justified by the
      brief or intent.
- [ ] Instrumental sections, if any, have a musical reason.
- [ ] Layer entries and exits have musical reasons and functions.
- [ ] Density and texture per section are coherent with Style and intent.
- [ ] Transitions that alter form are labeled as formal events.
- [ ] No duplication of global sound (Style) or execution intensity
      (Performance).
- [ ] Sung structure is respected; any change to sung section sequence is
      coordinated with Lyrics.
- [ ] No standardized structure was imposed by default.
- [ ] Discrepancies, if any, are reported rather than silently corrected.
- [ ] Humanization: descriptions are specific, natural, and non-generic.

## Language selection

Arrangement descriptions use clear musical terms. The language of communication
with the user follows the language policy in `references/instructions/orchestration.md`;
arrangement descriptions are adapted to the destination when needed. Do not
default to English descriptions merely because these instructions are in
English.

## Notes

- Arrangement is guidance for interpretation and production, not a guaranteed
  command. Adherence varies by destination and by conflict with other
  directions. If a direction is not followed, reformulate or clarify the musical
  intent.
- Arrangement consults `references/library/arrangement/` when formal decisions are material
  to the task (creating, changing, or reviewing form, sections, order, relative
  durations, transitions, climax preparation or release, formal contrast,
  repetition with formal variation, or non-conventional forms). Consultation is
  targeted: pure layer, density, counterpoint, or transition revisions without
  formal change do not automatically require it. Consultation is mandatory when
  the relevant formal decision is in scope; using a retrieved concept is not
  (depends on musical adequacy). The library provides reference knowledge and
  never overrides this module.
- Arrangement consults `references/library/rhythm/` when rhythmic event density, meter,
  syncopation, or rhythmic organization materially informs a decision, even
  without formal restructuring. Changes in layer count alone do not automatically
  require Rhythm consultation. Consultation is targeted and proportional.
- Arrangement consults `references/library/production/` when texture mechanisms materially
  inform per-section decisions (e.g., dry vs. reverberant as audible texture,
  spatial width changes). Layer-count changes alone do not automatically require
  Production consultation. Consultation is targeted and proportional.
- Arrangement consults `references/library/harmony/` when harmonic changes, modulation, or
  harmonic rhythm materially inform formal decisions (e.g., cadential arrival,
  modulation as formal event, change of harmonic rhythm affecting form or
  balance). Pure layer, density, counterpoint, or transition revisions without
  harmonic implication do not automatically require Harmony consultation.
  Consultation is targeted and proportional.
- When a consulted Rhythm or Harmony entry materially informs a formal decision, write
  the decision in the arrangement — a metric change, a section's density level, a
  cadential arrival as a formal event — rather than the entry name. Harmony and Rhythm
  support decisions within this module's responsibility; they do not redefine global
  identity.
- Markers and tags are guidance for interpretation, not guaranteed commands.
  Adherence varies by destination and by conflict with other directions. If a
  direction is not followed, reformulate or clarify the musical intent.
