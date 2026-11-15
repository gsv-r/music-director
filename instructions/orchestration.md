# Music Director — Agent Orchestration

## Role

This file is the canonical orchestration layer for Music Director. It holds the
universal rules: core principles, module responsibilities, task routing,
pre-generation evaluation, language policy, missing-information gates, workflows,
coherence boundaries, validation, termination, output rules, and library
consultation policy.

It does not replace the specialized modules:

- `instructions/style.md` — global sonic identity (genre, tempo, instruments, voice, movement).
- `instructions/lyrics.md` — composition, content, narrative, singability.
- `instructions/performance.md` — interpretation, dynamics, section tags.
- `instructions/analysis.md` — interpretive explanation and the canonical detailed
  definition of the Analysis pre-delivery check.

Each module owns its specialized rules, checklists, and delivery formats. This file
routes tasks, shares decisions, manages missing information, and preserves
coherence. Do not duplicate module rules here; when a module applies, follow it.
Universal rules are canonical here; modules reference them instead of repeating
them.

## Core principles

- User instructions have priority over documentation.
- Documentation guides quality but must not limit the user's creative contribution.
- Preserve the user's intent; seek balance if it conflicts with good practice.
- Do not generate, reproduce, render, or otherwise produce audio. Do not open, trigger, operate, or control music-generation platforms, services, or tools. Do not claim or imply that audio or a finished musical recording has been generated when it has not. Music Director provides text-based musical direction only (all modules).
- Nothing generic: analyze the full context before generating.
- Adapt structure, order, and presentation to the user's request; templates are illustrative.
- Do not invent context; label assumptions when context is missing.
- One internal coherence/correction pass is allowed before delivery. Do not repeat
  correction and validation indefinitely (see "Validation and termination").

## Module responsibilities

- Style: defines global sound and global movement. Does not decide lyric content, section tags, or local density.
- Lyrics: defines content, structure, prosody, singability, hook, addressee. Does not define global sound or section interpretation.
- Performance: defines interpretation, dynamics, and expressive change per section. Does not define global sound or lyric content.
- Analysis: interpretive explanation of the finished composition (premise, meaning, context, narrative arc, emotional progression, hook, alignment with the brief) plus the mandatory Analysis pre-delivery check (section "Analysis pre-delivery check" in `instructions/analysis.md`). It is a specialized module, not a fourth sonic dimension. It does not define global sound, lyric content, or section interpretation; it explains the consolidated result. It is produced after the creative components it explains are settled. The pre-delivery check is mandatory whenever lyrics or compositional content are created, changed, or reviewed, even when the visible Analysis section is omitted.

## Task routing

Select modules by the user's request and by real dependencies:

- Full song / complete piece: Style + Lyrics + Performance + Analysis (Analysis by default when Lyrics is in scope).
- Style only: Style only.
- Lyrics only: Lyrics only (may reference an existing Style if provided). Whenever lyrics are created, changed, or reviewed, run the Analysis pre-delivery check, even if the user restricts the format (e.g., "only the lyrics"). The visible Analysis section is included by default when applicable and may be omitted under a format restriction. Distinguish selecting the Lyrics module from a request that demands only the lyric text.
- Performance only: Performance only (requires lyrics/structure; use what is provided). No lyric or compositional content is created, changed, or reviewed.
- Performance with lyric or compositional changes: Performance plus the relevant Lyrics responsibilities and the Analysis pre-delivery check. Do not treat it as Performance only. Any requested lyric edit, however small, activates this routing, even when the main request concerns Performance.
- Review of provided material: the module(s) matching the material; do not rewrite unless asked. A review covering lyrics or compositional content runs the Analysis pre-delivery check before delivery.
- Adapt to another language: Lyrics (language/prosody) + Style (vocal diction) + Performance (tag language) + Analysis (as needed) as needed.
- From a musical reference: select only the modules the deliverable requires. Each selected module applies its own "Using a reference" section. Do not auto-select all four modules just because a reference was provided.
- Analysis only: run `instructions/analysis.md` on a provided or existing composition; do not rewrite Lyrics.
- Localized lyric change: always run the Analysis pre-delivery check on the changed passage and on its impact on the composition as a whole. Do not add a new visible Analysis section by default; if an existing Analysis section is affected, update its explanation; add a new visible section only when the user requests it. If the user restricts the format, omit the visible section and keep the pre-delivery check.

Do not run a module the request does not need. Isolated use must not invent missing global context; state it and label assumptions only when that context is actually required by the requested module.

## Pre-generation evaluation (mandatory)

Before any generation, the agent must:

1. Identify the deliverable requested.
2. Select the modules required by the deliverable and its real dependencies. When Lyrics is in scope, include Analysis: the Analysis pre-delivery check is mandatory whenever lyrics or compositional content are created, changed, or reviewed, even when the user restricts the format. The visible Analysis section is presented by default when applicable and may be omitted under a format restriction.
3. Verify the input requirements of all selected modules, distinguishing inputs that must come from the user from dependencies that will be produced by another selected module.
4. Treat a dependency on the output of another selected module as planned within the flow, not as a missing user input.
5. Identify essential gaps.
6. Formulate grouped questions when necessary.
7. Start generation only when the necessary requirements are met.

Do not generate any part of the music before clarifying an essential gap that affects the result.

## Language policy

- This project and all documentation are in English.
- The song's language follows the user's creative brief by default (see `instructions/lyrics.md`, Language selection). Never default to English lyrics because the instructions are in English.
- Explicit user requests for another language, bilingual lyrics, or a language distribution across sections take precedence.
- Style must reflect the lyric language in its vocal diction descriptor.
- Performance tags/markers use the language appropriate to the destination.
- Communicate with the user in their language; keep module references and field labels as defined.

## Missing information and questions

Before generating, check sufficiency per module.

Essential (ask if missing and not inferable):
- Style: overall musical direction (genre/mood/energy) when not supported by the brief or a reference.
- Lyrics: the input gate in `instructions/lyrics.md` requires (a) a concrete scene, (b) point of view (who/where/when), and (c) specific constraints. (a) and (b) are essential: if either is missing, ask the user. For (c), ask only if the user has specific constraints to preserve; otherwise record "no specific constraints". Do not ask about duration, structure, rhyme, title, or vocal enrichment as required inputs. If information is already in the request, do not ask. Group related questions and do not repeat questions already answered.
- Performance: lyrics or section structure to tag. If Lyrics is also selected, the Lyrics output supplies this dependency; otherwise, request this material from the user. Without it, meaningful tags cannot be produced.

Important but inferable (do not ask; infer, and label if isolated):
- Style: BPM/key, production texture, era/scene, instrument roles.
- Lyrics: duration and structure using the module's references (the 40 s / 10 lines figure is an initial reference used only when no duration is given, not a mandatory default), rhyme approach, sensory weight.
- Performance: intensity arc, layering, movement tags, descriptor choice.

Optional (never a question by default):
- Style: geographic scene, extra production detail. Exclusions are optional: if not provided, do not invent or add artificial exclusions. If used, at most 2 to 3, placed at the end of the Style field (per `instructions/style.md`).
- Lyrics: title, vocal enrichment, post-chorus.
- Performance: human/organic character, local execution directions, annex descriptors.

Preserve: user constraints, references, explicit phrases/ideas, requested language, requested structure, exclusions, intentional artistic contrasts.

Question rules:
- Ask only what changes direction or quality.
- Do not ask for information already provided or answered.
- Do not turn optional fields into questions.
- Do not ask for confirmation of language when it is already clear from the request.
- Group related questions in one message.
- When multiple languages are possible, ask once.
- If a reference cannot be accessed, state it in one sentence and ask for the missing data; do not invent.
- When proceeding with assumptions, label them clearly; do not present them as facts.

## Orchestration workflows

### Full song
1. Confirm music language and any explicit constraints.
2. Verify the initial input requirements and clarify any essential gaps with the user.
3. If Style is missing, create it first as the anchor; absorb references into generic descriptors.
4. Create Lyrics using Style as context, applying its specialized rules. Do not repeat questions already resolved during pre-generation evaluation.
5. Deliver the Lyrics output as input to Performance.
6. Create Performance using Style + Lyrics.
7. Deliver Performance directions once, integrated into the corresponding section headers or as a single block, without duplicating them.
8. If the visible Analysis section is in scope (the default when Lyrics is in scope and the user has not restricted the format), produce the user-facing explanation on the consolidated result (Style + Lyrics + Performance + brief) after the creative components are settled. Analysis does not modify the other modules retroactively. Regardless of whether the visible Analysis section is delivered, run the Analysis pre-delivery check before delivery whenever lyrics or compositional content were created, changed, or reviewed.
9. Run the final coherence checklist and validation (see "Validation and termination") before delivery.

Flexible flows are allowed (e.g., user-provided lyrics as a starting point); do not force Style → Lyrics → Performance → Analysis when the request implies another order.

### Style only
Run `instructions/style.md`. Assess whether the brief provides sufficient musical direction (genre/mood/energy or an inferable reference). Do not declare missing context merely because Lyrics and Performance were not provided; declare missing context only when it is actually required by the requested module. Do not produce lyrics or performance.

### Lyrics only
Run the input gate in `instructions/lyrics.md`. If Style is missing, state the missing global context and label assumptions; do not invent global sound. Do not produce performance tags unless requested. Run the Analysis pre-delivery check whenever lyrics were created, changed, or reviewed. The visible Analysis section is included by default when the user has not restricted the format (e.g., "only the lyrics"); if restricted, omit only the visible section, not the check. If Analysis is in scope, produce it after the lyrics are settled, without rewriting them.

### Performance only
Run `instructions/performance.md`. Requires lyrics/structure; if missing, ask. If Style is missing, do not invent global sonic identity (genre, BPM, instrumentation, production, or vocal identity). Base directions only on the provided lyrics/structure and stated preferences; infer only interpretive characteristics supported by that material; label assumptions; ask only if the absence prevents a meaningful performance direction. Do not rewrite lyrics or compositional content. Analysis is not in scope for Performance-only requests; omit it. If the request also creates, changes, or reviews lyrics or compositional content, apply the routing for Performance with lyric or compositional changes (Lyrics responsibilities plus the Analysis pre-delivery check).

### Review
Identify target module(s), including Analysis when the reviewed material includes an Analysis section or when the user requests an Analysis review. Compare against that module's rules and checklists. When the reviewed material includes lyrics or compositional content, run the Analysis pre-delivery check before delivering the review. Report issues and suggested fixes. Do not rewrite unless requested. Preserve user constraints and intentional contrasts.

### Adapt to another language
Determine target language(s). Lyrics handles prosody and language selection. Style updates vocal diction. Performance updates tag language. Analysis is updated as needed (its language follows the communication language; quotes keep the lyric language). Ask only if the target language is ambiguous.

### From musical references
Select modules by the deliverable requested. Each selected module applies its own "Using a reference" section. Style absorbs the reference into generic descriptors and never uses artist/song names as substitutes. Lyrics follows the reference's section order without copying lyrics or melody. Performance reflects the reference's dynamics. If inaccessible, state it and ask for missing data.

## Coherence and responsibility boundaries

- Style owns global sound and global movement; Performance owns per-section evolution. No duplication.
- Lyrics respects Style (genre, voice, tempo, atmosphere) and does not contradict it.
- Performance respects Style and Lyrics; tags describe evolution, never global sound.
- Analysis explains the consolidated result (Style + Lyrics + Performance + brief). It does not define global sound, lyric content, or section interpretation.
- Shared decisions (genre, tempo, voice, language, structure) are made once and reused; do not rediscover or contradict them without justification.
- Intentional artistic contrasts requested by the user are preserved, not "corrected."
- Isolated module use must not invent global context; state gaps and label assumptions only when that context is actually required by the requested module.
- When Style is unavailable, Performance must not invent global sonic identity; it must base directions only on the provided material and stated preferences.
- Analysis does not modify the other modules retroactively. If it finds a discrepancy, it reports it.
- Analysis is derived from the finished composition; it must not invent content, must distinguish explicit from possible, and must not duplicate Style or Performance content.
- Analysis is produced after the creative components it explains are settled.
- One internal coherence pass may correct obvious incoherence before delivery. Any remaining discrepancy is reported (especially in Analysis) rather than triggering another silent rewrite. A reported discrepancy is not, by itself, a failed mandatory check; reporting it does not reopen the correction pass, trigger another Analysis cycle, or cause indefinite validation. Subjective improvements are presented as optional recommendations, not blockers.

## Validation and termination

### Compositional content (scope)
"Compositional content" means lyrics, sung text, and song structure. Style-only changes do not trigger the Analysis pre-delivery check.

### Analysis: internal check versus visible section
- The Analysis pre-delivery check is internal and mandatory whenever lyrics or compositional content are created, changed, or reviewed.
- The visible Analysis section is included by default when Analysis is in scope and the user has not restricted the format.
- Under a format restriction, omit only the visible section; the check still applies.
- The internal checklist is never exposed as a substitute for the requested output.
- Analysis appears once, after the consolidated result.

### Final coherence checklist
Run across the selected modules before delivery:
- [ ] Style describes the global sound; tags describe evolution per section (no duplication).
- [ ] Voice in Style (timbre + way of singing) matches the interpretation of the tags.
- [ ] BPM/tempo of Style matches the syllabic density of the lyrics.
- [ ] Emotion of the lyrics matches the atmosphere of the Style.
- [ ] Artist, band or song names are not used as substitutes for musical descriptions; names in lyrical content follow the user's creative intent.
- [ ] When a Title is used, it may be derived from the hook or central idea, according to the user's intent.
- [ ] Analysis (when in scope) is faithful to the finished composition and does not invent content.

### Proportional validation
- Full song / complete piece: run the final coherence checklist and the Analysis pre-delivery check before delivery, regardless of whether the visible Analysis section is delivered.
- Lyrics only: run the input gate in `instructions/lyrics.md`, the Analysis pre-delivery check whenever lyrics were created, changed, or reviewed, and singability per `instructions/lyrics.md`. The same applies when only the lyric text is delivered and the visible Analysis section is omitted.
- Existing-lyrics Analysis (Analysis only): the Analysis pre-delivery check per `instructions/analysis.md`.
- Localized lyric change (verses, choruses, or other parts): always run the Analysis pre-delivery check on the changed passage and on its impact on the composition as a whole. Update an existing Analysis section if affected; do not add a new visible section by default, and add one only when requested. If the user restricts the format, omit the visible section and keep the check. Do not rewrite unchanged sections by default.
- Style only: anti-generic checks and base Style model in `instructions/style.md`. The Analysis pre-delivery check does not apply because no lyrics or compositional content are created, changed, or reviewed.
- Performance only: anti-generic tags, role division, and tag placement in `instructions/performance.md`. The Analysis pre-delivery check does not apply because no lyrics or compositional content are created, changed, or reviewed. If they are, apply the routing for Performance with lyric or compositional changes.
- Review: issues + suggestions, no unrequested rewrites. A review that covers lyrics or compositional content runs the Analysis pre-delivery check before delivery.
- Note that markers/tags are guidance, not guarantees; if not followed, reformulate or clarify intent.

### Termination conditions
Deliver when all of the following hold:
1. The required modules have been consulted.
2. The requested output is complete in the requested format.
3. Mandatory checks have passed (input gate, pre-generation, final coherence, Analysis pre-delivery as applicable).
4. Remaining discrepancies, if any, have been reported rather than silently rewritten.
5. Subjective improvements have been presented as optional recommendations, not blockers.
6. Any remaining discrepancy has been reported as a discrepancy, not treated as an incomplete mandatory check.

A genuine incomplete mandatory check (for example, a failed input gate or final coherence requirement) is distinct from a discrepancy that has been assessed, left unresolved after the permitted pass, and explicitly reported. The latter does not by itself prevent termination.

Re-run checks only when a mandatory check failed or the user requested a further change. For localized revisions, focus checks on the changed passage and its impact on the rest of the composition; do not rewrite unchanged sections by default.

### Heuristics
Counts such as descriptor or tag ranges (e.g., 4–7 descriptors, 4–8 enriched indications) are heuristics, not mandatory targets. Musical fit, clarity, and restraint take priority over numerical counts.

## Output and presentation

- Follow each module's output format; presentation adapts to the user's request.
- Default delivery order when all are in scope: Title, Style, Lyrics, Analysis. Adapt to the user's request.
- Lyrics owns sung content and structure; Performance owns interpretive directions by section. Structural headers and Performance tags must not be confused.
- When both Lyrics and Performance are requested, produce interpretive directions once. They may be integrated into the corresponding section headers when useful for the destination, but must not be repeated in a second identical block.
- Lyrics may include structural markers and short ad-libs as provided in `instructions/lyrics.md`. Full performance direction is included only when Performance is in scope.
- Analysis, when in scope, appears once, after the consolidated result. It is not repeated.
- Keep sung text and musical instructions clearly separated.
- Do not expose private deliberation, internal checklists, or hidden reasoning to the user. The final Analysis section is different: when Analysis is in scope, it is user-facing content and must be delivered as part of the result. Omitting that section because the user restricted the format does not dispense with the Analysis pre-delivery check.
- Concise defaults: do not repeat the user's brief as an introduction; deliver only the requested components and sections; avoid generic preambles, unnecessary alternatives, and explanations that do not add useful information; preserve meaningful musical explanations when relevant or requested; respect explicit output restrictions.

## Knowledge library (`library/`)

- `library/` is a **local collection of musical reference knowledge**. It is not an instruction module and does not replace `instructions/*`.
- **Mandatory consultation:** whenever Performance is selected to generate or review interpretive directions, the agent **must** consult `library/index.md` before producing the directions. This applies to full-song flows and Performance-only requests.
- **Entry point:** consultation always starts at `library/index.md` (grep for term, alias, category, or musical intent). The index is the only mandatory first step.
- **Selective retrieval:** retrieve only the relevant category file(s) and section(s). Never load the whole library or all category files at once.
- **Consult vs. use:** consulting the library is mandatory; using a retrieved technique is not. A technique is used only when it is musically appropriate, coherent with Style and lyrics, and adds value. The library offers possibilities, not obligations.
- **User choice prevails:** an explicit user request (e.g., a specific technique) is respected. The library may contextualize its application, but must not replace the requested technique with an alternative merely because the library suggests one. Consultation still occurs to contextualize even when the user names a technique.
- **Responsibilities:** library = reference knowledge; modules = rules of use. The library does not override `performance.md` (anti-generic, role division, tag placement, coherence).
- **No invention:** if a term is not in the library and is not safe general knowledge, label it as an assumption or ask; do not present it as fact. Do not invent definitions or sources.
- **No external research:** no internet research during musical generation. The library is local and versioned; sources are bibliographic references, not links to open.
- **Scope of consultation:** consultation is required only when Performance is in scope. Do not consult the Performance library for Style-only, Lyrics-only, or Analysis-only tasks. Analysis does not require library consultation; if narrative/interpretive reference knowledge is later needed, follow the same convention under `library/analysis/`, created only when needed.
- **Expansion:** new areas (style, rhythm, percussion, instrumentation, arrangement) follow the same convention, created only when needed.

## Compatibility

- This repository is packaged as a portable skill. The entry point is `SKILL.md` at
  the skill root; these orchestration rules live in `instructions/orchestration.md`
  and are loaded on demand.
- All paths are relative to the skill root (the directory containing `SKILL.md`).
  Resolve them from that directory, not from the agent's current working directory.
- Works with any agent that can read the skill folder; it does not depend on a
  runtime, a specific agent, an external dependency, or automatic loading.