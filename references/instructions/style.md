# Guidelines for sonic identity

Music creation has four dimensions: Style (global sonic identity and global movement), Arrangement (form, layers, entries, exits, density, texture, and instrumental development), Lyrics (composition, content, narrative, and singability), and Performance (interpretation, dynamics, and expressive changes). This file covers global sonic identity. Title is optional identification metadata, not a dimension or a substitute for any of the others. This organization is one way to present a creation; adapt it to what the user requests while preserving the musical intent.

## Task limit

Do not generate, render, or produce audio or music (see `references/instructions/orchestration.md`, Core principles). The output of this file is textual only: a Style description. A concise single line is common, but presentation may vary. These instructions support AI collaboration, music production and work with human musicians.

## Shared musical context

Universal coherence requirements and user-priority rules are canonical in
`references/instructions/orchestration.md`. For Style, verify internally that genre, tempo,
instruments, voice, and atmosphere combine without contradictory descriptors, and
that no element clashes with the musical proposal without justified intent. If
something does not combine, correct it in one internal pass before delivery; report
any remaining discrepancy rather than rewriting repeatedly (see orchestration.md,
"Validation and termination"). Do not show this internal analysis to the user.

## Duration and structure (context for the Style)

- Duration and structure: respect the duration and structure defined by the brief or by the composition planning. Style must support the form established by Arrangement and by the brief or creative planning; it does not define that form.
- Style defines the global sonic identity and the global trajectory; Arrangement defines the form, layers, entries, exits, density, texture, and instrumental development; Performance defines the interpretation, the dynamics, and the expressive changes per section. Avoid overlapping responsibilities.
- The Style must support the chosen structure and describe the global trajectory that actually belongs to this composition. Do not duplicate the arrangement decisions of Arrangement or the performance direction of Performance.

## Using a reference, if provided (absorb without copying)

Follow the canonical Musical reference protocol in
`references/instructions/orchestration.md`. Apply the identification checklist, classify
each claim individually by evidence source and degree of interpretation, and
resolve conflicts per the protocol's triggers. Do not redefine the protocol here.

Style-specific application:
- Translate the reference into generic descriptors (timbre, way of singing,
  genre, era, instruments, groove, tempo, texture, dynamics). Never use artist,
  band, singer, or song names as a substitute.
- Give a function to each important sound using the instrument-role vocabulary
  in "Style rules".
- Describe how the singer sings, never who it is. Do not ask to copy melody or
  arrangement.
- If the reference cannot be accessed, say so in one sentence and ask for the
  missing data (genre, BPM, voice type, etc.), without inventing.
- Movement and development direction come from the brief/composition, not from
  the reference by default.

## Style rules

- Present the Style as a concise description; a single line with comma-separated terms is common, but adapt the presentation to the user's request.
- Size: adapt length to the request; keep only what adds value.
- Formula (order, from most to least important): genre and subgenre + era (if it changes the sound) + mood + tempo (feel/bpm) + main instruments (with function) + production texture (when it audibly shapes the result) + vocal direction + movement of the song.
- Musical terms: use musical terms (crescendo, legato, vibrato, reverb etc.) when they make an audible difference; do not employ a technical term merely to make the prompt sound sophisticated.
- Geographic, cultural, or temporal scene (optional): include only when it audibly shapes the sound, as a modifier rather than a substitute for musical description (e.g., "Detroit techno", "Nashville country", "80s synth-pop", "Brazilian deep house").
- Production texture: prefer audible, concrete descriptors. Equipment, instrument, amplifier, synthesizer, drum-machine, or recording-technique references are useful only when they change the result; do not add them merely to make the prompt sound technical (e.g., "close-mic vocals", "tape saturation", "spring reverb", "room bleed", "TR-808-style sub-bass"). Vague adjectives such as "polished", "modern", "powerful", "cinematic", "emotional", or "epic" are acceptable when anchored to concrete musical characteristics (instrumentation, tempo, groove, dynamics, texture, arrangement); otherwise replace them with one or more specific audible characteristics or omit them.
- Example (illustrative, single field): `Brazilian Portuguese vocals` (vocal diction descriptor), `120 bpm` (tempo). Full Style lines are never given as a copyable example; build them from the brief.
- Voice (gender): define according to musical intent, brief and sonic identity. When there is no specification, do not presume gender, timbre, intensity or vocal aesthetic.
- Language and diction: the lyric language follows the language policy in `references/instructions/orchestration.md`; the Style must reflect that language in its vocal diction (e.g., `Brazilian Portuguese vocals`, `English vocals`, `Spanish vocals`). Include this descriptor whenever the language is known.
- Describe the voice concretely, never with vague terms like "beautiful voice". Combine timbre + way of singing + emission technique:
  - Timbre: warm, bright, dark, smoky, raspy, gritty, velvety, airy, breathy, clear.
  - Way of singing: intimate, conversational, whispered, restrained, expressive, powerful, melodic, laid-back, subtle vibrato, sustained notes, layered harmonies.
  - Emission techniques (use only those that are heard): legato, staccato, vibrato, straight tone, belting, falsetto, melisma, runs, twang, breathy singing, grit/rasp, cry/sob, dynamic contrast, pitch bending, mixed voice, vocal fry, whistle register, growl, glottal stop, messa di voce, vowel modification.
  - Do not accumulate descriptors that contradict each other (e.g., whispered + powerful belting).
- Arrangement movement (global only): describe the global trajectory that actually belongs to this composition: it may be progressive, circular, episodic, stable, contrastive, transformative, or any other shape the intent justifies. Build, drop, breakdown, final surge and afterglow are possible descriptors, not required elements. Section-by-section form, layers, entries, exits and layer density belong to Arrangement; Performance describes execution and expressive behavior. Do not duplicate either here.
- Development direction (when it changes the result): describe, in one short phrase, how the composition develops when that shapes the global movement: for example, repetition-as-identity evolving through layers, subtraction, filter, space or late entry; a clear arc; or wide dynamic range with pauses and strong interpretation. These are illustrative references drawn from musical practice, not a classification system and not a mandatory label. Do not force the music into `hypnotic/loop`, `song-based` or `dramatic`; leave it unclassified when none of those references adds value. Discover the development from the identity and intent of this specific composition. The development direction is internal planning for the trajectory; it is not a Suno "Style of Music" tag, not a required prompt term, and it is not exported to the Suno Style field unless the user asks. It does not replace Performance's per-section plan or duplicate its tags.
- Instrument roles (when useful): pulse carrier, groove anchor, harmonic bed, counterline, hook, impact layer, texture glue, contrast color. Give a function to each important sound.
- When the user does not indicate another direction, do not impose a vocal or instrumental aesthetic; define the direction according to musical intent and the provided references.
- Follow the user's musical direction. Do not add genres or instruments they did not ask for. Do not mix incompatible genres.
- Fusion: combine at most 2 to 3 genres; one anchor + modifiers (e.g. "indie folk with subtle synth-pop textures"). Avoid lists of contradictory genres.
- Contextual coherence: do not introduce elements (instruments, voices, styles, textures) that clash with the proposal without clear intent. Experimental variations only when the user requests or justifies them.
- Use clear musical terms. English is commonly used for Style descriptions, but adapt the language to the user's request and destination when needed.
- Do not use artist, band, singer or song names as a substitute for describing musical characteristics. Describe the desired musical characteristics directly (timbre, way of singing, genre, era, instruments, groove and tempo).
- BPM and key: if the user does not specify, choose a plausible value for the genre and mood instead of omitting.
- Multiple options: vary the musical premise (acoustic/intimate, polished pop, dark cinematic, dance/club, live band, retro era); do not just swap adjectives.
- Descriptors: prefer specific musical descriptors over generic adjectives ("epic", "beautiful"). Aim for 4 to 7 specific descriptors. This does not relax the fusion limit of at most 2 to 3 genres. (Heuristic: counts are not mandatory targets; musical fit takes priority.)
- Exclusions: at most 2 to 3 (e.g., "no strings", "no reverb"), placed at the end of the Style field.
- Effects in natural musical language: describe effects as audible descriptors (e.g., "reverb-heavy vocals", "dry intimate vocal", "vocoder"), never as parameters or structured/JSON data.
- No DAW parameters in outputs: do not use percentages, dB, ms or Hz in the final Style; use musical terms.
- Beat: BPM is always accompanied by a tempo word + groove + drum pattern (e.g., "110 BPM, mid-tempo drive, shuffle, brushed drums"). Groove vocabulary: four-on-the-floor, halftime, shuffle, one-drop. Human feel: laid-back/pushed, behind or ahead of the beat.
- Field separation: the style field carries genre, instruments and vocal; lyric words and section tags belong to the lyrics field, not to Style. Short ad-libs (1-3 syllables, in parentheses) belong to the lyrics field (see `references/instructions/lyrics.md`).

### Platform note (Suno)
Empirical guidance (may change with model version; not an official Suno specification, so treat it as unconfirmed): reliable controls are vocal genre, delivery mode (whisper/rap/belt/speech), BPM and basic texture; named effects and performance tags are suggestions; DAW-style parameters are placebo. Style Influence is an external control outside the text: Loose for exploration, Strong for adherence. Official Suno documentation prevails over this note and over third-party guides.

## Language selection

The Style is written in clear musical terms. The lyric language follows the language policy in `references/instructions/orchestration.md` (and `references/instructions/lyrics.md`); never default to English lyrics simply because the Style is written in English. Reflect the chosen lyric language in the vocal diction descriptor (e.g., `Brazilian Portuguese vocals`).

## Good style practices (reference)

Based on musical practices and vocabulary (reference):
- Combine tempo terms with genres (e.g. "upbeat allegro pop", "slow adagio ballad").
- Use dynamics to shape emotional intensity ("crescendo into powerful chorus").
- Specify instrumentation for desired textures ("sparse piano and vocals" vs. "dense orchestral arrangement").
- Mix structural terms to guide form ("verse-chorus-verse with extended bridge").
- Layer production effects for atmosphere ("reverb-heavy ambient soundscape").
- Mix genres creatively, with anchor + modifiers ("jazz-influenced hip-hop with soulful vocals").

### Humanization of Style descriptions

Apply the universal guardrails in `references/instructions/orchestration.md` ("Textual humanization and singability") to the Style description. Use these as editorial guidance rather than fixed rules.

- Natural, specific, musical: descriptions should read as natural, specific, and musically coherent; avoid generic sequences of adjectives and descriptions that could fit any song.
- Fluency: vary phrasing and word choice so different Style lines do not follow the same mold; keep the line concise and purposeful.
- No loss of precision: humanization never relaxes musical specificity (BPM, instrument function, timbre, groove, texture). Keep concrete descriptors.
- No obligation: if a Style description is already natural, clear, specific, and coherent, do not rewrite it.
- No invention: never add genre, instrument, era, or production trait absent from the brief or unjustified by the reference.

## Anti-generic and common mistakes

To avoid generic results:
1. Do not use three generic adjectives ("beautiful, emotional, epic"). Replace them with one or more specific audible characteristics (e.g., "warm sub-bass", "driving four-on-the-floor kick").
2. Give a function to each sound (see "Instrument roles" in "Style rules").
3. Vary the musical premise, not just adjectives (acoustic/intimate vs. polished pop vs. dark cinematic vs. dance/club vs. live band vs. retro era).
4. Use concrete BPM instead of "fast/slow" when the genre calls for it.
5. Describe the voice as timbre + way of singing + technique, never "beautiful voice".
6. Indicate global trajectory and global movement (build, drop, breakdown, final surge, afterglow) when it changes the result; form, layers, entries, exits, and local density belong to Arrangement; interpretation, dynamics, and local expressive changes belong to Performance.
7. Keep indispensables + optionals only if they change the result.
8. Avoid contradictory descriptors, instrument lists without function, decorative technical terms, elements that clash with the proposal, using artist names as substitutes for musical descriptions, generic or excessively long Style.
9. Do not add equipment names merely to make the prompt look technical; follow the "Production texture" guidance in "Style rules" and include concrete references only when they audibly shape the result.

## Base Style model (essential)

Use this model as a reference. Each element must have justification; remove what does not add value.

Core elements (4 essentials):
1. Genre/subgenre (anchor).
2. BPM (or tempo feel).
3. 2 to 3 main instruments, with function (e.g., "synth lead", "808 bass").
4. Voice: timbre + way of singing (e.g., "low dark talk-sing").

Optional (only if they change the result):
- Production/recording detail: when it audibly shapes the result, use 1 to 2 concrete, purposeful terms (e.g., "close-mic vocals", "tape saturation", "spring reverb", "room bleed", "TR-808-style sub-bass", "JUNO-style pads"). Vague terms such as "polished modern" are acceptable only when anchored to concrete characteristics.
- Era/scene (e.g., "80s synth-pop").
- Global movement (e.g., "spacious build into drop").
- Technical terms from the glossary (e.g., "legato", "vibrato"), only if audible.
- Extra instrument roles (counterline, hook, impact).

Avoid:
- Long instrument lists without function.
- Decorative technical terms.
- Contradictory descriptors.
- Elements that clash with the proposal (contextual coherence).

## Illustrative style skeleton (not a template or default)

`[Style] <genre/subgenre>, <tempo>, <instrument (function)>, <instrument (function)>, <voice: timbre + way of singing>, <production texture if audible>, <vocal diction descriptor>`

Fill each slot from the brief or reference. No genre, BPM, instrument or voice is prescribed. Single-field illustrations (e.g., `Brazilian Portuguese vocals`) may appear elsewhere as illustrations only.

## Coherence with the other parts

Global coherence requirements, responsibility boundaries, and correction/termination rules are
canonical in `references/instructions/orchestration.md`. Style defines the global sound and global
movement; Arrangement owns form, layers and layer density per section; Performance describes how
parts are executed. Do not duplicate between them.
The lyrics must sound coherent with the Style (genre, voice, tempo). When a Title is used, it
may be derived from the hook or central idea, according to the user's intent, and should
combine with the Style.

## Library consultation

Style consults the library only when the relevant decisions are material.
Consultation is targeted and proportional, not automatic for every Style task.
The library provides reference knowledge and never overrides this module.

- `references/library/rhythm/` when groove and rhythmic identity decisions are
  material (swing/straight feel, shuffle, backbeat, syncopation, groove, rhythmic
  density, simple/compound meter).
- `references/library/production/` when production-texture descriptors are
  material (ambience, spatiality, saturation, reverb, delay/echo, compression).
- `references/library/harmony/` when harmonic identity is material (tonal center,
  key, mode/scale, chord color, harmonic rhythm, modulation,
  non-functional/static harmony).

When harmonic or rhythmic identity is material, make the global decision identifiable
in the Style: for example, a tonal center with its modal color, or a groove with its
meter and subdivision. These are concrete choices, not generic descriptors. Do not
repeat per-section decisions here: layer distribution, density and development belong
to Arrangement, and local execution belongs to Performance. No default progression,
meter or groove is implied; omit what does not change the result.

## Output format

The global final delivery format is canonical in `references/instructions/orchestration.md`, "Final delivery format (mandatory)". In a final answer, this module's content is written into the `[STYLE]` field; there is no separate Style document and no text outside the four fields. Inside the field, present a concise Style description. A single comma-separated line is common, but adapt the presentation to the user's request and destination. Treat the description as guidance for interpretation, not a guaranteed command; adherence varies by destination and by conflict with other directions. If a direction is not followed, reformulate or clarify the musical intent.
