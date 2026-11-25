# Music Director

Music Director is a text-only tool for AI-assisted music composition, direction, development, analysis and refinement. It gives an AI agent a method, specialized modules and organized technical knowledge, so its decisions have something to stand on.

The output is written guidance: style, arrangement, lyrics, performance direction and analysis. Nothing here generates audio or renders a recording. The tool develops material in text form from a brief; it does not deliver a finished song file.

It is for songwriters, producers, musicians, educators and anyone using AI-assisted music creation for music direction, arrangement, harmony and rhythm, lyrics and vocal performance, or musical analysis.

## Contents

- [A tool, not a one-click solution](#a-tool-not-a-one-click-solution)
- [Examples of useful direction](#examples-of-useful-direction)
- [What is Music Director?](#what-is-music-director)
- [How it works](#how-it-works)
- [Agent Skills standard](#agent-skills-standard)
- [Repository structure](#repository-structure)
- [Getting started](#getting-started)
- [Scope and limitations](#scope-and-limitations)

## A tool, not a one-click solution

Music Director is for musical thinking and refinement. It is not a button that returns a finished song.

What you get depends on what you bring. A brief with real musical context, clear intentions and firm constraints gives the agent far more to work with than "make me a song." Say what the music should communicate, how it should sound, what must stay, what to avoid and how finished the result should be. Then read it, question weak choices and ask for changes. Refinement is part of the work.

A few habits that help:

- Give the emotional and sonic intention alongside the genre.
- Include references and elements that have to survive the process.
- Scale the detail to the project. A sketch needs less than a developed arrangement.
- Keep reviewing as the piece takes shape.

## Examples of useful direction

The way you phrase a request changes how much the agent has to work with. These are illustrations, not templates to copy.

| A vague request | Something the agent can use |
|---|---|
| Make a song about longing. | Write about missing someone who is still present, with restrained nostalgia and no melodrama. |
| Make an indie folk song. | Use organic indie folk, acoustic guitar as the rhythmic foundation, close vocals, subtle chorus development and low rhythmic density. |
| Improve these lyrics. | Review prosody, imagery, natural phrasing, emotional development and singability. Keep what works and suggest only necessary changes. |

## What is Music Director?

An agent working on music has to turn intent into decisions about sound, form, text and performance, then check those decisions against each other. Music Director supplies that method. It routes each task to the modules the work actually needs, pulls in technical references when they help and reviews the result against the brief. Conventions inform the decisions; they do not settle them in advance. You make the final calls.

The work splits into specialized modules, which own a deliverable, and transversal domains, which inform several modules at once.

| Category | Areas | What it does |
|---|---|---|
| Specialized modules | Style, Arrangement, Lyrics, Performance, Analysis | Each owns an output. Style sets the global sonic identity. Arrangement handles form, layers, density and development. Lyrics writes and reviews sung text. Performance interprets each section. Analysis explains the consolidated result. Analysis is a module, not a sonic dimension. |
| Transversal domains | Creative Direction, Harmony, Rhythm, Production | These inform modules without owning a separate deliverable. Creative Direction organizes artistic intent. Harmony and Rhythm shape tonal and rhythmic decisions. Production covers acoustic, spatial and processing treatment: reverb, ambience, placement, recording character. Form, layers, density and section-by-section development stay with Arrangement, not Production. |
| Cross-cutting capabilities | Review of existing compositions, Musical reference handling | The same method applied to revising existing work, or to working from a reference without copying it. |

## How it works

```text
Brief → Intention → Module selection → References → Decisions → Review
```

1. You give a creative brief.
2. The agent reads the musical intention and constraints.
3. It selects the modules the task needs.
4. It consults technical references where relevant.
5. Decisions are developed and integrated.
6. The result is checked for coherence and handed back to you.

Not every module or reference is used every time. A style prompt, a lyric review and a full song each ask for different amounts of work. Technical knowledge supports judgment; conventions are options, not recipes.

## Agent Skills standard

The Agent Skills format is a folder with a `SKILL.md` file at its center. That file starts with YAML frontmatter holding two required fields, `name` and `description`. The description tells an agent when the skill applies. Music Director follows the format so a compatible agent can load it when the task fits.

The documentation has three parts:

| Path | What it holds |
|---|---|
| `SKILL.md` | Entry point: activation, navigation and module selection. |
| `references/instructions/` | Methodology and specialized instructions, including the canonical orchestration rules. |
| `references/library/` | Organized technical knowledge that informs decisions. |

Loading is progressive. The agent reads the entry point first and opens only the instruction and library sections the task needs, rather than reading everything at once. The relevant knowledge stays available without turning references into required reading.

`README.md` is the human-facing documentation. `SKILL.md` is for agents, and the operational rules live in `references/instructions/`.

## Repository structure

```text
music-director/
├── AGENTS.md
├── README.md
├── SKILL.md
└── references/
    ├── instructions/
    │   ├── analysis.md
    │   ├── arrangement.md
    │   ├── lyrics.md
    │   ├── orchestration.md
    │   ├── performance.md
    │   └── style.md
    └── library/
        ├── README.md
        ├── index.md
        ├── arrangement/
        ├── harmony/
        ├── performance/
        ├── production/
        └── rhythm/
```

- `SKILL.md` is the entry point for agents.
- `AGENTS.md` is a compatibility pointer for tools that auto-load that file. It is not a second set of rules.
- `README.md` is this file.
- `references/instructions/` holds the methodology: one canonical orchestration file plus one file per module.
- `references/library/` holds local reference knowledge by area, with an index for navigation and a README describing the collection.

## Getting started

Three steps.

1. Make the skill available to your agent. Put this folder, or a copy or symlink of it, where your agent looks for skills, or register it through the agent's own mechanism. The folder name and the declared skill name are both `music-director`. Keep the folder intact: `SKILL.md` and both `references/` trees are part of the skill. Install and discovery differ between agents and versions, so follow your platform's docs instead of assuming a universal command.
2. Let the agent read `SKILL.md`. It is the entry point and points to the right instructions and the knowledge index.
3. Open complementary references only as needed. Nothing has to be read up front. Agents resolve these paths relative to the skill root.

Then describe the work, a full song, a style direction, lyrics, performance direction, an arrangement or an analysis, and iterate.

## Scope and limitations

- Music Director gives textual musical guidance only.
- It does not generate, render or produce audio, operate a music-generation platform or claim a recording exists.
- You keep the creative decisions. The tool supplies criteria, vocabulary, methods, questions and checks, and develops material from your brief rather than from a default composition.
- Technical knowledge grounds decisions without becoming a formula. No lyrics, full style description, structure or development arc comes ready-made to copy.
- References are consulted according to the skill's rules and the needs of the task, not all at once.
- Results depend on the brief, the context, the direction and the refinement. The documentation is in English; the language of the song follows your brief.
