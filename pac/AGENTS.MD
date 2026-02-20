# AGENTS.MD (pac/)

This folder contains the public documentation set for the BitGN **challenge**:
**BitGN Agent Challenge: Personal & Trustworthy** (short: **BitGN PAC**, “Personal Agent Challenge”).

These documents are intended to be edited by automated agents (e.g., OpenAI Codex) with a focus on correctness, consistency, and small diffs.

## File map (what each doc is for)
- `01_overview.md` — First touch. What it is, why it matters, how it works (high level).
- `02_participant_quickstart.md` — Builder onboarding. “First successful run” path.
- `03_competition_rules_fair_play.md` — Enforceable rules, minimal legalese.
- `04_scoring_penalties_leaderboards.md` — Scoring model, penalty categories, leaderboard explanation.
- `05_trustworthiness_rubric.md` — Human-readable definition of “trustworthy” and examples.
- `06_hubs_program_guide.md` — How to host a hub; neutrality/data/liability boundaries.
- `07_code_of_conduct.md` — Baseline community and hub conduct requirements.
- `handbook.md` — Canonical “single-source-of-truth” for the entire challenge.
- `faq.md` — Short homepage FAQ derived from the handbook.

## Terminology policy (pac/)
- Treat **challenge** as the umbrella term.
- Preserve existing user-facing terms that include “competition” unless explicitly asked to rename them:
  - filenames like `03_competition_rules_fair_play.md`
  - phrases like “competition window”, “competition day”, “competition submission”
  - UI labels (e.g., “Submit to Hall of Fame”)
If you do rename user-facing wording, do it as an intentional, repo-wide change across all pac docs and the UI/product copy.

## Canonical source rule
`handbook.md` is the canonical source. If a change affects definitions, mechanics, or policies:
1) Update `handbook.md` first.
2) Propagate changes to the numbered docs.
3) Update `faq.md` if impacted.

Avoid drifting definitions between docs.

## Concepts that must stay consistent across all pac docs
### Branding and identity
- Full name: **“BitGN Agent Challenge: Personal & Trustworthy”**
- Short name: **“BitGN PAC”** (Personal Agent Challenge)
- Organizer: **“BitGN by Rinat Abdullin”**
- Name spelling: **Rinat Abdullin**
- “BitGN” does not stand for anything.

### Canonical links (must match everywhere)
- Website: `https://bitgn.com`
- Newsletter: `https://bitgn.substack.com`
- Status page: `https://status.bitgn.com`
- Support contact: `biz@abdullin.com`

### Schedule anchor
- Official schedule is anchored to **Vienna time (Europe/Vienna)**.
- Main event date: **April 11, 2026**.
- Rollout phases:
  - Smoke test / minimal sandbox: **March 2026** (month-level is OK).
  - Full API + limited practice tasks: **at least two weeks before April 11, 2026**.
- Exact event window times can remain **TBD** unless explicitly specified elsewhere.

### Platform mechanics (do not contradict)
- Deterministic simulated environment; evaluation is outcome-based (tool calls + side effects + required flags/references).
- Avoid claiming “LLM-as-a-judge”; the intent is deterministic evaluation.
- Tasks can be generated per session with seeded variability to reduce overfitting.

### Definitions (must match everywhere)
- **Task:** one unit of work with deterministic success criteria.
- **Run:** one attempt on one task instance (**one task = one run**).
- **Session:** a batch run across all tasks in a task set (practice or main event). Sessions may run tasks sequentially or in parallel.

### Integrity rules (must match everywhere)
- During-run rule: **no human-in-the-loop inside a run**.
- Blind scoring window: during the event window, detailed feedback is suppressed.
- Hall of Fame vs Live:
  - **Hall of Fame:** frozen leaderboard from blind-window submissions.
  - **Live leaderboard:** ongoing runs before/after, with feedback after the blind window.
- Hall of Fame submission mechanics:
  - Participants can run multiple sessions.
  - They select one via UI text: **“Submit to Hall of Fame”**.
  - If not selected, **last completed session before cutoff is auto-submitted**.

### Scoring model (keep stable unless explicitly changed)
- Each task yields up to **1.0** points; penalties can reduce to **0.0**.
- Scores are summed and normalized (often described as 0–100).
- API-call cap is described conceptually (anti-bloat); avoid over-specifying implementation.
- Mention typical penalty categories consistently (prompt injection/exfiltration, unsafe tool use, constraint violations, protocol failures, missing grounding).

### Hubs boundaries (do not blur)
- Hubs manage venue, logistics, marketing, sponsors, and prizes.
- BitGN provides in-platform proposal flows (`/me`, `/me/hubs/new`, `/me/hubs`), approval-gated revisioned listings, hub code/QR on-site check-in attribution, and local leaderboard views.
- **No charging participants for challenge participation** (non-negotiable).
- Data boundary: BitGN does not share platform registration data with hubs.
- Liability boundary: hub event is hub organizer’s responsibility; platform + listing are provided by BitGN.

## Editing guidelines (Codex)
### Make minimal diffs
- Do not rewrap paragraphs, reorder sections, or rename headings unless necessary.
- Preserve anchors and filenames.

### Prefer concrete, testable wording
- Rules should be enforceable and unambiguous.
- If a detail is unknown, mark it **TBD** rather than guessing.

### Avoid accidental scope creep
Do not introduce:
- new APIs/tools not listed (unless explicitly approved in the docs)
- new leaderboards/tracks beyond what is described
- new eligibility restrictions
- new sponsor relationships (global sponsorship is explicitly absent; hubs can have local sponsors)

### Cross-document update rule
If you change any of the following, you must update all impacted docs:
- definitions (task/run/session)
- submission mechanics (Hall of Fame selection / auto-submit)
- date/time claims or time zone anchor
- penalty categories or scoring normalization
- hub non-negotiables or boundaries
- canonical links/contact

## Quick consistency checklist (pac/)
- [ ] `handbook.md` updated first (if the change is conceptual).
- [ ] All references to April 11, 2026 and Vienna time remain correct.
- [ ] “Hall of Fame” vs “Live leaderboard” definitions match.
- [ ] “No human-in-the-loop inside a run” appears consistently where relevant.
- [ ] Links and support contact match the canonical list.
- [ ] Hub rules include “no charging participants” + data/liability boundaries.
- [ ] No new facts were invented; unknowns remain TBD.

## What to do when unsure
- Add `TBD` for missing details.
- Add a short `TODO:` note describing what must be confirmed.
- Do not guess or introduce new policy.
