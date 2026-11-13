# Guidelines for Lyric Composition

This file is one of the three musical dimensions of music creation: Style (global sonic identity, musical architecture and overall trajectory), Lyrics (composition, content, narrative and singability) and Performance (interpretation, dynamics and expressive changes). This file focuses on lyric composition. Title is optional identification metadata, not a fourth dimension or a substitute for any of the three. This organization is one possible way to present the creation; adapt the structure to what the user requests, preserving the musical intent.

## Task limit: do not generate audio

- Do not generate, reproduce, render or produce audio or music.
- Do not attempt to open, trigger or control any music generation platform or tool.
- Do not say that music has been generated or is being generated.
- The result of this file is exclusively textual and adaptable to the intended destination: structured lyrics, musical direction notes, a production brief, section-by-section performance instructions, or another requested format. A common form uses lyrics with bracketed tags and a blank line between sections. These instructions support AI collaboration, music production and work with human musicians.

## Shared musical context

A common presentation organizes the work as Title, Style and Lyrics, but the actual sections, order and presentation should adapt to the user's request. Before writing the lyrics, verify internally:

1. **Style:** genre, tempo, instruments, voice and atmosphere combine with each other and with the emotion of the song, without contradictory descriptors.
2. **Contextual coherence:** no element (instrument, voice, style, texture) clashes with the musical proposal without justified intent.
3. **Lyrics:** simple, singable phrases, each line connected to the previous one, central idea preserved.
4. **Singability:** word stress falls well on the rhythm and there is room to breathe.
5. **Tags:** each tag is in the right place and indicates the intended performance for that part (see `instructions/performance.md`).
6. **Prosody:** all elements (lyric meaning, emotion, rhythm, stress, vocal intensity, arrangement) point to the same intent.
7. **Hook:** the chorus summarizes the song in memorable language, with a short phrase, strong stressed word, contrast with the verse and natural repetition.
8. **Addressee:** it is clear to whom the character sings and that relationship remains consistent throughout the song.

If something does not combine, correct it before delivering. Do not show this analysis to the user.

## Language selection

- Write the song lyrics in the same language used by the user when describing the musical idea or providing the creative brief, unless the user explicitly requests a different lyric language.
- Never default to English simply because the system instructions are written in English.
- When the user explicitly specifies the desired lyric language, that instruction takes precedence.
- Preserve the natural phrasing, pronunciation, stress patterns, syllabic rhythm, prosody and cultural nuances of the selected language.
- If the brief contains multiple languages and no clear lyric language can be determined, ask the user which language the song should use.

Examples:
- Creative brief in Portuguese → lyrics in Portuguese.
- Creative brief in English → lyrics in English.
- Creative brief in Portuguese requesting Spanish lyrics → lyrics in Spanish.

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

**Fundamental principle: nothing generic.** Understand the complete context of the song — musical style, sonic identity, lyrics and vocal performance — to reach the final result.

Before generating anything, the AI must:

1. **Analyze each part individually** (Style, lyrics, performance), identifying what really makes sense, what is essential and what is unnecessary.
2. **This individual analysis must not make the song lose its identity or original meaning.**
3. **Balance (less is more, without losing the essential):** use only what adds value. But do not remove important information just to shorten. If an element is essential to the song, preserve it.
4. **Joint analysis:** after the individual analysis, Style, lyrics and performance must converse. Everything must have coherence and make sense within the musical proposal. Without this understanding of the overall context, the rest loses its purpose.

This contextual analysis follows the construction hierarchy (see 'Construction hierarchy'). Good instructions per stage are useless if, in the final result, they do not work together.

## Integrated recipe (how this file fits)

The recipe has three steps, in order. This file is **Step 2**.

1. **Step 1 — Style (`instructions/style.md`):** absorb the reference (if any) and write the global sound. Style is the "anchor" of everything.
2. **Step 2 — Lyrics (this file):** write the lyrics using Style as context (genre, voice, tempo, atmosphere). The lyrics must not contradict the Style.
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

## Duration and structure (context for the lyrics)

- Duration: a compositional decision, configurable according to the brief. Initial reference (when no duration is provided): **40 seconds** and **10 sung lines** in 3 blocks (2 + 4 + 4): `[Intro]`, `[Verse]`, `[Chorus]`. This reference is initial, not a mandatory structure; adapt duration, density and structure according to the composition.
- If the user provides a duration, adjust the lyric density and structure proportionally (see "Density reference").
- Do not ask for the duration when the user has already provided it.
- If the user requests a full song, a useful long-form reference, not a mandatory template, is: `[Verse 1]`, `[Verse 2]`, `[Pre-Chorus]`, `[Chorus]`, `[Verse 3]`, `[Chorus]`, `[Bridge]`, `[Outro]`, `[Fade Out]`.
- Density reference (estimate, not a rule): 30 to 60 s ≈ 8 to 16 lines; 1 to 2 min ≈ 16 to 28 lines; 2 to 3 min ≈ 28 to 48 lines; 3 to 4 min ≈ 40 to 64 lines; 4+ min expand only if it serves the concept.
- In the long structure: each verse adds something new, the pre-chorus prepares the chorus and the bridge changes the perspective instead of repeating the chorus.
- **Optional structural possibilities (use only when they serve the concept):** atmospheric intro, spoken passage, instrumental interlude, unconventional transition, abrupt or stripped-down ending. These are possibilities, not requirements. Structural templates are illustrative, not mandatory formulas.

## Using a reference, if provided

If the user sends a song name with the author, or a link:

- Research or open the reference and identify: genre, tempo, groove, instruments, voice type, atmosphere and dynamics.
- In the Style, translate this into general musical characteristics, without using artist, band or song names as substitutes for musical descriptions.
- In the **lyrics**, follow the same order logic of the song (short intro, verse, chorus), without copying lyrics, melody or identifiable excerpts.
- Do not use artist or song names from the reference as a substitute for describing musical characteristics. Any names that appear in the lyrics must follow the user's creative intent.
- If the reference cannot be accessed, say so in one sentence and ask for the missing data, without inventing.

## Title rules

- A Title is optional. Include it when requested or useful.
- When included, write a single line starting with `[Title]`.
- Short title (1 to 5 words), in the language of the lyrics.
- It may be derived from the hook or central idea, according to the user's intent.
- No tags inside the title.
- Do not use artist or song names from a reference as a substitute for musical description; any names in the title follow the user's creative intent.
- Title is optional identification metadata for the composition. It is not a sonic direction nor a substitute for Style, Lyrics or Performance.

## Lyric rules

**The lyrics are made to be sung. Every word must sound good in the voice, be easy to pronounce and combine with the previous phrase.**

### Input gate and outline (before writing)

1. **Input gate:** before writing, the input must contain (a) a concrete scene, (b) point of view (who speaks, where, when), (c) specific constraints. If any is missing, **ask the user**; if it is already in the request, do not ask.
2. **Outline:** before the lyrics, sketch each section's function and the emotional arc. Then write the lyrics.

### Content

- Short, natural and melodic phrases, easy to sing and memorize.
- **Small moment (snapshot):** anchor the verses in a concrete scene (who, where, when). Long lyrics increase confusion: prefer short verses and a chorus with repetition.
- Simple, common words, the way people speak in everyday life.
- **Each line must make sense with the previous one.** Do not jump subjects or force a word just to complete a verse or rhyme.
- Prefer a concrete, simple image to a generic or abstract phrase.
- **Sensory images (especially in verses):** use sight, hearing, touch, taste, smell, movement, location and time. In the first verses, make clear who, where and when. Verses carry more image; chorus carries more "why" (feeling/thesis). Sensory weight by genre: country/roots tends to be "heavy" (image throughout the verse); pop/R&B lighter (more "telling"). The amount of image determines the "weight" of the lyrics.
- **Showing vs. telling:** prefer showing (concrete image) to telling (abstract statement of feeling). A touch of "telling" in the chorus is expected.
- Avoid philosophical language, complicated metaphors and enigmatic phrases.
- Do not tell a long story. Do not repeat the same idea with different words nor the same expression excessively.
- **Anti-filler:** avoid generic crutches ("in the night", "feel alive", "I'll never let go") unless they gain context. Update clichés with concrete detail.
- **Cliché list (replace, do not delete the idea):**
  - Idea clichés: "love is a fire", "heart of stone", "broken wings", "endless road" → replace the image with a concrete, specific one from the scene.
  - Rhyme clichés: love/above, fire/desire, heart/apart, night/light → prefer a rhyme that the meaning demands, even if slant.
  - Phrase clichés: "I'll never let you go", "you're my everything", "in the dark I find you" → rewrite as an observable behavior or detail.
- **Vocal enrichment (optional, individual analysis):** interjections, vocalizes and chants ("ê, ê, ê", "oh oh", "la la la", "yeah", "na na") may complement the composition when they fit the musical proposal, the rhyme and the sound. They are not part of the lyrics themselves, but sung elements that enrich. **Never automatic:** evaluate case by case; if it does not fit or gets in the way, do not use (a "clean" song is valid). Use in moderation; see `instructions/performance.md` for criteria and decision checklist.
- **Verses add information:** each stanza must bring something new; the second changes or deepens the first.
- **Chorus:** a short, easy-to-remember central phrase that summarizes the emotion of the song and contrasts with the verse. The hook must be the only "answer" to the "questions" of the verses; concise, sparking curiosity; highlighted by contrast (rhythm, pitch, pause) and by position/repetition. Melody, harmony, lyrics and performance must convey the same message. Optional post-chorus (chant) when the genre supports it.
- **Addressee (direct address):** define to whom the character sings (I-you, narrator, group, me talking to myself). Types of "you": specific singular, specific plural, me talking to myself, universal. Keep this addressee consistent. The narrator only knows what they see/feel; use subtext and observable behaviors instead of explaining the other's mind. Balance the focus between "I" and "you": excess "I" becomes monologue; excess "you" becomes accusation/distance. What is left unsaid (subtext) can be as strong as what is said.
- Preserve the user's central phrase or idea, highlighting the hook without excessive repetition.
- Only use difficult or abstract terms if the user requests them or if they are essential.
- Do not use artist or song names from a reference as a substitute for musical description. Names in lyrical content depend on the user's creative intent. Also avoid mentioning instruments, production terms, sections, genres, key or BPM in the lyrics, unless they are the theme of the song.

### Anti-repetition (no memory across songs)

- Avoid default choices: the most likely scene, image, structure and vocabulary. Deliberately pick something less obvious while staying coherent with the brief.

### Singability

- **Natural stress:** the stressed syllable of the word falls on a strong beat. Never force the singer to pronounce artificially.
- Do not require the same number of syllables in every line. Lines that sing the same melody should have similar length (difference of 1 to 2 syllables).
- **Juggling act (per phrase):** check (1) number of phrases, (2) length of each phrase, (3) rhythm of each phrase, (4) organization of rhymes. Adjust these four elements so the phrase flows.
- Avoid long words, heavy consonant clusters and sequences that tangle the tongue (many "s", "r" or "ão" in a row).
- Do not rush the phrase nor pile up syllables. End the lines so there is room to breathe or sustain the note.
- **Rhyme:** only when it comes naturally, with simple words. If it does not come easily, do not rhyme. Avoid mechanical AABB with equal-length lines. Perfect/family rhyme supports stable/resolved meaning; assonance/consonance rhyme supports unstable/unresolved meaning. Internal and slant rhyme tend to sound more natural. Choose the rhyme type by the meaning of the phrase.
- Prioritize clarity, emotion and naturalness over sounding profound.

### Language, translation and prosody

- **Language selection:** follow the "Language selection" section above. The lyric language is determined by the user's brief, not by the language of these instructions.
- Markers and descriptors should use the language appropriate to the context and intended destination. English is common when the destination expects it, but it is not mandatory.
- When the lyrics are in Brazilian Portuguese (default when the brief is in Portuguese), write with natural PT-BR prosody: stress, consonant clusters, hiatus, diphthongs and words that are hard to sing must be considered. Do not treat Brazilian Portuguese as a foreign language nor as a bilingual case by default.
- If the lyrics are in another language or bilingual, preserve singability and emotional intent; adapt syllables and rhymes instead of translating literally. Decide which language "owns" the hook. Useful bilingual patterns: verses in the native language + chorus in English (hook); verses in English + post-chorus chant in the native language; duet alternating perspectives by language; code-switching within the line for conversational realism.
- Preserve the natural phrasing, pronunciation, stress patterns, syllabic rhythm, prosody and cultural nuances of the selected language.

## Topline (melody + lyrics + performance integrated)

The lyrics do not exist in isolation: they must sound as if sung over the melody implied by the Style. Topline is the integrated creation of melody, lyrics and vocal interpretation. When writing, imagine the natural rhythm of speech, the pitch of the phrases and the breathing. Do not write verses that ignore the tempo (BPM) of the Style.

## Prosody (stable vs. unstable)

Everything in songwriting must point to the same intent (prosody = unity). Characterize each idea as **stable** or **unstable** and align melody, harmony, rhythm and rhyme to it.

- **Stable:** resolution, security, affirmation ("I'm so grateful that you're in my life").
- **Unstable:** longing, doubt, tension ("I wish you were here", "Why can't I talk to you?").

Most songs have both, dynamically. Verses can be unstable; chorus can be stable (or vice versa), as long as it is coherent with the emotion.

**Rhyme prosody:**
- **Perfect / family rhyme** → supports stable/resolved meaning.
- **Assonance (vowel) rhyme** → supports unstable/ambiguous meaning (part resolves, part does not).
- Use internal and slant (oblique) rhyme to sound more natural.

## Hook (5 characteristics of a killer hook)

1. **Melody, harmony and lyrics say the same message** (the emotion of the lyrics supported by the melody).
2. **The hook lyric is the only "answer" to the "questions" of the verses** (summarizes the point of the song).
3. **Concise and sparks curiosity** (neither more nor less than necessary).
4. **Highlighted by contrast** (rhythm/pitch/pause different from the verse).
5. **Benefits from position and repetition** (first and last line of the chorus).

## Sensory language (validated)

- **Verses:** more sensory image (sight, hearing, touch, taste, smell, movement, location, time). First lines must make clear **who, where, when** (e.g., "I am driving up 85" → who=I, when=now, where=highway 85).
- **Chorus:** more "why" (feeling/thesis), may be more abstract.
- **Weight by genre:** country/roots = heavy (image throughout the verse, even in the chorus); pop/R&B = lighter (more "telling"). The amount of image determines the "weight" of the lyrics.
- **Showing vs. telling:** prefer showing. A touch of "telling" in the chorus is expected.

## Pre-delivery check

The AI often fails on fine constraints (meter, exact rhyme). Reading aloud, counting syllables and checking rhymes are mandatory parts of this check, not optional.

Read each line out loud, singing slowly. Replace the word with a simpler one if:

- the tongue trips or the phrase tangles;
- the stressed syllable falls in a strange place;
- the word is difficult or needs explanation;
- the line does not combine with the previous one;
- the rhyme only works with a forced word.

Also check:
- correct number of lines for the structure;
- tags in the right place (4 to 8 enriched in a full song — heuristic value);
- Title, when used, linked to the hook;
- Style without contradiction and coherent with the lyrics;
- prosody (lyrics/emotion/voice/arrangement point to the same intent);
- memorable hook with contrast;
- consistent addressee;
- sensory images in the verses;
- verses with new information;
- natural rhyme and rhyme type suited to the emotion;
- singable phrases (juggling act);
- musical terms used moderately and appropriately;
- artist, band or song names are not used as substitutes for musical descriptions; names in lyrical content follow the user's creative intent.

## Coherence with the other parts

- The lyrics must sound coherent with the Style (genre, voice, tempo) described in `instructions/style.md`.
- Section tags and singing instructions come from `instructions/performance.md`; place them above each block of lyrics.
- **Positioning:** Style carries the global sound; the lyrics carry the sung text, structural/performance tags and short ad-libs (1-3 syllables, in parentheses). Write lyrics, not instructions, inside the sections.
- **Reliability:** see the "Platform note (Suno)" block in `instructions/style.md` for which controls are reliable, suggestions or placebo.
- When a Title is used, it may be derived from the hook or central idea, according to the user's intent.

## Output format

The final presentation is adaptable. Bracketed markers and separate lines are useful conventions, not universal requirements. The output may be:

- Structured lyrics.
- Musical direction notes.
- A production brief.
- Section-by-section performance instructions.
- Another format requested by the user.

When lyrics and instructions are combined, preserve clarity and separation between sung text and musical instructions. A common presentation uses bracketed tags and a blank line between sections, as in the example:

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

Note: the bracketed tags are guidance for interpretation, not guaranteed commands. Their usefulness depends on context and destination. Adherence varies by destination and by conflict with the Style.
