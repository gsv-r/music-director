# Guidelines for Lyric Composition

Music creation has four dimensions: Style (global sonic identity and global movement), Arrangement (form, layers, entries, exits, density, texture, and instrumental development), Lyrics (composition, content, narrative, and singability), and Performance (interpretation, dynamics, and expressive changes). This file covers the Lyrics dimension. A Title is optional identification metadata, not a dimension and not a substitute for any of the others. Treat this division as a working frame and adapt the structure to what the user asks for while preserving the musical intent.

## Task limit

Do not generate, render, or produce audio or music (see `references/instructions/orchestration.md`, Core principles). The result of this file is exclusively textual and adaptable to the intended destination: structured lyrics, musical direction notes, a production brief, section-by-section performance instructions, or another requested format. A common form uses lyrics with bracketed tags and a blank line between sections. These instructions support AI collaboration, music production and work with human musicians.

## Shared musical context

Universal coherence requirements, user-priority rules, and correction/termination rules are
canonical in `references/instructions/orchestration.md`. For Lyrics, verify internally that Style (genre,
tempo, instruments, voice, atmosphere) combines with the emotion of the song, that lyrics are
simple and singable with each line connected to the previous one, that the central idea is
preserved, that word stress falls well on the rhythm with room to breathe, that prosody aligns
all elements, that the hook summarizes the song memorably, and that the addressee stays
consistent. If something does not combine, correct it in one internal pass before delivery;
report any remaining discrepancy rather than rewriting repeatedly. Do not show this internal
analysis to the user.

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

## User guidance (short reminder)

User instructions have priority; incorporate them across Style, lyrics and performance, not as isolated comments. The documentation guides quality but does not limit the user's creative contribution; resolve conflicts with documented recommendations by preserving the user's intent (see `references/instructions/orchestration.md`, "Core principles"). If used alone, state the missing global context and label assumptions; do not invent it. When lyrics are created, changed, or reviewed, run the Analysis pre-delivery check (see `references/instructions/analysis.md` and `references/instructions/orchestration.md`); it is mandatory even if the visible Analysis section is omitted because the user restricted the format.

## Duration and structure (context for the lyrics)

- Duration: a compositional decision, configurable according to the brief. Initial reference (when no duration is provided): 40 seconds and 10 sung lines in 3 blocks (2 + 4 + 4): `[Intro]`, `[Verse]`, `[Chorus]`. This reference is initial, not a mandatory structure; adapt duration, density and structure according to the composition.
- If the user provides a duration, adjust the lyric density and structure proportionally (see "Density reference").
- Do not ask for the duration when the user has already provided it.
- If the user requests a full song, a useful long-form reference, not a mandatory template, is: `[Verse 1]`, `[Verse 2]`, `[Pre-Chorus]`, `[Chorus]`, `[Verse 3]`, `[Chorus]`, `[Bridge]`, `[Outro]`, `[Fade Out]`.
- Density reference (estimate, not a rule): 30 to 60 s ≈ 8 to 16 lines; 1 to 2 min ≈ 16 to 28 lines; 2 to 3 min ≈ 28 to 48 lines; 3 to 4 min ≈ 40 to 64 lines; 4+ min expand only if it serves the concept.
- In the long structure, a verse may add something new, the pre-chorus may prepare the chorus, and the bridge may change the perspective instead of repeating the chorus (when those sections exist and serve the composition). Exact repetition and stability are valid when intended.
- Optional structural possibilities (use only when they serve the concept): atmospheric intro, spoken passage, instrumental interlude, unconventional transition, abrupt or stripped-down ending. These are possibilities, not requirements. Structural templates are illustrative, not mandatory formulas. When an instrumental interlude, transition, or instrumental section is involved, coordinate its occurrence and position with Arrangement. Lyrics defines whether and where the sung structure needs it, Arrangement defines its form and layers, and Performance defines how it is executed.

## Using a reference, if provided

Follow the canonical Musical reference protocol in
`references/instructions/orchestration.md`. Apply the identification checklist, classify
each claim individually by evidence source and degree of interpretation, and
resolve conflicts per the protocol's triggers. Do not redefine the protocol here.

Lyrics-specific application:
- In the Style, translate the reference into general musical characteristics.
- In the lyrics, follow the same order logic of the song (short intro, verse,
  chorus), without copying lyrics, melody, or identifiable excerpts.
- Do not use artist, band or song names from the reference as a substitute for musical
  description. Any names in the lyrics follow the user's creative intent.
- Preserve prosody and language nuances; adapt syllables and rhymes instead of
  translating literally.
- If the reference cannot be accessed, say so in one sentence and ask for the
  missing data, without inventing.

## Title rules

- A Title is optional. Include it when requested or useful.
- When included, write a single line starting with `[Title]`.
- Short title (1 to 5 words), in the language of the lyrics.
- The title text itself contains no brackets or tags.
- It may be derived from the hook or central idea, according to the user's intent.
- Any names in the title follow the user's creative intent (see "Using a reference").
- It is identification metadata, not a sonic direction or a substitute for Style, Lyrics or Performance.

## Lyric rules

The lyrics are made to be sung. Every word must sound good in the voice, be easy to pronounce and combine with the previous phrase.

### Input gate and outline (before writing)

1. Input gate (mode-aware): before writing, identify the lyric mode. Useful references include narrative, abstract, hook/chant, hypnotic, minimalist and texture-based, but these are illustrative, not a closed taxonomy. The Music Director may describe the function of the voice in free language when the proposal does not match any of these terms.
   - Narrative: requires (a) a concrete scene and (b) point of view (who speaks, where, when); these are essential, so ask if either is missing. For (c) specific constraints, ask only if the user has constraints to preserve; otherwise record "no specific constraints". Do not ask for information already in the brief.
   - Abstract / hook/chant / hypnotic / minimalist / texture-based: do not require a concrete scene, narrator, location, time, or vocal register. Instead require (a) the function of the voice (lead, texture, chant, hook), (b) the emotional/sonic intent, (c) the role of repetition (if any), (d) specific constraints. Ask only when an essential element for the chosen mode is missing and cannot be inferred; never ask for information already in the brief.
2. Outline: before the lyrics, sketch each section's function and the emotional arc. Also note, per section, what changes or is intentionally preserved (new detail, perspective turn, a changed line or word in a returning chorus, or deliberate exact repetition) so the plan reflects the composition's intent rather than assuming recurring sections must differ. Then write the lyrics.

### Content

- Short, natural and melodic phrases, easy to sing and memorize.
- Small moment (snapshot): anchor the verses in a concrete scene (who, where, when). Long lyrics increase confusion: prefer short verses and a chorus with repetition.
- Simple, common words, the way people speak in everyday life.
- Each line must make sense with the previous one. Do not jump subjects or force a word just to complete a verse or rhyme.
- Prefer a concrete, simple image to a generic or abstract phrase.
- Sensory images (especially in verses): use sight, hearing, touch, taste, smell, movement, location and time. In the first verses, make clear who, where and when. Verses carry more image; chorus carries more "why" (feeling/thesis). Sensory weight by genre: country/roots tends to be "heavy" (image throughout the verse); pop/R&B lighter (more "telling"). The amount of image determines the "weight" of the lyrics.
- Showing vs. telling: prefer showing (concrete image) to telling (abstract statement of feeling). A touch of "telling" in the chorus may appear; it is common, not required.
- Avoid philosophical language, complicated metaphors and enigmatic phrases.
- Do not tell a long story. Do not repeat the same idea with different words nor the same expression excessively.
- Anti-filler: avoid generic crutches ("in the night", "feel alive", "I'll never let go") unless they gain context. Update clichés with concrete detail.
- Cliché list (replace, do not delete the idea):
  - Idea clichés: "love is a fire", "heart of stone", "broken wings", "endless road" → replace the image with a concrete, specific one from the scene.
  - Rhyme clichés: love/above, fire/desire, heart/apart, night/light → prefer a rhyme that the meaning demands, even if slant.
  - Phrase clichés: "I'll never let you go", "you're my everything", "in the dark I find you" → rewrite as an observable behavior or detail.
- Vocal ad-libs (optional, individual analysis): interjections, vocalizes and chants ("ê, ê, ê", "oh oh", "la la la", "yeah", "na na") may complement the composition when they fit the musical proposal, the rhyme and the sound. They are not part of the lyrics themselves, but sung elements that enrich. Never automatic: evaluate case by case; if it does not fit or gets in the way, do not use (a "clean" song is valid). Use in moderation; see `references/instructions/performance.md` for criteria and decision checklist.
- Verses add information (when applicable): a stanza may bring something new or deepen what came before; this is a common practice, not a requirement. Exact repetition and stability are valid when intended.
- Chorus (when present): a central phrase that may summarize the emotion of the song and contrast with the verse. The hook can be the "answer" to the "questions" of the verses, but it need not be; concise, sparking curiosity; highlighted by contrast (rhythm, pitch, pause) and by position/repetition when useful. Melody, harmony, lyrics and performance should convey the same message. Optional post-chorus (chant) when the genre supports it. A composition without a conventional chorus is valid. If a returning chorus changes a line or word, write that variation in the lyrics; a performance tag cannot create it.
- Addressee (direct address, when the composition uses these functions): define to whom the character sings (I-you, narrator, group, me talking to myself). Types of "you": specific singular, specific plural, me talking to myself, universal. Keep this addressee consistent. The narrator only knows what they see/feel; use subtext and observable behaviors instead of explaining the other's mind. Balance the focus between "I" and "you": excess "I" becomes monologue; excess "you" becomes accusation/distance. What is left unsaid (subtext) can be as strong as what is said. Abstract, mantra or texture-based lyrics need not define a narrator or addressee.
- Preserve the user's central phrase or idea, and highlight the hook without excessive repetition.
- Only use difficult or abstract terms if the user requests them or if they are essential.
- Names in lyrical content follow the user's creative intent (see "Using a reference"). Also avoid mentioning instruments, production terms, sections, genres, key or BPM in the lyrics, unless they are the theme of the song.

### Anti-repetition (no memory across songs)

- Avoid default choices: the most likely scene, image, structure and vocabulary. Deliberately pick something less obvious while staying coherent with the brief.

### Singability

- Natural stress: the stressed syllable of the word falls on a strong beat. Never force the singer to pronounce artificially.
- Do not require the same number of syllables in every line. Lines that sing the same melody should have similar length (difference of 1 to 2 syllables).
- Juggling act (per phrase): check (1) number of phrases, (2) length of each phrase, (3) rhythm of each phrase, (4) organization of rhymes. Adjust these four elements so the phrase flows.
- Avoid long words, heavy consonant clusters and sequences that tangle the tongue (many "s", "r" or "ão" in a row).
- Do not rush the phrase nor pile up syllables. End the lines so there is room to breathe or sustain the note.
- Rhyme: only when it comes naturally, with simple words. If it does not come easily, do not rhyme. Avoid mechanical AABB with equal-length lines. Perfect/family rhyme supports stable/resolved meaning; assonance/consonance rhyme supports unstable meaning (see "Prosody (stable vs. unstable)"). Internal and slant rhyme tend to sound more natural. Choose the rhyme type by the meaning of the phrase.
- Prioritize clarity, emotion and naturalness over sounding profound.

### Language, translation and prosody

- Language selection: follow the "Language selection" section above. The lyric language is determined by the user's brief, not by the language of these instructions.
- Markers and descriptors should use the language appropriate to the context and intended destination. English is common when the destination expects it, but it is not mandatory.
- When the lyrics are in Brazilian Portuguese (default when the brief is in Portuguese), write with natural PT-BR prosody: stress, consonant clusters, hiatus, diphthongs and words that are hard to sing must be considered. Do not treat Brazilian Portuguese as a foreign language nor as a bilingual case by default.
- If the lyrics are in another language or bilingual, preserve singability and emotional intent; adapt syllables and rhymes instead of translating literally. Decide which language "owns" the hook. Useful bilingual patterns: verses in the native language + chorus in English (hook); verses in English + post-chorus chant in the native language; duet alternating perspectives by language; code-switching within the line for conversational realism.
- Preserve the natural phrasing, pronunciation, stress patterns, syllabic rhythm, prosody and cultural nuances of the selected language.

### Humanization and singability (editorial sense)

Apply the universal guardrails in `references/instructions/orchestration.md` ("Textual humanization and singability") to the lyric text. Treat them as editorial judgment, not a fixed list of bans. Notice when a word does not work well sung, when a phrase sounds artificial, or when a construction could be expressed more fluently.

- Singability first: prefer words and expressions that are natural to sing; avoid hard-to-articulate terms and constructions that stall vocal delivery. (Reinforces the existing "Singability" rules; do not duplicate them.)
- Natural phrasing: avoid artificial phrasing, needlessly ornate words, and expressions chosen only to complete a rhyme. Rhyme serves meaning, not the reverse.
- Fluency over the page: consider the sound of words, natural stress, phrase rhythm, and ease of vocal interpretation; when two constructions communicate the same intent, prefer the more natural and singable one.
- Keep the poetry: preserve the language, poetry, vocabulary, and genre-specific character. Do not simplify indiscriminately; artistic devices (metaphor, imagery, repetition, ambiguity) remain valid when they serve the composition.
- Fidelity: do not change meaning, narrative, or emotional intent solely to make the lyric simpler or more elaborate.
- No obligation: if a lyric is already natural, clear, expressive, and singable, do not rewrite it. Humanization improves expression; it never compromises precision, prosody, or content.
- Variation: vary phrasing and word choice so different songs do not follow the same mold; avoid generic clichés unless they gain context (see "Anti-filler" and the cliché list).
- No invention: never add information, characters, events, or emotional claims absent from the brief or the composition.

## Topline (melody + lyrics + performance integrated)

The lyrics do not exist in isolation: they must sound as if sung over the melody implied by the Style. Topline is the integrated creation of melody, lyrics and vocal interpretation. When writing, imagine the natural rhythm of speech, the pitch of the phrases and the breathing. Do not write verses that ignore the tempo (BPM) of the Style.

## Prosody (stable vs. unstable)

Everything in songwriting must point to the same intent (prosody = unity). Characterize each idea as stable or unstable and align melody, harmony, rhythm and rhyme to it.

- Stable: resolution, security, affirmation ("I'm so grateful that you're in my life").
- Unstable: longing, doubt, tension ("I wish you were here", "Why can't I talk to you?").

Most songs have both, dynamically. Verses can be unstable; chorus can be stable (or vice versa), as long as it is coherent with the emotion.

Rhyme prosody:
- Perfect / family rhyme → supports stable/resolved meaning.
- Assonance and consonance rhyme → supports unstable/ambiguous meaning (part resolves, part does not).
- Use internal and slant (oblique) rhyme to sound more natural.

## Hook (reference characteristics of a strong hook)

1. Melody, harmony and lyrics say the same message (the emotion of the lyrics supported by the melody).
2. The hook lyric can be the "answer" to the "questions" of the verses (summarizes the point of the song), one compositional possibility among many.
3. Concise and sparks curiosity (neither more nor less than necessary).
4. Highlighted by contrast (rhythm/pitch/pause different from the verse).
5. Benefits from position and repetition (first and last line of the chorus).

These are reference characteristics, not requirements. A hook may be strong without all five; repetition, chant, texture or minimalism can carry a composition without a conventional hook.

## Sensory language (validated)

- Verses: more sensory image (sight, hearing, touch, taste, smell, movement, location, time). In narrative lyrics, first lines may make clear who, where, when (e.g., "I am driving up 85" → who=I, when=now, where=highway 85). This is appropriate for narrative songs, not a universal requirement.
- Chorus: more "why" (feeling/thesis), may be more abstract.
- Weight by genre (reference, not rule): country/roots tends to be "heavy" (image throughout the verse, even in the chorus); pop/R&B tends to be lighter (more "telling"). The amount of image determines the "weight" of the lyrics. Adapt to the composition; do not apply automatically.
- Showing vs. telling (reference, not rule): prefer showing (concrete image) to telling (abstract statement of feeling). A touch of "telling" in the chorus is common, not required. Adapt to the composition's intent.

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
- tag enrichments in the right place (4 to 8 enriched indications in a full song, heuristic value);
- Title, when used, linked to the hook;
- Style without contradiction and coherent with the lyrics;
- prosody (lyrics/emotion/voice/arrangement point to the same intent);
- memorable hook with contrast;
- consistent addressee;
- sensory images in the verses;
- verses with new information;
- natural rhyme and rhyme type suited to the emotion;
- singable phrases (juggling act);
- humanization and singability: lyric reads naturally when sung, no artificial phrasing or rhyme-forced word, and no change to meaning or intent;
- musical terms used moderately and appropriately;
- artist, band or song names are not used as substitutes for musical descriptions; names in lyrical content follow the user's creative intent.

## Library consultation

Lyrics may consult `references/library/rhythm/` when prosody makes rhythmic theory relevant
(syncopation, backbeat, accent, simple/compound meter). Consultation is optional and
targeted. The library provides reference knowledge and never overrides this module.

Lyrics may consult `references/library/harmony/` when prosody or topline makes harmonic theory
relevant (tonal center, mode/scale, chord color, harmonic rhythm, expectation).
Consultation is optional and targeted. The library provides reference knowledge and
never overrides this module.

## Coherence with the other parts

Coherence boundaries, responsibility division, correction/termination rules, and language policy are
canonical in `references/instructions/orchestration.md`. Lyrics must sound coherent with the Style (genre,
voice, tempo) described in `references/instructions/style.md` and with the form and sung section sequence
established by Arrangement when it is in scope. Section tags and singing instructions come
from `references/instructions/performance.md`; place them above each block of lyrics. Style carries the global
sound; Arrangement carries the form, layers, entries, exits, density, texture, and transitions; the
lyrics carry the sung text, structural/performance tags and short vocal ad-libs (1-3 syllables,
in parentheses). Write lyrics, not instructions, inside the sections. Reliability guidance is in the
"Platform note (Suno)" block of `references/instructions/style.md`. When a Title is used, it may be derived
from the hook or central idea, according to the user's intent.

## Output format

The final presentation is adaptable. Bracketed markers and separate lines are useful conventions, not universal requirements. The output may be:
- Structured lyrics.
- Musical direction notes.
- A production brief.
- Section-by-section performance instructions.
- Another format requested by the user.

When lyrics and instructions are combined, preserve clarity and separation between sung text and musical instructions. A common presentation uses bracketed tags and a blank line between sections, as in the example:

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

Note: the bracketed tags are guidance for interpretation, not guaranteed commands. Their usefulness depends on the context and destination, and adherence varies with the destination or with conflict with the Style. Counts such as "4 to 8 tag enrichments" are heuristics, not mandatory targets.
