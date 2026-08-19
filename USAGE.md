<!-- title: The Scientist Usage Guide -->

# How to Use The Scientist

A quick guide - doesn't repeat what's already in `README.md`
(architecture) or in each agent/skill's own file (detailed rules).

## The simplest way: full automation

If you want the whole cycle (intake → structure → language →
evidence/verdict → final report), say something like:

> "Run the full pipeline on the manuscript at `~/path/to/article.md`"
> "Full automation on this article"
> "Start-to-finish diagnostic"

This triggers the `pipeline-orchestrator` skill, which calls the 4
agents in sequence on its own and at the end asks which format you want
the report in (chat, HTML with charts, or PDF - if a converter is
available on the machine).

## Targeted review (without running everything)

For something specific, just ask directly, no need for the full
automation:

- **"Review the Discussion of this article"** / **"Check the
  citations"** → talks to `scientific-review` directly.
- **"Rewrite this paragraph, make it sound more natural"** → triggers
  `manuscript-rewriter` (actually edits the file, doesn't just suggest).
- **"Is this ready to submit? What's the desk-reject risk?"** →
  triggers the `publication-strategist` skill (a fast strategic
  assessment, not the full layered review).
- **"Write the response letter to reviewers"** → triggers
  `revision-response-composer`.

## What the system will ask you first

Whenever you bring a new manuscript, expect to answer (once, not on
every message):

1. Which language you want the conversation to happen in.
2. The authors' country (and whether there's funding to declare -
   CAPES or the country's equivalent).
3. Where the manuscript is, and the target journal (if you already have
   one).
4. Whether this is the first review or a re-review of something already
   assessed before.

This is `receptionist` doing intake - it doesn't evaluate any content,
it just collects this information and passes it along.

## Rules that never change, regardless of the request

- Zero em dashes in manuscript text.
- No citation ever goes in without being actually verified (never from
  memory).
- Real limitations are never softened or hidden, even if you ask.
- AI-usage disclosure is always complete, even when asked to keep it
  "minimal."
- Funding (CAPES or equivalent) is always checked when applicable.

If a request runs into one of these rules, the agent will refuse that
specific part and explain why - that's expected, not a bug.

## Where things live

- Review reports: `~/Documentos/The Scientist/`.
- The manuscript itself: stays in its own project, never moved into the
  folder above.
- Agent/skill definitions: `~/.claude/agents/` and `~/.claude/skills/`
  (mirrored in this repository).

## If something isn't available

Before promising a format/tool (e.g. exporting a PDF, publishing HTML),
the agents check the machine first - if something isn't installed, you
get a clear warning instead of a promise that won't hold.
