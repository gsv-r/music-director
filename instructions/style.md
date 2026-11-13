# Guidelines for Sonic Identity

This file is one of the three musical dimensions of music creation: Style (global sonic identity, musical architecture and overall trajectory), Lyrics (composition, content, narrative and singability) and Performance (interpretation, dynamics and expressive changes). This file focuses on global sonic identity. Title is optional identification metadata, not a fourth dimension or a substitute for any of the three. This organization is one possible way to present the creation; adapt the structure to what the user requests, preserving the musical intent.

## Task limit: do not generate audio

- Do not generate, reproduce, render or produce audio or music.
- Do not attempt to open, trigger or control any music generation platform or tool.
- Do not say that music has been generated or is being generated.
- The result of this file is exclusively textual: a Style description. A concise single line is common, but presentation may vary. These instructions support AI collaboration, music production and work with human musicians.

## Shared musical context

A common presentation organizes the work as Title, Style and Lyrics, but the actual sections, order and presentation should adapt to the user's request. Before writing the Style, keep in mind:

1. **Style:** genre, tempo, instruments, voice and atmosphere combine with each other and with the emotion of the song, without contradictory descriptors.
2. **Contextual coherence:** no element (instrument, voice, style, texture) clashes with the musical proposal without justified intent. Do not introduce incompatible elements (e.g., choir/opera in electronic music) unless the user requested them or there is a clear justification. Experimental variations come from the user.
3. **Prosody:** all elements (lyric meaning, emotion, rhythm, stress, vocal intensity, arrangement) point to the same intent. A lyric about fragility does not combine with aggressive interpretation and grandiose production from the first second.
4. **Addressee:** it is clear to whom the character sings and that relationship remains consistent throughout the song.

If something does not combine, correct it before delivering. Do not show this analysis to the user.

## User guidance (priority and context)

The user can direct the creation in many ways: a reference song, an artist name, singing a passage, imitating the sound of an instrument, detailed explanations of how they imagine the song, sensations that certain parts should convey (e.g., "more natural voice with pauses, then the intensity increases, further on a shout comes in"). They may also be spontaneous ideas or vocal demonstrations.

**Rules:**
- **All of this information must be understood, considered and kept in context** throughout the entire creation process.
- **Do not ignore or treat it as isolated comments.** Incorporate it into the overall context of the song.
- **The documentation guides and improves quality**, but **it must not limit the user's contribution**. The user is the one who directs what they want to create; their ideas, preferences and creative touch are part of the process.
- If a user instruction conflicts with good practices, seek balance: preserve the user's intent and adapt the technique without losing the idea.
- Interpret and incorporate these instructions into the Style, the lyrics and the performance coherently.

This section has priority over generic formatting rules.

## Contextual analysis

**Fundamental principle: nothing generic.** Understand the complete context of the song — style, sonic identity, lyrics and vocal performance.

Before generating, the AI must:
1. Analyze each part (Style, lyrics, performance), identifying the essential and the unnecessary.
2. Not let the individual analysis make the song lose its original identity.
3. Balance (less is more, without losing the essential): use only what adds value.
4. Joint analysis: Style, lyrics and performance must converse and make sense within the musical proposal.

This contextual analysis follows the construction hierarchy (see 'Construction hierarchy'). Good instructions per stage are useless if, in the final result, they do not work together.

## Integrated recipe (how this file fits)

The recipe has three steps, in order. This file is **Step 1**.

1. **Step 1 — Style (this file):** absorb the reference (if any) and write the global sound. Style is the "anchor" of everything.
2. **Step 2 — Lyrics (`instructions/lyrics.md`):** write the lyrics using Style as context (genre, voice, tempo, atmosphere). The lyrics must not contradict the Style.
3. **Step 3 — Performance (`instructions/performance.md`):** write the tags per section using Style + lyrics. Tags define the evolution (soft → full), never the global sound.

**Construction hierarchy (standard order):**
1. User instructions.
2. Style — global sonic identity.
3. Lyrics — content, structure and prosody.
4. Performance — interpretation per section.
5. Formatting — correct presentation of the output.

Standard order of construction and priority, not a rigid rule; other flows (e.g., finished lyrics as a starting point) are allowed.

**Final coherence checklist (run across all three files):**
- [ ] Style describes the global sound; tags describe evolution per section (no duplication).
- [ ] Voice in Style (timbre + way of singing) matches the interpretation of the tags.
- [ ] BPM/tempo of Style matches the syllabic density of the lyrics.
- [ ] Emotion of the lyrics matches the atmosphere of the Style.
- [ ] Artist, band or song names are not used as substitutes for musical descriptions; names in lyrical content follow the user's creative intent.
- [ ] When a Title is used, it may be derived from the hook or central idea, according to the user's intent.

## Duration and structure (context for the Style)

- Duration and structure: respect the duration and structure defined by the brief or by the composition planning. Style must respect the composition structure established by the brief or creative planning.
- Style defines the sonic identity, the musical architecture and the global trajectory; Performance defines the interpretation, the dynamics and the expressive changes per section. Avoid overlapping responsibilities.
- The Style must support the chosen structure, indicating global movement per section when it makes a difference (crescendo, build, drop, breakdown, final surge, afterglow), without duplicating the performance direction of Performance.

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
- **Size:** 20 to 35 words by default when a compact single-line form is used. Up to 50 only in complex fusions or when the user requests more detail. Less is more: excess confuses the AI.
- **Formula (order, from most to least important):** genre and subgenre + era (if it changes the sound) + mood + tempo (feel/bpm) + main instruments (with function) + production texture (when it audibly shapes the result) + vocal direction + movement of the song.
- **Musical terms:** use musical terms (crescendo, legato, vibrato, reverb etc.) when they make an audible difference; do not employ a technical term merely to make the prompt sound sophisticated.
- **Geographic, cultural, or temporal scene (optional):** include only when it audibly shapes the sound, as a modifier rather than a substitute for musical description (e.g., "Detroit techno", "Nashville country", "80s synth-pop", "Brazilian deep house").
- **Production texture:** prefer audible, concrete descriptors. Equipment, instrument, amplifier, synthesizer, drum-machine, or recording-technique references are useful only when they change the result; do not add them merely to make the prompt sound technical (e.g., "close-mic vocals", "tape saturation", "spring reverb", "room bleed", "TR-808-style sub-bass"). Vague adjectives such as "polished", "modern", "powerful", "cinematic", "emotional", or "epic" are acceptable when anchored to concrete musical characteristics (instrumentation, tempo, groove, dynamics, texture, arrangement); otherwise replace them with one or more specific audible characteristics or omit them.
- Example: `[Style] Brazilian deep house, melodic dance, atmospheric synth pads, driving four-on-the-floor kick drum, warm sub-bass, emotional breathy vocals, melancholic club vibe, 120 bpm`
- **Voice (gender):** define according to musical intent, brief and sonic identity. When there is no specification, do not presume gender, timbre, intensity or vocal aesthetic.
- **Language and diction:** the lyric language follows the "Language selection" principle in `instructions/lyrics.md`; the Style must reflect that language in its vocal diction (e.g., `Brazilian Portuguese vocals`, `English vocals`, `Spanish vocals`). Include this descriptor whenever the language is known.
- **Describe the voice concretely**, never with vague terms like "beautiful voice". Combine timbre + way of singing + emission technique:
  - Timbre: warm, bright, dark, smoky, raspy, gritty, velvety, airy, breathy, clear.
  - Way of singing: intimate, conversational, whispered, restrained, expressive, powerful, melodic, laid-back, subtle vibrato, sustained notes, layered harmonies.
  - Emission techniques (use only those that are heard): legato, staccato, vibrato, straight tone, belting, falsetto, melisma, runs, twang, breathy singing, grit/rasp, cry/sob, dynamic contrast, pitch bending, mixed voice, vocal fry, whistle register, growl, glottal stop, messa di voce, vowel modification.
  - Do not accumulate descriptors that contradict each other (e.g., whispered + powerful belting).
- **Arrangement movement:** when it makes a difference, indicate the evolution per section (e.g., crescendo, build, drop, breakdown, final surge, afterglow). Keep coherence with the emotion.
- **Instrument roles (when useful):** pulse carrier, groove anchor, harmonic bed, counterline, hook, impact layer, texture glue, contrast color. Give a function to each important sound.
- When the user does not indicate another direction, do not impose a vocal or instrumental aesthetic; define the direction according to musical intent and the provided references.
- Follow the user's musical direction. Do not add genres or instruments they did not ask for. Do not mix incompatible genres.
- **Fusion:** combine at most 2 to 3 genres; one anchor + modifiers (ex.: "indie folk with subtle synth-pop textures"). Avoid lists of contradictory genres.
- **Contextual coherence:** do not introduce elements (instruments, voices, styles, textures) that clash with the proposal without clear intent. Experimental variations only when the user requests or justifies them.
- Use clear musical terms. English is commonly used for Style descriptions, but adapt the language to the user's request and destination when needed.
- Do not use artist, band, singer or song names as a substitute for describing musical characteristics. Describe the desired musical characteristics directly (timbre, way of singing, genre, era, instruments, groove and tempo).
- **BPM and key:** if the user does not specify, choose a plausible value for the genre and mood instead of omitting.
- **Multiple options:** vary the musical premise (acoustic/intimate, polished pop, dark cinematic, dance/club, live band, retro era); do not just swap adjectives.

## Language selection

- The Style is written in clear musical terms.
- The lyric language follows the user's creative brief (see `instructions/lyrics.md`), not the language of these instructions.
- Reflect the chosen lyric language in the vocal diction descriptor (e.g., `Brazilian Portuguese vocals`).
- Never default to English lyrics simply because the Style is written in English.

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
6. Indicate global trajectory and musical architecture per section when it changes the result (build, drop, breakdown, final surge, afterglow); interpretation, dynamics and local expressive changes belong to Performance.
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
- Movement per section (e.g., "spacious build into drop").
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

- The Style defines the global sound; the tags (instructions/performance.md) define the evolution per section. Do not duplicate in the tag what is already in the Style, and vice versa.
- The lyrics (instructions/lyrics.md) must sound coherent with the Style (genre, voice, tempo). Avoid citing in the Style terms that conflict with the lyrics.
- When a Title is used, it may be derived from the hook or central idea, according to the user's intent, and should combine with the Style.

## Output format

A concise Style description; a single comma-separated line is common, but adapt the presentation to the user's request and destination.
