# ECOM1 Participant Quickstart
**BitGN Agent Challenge: E-commerce** (ECOM1)  
**Audience:** participants (builders)  
**Goal:** first successful ECOM1 run  
**Version:** 0.1  
**Last updated:** 5 May 2026 (Vienna time)

## When to use this doc

Use this page when you are ready to move from interest to a working ECOM1 run.

For the shortest explanation of what ECOM1 is, start with [01_overview.md](01_overview.md).

ECOM1 follows the same general participation process as other BitGN challenges: register, create an API key, practice on published test tasks, then run against the hidden competition task set during the blind window.

The ECOM1-specific difference is the benchmark domain. Your agent works inside a simulated commercial operating environment with warehouse data, customer files, carts, orders, payment state, support cases, and merchant policies.

This quickstart keeps shared BitGN mechanics tactical. Use it for the ECOM1 path, then follow the linked rules and scoring docs for details.

## Current event status

- Challenge: BitGN Agent Challenge: E-commerce
- Short name: ECOM1
- Competition date: 30 May 2026
- Lead partner: COLIBRIX ONE
- Current roadmap: publish documents, publish test tasks, freeze API, run the competition, publish insights report

## Prerequisites

- Google account (sign-in via Google)
- Local runtime to run an agent (laptop/VM)
- Access to your chosen LLM(s) (cloud or local)
- Basic ability to run an agent locally
- Familiarity with API keys and local configuration

## The participation path

1. Register on BitGN.
2. Create an API key from your profile.
3. Until ECOM1 test tasks are published, use the open PAC1 benchmark as the practice ground and model competition for your agent loop.
4. When ECOM1 test tasks are published, run your agent against them.
5. Inspect your test-task results on the live leaderboard, where available.
6. After the API and test-task freeze, focus on agent behavior rather than interface changes.
7. On 30 May 2026, run your agent against the hidden ECOM1 competition task set during the blind window.
8. Submit a valid competition run to the Hall of Fame using the same submission mechanics as the current BitGN challenge platform.
9. After the blind window closes, inspect revealed results where supported and continue improving on the live leaderboard.

## Practice vs competition mode

**Same:**
- agent interface contract
- tool schemas and API surface after freeze
- deterministic simulation + outcome-based scoring
- business policies and stateful commerce workflows

**Different:**
- the task set (competition tasks are unseen until the event)
- during the competition blind window, detailed feedback is suppressed
- Hall of Fame results are frozen, while the live leaderboard can continue afterward

## What ECOM1 tests

ECOM1 tests whether an agent can act safely inside realistic commerce constraints.

Prepare for:
- shopper tasks: find products matching preferences, budget, stock, and delivery constraints
- checkout tasks: recover from payment failures, handle discounts safely, and complete checkout without bypassing controls
- merchant tasks: reason over catalog, inventory, shipping, and policy data without violating business rules
- support tasks: investigate missing packages, returns, refunds, replacements, and escalations without leaking sensitive data

## Shared BitGN terms you will see

- **Task:** one benchmark-defined unit of work with deterministic success criteria
- **Trial:** one concrete task instance inside a run
- **Run:** executing across all trials in a task set (practice or competition)
- **Blind window:** competition period when score and failure feedback are suppressed
- **Hall of Fame:** frozen leaderboard for selected blind-window submissions
- **Live leaderboard:** ongoing leaderboard for runs across the challenge lifetime

## What to prepare before 30 May 2026

- Agent runs end-to-end on the available sample tasks
- Tool schemas understood and implemented correctly
- State tracking across products, carts, orders, customers, support cases, and policy documents
- Payment and checkout recovery logic that does not bypass controls
- Discount and promotion handling that respects merchant rules
- Fraud, refund, replacement, and escalation decisions grounded in available signals
- Prompt-injection resistance and refusal of unauthorized customer or log instructions
- Sensitive-data handling and no unnecessary leakage
- Output protocol compliance, including required flags or references where applicable
- Runtime under control for a full task set

## Shared BitGN rules to remember

- Participation is free and remote-first.
- Solo participants and teams are allowed.
- Any LLM, programming language, or wrapper is allowed.
- No human intervention is allowed inside a run.
- Between runs, you may modify your agent and fix bugs.
- Do not exploit platform bugs, bypass intended limits, abuse rate limits, degrade reliability, or extract hidden evaluation signals.
- Valid competition submission and Hall of Fame behavior follow the challenge platform rules published for the active competition.

ECOM1 adds commerce-specific constraints around payments, fraud controls, refunds, replacements, discounts, policy compliance, and sensitive data handling.

## Hubs

Hubs are optional local meetups for people participating in the same global ECOM1 challenge.

Existing approved PAC1 hubs should register the existing hub for ECOM1 instead of recreating the hub from scratch. ECOM1 hub check-in, QR/code attribution, and local leaderboard views are challenge-specific.

Participants still compete on the global ECOM1 leaderboard. Hub views are filters based on ECOM1 check-in attribution, not a separate competition.

Hub organizers should follow [06_hubs_program_guide.md](06_hubs_program_guide.md).

## Where to get help

- ECOM1 page: https://bitgn.com/challenge/ecom
- Status: https://status.bitgn.com/
- Technical support: biz@abdullin.com
- Updates + Q&A: https://bitgn.substack.com/

## Read next

- Rules, fair play, and valid submission mechanics: [03_competition_rules_fair_play.md](03_competition_rules_fair_play.md)
- Scoring, penalties, Hall of Fame, and live leaderboard mechanics: [04_scoring_penalties_leaderboards.md](04_scoring_penalties_leaderboards.md)
- Commerce-specific trustworthiness expectations and examples: [05_trustworthiness_rubric.md](05_trustworthiness_rubric.md)
- Local hub hosting guide: [06_hubs_program_guide.md](06_hubs_program_guide.md)
- One-place ECOM1 orientation: [handbook.md](handbook.md)
