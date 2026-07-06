---
name: Imprompt-U
dates: March 7, 2026
status: archived
type: hackathon
role: Team lead (4 total, incl. 3 beginners); owned integration across all three subsystems — PDF parser, mastery engine, UI — and fine-tuned each component individually.
repo: https://github.com/ET5008/Imprompt-U
skills: [react, typescript, vite, express, supabase, claude api, pdf parsing]
metrics: []          # none verified — see Metric sources
angles: [full-stack, ai-product]
verified: false
---

## Variant: full-stack
<!-- 2-4 bullets. Action verb + mechanism + quantified outcome. -->
- Integrated a PDF parser, Socratic mastery engine, and React/TypeScript frontend into a single working pipeline across a 4-person hackathon team, personally fine-tuning each subsystem end-to-end.
- Chose a heading-based PDF parsing library over a RAG pipeline for chapter extraction, trading marginal retrieval utility for lower latency and reduced API overhead under a 12-hour build constraint.
- Optimized Claude API usage through response caching and call-reduction, keeping the tutoring loop responsive within a fixed compute/time budget.
- Cut scope from a multi-source "NotebookLM for Claude" vision to a single-PDF workflow under time pressure, prioritizing a complete end-to-end loop over partial multi-feature coverage.

```latex
% Ready to paste into the resume .tex for this variant.
\resumeProjectHeading
  {\textbf{Imprompt-U} $|$ \emph{React, TypeScript, Express, Supabase, Claude API}}{March 2026}
  \resumeItemListStart
    \resumeItem{Integrated a PDF parser, Socratic mastery engine, and React/TypeScript frontend into a single working pipeline across a 4-person hackathon team, personally fine-tuning each subsystem end-to-end.}
    \resumeItem{Chose a heading-based PDF parsing library over a RAG pipeline for chapter extraction, trading marginal retrieval utility for lower latency and reduced API overhead under a 12-hour build constraint.}
    \resumeItem{Optimized Claude API usage through response caching and call-reduction, keeping the tutoring loop responsive within a fixed compute/time budget.}
    \resumeItem{Cut scope from a multi-source "NotebookLM for Claude" vision to a single-PDF workflow under time pressure, prioritizing a complete end-to-end loop over partial multi-feature coverage.}
  \resumeItemListEnd
```

## Variant: ai-product
- Designed a Socratic tutoring loop that withholds direct answers via prompt engineering, keeping Claude questioning rather than resolving user confusion outright — directly targeting the answer-dispensing failure mode observed in tools like NotebookLM.
- Built a mastery-detection mechanic where Claude extracts a chapter's key concepts, then aggregates the user's demonstrated understanding into the same structural format for direct comparison, marking mastery once the two converge.
- Scoped and shipped a single-PDF MVP in 12 hours by deliberately deferring a broader multi-source vision, prioritizing a complete Socratic-tutoring loop over partial multi-feature breadth.

```latex
\resumeProjectHeading
  {\textbf{Imprompt-U} $|$ \emph{Claude API, React, TypeScript}}{March 2026}
  \resumeItemListStart
    \resumeItem{Designed a Socratic tutoring loop that withholds direct answers via prompt engineering, keeping Claude questioning rather than resolving user confusion outright — directly targeting the answer-dispensing failure mode observed in tools like NotebookLM.}
    \resumeItem{Built a mastery-detection mechanic where Claude extracts a chapter's key concepts, then aggregates the user's demonstrated understanding into the same structural format for direct comparison, marking mastery once the two converge.}
    \resumeItem{Scoped and shipped a single-PDF MVP in 12 hours by deliberately deferring a broader multi-source vision, prioritizing a complete Socratic-tutoring loop over partial multi-feature breadth.}
  \resumeItemListEnd
```

## Raw notes
<!-- Problem / approach / result. Failures, debugging stories, design
     decisions, war stories. Interview material — never goes on a resume
     directly. -->
Built at SODA Hacks (March 7, 2026, 12-hour build) as a direct reaction to NotebookLM's shortcomings — hallucinated content, and a design that made it too easy to get answers instead of actually learning. Wanted a Socratic tutor instead: upload a PDF textbook chapter, get quizzed by Claude, mastery tracked until demonstrated understanding matches the material.

Team of 4 — Ethan led 3 beginner teammates. Instead of owning a single subsystem, Ethan connected and fine-tuned all three: PDF parser, mastery engine, and UI. This was his first project requiring real scoping and delegation across less-experienced teammates, and he cites it as where he learned to do both properly.

Mastery mechanic: Claude extracts key concepts from the chapter, then aggregates the user's demonstrated understanding into the same structural format as those key concepts. Mastery marked reached once the aggregated understanding sufficiently matches the key-concept set.

Chapter extraction: used an existing PDF parsing library to split content by heading structure, rather than building a RAG pipeline. Deliberate tradeoff — RAG would have added marginal retrieval utility at meaningfully higher overhead and complexity for a single-document use case, not worth it in a 12-hour build. (Specific library name and what broke during integration — still held over, not yet revisited.)

API cost: learned to optimize Claude API usage via caching and reducing call volume, offloading what could be handled by libraries/other features instead of repeated API calls.

Original ambition was broader — effectively "NotebookLM for Claude," multi-source. Time constraints forced a hard cut to single-PDF-source scope to ship a complete loop rather than a partial multi-source one.

Result: team says they won the Education track. **No verifiable source — only photos exist, no Devpost page or announcement found/provided.** Treat as unconfirmed until a checkable source turns up.

Status: local-only, never deployed past the hackathon. Archived.

## Metric sources
<!-- Where each number came from: commit hash, log file, submission link.
     A metric without a source here doesn't get used. -->
- **Education track win (SODA Hacks):** UNCONFIRMED. Only photographic evidence exists — not independently checkable, so it does not appear in `metrics` or in any bullet. If SODA Hacks published a results page, Devpost submission, or organizer announcement, get that link and this can be revisited.
- No other quantitative claims made (no accuracy figures, no usage/session counts, no latency numbers for the caching work) — none were volunteered, so none are fabricated here.