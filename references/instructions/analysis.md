# Guidelines for Analysis (interpretive explanation)

Music Director has four musical dimensions: Style (global sonic identity and global movement), Arrangement (form, layers, entries, exits, density, texture, and instrumental development), Lyrics (composition, content, narrative, and singability), and Performance (interpretation, dynamics, and expressive changes per section). It also has a specialized module, Analysis. Analysis is not itself a musical dimension. It does not define sound, form, lyric content, layers, or section interpretation. It explains the composition that has already been produced. Title is optional identification metadata, not a dimension and not a substitute for any of the musical dimensions or for Analysis. Adapt this organization to what the user requests while preserving the musical intent.

## Task limit

Do not generate, render, or produce audio or music (see `references/instructions/orchestration.md`, Core principles). The result of this file is exclusively textual: an interpretive explanation of the finished composition. These instructions support AI collaboration, music production and work with human musicians.

## Shared musical context

Universal coherence requirements, user-priority rules, and correction/termination rules are canonical in `references/instructions/orchestration.md`. For Analysis, verify internally that Style, Arrangement, Lyrics, and Performance combine (when available), that the sung text or formal structure, hook, and addressee (when applicable) are the object of the explanation, that tags and per-section dynamics describe evolution, that prosody aligns all elements, that the addressee stays consistent, and that every statement is traceable to an observable element of the finished composition or to the user's brief. After the single internal coherence pass allowed by `references/instructions/orchestration.md`, if Style, Arrangement, Lyrics, and Performance still do not combine, identify and explain the discrepancy in the Analysis instead of silently correcting it or rewriting those modules. A reported discrepancy is not, by itself, a failed mandatory check; it does not reopen the correction pass, trigger another Analysis cycle, or cause indefinite validation (see `references/instructions/orchestration.md`, "Validation and termination"). Analysis does not alter Style, Lyrics, or Performance retroactively. When Analysis is part of the request, present the final Analysis section to the user. Do not expose private deliberation, internal checklists, or hidden reasoning.

## User guidance (short reminder)

User instructions have priority; incorporate them across Style, lyrics, performance and Analysis, not as isolated comments. The documentation guides but does not limit the user; seek balance if they conflict with good practices. If used alone (a finished lyric provided by the user), state the missing global context and label assumptions; do not invent it. If the user restricts the format (e.g., "only the lyrics"), omit the visible Analysis section only; the Analysis pre-delivery check remains mandatory whenever lyrics or compositional content were created, changed, or reviewed.

## Input requirements

Analysis requires the finished composition. Its minimum input is the Lyrics (the sung text and structure) for vocal music, or the Arrangement timeline (form, sections, and layers) for instrumental music; no lyric content is invented for instrumental music. Style, Arrangement, and Performance are used when available and enrich the explanation (context, global sound, form and layers, per-section evolution). When a dimension is not available:
- Do not invent its content to fill the gap.
- State the gap briefly ("Style not provided; global sound not referenced", "Arrangement not provided; form and layers not referenced").
- Base the explanation on what is available (the lyrics or the arrangement, and the brief if provided).

If no lyrics and no arrangement are available, Analysis cannot be meaningfully produced; ask for the composition (lyrics or arrangement) instead.

Staged deliveries and localized changes: run the pre-delivery check on the final composition and, for localized changes, on the changed passage and its impact on the whole. Do not add a new visible Analysis section by default; update an affected one, and add a new section only when the user requests it. If the user restricts the format, omit the visible section and keep the check (see "User guidance" above).

## Purpose

Analysis explains interpretatively the composition that has effectively been produced. It is not a summary of the lyrics and it must not expose the AI's private internal reasoning.

Analysis answers, when pertinent: what the composition proposes, what it means, in what context it operates, how it is narratively constructed, and how its emotion evolves. It explains creative intent that is supported by the user's brief or inferable from observable choices in the result (for example, how contrasts between verses and choruses, narrative perspective, images, dynamics, or structure contribute to what the song communicates). It does not explain decisions that were merely considered during creation, nor does it reveal private reasoning or behind-the-scenes justifications not sustained by the brief or the result.

## Responsibilities

Analysis may explain, when pertinent, the following topics. They are possibilities, not mandatory fields. Use only those that apply to the composition at hand; omit the rest. A short, simple song may need only two or three.

1. **Premise and Context**: the creative premise and the context (user's brief, situation, genre, atmosphere, references absorbed into generic descriptors).
2. **Narrative Arc**: the narrative arc (beginning, development, climax, resolution), only when the composition has one.
3. **Speaker and Perspective**: who speaks, to whom, from what grammatical person (first/second/third), and how that perspective is positioned.
4. **Core Meaning and Themes**: the central meaning and the themes the composition carries.
5. **Imagery and Metaphors**: the images and metaphors used and their role in the composition.
6. **Emotional Progression**: how the emotion evolves section by section.
7. **Hook Interpretation**: what the hook means and why it concentrates the thesis of the composition.
8. **Creative Alignment with the User's Brief**: how the result corresponds to (or diverges from) the original brief, including intentional or unintentional divergences.

Section roles (when pertinent): explain the role of verses, choruses, bridges, and other sections when doing so helps the user understand the composition. Do not impose a mechanical comment on every line or section; keep the explanation proportional to the complexity of the song.

## Fundamental rules

- **Fidelity to the finished composition.** Every statement about images, scene, events or characters must be supported by a line of the lyrics or a phrase of the brief. If no line or phrase supports it, remove the statement or label it explicitly as inference ("possible reading: ...", "may suggest ..."). Do not describe a composition that was not produced. Verify against the final version as it will be delivered (Lyrics, Arrangement, Style, Performance, Production and any other relevant decision, together with the brief), not against an earlier draft.
- **Differentiate explicit from possible.** Elements that are explicitly in the lyrics are presented as facts ("the lyrics mention X"). Possible interpretations are presented as possibilities ("may suggest Y", "one possible reading is..."). Never present an interpretation as a fact.
- **Do not invent events, characters or relationships.** If an event, character or relationship is not in the composition, do not add it. If something is inferred, label it as an inference.
- **Do not confuse the speaker with the user.** The "I" of the lyrics is a speaker/character, a construction. It is not the user, even when they coincide. Do not attribute to the speaker knowledge the lyrics do not give them.
- **Recognize abstract and non-narrative lyrics.** If the lyrics do not tell a linear story, say so. Describe what the lyrics *do* (images, repetitions, patterns, fragments) instead of inventing what they *tell*.
- **Do not force a narrative arc.** Use "Narrative Arc" only when the composition has one. For abstract/conceptual compositions, omit it or describe the absence explicitly.
- **Do not reproduce the whole lyric.** Cite a short verse (up to one line) only when necessary to anchor an interpretation. Do not paste the entire lyric into the Analysis.
- **Do not praise generically.** Avoid vague adjectives ("beautiful", "moving", "touching"). If praise appears, it must be specific and anchored ("the hook concentrates the theme in five words").
- **Do not invent justifications.** Do not say "X was chosen because Y" when Y does not appear in the result. Describe what is in the result, not the process that produced it.
- **Do not duplicate Style or Performance.** Analysis does not redescribe the global sound (genre, BPM, instruments, voice) nor per-section tags. It may reference them; it does not repeat them.
- **Evaluate alignment with the original brief.** State how the result corresponds to the brief, and flag divergences (intentional or not).
- **Proportionality.** The Analysis must be proportional to the complexity of the composition. A short, simple composition gets a short Analysis. A dense composition gets a more detailed one. The Analysis should not be longer than the composition without justification.
- **No internal reasoning.** Do not expose the AI's private deliberation ("I decided to...", "I considered..."). Explain the result, not the process.

## Using a reference, if provided

Follow the canonical Musical reference protocol in `references/instructions/orchestration.md`. Analysis may mention the reference's influence only in generic terms (absorbed into descriptors), never by artist/song name, and only when it is observable in the result. Each claim about the reference must be classified individually by evidence source and degree of interpretation; do not present inferences or metadata as directly observed characteristics. Do not invent reference-derived justifications that do not appear in the composition.

## Analysis rules

### Premise and Context
- State the creative premise in one or two sentences, grounded in the user's brief and the observable result.
- Include context (genre, atmosphere, situation) only when it shapes the explanation. Do not redescribe the Style.
- When the brief is short, mark the premise as inferred from the composition.

### Narrative Arc
- Do not force a narrative arc. Use the Narrative Arc topic to describe an arc only when the composition has one; otherwise, omit the topic or state briefly that no explicit narrative arc is present.
- Identify beginning, development, climax and resolution as they appear in the sections.

### Speaker and Perspective
- Identify the grammatical person of the speaker (first, second, third) and the addressee.
- Flag perspective shifts when they occur ("the bridge shifts from 'I' to 'you'").
- Do not attribute to the speaker knowledge the lyrics do not provide.

### Core Meaning and Themes
- State the central meaning in one or two sentences.
- List the themes the composition carries, grounded in observable elements.
- Distinguish the stated thesis (often in the hook) from implied themes.

### Imagery and Metaphors
- Identify the concrete images and metaphors used.
- Explain their role (grounding, contrast, escalation, ambiguity).
- Note when a metaphor is ambiguous or carries a double meaning, and present both readings as possible without privileging one.

### Emotional Progression
- Describe how the emotion evolves section by section, using the lyrics (and Performance tags when available) as evidence.
- Use observable markers (words, images, register changes) rather than asserted feelings.
- Do not duplicate Performance's per-section tags; reference them when useful.

### Hook Interpretation
- Explain what the hook means and how it concentrates the thesis of the composition.
- Note why it is memorable (position, repetition, contrast, brevity) when observable.
- Do not redescribe the melody or harmony; those belong to Style/Performance.

### Creative Alignment with the User's Brief
- State how the result corresponds to the brief.
- Flag divergences, intentional or not, and whether they serve the composition.
- When the brief is very short, keep this section short and mark inferences.

### Humanization of Analysis

Apply the universal guardrails in `references/instructions/orchestration.md` ("Textual humanization and singability") to the Analysis. Treat these as editorial guidance, not a set of hard restrictions.

- **Contextualized and specific:** observations should be specific to this composition; avoid superficial, repetitive comments or mere reformulation of information already present in the lyrics, Style, or Performance.
- **No duplication:** each topic must add something new; do not redescribe global sound or per-section tags.
- **No obligation:** if an observation is already natural, clear, and specific, do not rewrite it.
- **No invention:** never add events, characters, relationships, or meanings absent from the composition or the brief.

## Anti-generic and common mistakes

The fundamental rules above and the pre-delivery check below cover the common failure modes: generic praise, private reasoning, invented content, forced arcs, unmarked interpretations, unnecessary lyric reproduction, duplication of other modules, and disproportionate length. Apply them to every topic; do not add generic or unsupported observations.

## Coherence with the other parts

Coherence boundaries are canonical in `references/instructions/orchestration.md`. Analysis is produced after Style, Arrangement, Lyrics, and Performance are settled; it explains the consolidated result. Analysis must be coherent with Style (genre, voice, tempo, atmosphere): do not say "upbeat and celebratory" if the Style is melancholic, unless the lyrics create an intentional contrast (then flag it). Analysis must be coherent with Arrangement (form, layers, density, transitions): do not describe a formal arc the Arrangement does not support. Analysis must be coherent with Lyrics: every claim about content must be traceable to the lyrics. Analysis must be coherent with Performance: per-section emotional claims must match the tags when available. Analysis does not modify the other modules retroactively. If a discrepancy is found, report it; do not silently rewrite the lyrics, arrangement, or tags. When a Title is used, it may be derived from the hook or central idea, according to the user's intent, and should combine with the Analysis.

## Output format

Present the Analysis after the creative components it explains. An explicit user request for a different final format prevails. The internal organization is adaptable. Presentation in the fixed delivery format follows `references/instructions/orchestration.md`, "Final delivery format (mandatory)". A common checklist of topics is:

```
- Premise and Context: ...
- Narrative Arc: ...
- Speaker and Perspective: ...
- Core Meaning and Themes: ...
- Imagery and Metaphors: ...
- Emotional Progression: ...
- Hook Interpretation: ...
- Creative Alignment with the User's Brief: ...
```

Format rules:
- Include only the topics that apply; omit the rest. Do not force all eight.
- Each topic in 1 to 4 sentences.
- Short verse citations in quotes, in the language of the lyrics, only when needed to anchor.
- Language: Analysis is written in the language used to communicate with the user, unless the user requests another. Do not confuse with the lyric language.
- Do not reproduce lyrics or Style content inside the Analysis; short anchoring citations are enough.
- Adapt the presentation to the user's request; templates are illustrative, not mandatory.

Format validation (adaptable):
- Clearly organize the parts of the composition.
- Differentiate Analysis from sung text and from musical instructions.
- Preserve the musical divisions.
- Adapt the presentation to the informed destination.
- Keep a structure that is easy to copy and reuse.

## Analysis pre-delivery check

This is the canonical detailed definition. Orchestration and SKILL summarize it.

Run this check before every delivery whenever lyrics or compositional content were created, changed, or reviewed, regardless of whether the visible Analysis section is delivered. The check evaluates the composition and the content effectively produced or revised; it is never conditioned on producing the visible section.

Applicable in every run, whether or not the Analysis section is shown:
- [ ] Analysis is faithful to the finished composition: every concrete claim is traceable to the final consolidated composition as delivered (Lyrics, Arrangement, Style, Performance, Production and other decisions) or to the brief; re-read the final version after the last revision before checking, so details from earlier drafts cannot remain.
- [ ] Explicit elements are presented as facts; interpretations are marked as possible.
- [ ] No invented events, characters, relationships or meanings.
- [ ] Speaker is not confused with the user.
- [ ] Abstract/non-narrative lyrics are recognized as such; no forced arc.
- [ ] No invented justifications.
- [ ] No duplication of Style or Performance content.
- [ ] Alignment with the brief is evaluated.
- [ ] Proportional to the composition's complexity.
- [ ] Humanization: observations are specific and contextualized, not superficial reformulation; no generic praise.
- [ ] No private internal reasoning exposed.

Applicable only when the Analysis section will be shown:
- [ ] Only applicable topics are included.
- [ ] Analysis appears once, after the consolidated result.
- [ ] No full lyric reproduction; only short anchoring citations.

A format restriction may omit the visible section when the user explicitly requests a different final format; otherwise the canonical delivery format in `references/instructions/orchestration.md` applies. It never disables the criteria applicable in every run. The internal checklist is never exposed as a substitute for the requested output.

## Language selection

- Analysis is written in the language used to communicate with the user, unless the user explicitly requests another. The language of the instructions does not impose the language of the Analysis.
- When the composition's lyrics are in another language, quote short fragments in the lyric language and explain in the communication language, unless requested otherwise.
- Preserve the natural phrasing and cultural nuances of the quoted fragments. Do not translate quotes unless the user asks.

## Notes

- Analysis is interpretive guidance, not a guaranteed or definitive reading. Interpretations are possibilities; the listener's reading may differ.
- Analysis does not require consultation of the `references/library/`. If narrative/interpretive reference knowledge is later needed, it should follow the same convention under `references/library/analysis/`, created only when needed.
- Markers and tags are guidance for interpretation, not guaranteed commands. Adherence varies by destination and by conflict with other directions. If a direction is not followed, reformulate or clarify the musical intent.
