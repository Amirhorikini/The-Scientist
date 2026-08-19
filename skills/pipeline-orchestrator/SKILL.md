---
name: pipeline-orchestrator
description: Runs The Scientist's full pipeline automatically and systematically - triggers receptionist, research-design, semantic-reviewer, and scientific-boss in sequence, passing each stage's output to the next, and assembles the Final Diagnostic Report at the end. Use when the user asks to "run all the agents", wants "full automation", "run the whole pipeline", or a "start-to-finish diagnostic" on a manuscript - instead of invoking each agent manually one by one.
---

# Pipeline Orchestrator

A single trigger to run **The Scientist**'s stages systematically,
without requiring the user (or you) to invoke each agent manually one
at a time. You (whoever invoked this skill) need to have the `Agent`
tool available.

## Before starting

Confirm you have the manuscript's location - ask if you don't. Never
invent a path.

Also ask, **before the first agent call**, which format the user wants
the Final Diagnostic Report in (chat/HTML/PDF - see the full criteria
in `scientific-review.md` § "Final Diagnostic Report", including
checking whether a PDF converter is available before promising that
format). Knowing this from the start avoids having to circle back and
ask after everything has already run.

## Execution sequence

Run these in this exact order, **one stage at a time - never in
parallel** (each stage depends on the previous one's full result):

1. **`receptionist`**: `Agent({subagent_type: "receptionist", prompt: "<manuscript path, and that the request is a full pipeline run>"})`.
   Collect the Intake Card (language, country/funding, target journal,
   review round). Keep it in full - it gets passed to every following
   stage.
2. **`research-design`**: `Agent({subagent_type: "research-design", prompt: "<Intake Card + manuscript path>"})`.
   Keep the full Design Report.
3. **`semantic-reviewer`**: `Agent({subagent_type: "semantic-reviewer", prompt: "<Intake Card + full Design Report>"})`.
   Keep the full Language Report.
4. **`scientific-boss`**: `Agent({subagent_type: "scientific-boss", prompt: "<Intake Card + Design Report + Language Report, both in full>"})`.
   Keep the full Decision Letter.
5. **Final Diagnostic Report**: assemble it yourself now, following
   exactly the structure already defined in `scientific-review.md` §
   "Final Diagnostic Report" - executive summary, result of each
   checklist, each agent's isolated conclusion (reproduced in full,
   never merged into one voice), charts, a journal suggestion with a
   freshly verified impact factor, and a 3-tier action plan
   (Urgent/Intermediate/Light).

An explicit call to `scientific-review` as its own step is optional -
the Intake Card + Design Report already cover Layer 1; include that
call only if you want its independent diagnostic read before
`research-design`, it's not required for the pipeline to work.

## Rules

- **Never invent content for a stage that didn't actually run.** If a
  stage fails or doesn't return a complete report, stop and tell the
  user - don't proceed as if it had worked, and don't fill the gap with
  invented findings.
- **Preserve each report in full between stages** - don't summarize the
  Design Report before passing it to `semantic-reviewer`, for example.
  Each stage needs the previous stage's complete report; a summary can
  hide a finding the next stage needed to know about.
- **A failure in one stage doesn't silently take down the others** - if
  `research-design` doesn't finish, record that explicitly in the Final
  Diagnostic Report instead of omitting the section.
- All of the project's rigor rules (em dash, citations, limitations,
  funding, AI, untrusted data) keep applying at every stage - this
  skill only orchestrates the sequence, it doesn't replace or loosen
  any agent's rigor rule.

## When NOT to use this

For a targeted review (just the Discussion, just checking citations,
just rewriting a paragraph), don't trigger this automation - talk
directly to `scientific-review` or invoke the specific skill
(`manuscript-rewriter`, `narrative-architecture`, etc.). This skill is
for when the user wants the complete cycle, start to finish, ending in
the Final Diagnostic Report.
