# Guidelines for Sonic Identity

This file is one of the three musical dimensions of music creation: Style (global sonic identity, musical architecture and overall trajectory), Lyrics (composition, content, narrative and singability) and Performance (interpretation, dynamics and expressive changes). This file focuses on global sonic identity. Title is optional identification metadata, not a fourth dimension or a substitute for any of the three. This organization is one possible way to present the creation; adapt the structure to what the user requests, preserving the musical intent.

## Task limit

Do not generate, render, or produce audio or music (see `instructions/orchestration.md`, Core principles). The result of this file is exclusively textual: a Style description. A concise single line is common, but presentation may vary. These instructions support AI collaboration, music production and work with human musicians.

## Shared musical context

Universal coherence requirements and user-priority rules are canonical in
`instructions/orchestration.md`. For Style, verify internally that genre, tempo,
instruments, voice, and atmosphere combine without contradictory descriptors, and
that no element clashes with the musical proposal without justified intent. If
something does not combine, correct it in one internal pass before delivery; report
any remaining discrepancy rather than rewriting repeatedly (see orchestration.md,
"Validation and termination"). Do not show this internal analysis to the user.

## Duration and structure (context for the Style)

- Duration and structure: respect the duration and structure defined by the brief or by the composition planning. Style must respect the composition structure established by the brief or creative planning.
- Style defines the sonic identity, the musical architecture and the global trajectory; Performance defines the interpretation, the dynamics and the expressive changes per section. Avoid overlapping responsibilities.
- The Style must support the chosen structure, indicating global architecture (build, drop, breakdown, final surge, afterglow) when it makes a difference, without duplicating the performance direction of Performance.

## Using a reference, if provided (absorb without copying)

If the user sends a song name with the author, or a link:

### Analysis procedure (checklist)

Identify, in the reference:
1. **Genre and subgenre** (anchor + modifiers).
2. **Era/scene** (if it changes the sound: "80s synth-pop", "2010s EDM").
3. **Mood/atmosphere** (melancholic, euphoric, dark, intimate).
4. **Tempo** (BPM or feel: slow, mid-tempo, driving).
5. **Groove** (four-on-the-floor, swing, half-time, laid-back).
6. **Main instruments** (with function: pulse carrier, groove anchor, harmonic bed, counterline, hook, impact layer, texture glue, contrast color).
7. **Voice type** (female/male, timbre, way of singing, techniques).
8. **Production texture** (polished modern, lo-fi, close-mic, reverb-heavy, analog warmth).
9. **Dynamics** (crescendo, build, drop, breakdown, final surge, afterglow).
10. **Density** (sparse vs. dense).

### Translation into generic descriptors (mandatory)

- Do not use artist, band, singer or song names as a substitute for describing musical characteristics. Describe the desired musical characteristics directly (timbre, way of singing, genre, era, instruments, groove and tempo).
- Describe **how** the singer sings (timbre, way of singing, technique) without saying **who** it is.
- Do not ask to copy melody or arrangement. Describe general musical characteristics.
- If the reference cannot be accessed, say so in one sentence and ask for the missing data, without inventing.

### Decomposition example (reference → Style)

Suppose a melancholic deep house reference. Decomposition:
- Genre: Brazilian deep house, melodic dance (anchor + modifier)
- BPM: 120
- Instruments: atmospheric synth pads (harmonic bed), driving four-on-the-floor kick (groove anchor), warm sub-bass (groove anchor)
- Voice: emotional breathy vocals (timbre + way of singing)
- Production: use "polished modern" only when anchored to audible specifics (e.g., close-mic vocals, tight drum transients); otherwise omit it or describe the production characteristics directly.
- Atmosphere: melancholic club vibe
- Movement: spacious build into drop

Result: `[Style] Brazilian deep house, melodic dance, atmospheric synth pads, driving four-on-the-floor kick drum, warm sub-bass, emotional breathy vocals, melancholic club vibe, 120 bpm`

### If the reference cannot be accessed

Say in one sentence that it could not be accessed and ask for the missing data (genre, BPM, voice type etc.), without inventing.

## Style rules

- Present the Style as a concise description; a single line with comma-separated terms is common, but adapt the presentation to the user's request.
- **Size:** less is more; excess confuses the AI. Adapt length to the request; keep only what adds value.
- **Formula (order, from most to least important):** genre and subgenre + era (if it changes the sound) + mood + tempo (feel/bpm) + main instruments (with function) + production texture (when it audibly shapes the result) + vocal direction + movement of the song.
- **Musical terms:** use musical terms (crescendo, legato, vibrato, reverb etc.) when they make an audible difference; do not employ a technical term merely to make the prompt sound sophisticated.
- **Geographic, cultural, or temporal scene (optional):** include only when it audibly shapes the sound, as a modifier rather than a substitute for musical description (e.g., "Detroit techno", "Nashville country", "80s synth-pop", "Brazilian deep house").
- **Production texture:** prefer audible, concrete descriptors. Equipment, instrument, amplifier, synthesizer, drum-machine, or recording-technique references are useful only when they change the result; do not add them merely to make the prompt sound technical (e.g., "close-mic vocals", "tape saturation", "spring reverb", "room bleed", "TR-808-style sub-bass"). Vague adjectives such as "polished", "modern", "powerful", "cinematic", "emotional", or "epic" are acceptable when anchored to concrete musical characteristics (instrumentation, tempo, groove, dynamics, texture, arrangement); otherwise replace them with one or more specific audible characteristics or omit them.
- Example: `[Style] Brazilian deep house, melodic dance, atmospheric synth pads, driving four-on-the-floor kick drum, warm sub-bass, emotional breathy vocals, melancholic club vibe, 120 bpm`
- **Voice (gender):** define according to musical intent, brief and sonic identity. When there is no specification, do not presume gender, timbre, intensity or vocal aesthetic.
- **Language and diction:** the lyric language follows the language policy in `instructions/orchestration.md`; the Style must reflect that language in its vocal diction (e.g., `Brazilian Portuguese vocals`, `English vocals`, `Spanish vocals`). Include this descriptor whenever the language is known.
- **Describe the voice concretely**, never with vague terms like "beautiful voice". Combine timbre + way of singing + emission technique:
  - Timbre: warm, bright, dark, smoky, raspy, gritty, velvety, airy, breathy, clear.
  - Way of singing: intimate, conversational, whispered, restrained, expressive, powerful, melodic, laid-back, subtle vibrato, sustained notes, layered harmonies.
  - Emission techniques (use only those that are heard): legato, staccato, vibrato, straight tone, belting, falsetto, melisma, runs, twang, breathy singing, grit/rasp, cry/sob, dynamic contrast, pitch bending, mixed voice, vocal fry, whistle register, growl, glottal stop, messa di voce, vowel modification.
  - Do not accumulate descriptors that contradict each other (e.g., whispered + powerful belting).
- **Arrangement movement (global only):** indicate the global architecture (build, drop, breakdown, final surge, afterglow). Density and movement per section belong to performance; do not duplicate them here.
- **Instrument roles (when useful):** pulse carrier, groove anchor, harmonic bed, counterline, hook, impact layer, texture glue, contrast color. Give a function to each important sound.
- When the user does not indicate another direction, do not impose a vocal or instrumental aesthetic; define the direction according to musical intent and the provided references.
- Follow the user's musical direction. Do not add genres or instruments they did not ask for. Do not mix incompatible genres.
- **Fusion:** combine at most 2 to 3 genres; one anchor + modifiers (ex.: "indie folk with subtle synth-pop textures"). Avoid lists of contradictory genres.
- **Contextual coherence:** do not introduce elements (instruments, voices, styles, textures) that clash with the proposal without clear intent. Experimental variations only when the user requests or justifies them.
- Use clear musical terms. English is commonly used for Style descriptions, but adapt the language to the user's request and destination when needed.
- Do not use artist, band, singer or song names as a substitute for describing musical characteristics. Describe the desired musical characteristics directly (timbre, way of singing, genre, era, instruments, groove and tempo).
- **BPM and key:** if the user does not specify, choose a plausible value for the genre and mood instead of omitting.
- **Multiple options:** vary the musical premise (acoustic/intimate, polished pop, dark cinematic, dance/club, live band, retro era); do not just swap adjectives.
- **Descriptors:** prefer specific musical descriptors over generic adjectives ("epic", "beautiful"). Aim for 4 to 7 specific descriptors. This does not relax the fusion limit of at most 2 to 3 genres. (Heuristic: counts are not mandatory targets; musical fit takes priority.)
- **Exclusions:** at most 2 to 3 (e.g., "no strings", "no reverb"), placed at the end of the Style field.
- **Effects in natural musical language:** describe effects as audible descriptors (e.g., "reverb-heavy vocals", "dry intimate vocal", "vocoder"), never as parameters or structured/JSON data.
- **No DAW parameters in outputs:** do not use percentages, dB, ms or Hz in the final Style; use musical terms.
- **Beat:** BPM is always accompanied by a tempo word + groove + drum pattern (e.g., "110 BPM, mid-tempo drive, shuffle, brushed drums"). Groove vocabulary: four-on-the-floor, halftime, shuffle, one-drop. Human feel: laid-back/pushed, behind or ahead of the beat.
- **Field separation:** the style field carries genre, instruments and vocal; lyric words and section tags belong to the lyrics field, not to Style. Short ad-libs (1-3 syllables, in parentheses) belong to the lyrics field (see `instructions/lyrics.md`).

### Platform note (Suno)
Empirical guidance (may change with model version): reliable controls are vocal genre, delivery mode (whisper/rap/belt/speech), BPM and basic texture; named effects and performance tags are suggestions; DAW-style parameters are placebo. Style Influence is an external control outside the text: Loose for exploration, Strong for adherence.

## Language selection

The Style is written in clear musical terms. The lyric language follows the language policy in `instructions/orchestration.md` (and `instructions/lyrics.md`); never default to English lyrics simply because the Style is written in English. Reflect the chosen lyric language in the vocal diction descriptor (e.g., `Brazilian Portuguese vocals`).

## Good style practices (reference)

Based on musical practices and vocabulary (reference):
- **Combine tempo terms with genres** (ex.: "upbeat allegro pop", "slow adagio ballad").
- **Use dynamics to shape emotional intensity** ("crescendo into powerful chorus").
- **Specify instrumentation for desired textures** ("sparse piano and vocals" vs. "dense orchestral arrangement").
- **Mix structural terms to guide form** ("verse-chorus-verse with extended bridge").
- **Layer production effects for atmosphere** ("reverb-heavy ambient soundscape").
- **Mix genres creatively, with anchor + modifiers** ("jazz-influenced hip-hop with soulful vocals").
- **The more specific the musical vocabulary, the more control** over the result.

## Anti-generic and common mistakes

To avoid generic results:
1. Do not use three generic adjectives ("beautiful, emotional, epic"). Replace them with one or more specific audible characteristics (e.g., "warm sub-bass", "driving four-on-the-floor kick").
2. Give a function to each sound (pulse carrier, groove anchor, harmonic bed, counterline, hook, impact layer, texture glue, contrast color).
3. Vary the musical premise, not just adjectives (acoustic/intimate vs. polished pop vs. dark cinematic vs. dance/club vs. live band vs. retro era).
4. Use concrete BPM instead of "fast/slow" when the genre calls for it.
5. Describe the voice as timbre + way of singing + technique, never "beautiful voice".
6. Indicate global trajectory and musical architecture (build, drop, breakdown, final surge, afterglow) when it changes the result; interpretation, dynamics and local expressive changes belong to Performance.
7. Keep indispensables + optionals only if they change the result. Excess confuses.
8. Avoid contradictory descriptors, instrument lists without function, decorative technical terms, elements that clash with the proposal, using artist names as substitutes for musical descriptions, generic or excessively long Style.
9. Do not add equipment names merely to make the prompt look technical; follow the "Production texture" guidance in "Style rules" and include concrete references only when they audibly shape the result.

## Base Style model (essential)

Use this model as a reference. Each element must have justification; remove what does not add value.

**Core elements (4 essentials):**
1. Genre/subgenre (anchor).
2. BPM (or tempo feel).
3. 2 to 3 main instruments, with function (e.g., "synth lead", "808 bass").
4. Voice: timbre + way of singing (e.g., "low dark talk-sing").

**Optional (only if they change the result):**
- Production/recording detail: when it audibly shapes the result, use 1 to 2 concrete, purposeful terms (e.g., "close-mic vocals", "tape saturation", "spring reverb", "room bleed", "TR-808-style sub-bass", "JUNO-style pads"). Vague terms such as "polished modern" are acceptable only when anchored to concrete characteristics.
- Era/scene (e.g., "80s synth-pop").
- Global movement (e.g., "spacious build into drop").
- Technical terms from the glossary (e.g., "legato", "vibrato") — only if audible.
- Extra instrument roles (counterline, hook, impact).

**Avoid:**
- Long instrument lists without function.
- Decorative technical terms.
- Contradictory descriptors.
- Elements that clash with the proposal (contextual coherence).

## Essential example

`[Style] electronicore, eurodance metalcore, 150 bpm, bright trance synth, rave stabs, punchy electronic bass, downtuned chugging guitars, low dark talk-sing, powerful screamed hook, close-mic vocals, tight kick/bass separation, Brazilian Portuguese vocals`

## Coherence with the other parts

Global coherence requirements, responsibility boundaries, and correction/termination rules are
canonical in `instructions/orchestration.md`. Style defines the global sound and global
movement; performance defines density and movement per section. Do not duplicate between them.
The lyrics must sound coherent with the Style (genre, voice, tempo). When a Title is used, it
may be derived from the hook or central idea, according to the user's intent, and should
combine with the Style.

## Output format

A concise Style description; a single comma-separated line is common, but adapt the presentation to the user's request and destination. Note: the Style description is guidance for interpretation, not a guaranteed command (guidance, not guarantee); adherence varies by destination and by conflict with other directions. If a direction is not followed, reformulate or clarify the musical intent.