# AGENTS.MD (ecom/)

This folder contains the public documentation set for the BitGN **challenge**:
**BitGN Agent Challenge: E-commerce** (short: **ECOM1**).

These documents are intended to be edited by automated agents (e.g., OpenAI Codex) with a focus on correctness, consistency, and small diffs.

## File map (what each doc is for)
- `01_overview.md` -- First touch. What ECOM1 is, why it matters, how it works (high level).
- `02_participant_quickstart.md` -- Builder onboarding. "First successful ECOM1 run" path.
- `03_competition_rules_fair_play.md` -- Enforceable rules, fair-play boundaries, valid competition submissions.
- `04_scoring_penalties_leaderboards.md` -- Scoring model, penalty categories, leaderboard explanation.
- `05_trustworthiness_rubric.md` -- Commerce-specific definition of "trustworthy" and examples.
- `06_hubs_program_guide.md` -- How to host a hub; neutrality/data/liability boundaries.
- `07_code_of_conduct.md` -- Baseline community and hub conduct requirements.
- `handbook.md` -- Canonical "single-source-of-truth" for the entire challenge.
- `README.md` -- Folder index and doc-layering note.
- `faq.md` -- Not present yet; add only when a short public FAQ is needed and derive it from the handbook.

## Terminology policy (ecom/)
- Treat **challenge** as the umbrella term.
- Use **ECOM1** as the short challenge name.
- Preserve existing user-facing terms that include "competition" unless explicitly asked to rename them:
  - filenames like `03_competition_rules_fair_play.md`
  - phrases like "competition window", "competition date", "competition submission"
  - UI labels (e.g., "Submit to Hall of Fame")
If you do rename user-facing wording, do it as an intentional, repo-wide change across all ecom docs and the UI/product copy.

## Canonical source rule
`handbook.md` is the canonical source. If a change affects definitions, mechanics, or policies:
1. Update `handbook.md` first.
2. Propagate changes to the numbered docs.
3. Update `README.md`, `faq.md` (if present), and any impacted support docs if needed.

Avoid drifting definitions between docs.

## Concepts that must stay consistent across all ecom docs
### Branding and identity
- Full name: **"BitGN Agent Challenge: E-commerce"**
- Short name: **"ECOM1"**
- Lead partner: **COLIBRIX ONE**
- Organizer: **"BitGN by Rinat Abdullin"**
- Name spelling: **Rinat Abdullin**
- "BitGN" does not stand for anything.

### Canonical links (must match everywhere)
- Website: `https://bitgn.com`
- ECOM1 page: `https://bitgn.com/challenge/ecom`
- Newsletter: `https://bitgn.substack.com`
- Status page: `https://status.bitgn.com`
- Support contact: `biz@abdullin.com`
- Lead partner: `https://colibrix.one/agentic-ecommerce-challenge`

### Schedule anchor
- Official schedule is anchored to **Vienna time (Europe/Vienna)**.
- Competition date: **30 May 2026**.
- Rollout phases:
  - Publish documents.
  - Publish test tasks / practice materials.
  - Freeze API.
  - Run ECOM1 on 30 May 2026.
  - Publish insights report.
- Exact event window times can remain **TBD** unless explicitly specified elsewhere.

### Platform mechanics (do not contradict)
- Deterministic simulated environment; evaluation is outcome-based (tool calls + state changes + required flags/references).
- Avoid claiming "LLM-as-a-judge"; the intent is deterministic evaluation.
- ECOM1 is a commerce operating environment, not only a shopping-agent benchmark.
- Agents work across warehouse data, customer files, carts, orders, payment state, support cases, and merchant policies.

### Definitions (must match everywhere)
- **Task:** one benchmark-defined unit of work with deterministic success criteria.
- **Trial:** one concrete task instance inside a run.
- **Run:** execution across all trials in a task set (practice or competition).
- **Blind window:** competition period when score and failure feedback are suppressed.
- **Hall of Fame:** frozen leaderboard for selected blind-window submissions.
- **Live leaderboard:** ongoing leaderboard for runs across the challenge lifetime.

### Integrity rules (must match everywhere)
- During-run rule: **no human-in-the-loop inside a run**.
- Blind scoring window: during the event window, detailed feedback is suppressed.
- Hall of Fame vs Live:
  - **Hall of Fame:** frozen leaderboard from blind-window submissions.
  - **Live leaderboard:** ongoing runs before/after, with feedback after the blind window where supported.
- Hall of Fame submission mechanics:
  - Participants can execute multiple runs.
  - They select one via UI text: **"Submit to Hall of Fame"**.
  - If not selected, **last completed run before cutoff is auto-submitted**.

### ECOM1 commerce boundaries (do not soften)
- Agents must not force unauthorized discounts, coupons, refunds, replacements, credits, or installment approvals.
- Agents must not bypass payment safety controls, fraud-review boundaries, risk checks, or checkout constraints.
- Agents must not invent policy exceptions unsupported by the policy book.
- Agents must not leak customer, account, order, payment, merchant, or benchmark-sensitive data.
- Agents must not manipulate logs, warehouse evidence, order history, customer files, or support records to make an invalid action appear valid.
- Do not use real-world commerce systems, real customer data, or real payment flows as part of a benchmark run.

### Scoring model (keep stable unless explicitly changed)
- Each trial yields up to **1.0** points; penalties can reduce to **0.0**.
- Scores are summed and normalized (often described as 0-100).
- Trials are unweighted by default unless an ECOM1 doc explicitly says otherwise.
- API-call cap is described conceptually (fairness / anti-runaway-loop); avoid over-specifying implementation.
- Mention typical penalty categories consistently: unauthorized financial action, payment-control or fraud-boundary violation, policy violation, privacy leak, unsafe tool use, prompt-injection compliance, protocol violation, missing grounding.

### Hubs boundaries (do not blur)
- Hubs are optional local meetups for people participating in the same global ECOM1 challenge.
- Existing approved PAC1 hubs can use the same hub profile for ECOM1.
- ECOM1 registration links, QR/check-in attribution, and local leaderboard views are challenge-specific.
- Hubs manage venue, logistics, marketing, sponsors, prizes, attendee registration, reminders, and local communication.
- BitGN provides public hub listings, approval review, challenge-specific QR/code attribution, and local leaderboard views where supported.
- **No charging participants for challenge participation** (non-negotiable).
- Data boundary: BitGN does not share platform registration data with hubs.
- Liability boundary: hub event is hub organizer's responsibility; platform + listing are provided by BitGN.

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
- new sponsor relationships beyond COLIBRIX ONE as lead partner
- claims that ECOM1 uses real customer data, real payment flows, or live commerce systems

### Cross-document update rule
If you change any of the following, you must update all impacted docs:
- definitions (task/trial/run)
- submission mechanics (Hall of Fame selection / auto-submit)
- date/time claims or time zone anchor
- ECOM1 commerce boundaries
- penalty categories or scoring normalization
- hub non-negotiables or boundaries
- canonical links/contact

## Quick consistency checklist (ecom/)
- [ ] `handbook.md` updated first (if the change is conceptual).
- [ ] All references to 30 May 2026 and Vienna time remain correct.
- [ ] COLIBRIX ONE is described only as lead partner.
- [ ] "Hall of Fame" vs "Live leaderboard" definitions match.
- [ ] "No human-in-the-loop inside a run" appears consistently where relevant.
- [ ] Links and support contact match the canonical list.
- [ ] Commerce boundaries mention payments/fraud/refunds/discounts/privacy where relevant.
- [ ] Hub rules include "no charging participants" + data/liability boundaries.
- [ ] No new facts were invented; unknowns remain TBD.

## What to do when unsure
- Add `TBD` for missing details.
- Add a short `TODO:` note describing what must be confirmed.
- Do not guess or introduce new policy.
