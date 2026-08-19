---
name: human-natural-language
description: Qualitative checklist for identifying and reducing AI-writing mannerisms in academic/scientific prose (Portuguese and English) - sentence-length variation, trigger vocabulary, formulaic connectors, the rule of three, Portuguese linguistic calque. A style guide, not a reliable AI detector. Use when reviewing/rewriting a manuscript's prose so it sounds more natural and less robotic, without altering the scientific content or hiding AI-usage disclosure.
---

# Human Natural Language

A style checklist for giving academic/scientific prose a more human
voice, reducing patterns that signal AI-generated or heavily
AI-revised text. Based on 6 sources (two scientific papers plus notes
and comparison tables contributed by the project author).

## Honest limit before using this

This is **not an AI detector**. It's a qualitative style guide. Recent
research (PMC13061212, PLOS One 2026) measures these differences
statistically across large corpora; a human reviewer applying this
checklist to a single manuscript is making a qualitative approximation,
not a measurement. The research field itself (stylometry/LLM detection)
treats **hybrid text** (human draft + AI only polishing the language) as
one of the hardest problems to solve - don't promise the user that
following this checklist makes the text "undetectable". The real goal
is: reduce mannerisms that sound artificial to a trained human
reviewer, full stop.

This is **never** justification for shrinking or hiding an AI-usage
disclosure section required by the journal/institution - disclosure is
about honesty, this checklist is about prose style. The two are not to
be confused, and the first always takes priority over the second when
they conflict.

## The 8 convergent patterns

1. **Low sentence/paragraph length variation (burstiness)**. A human
   author alternates short sentences (5 words) with long, complex ones
   (40 words); AI tends to keep a homogeneous length. When reviewing,
   deliberately vary the rhythm - don't leave every paragraph with
   same-length sentences.
2. **Repetitive trigger vocabulary**, language-specific (see the table
   below). These aren't forbidden words in themselves (some have
   legitimate technical use) - the problem is repetition/abnormal
   frequency.
3. **Formulaic connectors and transitions**, used mechanically instead
   of varied (see the table below).
4. **Excessive em dashes**, used to create artificial drama instead of
   natural punctuation. General project rule: zero em dashes in
   manuscript text - rewrite with a comma, colon, semicolon, or
   parentheses.
5. **The rule of three applied mechanically** ("efficiency,
   scalability, and sustainability"). Not wrong by itself, but when it
   shows up repeatedly throughout the prose it's a sign of a formulaic
   pattern.
6. **Syntactic perfection with analytical emptiness**: grammatically
   flawless, but reuses generic concepts without citing specific
   nuances of the experiment/methodology. When reviewing, ask: could
   this sentence be in any paper in the field, or is it specific to
   this experiment?
7. **Absence of natural human idiosyncrasies**: an "encyclopedia-polish"
   tone with no regional markers, no strong adversative conjunctions
   (however/but), no register variation at all.
8. **In Portuguese, risk of linguistic calque from academic English**:
   LLMs tend to translate formal-English sentence structure in a way
   that sounds like a literal translation, even in grammatically correct
   Portuguese (Portuguese proclisis/enclisis, government, and cohesion
   rules are more complex than English's - don't simplify sentence
   structure the English way).

## Trigger-vocabulary and connector table, by language

| Category | English | Portuguese |
|---|---|---|
| Trigger vocabulary | delve, intricate, pivotal, showcase, underscore, crucial, multifaceted, testament to, leverage, foster, tapestry, navigate (metaphorical) | engajamento, crucial, primordial, multifacetado, orquestrar, teia, "desempenha um papel fundamental", aprofundar-se em, alavancar, fomentar |
| Transitions/connectors | furthermore, moreover, in light of, it is worth noting that, comprehensively | ademais, contudo, "é importante ressaltar que", "cumpre salientar", "no que tange a" |
| Cliché opening phrases | "in today's fast-paced digital landscape", "as the world continues to evolve", "looming challenges" | Portuguese equivalents: "no cenário atual em rápida evolução", "à medida que o campo continua a evoluir" |
| Formulaic structures | "It's not just X. It's also Y.", "Here's why that matters", "The result?", "And honestly?" | "não é apenas X, é também Y", "eis o motivo", rhetorical-question-then-answer constructions |
| Robotic self-disclosure | "as a large language model" (maximum red flag - should never appear in scientific prose) | "como um modelo de linguagem" (same red flag) |

## The 3 analysis axes (checklist structure)

Organize the style review into three axes, even without dedicated
computational tools (Spacy/Stanza, embeddings, a reference model for
perplexity aren't available in this workflow - this is a qualitative
approximation done by reading the text):

1. **Syntactic/Structural**: vary clause depth and type (subordinate
   vs. coordinate), vary punctuation, don't leave every paragraph with
   the same sentence "shape".
2. **Lexical/Semantic**: check vocabulary density and diversity - does
   the text repeat the same words/effect-phrases at an abnormal
   frequency? Prefer terms specific to the experiment over generic
   field terms.
3. **Statistical/Informational** (qualitative approximation, no real
   metric): does the text "flow" like something thought through with
   hesitations and adjustments, or like something generated all at once
   in a uniform way? There's no way to measure perplexity/entropy
   without a dedicated reference model - don't fake numerical precision
   you don't have.

## How to apply

1. Read the prose passage (Discussion, Introduction, Abstract - any
   section with running text, not Methods/Results, which are more
   descriptive by nature).
2. Mark occurrences of the 8 patterns above, with exact location.
3. For each occurrence, propose a concrete rewrite - it's not enough to
   flag "this sounds like AI," suggest the alternative sentence.
4. After rewriting, reread the whole paragraph (mentally, aloud) asking:
   does this sound like something a person would write while thinking
   as they go, or like text that came out finished and uniform?
5. Never apply this to reduce real scientific content, cut a disclosed
   limitation, or hide/shrink an AI-usage disclosure section - that's
   style scope, not content or honesty scope.
