---
name: Speechful
dates: October 24-26, 2025
status: archived
type: hackathon
role: Full-stack engineer (4 total); built the frontend and connected the ML pipeline (Claude, Deepgram, Lava, OpenAI) to the backend — integration owner across the stack.
repo: https://github.com/onKTun/speechful-cal-hacks-12.0
skills: [react, typescript, vite, express, node.js, claude api, deepgram, lava, openai]
metrics: []          # none verified — see Metric sources
angles: [full-stack, ai-product]
verified: false
---

## Variant: full-stack
<!-- 2-4 bullets. Action verb + mechanism + quantified outcome. -->
- Built the React/TypeScript frontend and wired it end-to-end to an Express/Node backend, integrating the ML analysis layer (Claude, OpenAI, Deepgram) as the connective piece across the stack.
- Implemented a periodic screenshot-capture pipeline (every few seconds) feeding backend ML calls, a deliberate latency/accuracy tradeoff chosen under hackathon time constraints.
- Owned integration across three independently-developed pieces — capture, ML analysis, feedback surface — the component that took the majority of build time to get working end-to-end.

```latex
% Ready to paste into the resume .tex for this variant.
\resumeProjectHeading
  {\textbf{Speechful} $|$ \emph{React, TypeScript, Express, Claude API, Deepgram}}{October 2025}
  \resumeItemListStart
    \resumeItem{Built the React/TypeScript frontend and wired it end-to-end to an Express/Node backend, integrating the ML analysis layer (Claude, OpenAI, Deepgram) as the connective piece across the stack.}
    \resumeItem{Implemented a periodic screenshot-capture pipeline (every few seconds) feeding backend ML calls, a deliberate latency/accuracy tradeoff chosen under hackathon time constraints.}
    \resumeItem{Owned integration across three independently-developed pieces — capture, ML analysis, feedback surface — the component that took the majority of build time to get working end-to-end.}
  \resumeItemListEnd
```

## Variant: ai-product
- Scoped the product as a user-driven improvement engine: surfaced raw quantitative feedback from Claude/Deepgram analysis and left interpretation and action to the user, rather than building a prescriptive coaching layer.
- Chose a periodic-screenshot capture model over continuous streaming to balance real-time feedback against processing latency, within a hackathon build timeline.
- Integrated multiple sponsor AI services (Claude, Lava, Deepgram, OpenAI) into a single feedback loop, prioritizing breadth of usable sponsor tooling within a fixed 48-hour build window.

```latex
\resumeProjectHeading
  {\textbf{Speechful} $|$ \emph{Claude API, Lava, Deepgram, OpenAI}}{October 2025}
  \resumeItemListStart
    \resumeItem{Scoped the product as a user-driven improvement engine: surfaced raw quantitative feedback from Claude/Deepgram analysis and left interpretation and action to the user, rather than building a prescriptive coaching layer.}
    \resumeItem{Chose a periodic-screenshot capture model over continuous streaming to balance real-time feedback against processing latency, within a hackathon build timeline.}
    \resumeItem{Integrated multiple sponsor AI services (Claude, Lava, Deepgram, OpenAI) into a single feedback loop, prioritizing breadth of usable sponsor tooling within a fixed 48-hour build window.}
  \resumeItemListEnd
```

## Raw notes
<!-- Problem / approach / result. Failures, debugging stories, design
     decisions, war stories. Interview material — never goes on a resume
     directly. -->
Built at Cal Hacks 12.0 (October 24-26, 2025, Palace of Fine Arts, SF). Team of 4: Ylann Bouis, Arthur Wang, Ethan (Ethan Tran), Kevin Tun.

Ethan's role: full-stack engineer. Built the frontend and connected the ML pieces to the backend — the integration layer across the whole stack was his.

Tech/sponsor choice: picked Claude + Lava specifically because it maximized track coverage and unlocked the most sponsor credits available — a resourcing decision as much as a technical one, made deliberately under hackathon constraints.

Architecture decision: took periodic screenshots (every few seconds) rather than continuous or frame-by-frame capture, as the right latency/accuracy tradeoff for the timeline.

Scope decision: built as a "user-driven improvement engine" — the app surfaces all the stats and quantitative feedback, but responsibility for acting on it sits with the user. The app's job was to generate honest quantitative feedback, not to prescribe behavior.

Hardest part / where time went: the feedback engine — taping together screenshot capture, ML analysis, and the feedback surface into one working loop was the main time sink and main technical challenge.

No numbers exist yet for any of this — not fabricated, just not measured.

No award/track win appears on the Devpost page for this project. Not a pending stub like Imprompt-U's — simply not a claim being made at all.

Status: local-only, no further work since the hackathon. Archived.

## Metric sources
<!-- Where each number came from: commit hash, log file, submission link.
     A metric without a source here doesn't get used. -->
- No quantitative claims made anywhere in raw notes (no latency numbers for the screenshot pipeline, no accuracy/consistency figures for the ML feedback, no usage counts) — none were volunteered, so none are fabricated here.
- No award/placement claimed — Devpost page shows no winner badge or track result, so there's nothing here needing a source.