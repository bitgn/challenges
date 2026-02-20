# AGENTS.MD (Repository Root)

This repository contains Markdown documentation for BitGN **challenges**. Each challenge lives in its own top-level folder (e.g., `pac/`). Future challenges (e.g., `e-commerce/`) should follow the same structure and conventions.

## High-level goals
- Keep documents **internally consistent** across a challenge folder (terminology, dates, links, rules).
- Make changes as **small, reviewable diffs** (avoid broad reformatting).
- Avoid inventing facts, features, timelines, or product UI that are not explicitly documented.

## Repository layout conventions
- Each challenge folder contains:
  - A numbered doc set (`01_...md` through `07_...md`)
  - `handbook.md` as the “single-source-of-truth”
  - `faq.md` as a short public FAQ derived from the handbook

## Terminology policy
- Use **challenge** as the umbrella term at the repository level.
- Within a specific challenge, some mechanics may still be described as a “competition window” or “competition day” if that wording exists in the published docs/UI. Do not rename such terms unless the change request explicitly includes updating the user-facing docs/UI text.

## Documentation standards (applies everywhere)
### Markdown style
- Use standard GitHub-flavored Markdown (GFM).
- Prefer `##` / `###` headings; avoid deep nesting unless necessary.
- Keep headings stable to preserve anchor links.
- Use fenced code blocks only for literal text snippets (URLs, commands, copy-paste blocks).
- Use relative links inside the repo when referencing other docs.

### Tone and voice
- Professional, direct, engineering-oriented.
- No marketing hype. Make claims only when supported by the docs.
- Prefer concrete definitions and crisp rules.

### Consistency rules
When editing, ensure cross-document consistency for:
- Names, branding, abbreviations
- Dates and time zone anchors (Europe/Vienna; use absolute dates where possible)
- Key links (website, status page, newsletter, support email)
- Core definitions used across docs (task/run/session, Hall of Fame vs Live)

If you change a core concept, update:
1) the challenge’s `handbook.md` first,
2) then the relevant numbered docs,
3) then `faq.md` and any impacted support docs if needed.

## Change workflow (Codex guidance)
1) Identify the challenge folder(s) affected.
2) Read `handbook.md` first to understand canonical definitions and mechanics.
3) Make the smallest change necessary.
4) Update dependent docs for consistency (especially `faq.md` and related challenge guides).
5) Run a quick self-review using the checklist below.

## Self-review checklist (before proposing changes)
- [ ] No new facts were invented (features, policies, numbers, dates, UI labels).
- [ ] Terminology matches the handbook and the repo terminology policy.
- [ ] Links are correct and consistent across docs.
- [ ] Any date/time claims are explicit and time zone anchored when relevant.
- [ ] Headings weren’t renamed unnecessarily (anchors preserved).
- [ ] Changes are minimal and localized (no bulk reflow).

## What to do if information is missing or uncertain
- Prefer adding a clearly-marked placeholder like: **“(TBD)”** or **“(To be announced)”**.
- If a decision is required, add a short `TODO:` note describing what must be confirmed.
- Do not guess.

## Adding a new challenge folder (future)
When creating a new challenge folder (e.g., `e-commerce/`):
- Mirror the `pac/` structure.
- Provide a `handbook.md` that acts as the canonical source.
- Keep cross-challenge conventions consistent (naming, style, and workflow rules).
