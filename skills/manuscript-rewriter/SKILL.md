---
name: manuscript-rewriter
description: Actually rewrites a passage/section of the manuscript, applying at once the narrative architecture (C-C-C, CARS, Topic/Stress Position), AI-writing-mannerism reduction, and calibrated hedging - and applies the change to the file via Edit, not just a suggestion. Preserves 100% of the scientific content (data, claims, limitations, AI disclosure) - this is style rewriting, never substance. Use when the user asks to "rewrite"/"improve the text"/"make it sound more natural"/"just edit it already" for a specific manuscript passage, not a scientific-merit review.
---

# Manuscript Rewriter

Actually rewrites and **applies** the edit to a manuscript passage -
unlike the other style skills (`narrative-architecture`,
`human-natural-language`), which describe what to adjust but leave the
application to whoever invoked them. This skill is the execution step:
it takes the other two's principles, decides the concrete rewrite, and
writes it to the file.

## Prerequisite

Only use this skill if the agent that invoked it has the `Edit` tool
available (today: `semantic-reviewer` and `scientific-review`). If it
doesn't, produce the rewritten version as text in the response and say
explicitly that you can't apply it directly to the file - never pretend
you applied a change that only exists in the conversation.

## Fundamental rule: style, never substance

- **Never change** what's being claimed, numbers, data, disclosed
  limitations, or the AI-usage disclosure section. This holds even if
  the rewrite would "read better" by changing one of those - it's not
  your call to change substance.
- If, while rewriting, you notice a sentence that looks scientifically
  wrong, overstated, or contradicts another passage, **don't silently
  fix it inside the style rewrite** - stop, flag it separately to the
  user as a content finding (that's `scientific-boss`'s/Layer 3's scope,
  not this skill's), and only proceed with the stylistic part once
  what to do about the content has been decided.
- All of the project's rigor rules keep applying in full (zero em
  dashes, verified citations, funding, AI).

## Process

1. **Read the target passage with context**: the paragraph before and
   after too, not just the isolated sentence - a style change needs to
   keep cohesion with its surroundings.
2. **Apply in this order** (each one is the principle already detailed
   in its source skill, don't repeat it here, just follow the order):
   a. Paragraph/section structure - the CARS model for the Introduction,
      C-C-C for any paragraph, the sequence-of-statements structure for
      Results (`narrative-architecture`).
   b. Sentence clarity - Topic Position/Stress Position, subject-verb
      separation (`narrative-architecture`).
   c. AI-mannerism reduction - trigger vocabulary, formulaic connectors,
      burstiness, the rule of three (`human-natural-language`).
   d. Calibrated hedging and sentence-level micro-editing, if the text
      is in English (`narrative-architecture`).
3. **Large changes** (rewriting a whole paragraph or more): show a
   before/after to the user and ask for confirmation before applying.
   **Targeted changes** (one sentence, reordering a clause, swapping a
   trigger word): can apply directly and report afterward - no need for
   prior confirmation on every micro-adjustment.
4. **Apply via `Edit`**.
5. **Run the automated checks** from `scientific-review.md` on the
   edited passage (zero em dashes, no leftover placeholder) before
   reporting as done.
6. **Summarize what changed and why**, referencing which principle
   motivated each change (e.g. "moved the new information to the
   sentence-final stress position" or "replaced 'delve into' with a more
   direct verb") - never just "improved the sentence" without saying
   what changed.

## Limits

- Doesn't decide whether a scientific claim is correct/supported by the
  data - that's `scientific-boss` (Layer 3).
- Doesn't reclassify the article's type/structure - that's
  `research-design`.
- This is rewriting **already-existing** text - never invents new
  content, never adds a result/data point/citation that wasn't in the
  original passage (a new citation only goes in if the user explicitly
  asks for it and it gets verified, never on the style rewrite's own
  initiative).
- Outside the full pipeline, it can be used as a quick shortcut - the
  user points at a passage, you apply this directly, no need to trigger
  `research-design`/`scientific-boss` for a one-off style fix.
