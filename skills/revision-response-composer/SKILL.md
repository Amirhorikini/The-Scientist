---
name: revision-response-composer
description: Composes the formal response letter to reviewers/editor (Reviewer Comment → Author Response → Change Made format, R→A→C) after a real or scientific-boss-simulated peer-review round. Includes a page-by-page change table, the correct way to disagree with a reviewer using evidence, and the rule that no comment can go unanswered. Use when the user has received reports (real or from scientific-boss's Panel/Re-review Mode) and needs to write the resubmission letter.
---

# Revision Response Composer

Puts together the formal response letter to reviewers/editor after a
review round, in the **R→A→C** (Reviewer comment → Author response →
Changes made) format journals expect.

## Non-negotiable rules

- **Every comment gets a response - none can be skipped**, even minor
  ones. A report's weakness list is unbounded; if `scientific-boss` (or
  a real reviewer) raised 12 items, the letter has 12 responses, not a
  summary of the "main ones".
- **Disagreeing requires evidence, never just "we disagree"**. See "How
  to disagree correctly" below.
- **Acknowledge strengths only when the report actually praised
  something** - don't fabricate praise to fill the section; if the
  report had no explicit positive point, skip that block instead of
  inventing one.
- **Every change needs an exact location** (page/paragraph in the
  revised version) - "we changed that" without saying where is a weak
  response that forces the reviewer to hunt for the edit.
- This is about **composing the letter**, not about deciding what to
  change - the changes themselves come from
  `semantic-reviewer`/`scientific-boss`/the user's decision; this skill
  only formats the response completely and traceably.

## Letter structure

```
# Response to Reviewer Comments

## Manuscript Information
- Title / Manuscript ID / Original submission date / This revision's
  date / Revision round

## Summary of Changes
[300-500 words summarizing this round's main changes]
- Structural changes (section reorganization, word count before →
  after)
- New content (analyses/data/references added)

## Response to Reviewer/Journal Fit
### Comment 1
> [direct quote of the comment]
**Author Response**: [...]
**Change Made**: [page X, paragraph Y - exactly what changed]

## Response to Reviewer 1 (Methodology)
### Strengths Acknowledged (only if the report cited something positive)
### R1-W1, R1-W2... [one entry per weakness raised, no quantity limit]
### R1 Questions
### R1 Minor Items (table: # | comment | action taken | location)

## Response to Reviewer 2 (Domain) / Reviewer 3 (Perspective) / Devil's Advocate
[same format above for each persona that produced findings]

## Response to Required Revisions (from scientific-boss's verdict)
[table: # | required revision | status (Complete/Partially Addressed) | summary | location]

## Page-by-Page Change Log
[table: original page | revised page | section | change description]

## Closing
[thanks, a statement that the revised version addresses the concerns
raised, or an honest explanation of what wasn't fully resolved and why]
```

## How to disagree correctly

Disagreeing with a reviewer is sometimes legitimate and expected - but
it needs structure, not just denial:

**Right**:
> Reviewer: suggests using Method X instead of Method Y.
>
> **Author Response**: We thank the reviewer for the suggestion. We
> chose Method Y for the following reasons: (1) it performs better for
> [specific data type] (verified citation); (2) Method X's assumptions
> (e.g. [assumption]) aren't satisfied in our design. However, we've
> added a robustness check using Method X in Appendix B, with
> consistent results.
>
> **Change Made**: Appendix B (p. 25-26) with the robustness check;
> justification for choosing Method Y in the Methods section (p. 9,
> §3).

**Wrong**:
> **Author Response**: We disagree. Method Y is appropriate.

The difference: the right response gives a specific reason, cites
evidence (verified, never from memory - the project's rigor rule), and
still offers the reviewer something (the robustness check) instead of
just refusing.

## Weak-response traits (avoid)

- **Perfunctory**: "Fixed" without saying what.
- **Evasive**: doesn't actually answer a hard question.
- **Defensive without explanation**: "the reviewer misunderstood" without
  saying why.
- **Overpromising**: acknowledges every problem but offers no solution
  for any of them.
- **No location marker**: change made but not saying where, forcing the
  reviewer to search for it.

## Relation to the rest of the pipeline

Use this after `scientific-boss` has already produced a verdict (first
round or Re-review Mode) - the letter consolidates the response to that
verdict. If the manuscript hasn't been reviewed yet at all, there's
nothing to respond to yet; run the full pipeline first.
