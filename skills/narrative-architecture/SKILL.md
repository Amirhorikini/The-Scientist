---
name: narrative-architecture
description: Narrative architecture and sentence-level clarity for scientific manuscripts - the Context-Content-Conclusion (C-C-C) framework applied at every level (sentence, paragraph, section, whole article), Swales' CARS Model for the Introduction (Territory/Niche/Occupying the Niche), the sequence-of-statements structure for Results, the Topic-Position/Stress-Position/Subject-Verb-Separation principles (Gopen & Swan) for first-pass sentence clarity, lexical cohesion (Halliday & Hasan) as an alternative to mechanical connectors, and academic-English micro-editing (adverb placement, nominal density, calibrated hedging). Use when reviewing/rewriting a manuscript's narrative (Introduction, Results, Discussion) or when the user wants to turn data into a coherent story.
---

# Narrative Architecture

Tools for giving a scientific manuscript a coherent narrative arc
(Problem → Gap → Solution → Implication) and sentences a reviewer
understands on the first read, without needing to reread. Based on
Mensh & Kording (2017, PLOS Computational Biology) and Gopen & Swan
(1990, American Scientist) - see the project's `REFERENCES.md`.

## The Context-Content-Conclusion (C-C-C) framework

Every good piece of scientific writing, at any scale, follows the same
three-part pattern - and avoids the reader's two frustrated questions:
"why are you telling me this?" (missing context) and "so what?"
(missing conclusion).

| Level | Context | Content | Conclusion |
|---|---|---|---|
| Sentence | Sets the topic | New data/idea | Memorable conclusion |
| Paragraph | First sentence: topic | Body: new idea | Last sentence: closes with a conclusion |
| Section | Introduction: gap | Results: data | Discussion: significance |
| Whole article | Introduction | Results | Discussion |

This maps directly onto the Problem → Gap → Solution → Implication
narrative arc: Problem/Gap = Context, Solution/Results = Content,
Implication = Conclusion. A manuscript without this clear correspondence
at every level is structurally weak, even if the data are solid.

**Common error to flag**: a chronological structure that follows the
actual research process ("first we tried X, it didn't work, so we tried
Y..."). Reviewers care about the final claim, not the autobiographical
path to it - this is also covered by the existing rigor rule of
"methodology as a clean narrative, not a debugging log".

## Research Gap Alignment (Swales' CARS Model)

The Introduction should progress through increasingly specific
paragraphs until it exposes exactly the gap the article fills. This has
a formal name in academic-genre linguistics: Swales' (1990) **CARS
model** (*Create a Research Space*), used as the gold standard by
editors to assess whether an Introduction has the right narrative
structure - three "moves," each with internal steps:

1. **Move 1 - Establishing a Territory**: claim the topic's
   centrality (why it matters), make generalizations about the field's
   state, review the relevant literature. Corresponds to the opening
   paragraph(s) - why the broad topic matters, and what the field as a
   whole still hasn't resolved (field-level gap).
2. **Move 2 - Establishing a Niche**: argue that there's a useful gap
   in the current literature - via four possible routes: counter-claim
   (contesting a prior finding), gap indication, question-raising, or
   continuing a research tradition. Corresponds to the middle
   paragraph(s) - what's specifically unknown about the study's subtopic
   (subfield-level gap).
3. **Move 3 - Occupying the Niche**: outline the work's purpose,
   announce the present research, announce the main findings (optional
   in some fields), indicate the article's structure. Corresponds to the
   last paragraph before the objective - the specific, testable gap this
   study addresses, and a compact preview of how the results fill it.

Every Move 1/2 paragraph follows the same micro-pattern: an orienting
sentence (context) → what the literature has already shown (known) →
a closing sentence exposing what's missing (unknown, the gap). If an
Introduction paragraph doesn't end by pointing to a real gap, it
probably shouldn't be there, or it's poorly cut.

**Practical test**: be able to state, in one sentence, "the literature
knows X, but doesn't know Y, and that matters because Z" - if you can't
complete that sentence with what's in the manuscript's Introduction, the
gap isn't clear enough for the reader. When reviewing, explicitly
identify which Move each Introduction paragraph is in and whether the
1→2→3 progression is complete - an Introduction that jumps straight from
Move 1 to Move 3 (without establishing the niche) is the most common
failure.

## Results as a sequence of statements

Every Results paragraph/subsection should answer an implicit question,
not just narrate what was done:

- **Opening sentence**: states the question the paragraph answers ("To
  verify that...", "To determine whether...", "We next tested...").
- **Middle**: the relevant data and logic.
- **Closing sentence**: directly answers the question posed in the
  opening sentence.

Figure titles should communicate the analysis's **conclusion**, not
just describe what's shown; the caption is what explains the
methodology. This matters because some readers skip from the
Introduction straight to the figures.

## Avoid zig-zag, use parallelism

- Touch each central idea exactly once, in one place - don't spread the
  same argument across non-consecutive points in the text.
- Group related sentences/paragraphs; similar ideas should sit
  consecutively.
- If there are multiple parallel reasons for an interpretation,
  communicate them with the same syntactic structure (e.g. always "X
  increases Y", not mixing in "there is an increase in Y caused by X") -
  varying the form for the same function confuses the reader about
  whether these are different concepts.

## Sentence clarity: Topic Position and Stress Position

Gopen & Swan's central principle, summed up in one sentence: **"Put in
the topic position the old information that links backward; put in the
stress position the new information you want the reader to
emphasize."**

- **Topic position** (start of the sentence): where the reader looks
  for context and connection to what's already been said. "Old"
  (already mentioned) information should appear here - not new
  information. A sentence whose opening doesn't connect to what came
  before breaks the reading thread.
- **Stress position** (end of the sentence, or right before a colon/
  semicolon): where the reader naturally places the most attention -
  the equivalent of "save the best for last." New, important
  information should appear here, not lost somewhere in the middle of
  the sentence.
- **Subject-verb separation**: the reader expects the verb to come
  right after the subject. Long material inserted between the two reads
  as an interruption of lesser importance, even when the author meant it
  to be important - if a piece of information deserves emphasis, it
  needs to be in the stress position, never buried between subject and
  verb.
- **A sentence isn't too long because of word count**, but when it has
  more candidates for "information that deserves emphasis" than there
  are stress positions available. Well-structured 100-word sentences
  read easily; poorly structured 20-word sentences don't.

**How to apply this in a review**: for each problematic sentence,
identify (1) what information the reader already knows at this point -
it should be at the start; (2) what's the new/important information in
this sentence - it should be at the end; (3) if the subject and verb are
separated by more than one short clause, move the inserted material
somewhere else (the start of the next sentence, or its own sentence)
instead of leaving it stuck in the middle.

## Sentence-level micro-editing (native academic English)

Targeted techniques for English prose to sound like an experienced
native author's, without rhetorical excess. Mostly applicable to
manuscripts written or translated into English (the common case for
international submission):

- **Lexical cohesion instead of mechanical connectors** (Halliday &
  Hasan, 1976): a text's cohesion comes from two types - grammatical
  cohesion (using connectors like "furthermore"/"moreover") and
  **lexical** cohesion (the natural flow of ideas through controlled
  repetition, synonyms, and semantic chains). Text that relies only on
  the first type sounds mechanical. Instead of opening every new
  sentence with a formal connector, embed the transition in the
  sentence's own subject or syntactic structure - e.g., instead of
  "Furthermore, the results indicate...", prefer picking the previous
  subject back up directly ("These results also indicate...", or simply
  connecting through repetition of the key term).
- **Adverb placement in compound verbs**: reposition adverbs into the
  middle of a compound verb instead of the start/end of the sentence -
  "is currently poorly understood" instead of "currently, we understand
  this poorly." This is a formal academic-English convention, not a
  matter of personal style.
- **Nominal density and present-participle clauses**: convert wordy
  sentences into dense noun groups, and use "-ing" clauses to tie a
  consequence to the previous sentence without needing a new connector -
  e.g. "..., thereby reducing X" or "..., paving the way for Y" instead
  of a new sentence starting with "This reduces X" or "This opens the
  way for Y".
- **Calibrated technical hedging**: swap absolute verbs ("proves",
  "shows", "demonstrates" when the design doesn't support full
  certainty) for attenuation appropriate to what the data actually
  allow ("suggests", "is consistent with", "strongly points toward").
  This **is not** the same as the rigor rule against "stacking hedges in
  Limitations" - here the goal is to calibrate the verb to the
  evidence's real strength once, not to repeatedly soften the same
  caveat. A claim backed by strong data can and should use a more direct
  verb; the error to fix is the opposite one, an absolute verb for
  moderate/correlational evidence.
- **The End-Weight Principle**: the same idea as the Stress Position
  above (Gopen & Swan) under another name - position the most complex/
  cognitively demanding information at the end of the clause, not the
  start. Not an additional technique, it's the same rule reappearing in
  the English style-writing literature - don't treat it as two different
  principles.

## Reframing limitations as forward hooks (framing, not concealment)

Real limitations can be exposed in a way that works as a hook for
future work, instead of sounding like a pure methodological flaw - this
is a matter of **rhetorical framing**, never of **omitting or softening
content**. The project's rigor rule (never soften or remove real
limitations) keeps applying in full: the data, the limitation itself,
and its complete honesty don't change. What can change is the closing
sentence right after stating the limitation - from a dead end ("this is
a weakness of the study") to a concrete bridge ("future studies with
[specific design] could resolve this gap by measuring [exactly what]").
This is only legitimate when the suggested future work is real and
specific - a vague bridge ("more research is needed") doesn't count and
is, itself, one of the clichés listed in the `human-natural-language`
skill.

## Relation to the rest of the pipeline

- Applied mainly by `semantic-reviewer` in Layer 2 (Reconstruction),
  after resolving structure/redundancy, while working sentence by
  sentence.
- The C-C-C framework and Gap Alignment reinforce and deepen the
  "Internal Coherence Line" in axis 4 of the `publication-strategist`
  skill - use the two together for an in-depth Introduction/Discussion
  review.
- Doesn't override the scientific rigor rules (em dash, citations,
  limitations, funding, AI) - all of them keep applying in full on top
  of any narrative-architecture decision.
