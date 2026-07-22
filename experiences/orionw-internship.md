---
name: OrionW
dates: Jun 2026 - Jul 2026
status: shipped
org: OrionW
role: Software Engineering Intern
location: Singapore
employment_type: internship
skills: [vector databases, ocr, full-stack, authentication, llm-based evaluation, postgresql]
metrics: []  # unofficial self-timed test below — not promoted to a formal metric until logged/screenshotted
angles: [ml-engineering, ai-product, full-stack]
verified: false
---

## Variant: ml-engineering
- Built an AI resume screener letting employers define quantifiable hiring criteria and score candidates against them with an LLM.
- Internal testing (self-timed, unofficial) showed screening time for 100+ resumes dropped from ~6 hours to ~1.5 hours.
- Built a vector database system for Singapore PDPC enforcement cases with OCR parsing that auto-populates structured case templates from source PDFs.

```latex
% Ready to paste into the resume .tex for this variant.
\resumeSubheading
  {OrionW}{Singapore}
  {Software Engineering Intern}{Jun. 2026 -- Jul. 2026}
  \resumeItemListStart
    \resumeItem{Built an AI resume screener enabling employers to define quantifiable hiring criteria and score candidates against them; internal testing showed screening time for 100+ resumes dropped from 6 hours to 1.5 hours.}
    \resumeItem{Built a vector database system for PDPC enforcement cases with OCR parsing that auto-populates structured case templates from source PDFs; supports comparative table views, full authentication, and an admin panel.}
  \resumeItemListEnd
```

## Variant: full-stack
- Designed and shipped two internal tools end-to-end: an AI resume screener and a legal case database.
- PDPC case tool: comparative table view across multiple cases, full user authentication, admin panel for access management.
- Owned both frontend and backend; integrated OCR parsing and LLM scoring pipelines into a working product used inside the firm.

```latex
\resumeSubheading
  {OrionW}{Singapore}
  {Software Engineering Intern}{Jun. 2026 -- Jul. 2026}
  \resumeItemListStart
    \resumeItem{Designed a full-stack legal case database with OCR-driven auto-fill, comparative table views, full authentication, and an admin panel for access management.}
    \resumeItem{Built an AI resume screener with employer-defined quantifiable hiring criteria and LLM-based candidate scoring.}
  \resumeItemListEnd
```

## Raw notes
- Role was admin/legal-ops oriented at the outset (boutique TMT/FinTech law firm); pivoted toward self-directed engineering work after Week 1 reconnaissance identified operational pain points.
- Resume screener: employer sets categories/weights, AI rates each resume per category. The "6 hrs -> 1.5 hrs" figure is Ethan's own before/after timing on a batch of 100+ resumes — not an official company-reported number.
- PDPC = Singapore's Personal Data Protection Commission. Case DB indexes PDPC enforcement decisions in a vector store for retrieval; OCR reads the source case PDF and fills a structured template automatically.
- No user-adoption or accuracy numbers exist yet for either tool — don't claim any until obtained.

## Metric sources
- "6 hrs -> 1.5 hrs" resume screening time: self-timed by Ethan, unofficial, no logged record. If a real log/screenshot/manager confirmation surfaces, upgrade metrics field and set verified: true. Until then this stays out of the frontmatter metrics list and is used only as prose in bullets, framed as "internal testing."