# Musical Performance Direction

This file is one of the three musical dimensions of music creation: Style (global sonic identity, musical architecture and overall trajectory), Lyrics (composition, content, narrative and singability) and Performance (interpretation, dynamics and expressive changes). This file focuses on musical performance direction. Title is optional identification metadata, not a fourth dimension or a substitute for any of the three. This organization is one possible way to present the creation; adapt the structure to what the user requests, preserving the musical intent.

## Task limit: do not generate audio

- Do not generate, reproduce, render or produce audio or music.
- Do not attempt to open, trigger or control any music generation platform or tool.
- Do not say that music has been generated or is being generated.
- The result of this file is exclusively textual: section tags and performance instructions. These instructions support AI collaboration, music production and work with human musicians.

## Shared musical context

A common presentation organizes the work as Title, Style and Lyrics, but the actual sections, order and presentation should adapt to the user's request. Before writing the tags, verify internally:

1. **Style:** genre, tempo, instruments, voice and atmosphere combine with each other and with the emotion of the song, without contradictory descriptors.
2. **Contextual coherence:** no element (instrument, voice, style, texture) clashes with the musical proposal without justified intent.
3. **Tags:** each tag is in the right place and indicates the intended performance for that part.
4. **Prosody:** all elements (lyric meaning, emotion, rhythm, stress, vocal intensity, arrangement) point to the same intent. A lyric about fragility does not combine with aggressive interpretation and grandiose production from the first second.
5. **Role division:** Style defines the sonic identity, the architecture and the global musical trajectory; Performance defines the interpretation, the dynamics and the expressive changes per section; markers are resources for organizing and communicating instructions.

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
5. Role division: Style defines the sonic identity, the architecture and the global musical trajectory; Performance defines the interpretation, the dynamics and the expressive changes per section; markers are resources for organizing and communicating instructions.

This contextual analysis follows the construction hierarchy (see 'Construction hierarchy'). Good instructions per stage are useless if, in the final result, they do not work together.

## Integrated recipe (how this file fits)

The recipe has three steps, in order. This file is **Step 3**.

1. **Step 1 — Style (`instructions/style.md`):** absorb the reference (if any) and write the global sound. Style is the "anchor" of everything.
2. **Step 2 — Lyrics (`instructions/lyrics.md`):** write the lyrics using Style as context (genre, voice, tempo, atmosphere). The lyrics must not contradict the Style.
3. **Step 3 — Performance (this file):** write the tags per section using Style + lyrics. Tags define the evolution (soft → full), never the global sound.

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

## Duration and structure (context for the tags)

- Duration and structure: respect the duration and structure defined by the brief or by the composition planning.

## Using a reference, if provided

If the user sends a song name with the author, or a link:

- Research or open the reference and identify: genre, tempo, groove, instruments, voice type, atmosphere and dynamics.
- In the **lyrics**, follow the same order logic of the song (short intro, verse, chorus), without copying lyrics, melody or identifiable excerpts.
- The tags must reflect the dynamics of the reference (build, drop, breakdown) without relying on the song or artist name as a description.

## Performance direction by section

Performance must be coherent with the sonic identity (Style) and with the lyrics (Lyrics):

- **Naming:** use markers to name the section (`[Intro]`, `[Verse]`, `[Pre-Chorus]`, `[Chorus]`, `[Bridge]`, `[Outro]`, `[Fade Out]`).
- **Behavior (useful convention when this tag format is chosen):** when it makes a difference, add up to 3 audible behavior words in the same tag, after a hyphen (e.g., `[Intro - Soft, Voice Only]`). Combining section and behavior in the same tag is not a universal requirement; adapt the presentation to the destination.
- **Movement:** use movement tags with moderation (musical organization conventions): `[Slow Build]`, `[Rising Tension]`, `[Big Chorus]`, `[Final Surge]`, `[Afterglow]`, `[Chanted Hook]`, `[Rubato Entrance]`. Prefer 4 to 8 enriched indications in full songs.
- **Audible descriptors:** use only descriptors that can be heard (intensity, voice, beat, instrument entry). No long instruction.
- **Positioning:** marker in the same tag as the section; do not split into two consecutive tags; avoid markers in the middle of verses. Markers preferably on their own line, above the block they describe; use language appropriate to the context and destination of the creation.
- **Role division:** Style defines the sonic identity, the architecture and the global musical trajectory; Performance defines the interpretation, the dynamics and the expressive changes per section; markers are resources for organizing and communicating instructions. Do not duplicate in the Style what is already in the marker, and vice versa.
- **Intensity per section (example of a structural possibility, not a mandatory formula):** verse contained/intimate, pre-chorus rising, chorus open and strong, bridge with a change of perspective, outro in afterglow/fade. Intensity must arise from musical intent and the chosen structure.
- **Instrument entry:** indicate locally when the entry or removal of an instrument affects the interpretation of a section. The global architecture and organization of instruments belong to the sonic identity (Style).
- **Emotional coherence:** the interpretation must not contradict the lyrics.
- **Optional human/organic character (when it serves the intent):** natural timing (rubato, slight push/pull), breathable phrasing, breath, dynamic fluctuation, and expressive variation. These describe intentional human character, not mandatory technical imperfection; polished, precise, or tightly controlled performances remain valid when intended.
- **Optional local execution directions (when audible and purposeful):** no drums, solo bass, breakdown, abrupt stop, instrumental interlude, crescendo, or stripped ending. The Lyrics dimension defines whether and where a structural element such as an instrumental interlude occurs; Performance defines how it is executed within the relevant section. Global architecture and production characteristics remain in the Style.
- **Guidance, not guarantee:** markers and descriptors are guidance; if the direction is not followed, reformulate or clarify the musical intent.

### Layering and density by section

- Verse stays lighter; the chorus grows with the whole arrangement, not only the vocal.
- Layers enter along the song: no doubles in the first verse, a response in the pre-chorus, full pair in the chorus, extra harmony in the last chorus. Possibility, not a rigid formula.

### Useful structures by genre

- **Pop:** `[Verse 1]`, `[Pre-Chorus]`, `[Chorus]`, `[Verse 2]`, `[Pre-Chorus]`, `[Chorus]`, `[Bridge]`, `[Final Chorus]`, `[Outro]`.
- **EDM:** `[Verse]`, `[Pre-Chorus]`, `[Build]`, `[Drop]`, `[Verse 2]`, `[Build]`, `[Drop]`, `[Bridge]`, `[Final Drop]`.
- **Rap:** `[Intro]`, `[Verse 1]`, `[Hook]`, `[Verse 2]`, `[Hook]`, `[Bridge]`, `[Final Hook]`.

## Vocal enrichment (ad-libs, interjections, vocalizes)

Additional elements that are not part of the lyrics themselves, but that the singer sings and that complement the composition: interjections ("yeah", "oh", "hey"), vocalizes ("ê, ê, ê", "la la la", "na na"), chants, ad-libs, melismas, scat. They can enrich a lot when they fit the musical proposal, work with the rhyme and contribute to the sound.

**Layer roles (function of each):** lead carries the melody and the lyric; doubles thicken the lead (used sparingly); harmonies support and color the lead; ad-libs fill space and reinforce emotion.

**Fundamental principle: individual analysis, never automatic.** Not every song needs this resource. Each composition must be evaluated case by case: if the element fits the proposal, the rhyme and the sound, use it; if it does not fit or gets in the way, do not use it. Do not add "by default" nor in every song.

**Decision checklist (answer before deciding):**
1. Does the genre support this type of element? (pop, R&B, soul, gospel, dance, afro, reggaeton, hip-hop with sung hooks → more likely; raw folk, piano-voice ballad, ambient, dense storytelling → less likely)
2. Is there space in the melody (pause, end of phrase, build, afterglow, post-chorus)?
3. Does the element reinforce the emotion or groove instead of distracting?
4. Does it work with the rhyme/sound (does not break prosody)?
5. Is there contrast (contained verse → chorus with chant)?
6. Does the arrangement have "breathing room" for the vocal (not saturated)?
If most are "yes", it is worth testing. If most are "no", do not use.

**When to use:** there is space in the melody, the genre supports it, it reinforces emotion/groove, it works with rhyme/sound, there is contrast (contained verse → chorus with chant) and the arrangement has space and breathing room for the vocal.

**When to avoid:** dense lyrics/storytelling, minimalist genres, incompatible emotion, filler, harm to singability/breathing, saturated arrangement, or when the song works better "clean".

**How to mark:** use movement tags embedded in the section, e.g., `[Chorus - Full Beat, Chanted Hook]`, `[Outro - Afterglow, Ad-libs]`, `[Bridge - Rubato Entrance]`. Optional post-chorus (chant) when the genre supports it. Use in moderation: 1 to 3 enrichments per song usually suffice. Tag restraint: avoid tag pollution (moderate number of bracketed lyric tags).

**Golden rule:** if in doubt, do not use. The "clean" song is always valid. Enrichment is optional and only enters when it improves the composition.

Note: the descriptors below communicate musical intent (e.g., Whispered = whispered interpretation; Belting = intense vocal emission; Rubato = expressive flexibility of tempo; Rising Tension = progressive growth of musical tension). CVT remains a reference for human vocal technique. If the interpretation does not convey the desired intent, reformulate or clarify the musical direction.

## Performance descriptor repertoire (reference)

Use these audible descriptors, aligned with Style and lyrics.

### Essential (recurrent use)

**Registers:** chest voice, head voice, falsetto, mixed voice.

**Common vocal techniques:** vibrato, belting, twang, breathy singing, grit/rasp, cry/sob, runs, melisma.

**Dynamics:** messa di voce, crescendo/diminuendo, forte/piano, staccato/legato, accent, rubato.

**Interpretive direction:** whispered, spoken word, rap, monotone, deadpan.

**Vocal arrangement:** choir, harmony, ad-libs, humming, backing vocals.
**Optional (audible, when it serves the intent):** natural timing/phrasing (rubato, slight push/pull, breathable phrasing, breath); human variation (natural dynamic fluctuation, expressive variation); arrangement changes (no drums, solo bass, breakdown, abrupt stop, instrumental interlude, stripped ending).

For additional descriptors, consult the **Annex — Expanded reference repertoire** at the end of this file.

## Anti-generic (tags)

To avoid generic tags:
1. Use **only audible descriptors** (intensity, voice, beat, instrument entry).
2. **Up to 3 behavior words** per tag, after the hyphen.
3. **4 to 8 enriched indications** in full songs (do not exaggerate). Heuristic value, not a documented limit.
4. **Do not duplicate** what is already in the Style.
5. **Do not drop tags in the middle of verses** nor split into two consecutive tags.
6. If the direction is not followed, **reformulate or clarify the musical intent**.

## Coherence with the other parts

- The tags must be coherent with the global Style (`instructions/style.md`): genre, voice, tempo and production. Movement and density per section are owned by performance; do not duplicate global sound here.
- The tags must follow the lyrics (`instructions/lyrics.md`): each tag sits above the corresponding lyric block.
- When a Title is used, it may be derived from the hook or central idea, according to the user's intent, and should combine with the Style.

## Output format

The final presentation is adaptable. Bracketed markers and separate lines are useful conventions, not universal requirements. The output may be:

- Structured lyrics.
- Musical direction notes.
- A production brief.
- Section-by-section performance instructions.
- Another format requested by the user.

When markers are used, place them so that sung text and musical instructions remain clearly separated. A common presentation uses markers alone on a line, above the block they describe, as in the example:

```
[Intro - Soft, Voice Only]
line 1
line 2

[Verse - Light Beat]
line 1
line 2
line 3
line 4

[Chorus - Full Beat, Open Vocal]
line 1
line 2
line 3
line 4
```

**Format validation (adaptable):**
- Clearly organize the parts of the composition.
- Differentiate performance instructions from sung text.
- Preserve the musical divisions.
- Adapt the presentation to the informed destination.
- Keep a structure that is easy to copy and reuse.

Use markers and descriptors in the language appropriate to the context and destination. Note: the bracketed markers are guidance for interpretation, not guaranteed commands. Their usefulness depends on context and destination. Adherence varies by destination and by conflict with the Style. If a direction is not followed, reformulate or clarify the musical intent.

## Annex — Expanded reference repertoire (optional)

For additional descriptors beyond the essential, consult this annex.

### Vocal execution techniques
- Detailed emission techniques: straight tone, dynamic contrast, pitch bending, vocal fry, whistle register, growl, glottal stop.
- Registers (detail): chest voice — rich, warm, powerful, grounded; head voice — lighter, with depth and projection, not breathy; falsetto — breathy, ethereal, flute-like, intimate; mixed voice — bridge between chest and head, with twang.
- Performance principles: less air, more compression on high notes (do not push); vibrato emerges naturally with good support and relaxed throat; do not force; vowel modification when ascending (Ah → Oh → Oo) to avoid tension; twang keeps the cords together in the passaggio.

### Vocal arrangement direction
- Harmonization, a cappella, call and response, scat, crooning, rapping (rapping: see direction markers: rap).

### Production and sound processing references
- Vocal processing (local): compression, distortion, filter.
- Spatialization: reverb, delay/echo, panning. Criterion: delay keeps the lyric clear; reverb creates distance; avoid excess that makes the vocal artificial. Each layer and effect must have a purpose.
- Production/editing: EQ, sampling, loop, fade in/out.
- Note: global production elements belong to the sonic identity and to the production of the music; here they figure only as references of processing applied to the voice.

### CVT (Complete Vocal Technique) modes — reference for human vocal technique
- Neutral: smooth, open, non-metallic; all vowels; volume 1–4/10 (head voice, falsetto).
- Curbing: contained, emotional, "light hold"; vowels UH/O/OO; volume 4–7/10 (mixed, cry/sob).
- Overdrive: clear, direct, shouty; vowels EH/OH; volume 4–10/10 (belting).
- Edge: sharp, bright, twangy; vowels I/EH/A/OE; volume 4–10/10 (twang, grit).

## Language selection (tags and markers)

- Markers and descriptors should use the language appropriate to the context and intended destination.
- The lyric language follows the user's creative brief (see `instructions/lyrics.md`).
- Never default to English lyrics simply because tags or markers are written in English.
