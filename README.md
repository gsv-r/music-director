# Music Director

**AI-powered Music Direction and Creation System.**

Music Director is a system of English-language instructions that guides an AI to work as a **musical director**: understanding artistic intent and coordinating musical identity and sound, composition and lyrics, vocal and musical performance, arrangement and instrumentation, and emotional development and coherence.

It is not merely a prompt generator, and it is not a music generation tool. It is an AI-assisted musical direction system: a system of instructions that guides AI collaboration, not software that automatically enforces musical coherence. These instructions support AI collaboration, music production and work with human musicians.

## What Music Director is

Music Director provides structured, reusable guidance for creating songs with an AI. Instead of asking for a "prompt", it asks the AI to reason like a musical director: to balance genre, sound, lyrics, performance, arrangement and emotion into one coherent piece.

The repository is composed of three core instruction files:

- `instructions/style.md` — Musical Identity
- `instructions/lyrics.md` — Lyrics and Composition
- `instructions/performance.md` — Musical Performance Direction

These files work together. They can be provided to any capable AI, which then collaborates with you to develop a song. Title, Style, Lyrics and Performance need not all appear as separate output blocks in every delivery; the AI adapts the presentation to the user's requested workflow and destination. Results depend on the AI, the context and the intended destination; adapt the process as needed.

## The problem it solves

Creating music with AI often produces generic, incoherent results: a style that fights the lyrics, lyrics that cannot be sung, performances that ignore the emotion, or prompts that are just long lists of adjectives. Music Director addresses this by separating concerns and encouraging coherence:

- Sonic identity is defined once, globally.
- Lyrics are written to be sung, with prosody and singability in mind.
- Performance evolves per section instead of duplicating the global sound.
- All three dimensions are checked against each other before delivery.

The result is a more coherent, intentional song rather than a random combination of descriptors. Music Director guides this process; it does not automatically enforce it.

## Project philosophy

Music Director treats the AI as a collaborator, not a button. The user directs the creation: references, preferences, sensations, vocal ideas, partial lyrics, or a vague feeling are all valid starting points. The documentation guides and improves quality, but it never limits the user's creative contribution.

Key principles:

- **Nothing generic.** Every element must earn its place.
- **Coherence over accumulation.** Style, lyrics and performance must converse.
- **User intent first.** When a user instruction conflicts with good practice, balance both: preserve the intent and adapt the technique.
- **Less is more, without losing the essential.** Use only what adds value; never remove what is essential just to shorten.
- **Textual output only.** Music Director never generates, renders or plays audio.

## The three musical dimensions

### `instructions/style.md` — Musical Identity

Defines the global sonic identity of the song: genre and subgenre, era or scene, mood, tempo, groove, main instruments and their roles, production texture, vocal direction, and the overall musical movement (build, drop, breakdown, final surge, afterglow).

Style is the anchor. Everything else must be coherent with it.

### `instructions/lyrics.md` — Lyrics and Composition

Defines composition, narrative, content, message, structure, prosody, singability and hooks. Lyrics are written to be sung: natural stress, manageable syllables, breathable phrasing, meaningful rhymes and a memorable hook.

### `instructions/performance.md` — Musical Performance Direction

Defines interpretation, vocal delivery, articulation, dynamics, expression, section-level changes and vocal arrangement. Markers such as `[Verse - Light Beat]` or `[Chorus - Full Beat, Open Vocal]` describe how each section evolves, never the global sound.

### How the three dimensions work together

1. **Style** establishes the global sound and identity.
2. **Lyrics** are written using Style as context, so they do not contradict the sound.
3. **Performance** adds section-level interpretation and dynamics on top of Style and lyrics.

Style is the anchor; Performance is the evolution. A good result requires all three to converse.

## Construction hierarchy

The standard construction order and priority is:

1. **User instructions.**
2. **Style** — global musical identity.
3. **Lyrics** — content, structure and prosody.
4. **Performance** — interpretation per section.
5. **Formatting** — correct presentation of the output.

This is the standard order, not a rigid restriction. Other flows are allowed, such as starting from finished lyrics or a sound reference.

## Repository structure

```
music-director/
├── README.md
└── instructions/
    ├── style.md
    ├── lyrics.md
    └── performance.md
```

- `README.md` — project overview and usage (this file).
- `instructions/style.md` — global sonic identity guidelines.
- `instructions/lyrics.md` — lyric composition guidelines.
- `instructions/performance.md` — performance and tag guidelines.

## Language selection

Although the repository and all instructions are written in English, **the language of the generated song follows the user's creative brief**.

- Write the song lyrics in the same language used by the user when describing the musical idea or providing the creative brief, unless the user explicitly requests a different lyric language.
- Never default to English simply because the system instructions are written in English.
- When the user explicitly specifies the desired lyric language, that instruction takes precedence.
- Preserve the natural phrasing, pronunciation, stress patterns, syllabic rhythm, prosody and cultural nuances of the selected language.
- If the brief contains multiple languages and no clear lyric language can be determined, ask the user which language the song should use.

Examples:
- Creative brief in Portuguese → lyrics in Portuguese.
- Creative brief in English → lyrics in English.
- Creative brief in Portuguese requesting Spanish lyrics → lyrics in Spanish.

Section markers and descriptors should use the language appropriate to the context and intended destination. English is common when the destination expects it, but it is not mandatory.

## Usage instructions

You do not need technical musical knowledge or a formal briefing template. You may start with a vague idea, an existing lyric, a sound reference or a vocal direction.

1. **Provide the three instruction files to an AI.** Give `instructions/style.md`, `instructions/lyrics.md` and `instructions/performance.md` to a capable AI as context.
2. **Describe your musical idea naturally.** In your own words, say what you want: a feeling, a story, a genre, a mood, a scene.
3. **Provide references and preferences.** A song name, an artist, a link, a hummed melody, an instrument sound, or a description of how you imagine the song all count.
4. **Collaborate to develop the composition.** Work with the AI iteratively: refine the Style, the lyrics and the performance until they feel right.
5. **Review and refine the result.** Read the lyrics out loud, check that tags match the sections, and ask the AI to adjust anything that does not fit.
6. **Adapt the final presentation to the intended destination.** Copy the output into your notes, score, DAW, music production workflow, or another destination, adjusting formatting as needed.

A common presentation includes a Title, a Style description and Lyrics with section markers, but these elements need not all appear as separate output blocks in every delivery. The AI adapts the presentation to the user's requested workflow and destination.

## Examples of application

- **Vague idea:** "A sad late-night song about missing someone on a train." The AI proposes a melancholic, intimate Style, short verses with concrete images and a contained performance.
- **Existing lyric:** You paste a verse you wrote. The AI builds a Style that fits it and adds performance tags without rewriting your words unnecessarily.
- **Sound reference:** You name a song or share a link. The AI decomposes it into generic musical characteristics (without using artist names as substitutes for musical descriptions) and writes an original Style, lyrics and performance inspired by it.
- **Vocal direction:** "Start whispered, then build to a shout in the chorus." The AI keeps the Style coherent and expresses the change through section markers.

## Platform independence

Music Director is platform-independent. Its output is plain text: a Style description, lyrics with bracketed section markers and an optional Title. It does not require any specific music generation platform or tool. Adapt the formatting, markers and controls to whatever destination you use.

## Project principles

- The repository and all instructions are in English.
- Generated songs follow the language of the user's creative brief, unless another language is explicitly requested.
- No audio is ever generated by Music Director; output is exclusively textual.
- Artist, band or song names are not used as substitutes for musical descriptions. Names in lyrical content follow the user's creative intent.
- Style defines the global sound; markers define the evolution per section. They must not duplicate each other.
- Title is optional identification metadata, taken from the hook or central phrase of the chorus when used.
- User instructions have the highest priority; documentation guides but does not limit.
- The three dimensions must be coherent with each other; nothing generic.
- Music Director is a system of instructions that guides AI collaboration, not software that automatically enforces musical coherence.

## Notes

The bracketed markers are guidance for interpretation, not guaranteed commands. Their usefulness depends on context and destination. Adherence varies by destination and by conflict with the Style. If a direction is not followed, reformulate or clarify the musical intent.
