# Thiago's Skills Toolkit

This repository collects four Claude Skills distilled from Thiago's personal prompt library — prompts he used separately, as standalone Word documents, to guide academic research, interview curation, and product development. The work here wasn't copying each prompt verbatim: it was reading each one carefully, understanding the method behind it, grouping the ones that share the same underlying reasoning engine into a single place, and returning that as a Skill Claude can load and follow on its own, without needing the whole prompt pasted in every time.

Each skill lives in its own folder under `skills/`, as a single `SKILL.md` file — YAML frontmatter (`name` and `description`) plus the instruction body. The `description` is what decides when that skill activates: it's written (and should be kept) with an eye toward how Claude will recognize the situation, not as a summary for humans.

## The four skills

### `orientador-hierarquico` (Hierarchical Advisor)

The broadest of the four. It merges four instruments Thiago used separately — a hierarchical editor/fact-checker, a Popper/Duhem-Quine-style scientific stress test, a journalistic rewrite editor, and a title reconstructor — all built on the same decimal hierarchy engine (THEME → SUBTHEME → SEGMENT → DETAIL → MICRO-ANALYSIS) and the same anti-hallucination discipline (every claim carries a status: STATED, DERIVED, or GAP WITH AN OWNER), later extended to treat citation-norm rules with the same rigor: no ABNT (Brazilian academic standards) edition is ever applied from memory without verifying it in the current session.

It serves any hierarchical text — from a routine article to a postdoctoral thesis — and also full books, always opening with dialogue rather than producing on the spot. It covers nine internal modes: research/write (R), title (T), content critique/stress-test (C), journalistic rewrite (J), audit pasted text (A), curate and close the bibliography (B), curate the glossary and terminological consistency across a work's chapters (G), audit ABNT formal compliance against the currently valid edition of the standard (N), and simulate a three-examiner oral defense (V). It includes a dedicated path for someone who arrives with nothing built yet — just an idea, a need, even just a dream — because not everyone starts already holding a draft or a bibliography, plus a fixed bibliographic-reference template anchored in Thiago's own real examples for every citation and reference list the skill produces. The style checklist also covers two typographic markers: every technical or theoretical key term is bolded on first appearance in each section, and every word or expression outside the document's native language is italicized with its definition in parentheses at first occurrence. Mode R's search step now follows the same source-quality hierarchy used to critique a finished text, names theme-specific institutional data wells (IBGE, the Central Bank, Brazil's CAPES journal portal, SciELO, among others), and chases citations backward and forward from the most central sources; every number derived by calculation is re-executed computationally before publishing, whenever a code-execution tool is available in the session.

### `curador-entrevistas-situacionais` (Situational Interview Curator)

Based on two complementary prompts — one for building situational interviews from scratch, another for revising and polishing interviews already written. The shared method: turn technical questions into everyday situations, so the person being interviewed feels like they're telling a story, not filling out a form. It originated from a project digitizing an Afro-Brazilian religious community's operations (a terreiro), but the method applies to any of Thiago's ventures where the relevant knowledge lives only in someone's head, never organized.

It has two modes — Create and Polish — and one inviolable boundary in both: before anything else, the skill asks what, in that specific project, plays the role the original called "cultural protection" (a trade secret, sensitive data, whatever applies) so it is never led into exposing it.

### `motor-produto-em-po` (Powder Product Engine)

Based on the "Diverse Commerce Powder Engine" prompt, a strictly staged flow for turning a recipe into a commercial powdered product for marketplaces (Shopee and similar): intake → sensory analysis → pricing → full commercial package (title, psychological triggers, positioning, keywords, packaging). It never advances a stage without explicit approval, and never invents technical data that would require a real lab report or analysis (nutrition facts, shelf life, chemical composition).

### `pipeline-design-system`

The most extensive one: it walks a complete Design System build, from raw uploaded material to the final `Design.md`, across 15 specialized stages (audit, context, strategic research, market research, visual strategy, visual language, color, typography, tokens, components, accessibility, layout, motion, governance, and final consolidation). Each stage decides only what belongs to it — never re-deciding what an earlier stage already settled, never reaching ahead into a later stage's territory — and closes with a handoff block the next stage consumes without re-reading everything from scratch. The final stage resolves conflicts between specialists using a fixed, documented precedence order.

## How to install

Each folder under `skills/` is a complete, self-contained Skill. To use one in a Claude session (Claude Code, Cowork, or any environment that supports Skills), copy the corresponding folder into your project's or account's skills directory — Claude reads the frontmatter `description` itself and loads the `SKILL.md` when a request matches it. There's no need to invoke the skill by name; it triggers on its own when the request fits the description.

## Origin

Everything here was synthesized from prompts Thiago wrote and used by hand, pasting them in full at the start of every new conversation. The point of this toolkit is to remove that repetition: the method is still his — it's just loaded automatically by Claude now, whenever the situation calls for it.
