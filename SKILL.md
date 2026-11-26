---
name: music-director
description: >-
  Turns a creative brief into structured, text-only musical direction: lyrics
  with section and performance markers, a one-line Style description, a title,
  and a short analysis for the user. Use when the user wants to write a song,
  draft or review lyrics, build a sound/style prompt, direct vocal performance
  per section, plan a song's form, analyze existing lyrics, adapt a song to
  another language, or work from a musical reference. Never generates, renders,
  or produces audio.
---

# Music Director

A text-only skill. Given a brief, it delivers three copyable fields, lyrics,
style and title, plus a short analysis written for the user. It never generates
or produces audio, and it does not operate any music-generation platform.

## Read order

1. `references/instructions/orchestration.md`: canonical rules, principles,
   field mapping, coherence, delivery format and validation.
2. `references/instructions/best-practices.md`: the short guide to what actually
   improves the three fields. Read it before any generation.
3. Open only the modules the request needs (table below).
4. Open `references/library/index.md` only when a term or audible effect needs
   grounding, then read the pointed section, not the whole file.

If two files seem to disagree, `orchestration.md` governs.

## Modules

| File | Open when | What it contributes |
|---|---|---|
| `orchestration.md` | Always | Universal rules and final delivery format |
| `best-practices.md` | Always, before generating | Concrete criteria for lyrics, style, title, analysis |
| `style.md` | A global sound is needed | One-line sonic identity |
| `lyrics.md` | Sung text is created, changed or reviewed | Content, structure, singability |
| `performance.md` | Section marks are needed | Audible indications inside the lyrics |
| `arrangement.md` | Form and layers are planned | Internal plan folded into lyrics and style |
| `analysis.md` | Analysis is in scope | Short explanation for the user |

Form and layer decisions are internal planning: they are written into the
section markers of the lyrics and the description of the style, never delivered
as a separate field.

## Knowledge library

`references/library/` is local vocabulary: what a term means, its audible
effect, when it fits and when it does not. Start at `references/library/index.md`
and open only the pointed file and section. The library informs decisions; it
never overrides the modules. No external research during generation. No
tool-specific directives or tool-specific tags belong in the library.

## Selecting modules

| Request | Modules |
|---|---|
| Full song | Style, Lyrics, Performance, Analysis (Arrangement as internal plan) |
| Style only | Style |
| Lyrics only | Lyrics, plus the Analysis check |
| Instrumental | Style, Performance, Arrangement (no sung text invented) |
| Review | Modules matching the material |
| Adapt to another language | Lyrics, Style, Performance as needed |
| From a reference | Only the modules the deliverable needs |

Do not run a module the request does not need. The base always comes from the
user's brief: no ready-made lyrics, style lines, structures or arcs.
