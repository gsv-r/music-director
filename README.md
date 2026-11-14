# Music Director

Music Director is a set of instructions that guides the AI to act as a musical director. It improves the quality of its responses by applying real-world best practices of composition, production and performance, to generate better lyrics, style and performance and to better understand the requested style.

It does not create music on its own. Anyone who wants the lyrics or the music still needs to give their own instructions (what they want to create, an idea, references).

## Architecture

- `AGENTS.md` — orchestration, task routing, missing information, coherence.
- `instructions/style.md` — global sonic identity (genre, tempo, instruments, voice, movement).
- `instructions/lyrics.md` — composition and lyrics (structure, prosody, singability, hooks).
- `instructions/performance.md` — interpretation and Performance direction per section (tags, dynamics).
- `library/` — local musical reference knowledge. Consulted during Performance creation/review via `library/index.md`, without loading all of its contents.

## How to use

1. Provide the instruction files (and `library/` when Performance is in scope) to a capable AI.
2. Describe your musical idea naturally (a feeling, a story, a genre, references).
3. Collaborate iteratively to refine Style, lyrics and performance.
4. Review the result and adjust as needed.

## Library

The `library/` is consulted during Performance generation/review. Consultation starts at `library/index.md` and retrieves only the relevant category files. It is local and independent of internet access during musical generation. See `library/README.md` for details.