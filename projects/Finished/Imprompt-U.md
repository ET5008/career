---
name: Imprompt-U — AI Socratic Tutor
dates: Mar 2026
status: shipped
type: hackathon
role: backend, database, Claude API integration, token optimization (team of 4, SodaHacks)
repo: https://github.com/ET5008/Imprompt-U
skills: [node.js, express.js, typescript, postgresql, supabase, claude api, sse streaming, pdf parsing]
metrics: []  # "won education track" is a qualitative outcome, not a numeric metric with baseline
angles: [ml-engineering, ai-product, full-stack]
verified: false
---

## Variant: ml-engineering
- Architected a two-call Claude pipeline per turn: one call scores the student's answer and diagnoses concept gaps, a second generates the next Socratic question informed by that gap analysis.
- Owned backend and database: PDF-to-topic extraction pipeline, PostgreSQL schema (Supabase), Claude API integration with token-usage optimization.
- Won the education track at SodaHacks (Berkeley CSUA hackathon), built with a team of 4.

```latex
% Ready to paste into the resume .tex for this variant.
\resumeProjectHeading
  {\textbf{Imprompt-U --- AI Socratic Tutor} $|$ \emph{React, TypeScript, Express.js, Claude API, PostgreSQL (Supabase)}}{Mar. 2026}
  \resumeItemListStart
    \resumeItem{Built at SodaHacks (Berkeley CSUA hackathon) with a team of 4; won the education track. Owned the backend and database: PDF-to-topic extraction pipeline, PostgreSQL schema, and Claude API integration with token-usage optimization.}
    \resumeItem{Architected a two-call Claude pipeline per turn --- one call scores the student's answer and diagnoses concept gaps, a second generates the next Socratic question informed by that gap analysis --- streamed to the client over SSE.}
  \resumeItemListEnd
```

## Variant: ai-product
- Built an AI-powered Socratic tutor: upload a PDF textbook, get quizzed by Claude, track mastery in real time.
- The tutor never gives the answer directly — it diagnoses exactly which concept the student is missing and adapts the next question to that gap.
- Won the education track at SodaHacks with a team of 4.

```latex
\resumeProjectHeading
  {\textbf{Imprompt-U --- AI Socratic Tutor} $|$ \emph{React, TypeScript, Express.js, Claude API, PostgreSQL (Supabase)}}{Mar. 2026}
  \resumeItemListStart
    \resumeItem{Built an AI-powered Socratic tutor that diagnoses a student's specific knowledge gaps per turn and adapts follow-up questions accordingly, rather than lecturing or giving direct answers.}
    \resumeItem{Owned backend, database schema, and Claude API integration for a team of 4; won the education track at SodaHacks.}
  \resumeItemListEnd
```

## Raw notes
- Tech stack per repo README (verified via web_fetch, Jul 2026): React 19, TypeScript, Vite, Tailwind, Framer Motion (frontend); Node/Express/TypeScript (backend); Claude Sonnet 4.6; Supabase (Postgres + object storage); pdf-parse.
- Architecture detail from earlier discussion: SSE streaming, custom mastery algorithm, PDF-to-TOC pipeline with regex heuristics, batched DB inserts, dynamic system prompt injection with gap context — this is the interview-depth material, don't try to cram it all into resume bullets.
- CLAUDE.md in the repo indicates Claude Code was used in development — worth having a clear answer ready for "how much of this did you write yourself" in an interview.
- Ownership was self-reported as "database, backend queries, Claude API calls, token optimization, majority of the backend" — accurate framing on resume, but be ready to specifically describe your commits if asked to walk through the codebase live.

## Metric sources
- "Won education track at SodaHacks": a real, verifiable outcome (event result), but it's not a quantitative metric with a baseline — keep it as a qualitative achievement statement, not in the metrics list.
- No accuracy, retention, or usage numbers exist for the tutor's mastery-scoring quality — don't invent one if asked to quantify effectiveness.