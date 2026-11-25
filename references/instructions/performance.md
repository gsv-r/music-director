# Musical performance direction

Music creation has four parts: Style (global sonic identity and global movement), Arrangement (form, layers, entries, exits, density, texture, and instrumental development), Lyrics (composition, content, narrative, and singability), and Performance (interpretation, dynamics, and expressive changes). This file covers performance direction. Title is optional identification metadata, not a dimension or a substitute for any of the others. Treat this division as an editorial convenience, not a requirement. Adapt the structure to what the user requests while preserving the musical intent.

## Task limit

Do not generate, render, or produce audio or music (see `references/instructions/orchestration.md`, Core principles). The result of this file is exclusively textual: section tags and performance instructions. These instructions support AI collaboration, music production and work with human musicians.

## Shared musical context

Universal coherence requirements, user-priority rules, and correction/termination rules are canonical in `references/instructions/orchestration.md`. For Performance, verify internally that Style (genre, tempo, instruments, voice, atmosphere) combines with the emotion of the song, that each tag is in the right place and indicates the intended performance for that part, that prosody aligns lyric meaning, emotion, rhythm, stress, vocal intensity, and arrangement, and that role division is preserved (Style defines sonic identity and global trajectory; Arrangement defines architecture, layers, entries, exits and density; Performance defines interpretation, dynamics, and expressive changes per section). If something does not combine, correct it in one internal pass before delivery. Report any remaining discrepancy rather than rewriting repeatedly. Do not show this internal analysis to the user.

## User guidance (short reminder)

User instructions have priority; incorporate them across Style, lyrics and performance, not as isolated comments. The documentation guides but does not limit the user; seek balance if they conflict with good practices. If used alone, state the missing global context and label assumptions; do not invent it. A Performance-only delivery does not create, change, or review lyrics or compositional content, so it does not require the Analysis pre-delivery check. A Performance request that also creates, changes, or reviews lyrics or compositional content routes to the relevant Lyrics responsibilities and to the Analysis pre-delivery check (see `references/instructions/orchestration.md`). Do not rewrite lyrics in a Performance-only task.

## Duration and structure (context for the tags)

- Duration and structure: respect the duration and structure defined by the brief or by the composition planning.

## Using a reference, if provided

Follow the canonical Musical reference protocol in `references/instructions/orchestration.md`. Apply the identification checklist, classify each claim individually by evidence source and degree of interpretation, and resolve conflicts per the protocol's triggers. Do not redefine the protocol here.

Performance-specific application:

- Examine the reference when it is accessible from the brief or provided material, never through external research during generation. Identify genre, tempo, groove, instruments, voice type, atmosphere, and dynamics. If inaccessible, state it in one sentence and ask for the missing data.
- The tags must reflect the dynamics of the reference (build, drop, breakdown) without relying on the song or artist name as a description.
- Performance owns the resulting tags; Creative Direction does not decide vocal or instrumental techniques.

## Performance direction by section

Performance must be coherent with the sonic identity (Style) and with the lyrics (Lyrics):

- **Naming:** use markers to name the section (`[Intro]`, `[Verse]`, `[Pre-Chorus]`, `[Chorus]`, `[Bridge]`, `[Outro]`, `[Fade Out]`).
- **Behavior (useful convention when this tag format is chosen):** when it makes a difference, add up to 3 comma-separated audible indications in the same tag, after a hyphen (e.g., `[Intro - Soft, Voice Only]`). Combining section and behavior in the same tag is not a universal requirement; adapt the presentation to the destination.
- **Movement:** use movement tags with moderation: `[Slow Build]`, `[Rising Tension]`, `[Big Chorus]`, `[Chanted Hook]`, `[Rubato Entrance]`. Prefer 4 to 8 enriched indications in full songs. (Heuristic: counts are not mandatory targets; musical fit takes priority.)
- **Audible descriptors:** use only descriptors that can be heard (intensity, voice, beat, instrument entry). No long instruction.
- **From intention to audible behavior (when it changes the result):** translate the intention into one or more audible parameters: attack, articulation, dynamic level or change, register, breath placement and phrase length (breath applies to voice and wind instruments; for other instruments use articulation, bow, sustain and instrument-specific equivalents), timing placement (ahead/behind, rubato), and sustain (straight tone or vibrato, length of held note). These are available parameters, not a mandatory checklist: choose only what this section needs and keep the existing tag limit. Prefer a specific behavior when a generic adjective would not make the execution clear; the selection remains an interpretive decision. Metaphorical phrasing language remains valid when it communicates the intended execution.
- **Positioning:** marker in the same tag as the section; do not split into two consecutive tags; avoid markers in the middle of verses. Markers preferably on their own line, above the block they describe; use language appropriate to the context and destination of the creation.
- **Role division:** Style defines the global sonic identity and the global movement; Arrangement defines the form, layers, entries, exits, density, texture, and instrumental development; Performance defines the interpretation, the dynamics, and the expressive changes per section; markers are resources for organizing and communicating instructions. Do not duplicate in Style or Arrangement what is already in the marker, and vice versa. Performance consumes Arrangement and does not redefine layers or entries.
- **No defaults by section type:** do not assign a default intensity, density, or final surge/lift to any section type (verse, pre-chorus, chorus, bridge, outro). Describe what belongs to this composition; adapt, omit or invert as required.
- **Instrument entry:** indicate locally when the entry or removal of an instrument affects the interpretation of a section (e.g., strings only in the chorus; no full drums until the chorus). The global architecture, layers, entries, and exits belong to Arrangement (and the global palette to Style); Performance describes their interpretive effect, not the decision itself.
- **Emotional coherence:** the interpretation must not contradict the lyrics.
- **Optional human/organic character (when it serves the intent):** natural timing, breathable phrasing and human variation are available (see "Optional" under "Performance descriptor repertoire"). They describe intentional human character, not mandatory technical imperfection; polished, precise, or tightly controlled performances remain valid when intended.
- **Optional local execution directions (when audible and purposeful):** no drums, solo bass, breakdown, abrupt stop, instrumental interlude, crescendo, or stripped ending. These belong in Performance only when they describe how a part is executed; their occurrence, formal position and layer changes belong to Arrangement. A crescendo performed by the musician through intensity is Performance; a crescendo produced by adding layers is Arrangement. Local interpretive directions remain available. Lyrics defines whether and where a sung structural element occurs; Arrangement defines the form, layers, and transitions of an instrumental interlude or section. Global palette remains in Style; space, reverb, stereo placement and processing are Production decisions, not Performance parameters.
- **Guidance, not guarantee:** markers and descriptors are guidance; if the direction is not followed, reformulate or clarify the musical intent.

### Layer changes by section

- Layers enter or leave along the song when the composition needs it. Arrangement decides what changes, where, and why from the brief and the material; Performance describes how the resulting parts are executed.

### Development across the song

Before writing tags, build a short internal development map: for each section, its role and what changes versus its previous appearance (or "intentional repetition" when repetition is the effect). The map is planning, not output; it must not add tags beyond the budget in "Anti-generic (tags)".

Development direction: use the direction declared in Style, if any, as internal planning. It is not a Suno "Style of Music" tag and need not appear in the final prompt. Do not force `hypnotic/loop`, `song-based` or `dramatic`; respect an explicit `unclassified` declaration by not inferring another profile or direction. If Style is unavailable or silent, infer a direction from the brief only when materially useful and label it as an assumption. Do not invent global sound; discover the development from this composition's identity and intent.

Axes of change (possible dimensions to consider, not obligations): vocal register/intensity; rhythmic phrasing; intensity of execution (not layer count; adding or removing layers belongs to Arrangement); space/silence. Lyric content/perspective is an axis too, but it is owned by Lyrics. Coordinate with it; do not define lyric content here. Exact repetition and stability are legitimate decisions; vary elements only when the composition calls for it, and always with a musical reason.

- A performance tag names an audible change; it does not create lyric variation. Write any changed line or word in Lyrics.
- The final section's tag must describe the audible change that belongs to this composition (or intentional stability), derived from the brief.

Principles:

- Consider how the composition opens; presenting the identity first is one possibility, not a requirement. A piece may open with contrast, ambiguity, density or silence when that serves the intent.
- A second verse, when it exists, adds something only when there is narrative or musical development; a song with a single verse or a non-narrative form does not need a second verse.
- A bridge, when it exists, presents a new perspective only when the composition calls for contrast; songs without a bridge are valid.
- The final section presents a conclusion or an intentional transformation.
- The ending has intent (natural conclusion, fade, dry cut, or final image).
- Intentional repetition is valid and must not be "corrected." Exact repetition can increase engagement (Elizabeth Hellmuth Margulis, *On Repeat*, Oxford University Press, 2013).
- Larger changes, when present, should have a musical reason and land where the composition needs them. Keep the rest proportionate to the intent.
- Include only the events the music actually needs. Calibrate to duration and intent.
- Never place the next section's tag inside the current tag. Keep each tag to no more than 3 comma-separated audible indications, and stay within the 4-8 enriched indications budget. (Heuristic: not a mandatory target.)

## Vocal enrichment (ad-libs, interjections, vocalizes)

Additional elements that are not part of the lyrics themselves, but that the singer sings and that complement the composition: interjections ("yeah", "oh", "hey"), vocalizes ("ê, ê, ê", "la la la", "na na"), chants, ad-libs, melismas, scat. They can enrich a lot when they fit the musical proposal, work with the rhyme and contribute to the sound.

Layer roles (function of each): lead carries the melody and the lyric; doubles thicken the lead (used sparingly); harmonies support and color the lead; ad-libs fill space and reinforce emotion.

Fundamental principle: individual analysis, never automatic. Not every song needs this resource. Each composition must be evaluated case by case: if the element fits the proposal, the rhyme and the sound, use it; if it does not fit or gets in the way, do not use it. Do not add "by default" nor in every song.

Decision checklist (answer before deciding):

1. Does the genre support this type of element? (pop, R&B, soul, gospel, dance, afro, reggaeton, hip-hop with sung hooks → more likely; raw folk, piano-voice ballad, ambient, dense storytelling → less likely)
2. Is there space in the melody (pause, end of phrase, build, post-chorus)?
3. Does the element reinforce the emotion or groove instead of distracting?
4. Does it work with the rhyme/sound (does not break prosody)?
5. Is there contrast between sections?
6. Does the arrangement have "breathing room" for the vocal (not saturated)?

If most are "yes", it is worth testing. If most are "no", do not use.

When to avoid: dense lyrics/storytelling, minimalist genres, incompatible emotion, filler, harm to singability/breathing, saturated arrangement, or when the song works better "clean".

How to mark: use movement tags embedded in the section, e.g., `[Chorus - Full Beat]`, `[Bridge - Rubato Entrance]`. Optional post-chorus (chant) when the genre supports it. Use in moderation: 1 to 3 vocal ad-libs per song usually suffice. Tag restraint: avoid tag pollution (moderate number of bracketed lyric tags).

Default: if in doubt, do not use; the "clean" song is always valid.

Note: the descriptors below communicate musical intent (e.g., Whispered = whispered interpretation; Belting = intense vocal emission; Rubato = expressive flexibility of tempo; Rising Tension = progressive growth of musical tension). CVT remains a reference for human vocal technique. If the interpretation does not convey the desired intent, reformulate or clarify the musical direction.

## Performance descriptor repertoire (reference)

Use these audible descriptors, aligned with Style and lyrics.

### Essential (recurrent use)

Registers: chest voice, head voice, falsetto, mixed voice.

Common vocal techniques: vibrato, belting, twang, breathy singing, grit/rasp, cry/sob, runs, melisma.

Dynamics: messa di voce, crescendo/diminuendo, forte/piano, staccato/legato, accent, rubato.

Interpretive direction: whispered, spoken word, rap, monotone, deadpan.

Vocal arrangement: choir, harmony, ad-libs, humming, backing vocals.

### Optional (audible, when it serves the intent)

- natural timing/phrasing (rubato, slight push/pull, breathable phrasing, breath)
- human variation (natural dynamic fluctuation, expressive variation)
- arrangement changes (no drums, solo bass, breakdown, abrupt stop, instrumental interlude, stripped ending)

For additional descriptors, consult the Annex: Expanded reference repertoire at the end of this file.

### Humanization of performance directions

Apply the universal guardrails in `references/instructions/orchestration.md` ("Textual humanization and singability") to performance directions. Read them as editorial guidance, not an additional checklist.

- **Clear and natural:** vocal directions should communicate interpretive intent in a clear, natural way; avoid mechanical, generic, or adjective-heavy instructions without practical function.
- **Singable clarity:** directions must be easy to understand and act on; prefer concise audible descriptors over ornate phrasing.
- **No loss of precision:** humanization never inflates tag length (keep up to 3 comma-separated audible indications per tag) nor relaxes the audible-descriptor rule.
- **No obligation:** if a direction is already natural, clear, and specific, do not rewrite it.
- **No invention:** never add a performance event or dynamic not supported by the composition, the Style, or the brief.

## Anti-generic (tags)

To avoid generic tags:

1. Use only audible descriptors (intensity, voice, beat, instrument entry).
2. Up to 3 comma-separated audible indications per tag, after the hyphen.
3. 4 to 8 enriched indications in full songs (do not exaggerate). Heuristic value, not a documented limit.
4. Do not duplicate what is already in the Style.
5. Do not drop tags in the middle of verses nor split into two consecutive tags.
6. If the direction is not followed, reformulate or clarify the musical intent.
7. Do not stack tags; vary only one thing per generation. Regenerate when the overall sound, voice or groove is wrong; edit only when a single passage needs repair.
8. Do not default to a final surge or to variation tags (e.g., "Last-line Variation", "Final variation"); derive the final tag from what audibly changes in this composition. A tag must never replace a changed line or word in the lyrics.
9. Breakdown/pause tags describe what is actually heard; do not combine an audible instrument with a silence instruction, and do not put natural-language descriptions or parentheticals in the lyric field; they may be sung or treated as backing vocals (third-party guides; not confirmed by official Suno documentation).
10. When an adjective does not communicate the execution clearly, prefer a named behavior ("straight tone", "short breath", "soft attack") to a generic intensity adjective ("bright", "open", "faded").

## Using the library (`references/library/`): mandatory procedure

When Performance is selected (full song or Performance-only), library consultation is mandatory and canonical rules are in `references/instructions/orchestration.md` and `references/library/README.md`. Summary:

A. **Analyze the musical context** (Style, lyrics, section, intent, user constraints).
B. **Search `references/library/index.md`** (grep for term, alias, category, or musical intent).
C. **Retrieve relevant category entries** (read only the pertinent file(s)/section(s)).
D. **Evaluate applicability and limitations** (when to use/avoid, conflicts, compatible combinations).
E. **Select and combine appropriate resources** (only those that add value and are coherent).
F. **Generate section-specific Performance directions** (tags per section, per `references/instructions/performance.md` rules).
G. **Validate coherence and requested output format** (anti-generic, role division, no duplication with Style, format).

Consulting the library is mandatory; using a retrieved technique is not. The library provides reference knowledge only and never overrides this module. If a term is not found, label it as an assumption or ask; do not invent definitions or sources. No external research during generation.

The Performance library (`references/library/performance/`) remains mandatory and authoritative for execution. Performance may also consult, optionally and in a targeted way:

- `references/library/rhythm/` when timing feel is material (swing/straight feel, shuffle, groove).
- `references/library/production/` when vocal processing is material.
- `references/library/harmony/` when harmonic tension and resolution are material (e.g., expectation, release, suspension); Performance interprets tension and resolution expressively but does not make harmonic decisions.

A consulted entry becomes a direction only as an audible behavior in the tag; the entry name alone is not a tag.

## Coherence with the other parts

Coherence boundaries and responsibility division are canonical in `references/instructions/orchestration.md`. Tags must be coherent with the global Style (`references/instructions/style.md`): genre, voice, tempo and production; with the form, layers, entries, exits, density, texture, and transitions of Arrangement when it is in scope; and with the lyrics (`references/instructions/lyrics.md`): each tag sits above the corresponding lyric block. Movement and intensity of execution per section are described by Performance, while form, layers and layer density belong to Arrangement; do not duplicate global sound or form here. When a Title is used, it may be derived from the hook or central idea, according to the user's intent, and should combine with the Style.

## Output format

Integrate Performance directions into the sections they describe, written once and not repeated in a separate block. The organization is adaptable. Bracketed markers and separate lines are useful conventions, not universal requirements. Presentation in the fixed delivery format follows `references/instructions/orchestration.md`, "Final delivery format (mandatory)". The content may be:

- Structured lyrics.
- Musical direction notes.
- A production brief.
- Section-by-section performance instructions.
- Another format requested by the user.

When markers are used, place them so that sung text and musical instructions remain clearly separated. A common presentation uses markers alone on a line, above the block they describe, as in the example:

```
[Intro - <audible change from this song>]
line 1
line 2

[Verse - <audible change from this song>]
line 1
line 2
line 3
line 4

[Chorus - <audible change from this song>]
line 1
line 2
line 3
line 4
```

Format validation (adaptable):

- Clearly organize the parts of the composition.
- Differentiate performance instructions from sung text.
- Preserve the musical divisions.
- Adapt the presentation to the informed destination.
- Keep a structure that is easy to copy and reuse.

Use markers and descriptors in the language appropriate to the context and destination. Bracketed markers are guidance for interpretation, not guaranteed commands. Their usefulness depends on context and destination, and adherence varies by destination and by conflict with the Style.

## Annex: Expanded reference repertoire (optional)

For additional descriptors beyond the essential, consult this annex.

### Vocal execution techniques

- Detailed emission techniques: straight tone, dynamic contrast, pitch bending, vocal fry, whistle register, growl, glottal stop.
- Registers (detail): chest voice: rich, warm, powerful, grounded; head voice: lighter, with depth and projection, not breathy; falsetto: breathy, ethereal, flute-like, intimate; mixed voice: bridge between chest and head, with twang.
- Performance principles: less air, more compression on high notes (do not push); vibrato emerges naturally with good support and relaxed throat; do not force; vowel modification when ascending (Ah → Oh → Oo) to avoid tension; twang keeps the cords together in the passaggio.

### Vocal arrangement direction

- Harmonization, a cappella, call and response, scat, crooning, rapping (rapping: see direction markers: rap).

### Production and sound processing references

- Vocal processing (local): compression, distortion, filter.
- Spatialization: reverb, delay/echo, panning. Criterion: delay keeps the lyric clear; reverb creates distance; avoid excess that makes the vocal artificial. Each layer and effect must have a purpose.
- Production/editing: EQ, sampling, loop, fade in/out.
- Note: global production elements belong to the sonic identity and to the production of the music; here they figure only as references of processing applied to the voice.

### CVT (Complete Vocal Technique) modes: reference for human vocal technique

- Volume scales below (e.g., 1-4/10) are human-technique references only; do not export them to the output.
- Neutral: smooth, open, non-metallic; all vowels; volume 1-4/10 (head voice, falsetto).
- Curbing: contained, emotional, "light hold"; vowels UH/O/OO; volume 4-7/10 (mixed, cry/sob).
- Overdrive: clear, direct, shouty; vowels EH/OH; volume 4-10/10 (belting).
- Edge: sharp, bright, twangy; vowels I/EH/A/OE; volume 4-10/10 (twang, grit).

## Language selection (tags and markers)

Markers and descriptors should use the language appropriate to the context and intended destination. The lyric language follows the language policy in `references/instructions/orchestration.md` (and `references/instructions/lyrics.md`). Never default to English lyrics simply because tags or markers are written in English.
