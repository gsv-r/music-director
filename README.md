# Music Director

Music Director is a text-only skill for AI-assisted music composition and direction. It gives an agent a structured method for turning a creative brief into written musical guidance: global style direction, lyrics, form and arrangement, performance directions for each section, and an interpretation of the finished result. The output is meant to be read, questioned and revised by people. Music Director does not generate or render audio, and it does not open, trigger, control or operate a music-generation platform. It is for songwriters, producers, musicians and educators who want written direction they can examine and take into their own work.

## What you can use it for

Music Director works on vocal and instrumental music, from a first sketch to a developed arrangement. Typical requests include:

- Developing a vocal or instrumental composition from a brief.
- Building a global style direction you can hand to a producer or use as a prompt elsewhere.
- Writing lyrics, or reviewing existing lyrics for prosody, imagery, singability and emotional development.
- Planning form and arrangement: section order, layers, entries and exits, density and transitions.
- Writing performance directions section by section, including dynamics and vocal delivery.
- Analyzing or reviewing an existing composition against your intentions.
- Adapting lyrics to another language, with prosody and vocal diction adjusted to the target language.
- Working from a musical reference and translating what it does into generic descriptors rather than copying its material.

## How the method works

An agent working on music has to turn intent into decisions about sound, form, text and performance, then check those decisions against each other. Music Director gives that work a structure. Specialized modules own a deliverable; transversal domains inform the modules without owning one.

| Category | Areas | What it does |
|---|---|---|
| Specialized modules | Style, Arrangement, Lyrics, Performance, Analysis | Style owns the global sonic identity: genre, tempo, instruments with their functions, voice and overall movement. Arrangement owns form, sections, order, relative durations, layers, entries and exits, density, texture, transitions and instrumental development across sections. Lyrics owns sung text: content, structure, prosody, singability, hook and addressee. Performance owns interpretation and execution of the parts: per-section dynamics, expressive change, articulation, timing and delivery. Analysis is an interpretive module, not a sonic dimension. It explains the consolidated result against the brief and checks it for coherence before delivery. |
| Transversal domains | Creative Direction, Harmony, Rhythm, Production | Creative Direction organizes artistic intent: premise, contrast, density, emotional trajectory and constraints. Harmony informs tonal center, scales and modes, consonance and dissonance, function, cadence and harmonic rhythm. Rhythm informs meter, groove, feel, syncopation and rhythmic density. Production owns acoustic, spatial and processing treatment: ambience, reverb, placement and recording character. Form, layers, density and instrumental development remain with Arrangement. |

The sequence is:

```text
Brief → Intention → Module selection → References → Decisions → Review
```

Reference knowledge covers performance, form and structure, rhythm and groove, production texture, harmony and tonality, and lyrical meaning. Technical knowledge informs decisions without determining them: a convention describes common practice, and which ones apply is decided for each piece. Not every task uses every module or reference. A style direction, a lyric review and a full song ask for different amounts of work.

## Working with the agent

The brief is the starting material. Give the agent the context you have: what the music should communicate, how it should sound, what must survive, what to avoid and how finished the result should be. Include references and constraints that matter to you. Match the detail to the project; a sketch needs less than a developed arrangement.

The agent develops material from that brief and presents its decisions for review. Read what comes back, question weak choices and ask for specific changes as the piece takes shape. Music Director supplies criteria, vocabulary, methods, questions and checks. It does not supply ready-made lyrics, complete Style lines, structures or development arcs to copy as defaults. The documentation is in English; the language of the song follows your brief.

## Delivery format

The creative process stays open: Style, Arrangement, Lyrics, Performance, Analysis, Creative Direction and the technical library contribute as much as the task needs. The final answer translates that work into four fields in a fixed order: lyrics, style, title, analysis. The first three are code blocks containing only the generated text; the fourth is readable prose for the user to understand the composition. Field labels are never written in the answer, so copying a block gives only the generated text. The canonical definition of the format, including what each field contains, lives in `references/instructions/orchestration.md`, "Final delivery format (mandatory)", as part of the execution flow rather than as a separate document.

## Examples of useful direction

The way you phrase a request changes how much the agent has to work with. These are illustrations, not templates to copy.

| A vague request | Something the agent can use |
|---|---|
| Make a song about longing. | Write about missing someone who is still present, with restrained nostalgia and no melodrama. |
| Make an indie folk song. | Use organic indie folk, acoustic guitar as the rhythmic foundation, close vocals, subtle chorus development and low rhythmic density. |
| Improve these lyrics. | Review prosody, imagery, natural phrasing, emotional development and singability. Keep what works and suggest only necessary changes. |

## Technical format and getting started

Music Director is packaged as an Agent Skill: a directory with `SKILL.md` at its center. That file begins with YAML frontmatter containing the required `name` and `description` fields. Both the directory name and the declared name are `music-director`. Compatible agents use the description to decide when the skill applies. `SKILL.md` is the entry point; the agent opens instruction modules and library files only as the task needs them, starting from the library index. Keep the folder intact, including both `references/` trees.

The documentation is split by audience and purpose:

- `README.md` presents the project to people.
- `SKILL.md` gives agents activation, navigation and module selection.
- `references/instructions/` holds the methodology, with `orchestration.md` as the canonical rule set.
- `references/library/` holds technical and musical reference knowledge that informs decisions.

Getting started takes two steps:

1. Make the skill available to your agent. Put this folder, or a copy or symlink of it, where the agent looks for skills, or register it through the agent's own mechanism. Installation and discovery differ between agents and versions, so follow your platform's documentation rather than assuming a universal command.
2. Give the agent a brief describing the work you want and the context you have.

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
        ├── lyrics/
        ├── performance/
        ├── production/
        └── rhythm/
```

`AGENTS.md` is a compatibility pointer for tools that auto-load that file. It is not a second set of rules.
