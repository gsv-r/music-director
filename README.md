# Music Director

Music Director is a text-only tool for AI-assisted music composition, direction,
development, analysis and refinement. It works with **textual musical guidance**
and does **not** generate, render or produce audio.

It gives an AI agent a methodology, specialized modules and organized technical
knowledge so it can make better-founded musical decisions. It is for
songwriters, producers, musicians, educators and anyone using
AI-assisted music creation for music direction, musical arrangement, harmony
and rhythm, lyrics and vocal performance, or musical analysis.

**In short:** Music Director turns a creative brief into structured musical
direction — style, arrangement, lyrics, performance and an interpretive
analysis — as text. It can develop musical material in text form, but it does
not generate or render audio or deliver a finished recording.

## Contents

- [A Tool, Not a One-Click Solution](#a-tool-not-a-one-click-solution)
- [Examples of Useful Direction](#examples-of-useful-direction)
- [What is Music Director?](#what-is-music-director)
- [How it Works](#how-it-works)
- [Agent Skills Standard](#agent-skills-standard)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Scope and Limitations](#scope-and-limitations)

## A Tool, Not a One-Click Solution

Music Director is a tool for musical thinking, development and refinement — not
a one-click song generator.

Results depend on how the tool is used. A clear brief with relevant musical
context, specific intentions and well-defined constraints gives the agent a
much stronger basis for decisions than a vague request.

Your involvement matters. Say what the music should communicate, how it should
sound, what to preserve, what to avoid and how detailed the result should be.
Then review it, question weak decisions and ask for adjustments — refinement is
part of the process.

In practice:

- State the emotional, sonic and artistic intention, not just a genre.
- Include constraints, references and elements that must be preserved.
- Match the level of detail to the project: a simple idea needs little, while a
  developed composition needs more context and refinement.
- Review the result, question decisions and provide additional context as the
  project develops.

**Music Director provides the tools, knowledge and methodology. The user
provides the creative direction, judgment and decisions.**

## Examples of Useful Direction

Small changes in how a request is framed can change how much useful material the
agent has to work with. These illustrations are not required templates — they
simply show the difference between a vague request and a useful direction.

| Vague request | More useful direction |
|---|---|
| Make a song about longing. | Write about missing someone who is still present, with restrained nostalgia and no melodrama. |
| Make an indie folk song. | Use organic indie folk, acoustic guitar as the rhythmic foundation, close vocals, subtle chorus development and low rhythmic density. |
| Improve these lyrics. | Review prosody, imagery, natural phrasing, emotional development and singability. Preserve what works and suggest only necessary changes. |

## What is Music Director?

An agent working on music needs a way to turn creative intent into decisions
about sound, form, text and performance, and to check those decisions against
one another. Music Director supplies that method: it routes each task to the
modules it actually needs, draws on transversal domains and local technical
references when they are pertinent, and reviews the integrated result against
the brief. Musical conventions inform those decisions but never fix them in
advance; the user makes the final calls.

The project covers several areas of activity. They are deliberately divided
into **specialized modules**, which own a deliverable, and **transversal
domains**, which inform decisions across modules.

| Category | Areas | Role |
|---|---|---|
| Specialized modules | **Style**, **Arrangement**, **Lyrics**, **Performance**, **Analysis** | Own a specific output. Style defines global sonic identity; Arrangement handles form, layers, density and development; Lyrics writes and reviews sung text; Performance interprets each section; Analysis explains the consolidated result. Analysis is a module, not a sonic dimension. |
| Transversal domains | **Creative Direction**, **Harmony**, **Rhythm**, **Production** | Inform several modules at once without owning a separate deliverable. Creative Direction organizes artistic intent; Harmony and Rhythm shape tonal and rhythmic decisions; Production covers acoustic, spatial and processing treatment — reverb, ambience, placement and recording character — while Arrangement owns form, layers, density and section-by-section development. Production is a transversal decision domain, not an independent specialized module. |
| Cross-cutting capabilities | **Review of existing compositions**, **Musical reference handling** | Apply the same methodology to analyzing or revising existing work and to working from a reference without copying it. |

## How it Works

```text
Brief → Intention → Module selection → References → Decisions → Review
```

1. The user provides a creative brief.
2. The agent interprets the musical intention and constraints.
3. Relevant specialized modules are selected.
4. Technical references are consulted when appropriate.
5. Musical decisions are developed and integrated.
6. The result is reviewed for coherence and delivered for user evaluation.

Not every module or reference is used in every composition. The methodology
adapts to the task: a style prompt, a lyric review and a full song each call for
a different amount of work. Technical knowledge informs judgment rather than
replacing it, and conventions are treated as possibilities, not mandatory
recipes.

## Agent Skills Standard

The Agent Skills format packages a skill as a folder containing a `SKILL.md`
file. That file begins with YAML frontmatter containing two required fields,
`name` and `description`; the description tells an agent when the skill is
relevant. Music Director follows that format, so a compatible agent can load it
when the task matches.

The documentation is organized into three parts:

| Path | Function |
|---|---|
| `SKILL.md` | Entry point and initial guidance for the agent: activation, navigation and module selection. |
| `references/instructions/` | Methodology and specialized instructions, including the canonical orchestration rules. |
| `references/library/` | Organized technical knowledge and musical references that inform decisions. |

Loading is progressive: the agent reads the entry point first, then opens only
the instructions and library sections the task requires, instead of loading the
whole documentation at once. This keeps the relevant knowledge available without
turning references into mandatory reading.

`README.md` is the human-facing documentation you are reading. `SKILL.md` is the
instruction file for agents; operational rules live under
`references/instructions/`.

## Repository Structure

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

- `SKILL.md` — the skill entry point for agents.
- `AGENTS.md` — a short compatibility pointer for tools that automatically load
  that file. It is not a second source of rules.
- `README.md` — this public, human-facing documentation.
- `references/instructions/` — the methodology: one canonical orchestration file
  and one file per specialized module.
- `references/library/` — local reference knowledge, organized by area
  (arrangement, harmony, performance, production and rhythm), with an index for
  navigation and a README describing the collection.

## Getting Started

These are three distinct steps:

1. **Make the skill available to your agent.** Place this folder — or a copy or
   symbolic link of it — where your agent looks for skills, or register it
   through the agent's own mechanism. The folder name and the declared skill name
   are both `music-director`. Keep the folder together: `SKILL.md` and the two
   `references/` trees are all part of the skill. Installation and discovery
   differ across agents and versions, so follow your platform's documentation
   rather than assuming a universal command.
2. **Let the agent read `SKILL.md`.** That file is the entry point. It directs
   the agent to the applicable instructions and to the knowledge index.
3. **Consult complementary references as needed.** Additional instructions and
   library entries are opened only when the task calls for them; there is no
   requirement to read everything up front. Agents resolve these paths relative
   to the skill root.

Then describe what you want — a full song, a style direction, lyrics,
performance direction, an arrangement or an analysis — and work iteratively from
there.

## Scope and Limitations

- Music Director provides **textual musical guidance** only.
- It does **not** generate, render or produce audio, and it does not operate
  music-generation platforms or claim that a recording has been made.
- The user keeps control of the creative decisions; the tool supplies criteria,
  vocabulary, methods, questions and checks, and develops musical material from
  the brief instead of starting from a default composition.
- Technical knowledge grounds decisions but is not a mandatory formula. No
  lyrics, complete style description, structure or development arc is supplied
  as a default to copy.
- Reference consultation follows the skill's rules and depends on relevance to
  the task; not every reference is opened for every composition.
- Results depend on the brief, the context, the direction and the refinement
  process. The documentation in English does not set the language of the song —
  that follows the user's brief.
