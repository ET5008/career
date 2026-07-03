# CLAUDE.md

## 1. PURPOSE

This repo is a master resume. Each file in `projects/` and `experiences/` is
canonical source material. When given a job description, generate a
tailored one-page resume in `outputs/`.

## 2. SELECTION LOGIC

- Extract required skills and keywords from the JD
- Match against each file's `angles` and `skills` frontmatter
- Select the 3-4 strongest entries; prefer entries with verified metrics
- Use the angle variant that best matches the JD language

## 3. REPHRASING RULES

- Adapt bullet phrasing to mirror JD terminology, but only where accurate
- One page maximum, reverse-chronological within sections
- Every bullet: action verb + mechanism + quantified outcome

## 4. HARD CONSTRAINTS (non-negotiable)

- NEVER invent, estimate, or inflate metrics or scope
- If a needed metric is absent from the source file, insert [NEEDS METRIC]
  and list it at the top of the output file as a TODO
- Only use content that exists in projects/ or experiences/ files
- If a JD requirement has no honest match, omit it — do not stretch

## 5. OUTPUT FORMAT

Save to `outputs/resume-<role-slug>.md` with a header comment listing: JD
source, date generated, entries used, TODOs.
