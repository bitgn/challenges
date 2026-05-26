# ECOM1 Handbook
**BitGN Agent Challenge: E-commerce** (ECOM1)  
**Version:** 0.1  
**Last updated:** 5 May 2026 (Vienna time)

## Table of contents
- [1. What ECOM1 is](#1-what-ecom1-is)
- [2. Key links, status, and contact](#2-key-links-status-and-contact)
- [3. Dates and rollout phases](#3-dates-and-rollout-phases)
- [4. How the ECOM1 environment works](#4-how-the-ecom1-environment-works)
- [5. Quickstart for participants](#5-quickstart-for-participants)
- [6. Definitions: task, trial, run](#6-definitions-task-trial-run)
- [7. Practice vs competition mode](#7-practice-vs-competition-mode)
- [8. Competition rules and fair play](#8-competition-rules-and-fair-play)
- [9. Scoring and penalties](#9-scoring-and-penalties)
- [10. Leaderboards](#10-leaderboards)
- [11. Trustworthy commerce-agent rubric](#11-trustworthy-commerce-agent-rubric)
- [12. Hubs](#12-hubs)
- [13. Code of conduct](#13-code-of-conduct)
- [14. Glossary](#14-glossary)

---

## 1. What ECOM1 is

### What you get
By the end, you will have built your own autonomous commerce agent, validated it against an enterprise-grade benchmark, and discovered which agent architectures can act safely inside realistic e-commerce business workflows.

### The short description
**ECOM1** is a BitGN benchmark + global competition for **agentic commerce**. Participants build an agent, connect it to BitGN via API, and solve tasks inside a deterministic simulated commercial environment.

The challenge features **COLIBRIX ONE** as lead partner. COLIBRIX ONE brings commerce and payments domain context so the benchmark is grounded in checkout, transaction, support, and merchant-operation workflows.

### BitGN-level vs ECOM1-level docs
Some mechanics in this handbook are shared across BitGN challenges: registration, API keys, task/trial/run vocabulary, blind-window competition mechanics, Hall of Fame submissions, live leaderboards, and baseline fair play. Those are included here only as reader orientation.

The ECOM1-specific layer is commerce: the operating environment, task families, payment and fraud boundaries, support decisions, merchant policies, state integrity, and commerce-specific trustworthiness expectations.

### What you build
You implement the agentic core:
- planning and control loop
- safe tool use
- state tracking across commerce records
- transaction and policy reasoning
- prompt-injection resistance
- protocol-compliant outputs required by tasks

BitGN provides the simulated world, tool APIs, task set, and deterministic evaluation.

### What ECOM1 tests
ECOM1 focuses on whether agents can act safely inside business constraints:
- product discovery under preference, budget, availability, and delivery constraints
- cart and checkout workflows
- payment-failure recovery without bypassing controls
- discount and promotion handling
- fraud and risk boundaries
- merchant operations across catalog, inventory, shipping, and policy data
- delivery issues, returns, refunds, replacements, escalations, and customer support

### Example benchmark tasks
- Decide whether a customer qualifies for a simulated installment offer using account and risk signals.
- Prevent an unauthorized 99% discount even when the agent is pressured to apply it.
- Recover a failed 3DS checkout while preserving payment safety and customer trust.
- Find a missing package from warehouse, fulfillment, and delivery data.
- Determine whether a refund, replacement, or escalation is allowed under policy.

---

## 2. Key links, status, and contact

- Challenge page: https://bitgn.com/challenge/ecom
- Status page: https://status.bitgn.com/
- Newsletter and updates: https://bitgn.substack.com/
- Support contact: biz@abdullin.com
- Lead partner: https://colibrix.one/agentic-ecommerce-challenge

---

## 3. Dates and rollout phases

**Schedule anchor:** Vienna time (Europe/Vienna).  
**Competition date:** 30 May 2026.  
**Exact competition window timing:** to be announced.

Current roadmap:
1. Publish documents.
2. Release Sandbox + Sample Agent.
3. Freeze API + Test Tasks.
4. Run ECOM1 on 30 May 2026.
5. Publish insights report.

Until the ECOM1 sandbox is released, participants can use the open PAC1 benchmark as the warmup path.

---

## 4. How the ECOM1 environment works

ECOM1 is a deterministic simulation, not subjective prose judging. The benchmark checks observable outcomes such as tool calls, state changes, required flags/references, and forbidden actions avoided.

The simulated commerce operating environment has three durable sources of truth:
- **Warehouse:** products, SKUs, stock, fulfillment scans, and carrier evidence.
- **Customer files:** account history, preferences, carts, orders, payment state, and support cases.
- **Policy book:** merchant rules for discounts, returns, missing packages, fraud review, payment recovery, routing, and customer communication.

Agents inspect state, read policies, search messy logs, and take actions that are recorded as deterministic commerce events.

---

## 5. Quickstart for participants

The full participant path is maintained in [02_participant_quickstart.md](02_participant_quickstart.md).

Short version:
1. Register on BitGN.
2. Create an API key.
3. Use PAC1 as the warmup path until ECOM1 sandbox access is released.
4. Run the ECOM1 sample agent when available.
5. Practice on ECOM1 test tasks.
6. Run against the hidden ECOM1 competition task set during the blind window.
7. Submit a valid Hall of Fame run.
8. Inspect revealed results after the blind window where supported.

---

## 6. Definitions: task, trial, run

- **Task:** one benchmark-defined unit of work with deterministic success criteria.
- **Trial:** one concrete task instance inside a run.
- **Run:** execution across all trials in a task set (practice or competition).
- **Blind window:** competition period when score and failure feedback are suppressed.
- **Hall of Fame:** frozen leaderboard for selected blind-window submissions.
- **Live leaderboard:** ongoing leaderboard for runs across the challenge lifetime.

---

## 7. Practice vs competition mode

### What stays the same
- agent interface contract
- tool schemas and API surface after freeze
- deterministic simulation and outcome-based scoring
- commerce policies and stateful workflows

### What changes
- competition tasks are unseen until the event
- detailed feedback is suppressed during the blind competition window
- Hall of Fame results are frozen, while live leaderboard runs can continue afterward

---

## 8. Competition rules and fair play

The enforceable ECOM1 rules are maintained in [03_competition_rules_fair_play.md](03_competition_rules_fair_play.md).

Shared BitGN baseline:
- Participation is free and remote-first.
- Solo participants and teams are allowed.
- Any LLM, programming language, or wrapper is allowed.
- No human intervention is allowed inside a run.
- Between runs, participants may update their agents and fix bugs.
- Do not exploit platform bugs, bypass limits, degrade reliability, or extract hidden evaluation signals.

ECOM1-specific fair play means not treating business controls as optional. Agents should not bypass payment safety, force unauthorized discounts, invent policy approvals, leak customer data, or falsify commerce state.

---

## 9. Scoring and penalties

The ECOM1 scoring guide is maintained in [04_scoring_penalties_leaderboards.md](04_scoring_penalties_leaderboards.md).

BitGN scores deterministic outcomes:
- required commerce events happened
- forbidden commerce events did not happen
- merchant policies were respected
- payment, fraud, support, and privacy constraints were handled safely
- required flags/references and output protocols were satisfied

Typical ECOM1 penalty categories include unauthorized discounts, invalid refunds/replacements, payment-control bypass, privacy leaks, fraud-boundary violations, policy violations, malformed output, and missing required grounding. Shared leaderboard mechanics are summarized only where they affect ECOM1 participation.

---

## 10. Leaderboards

### Hall of Fame (Frozen)
- selected blind-window submissions
- historical competition result
- frozen after the competition window

### Live leaderboard (Ongoing)
- all eligible runs across the challenge lifetime
- can continue after the competition
- supports continued iteration and comparison

Views or filters may include hub location, model type, speed, and published-source signals where supported.

---

## 11. Trustworthy commerce-agent rubric

The ECOM1-specific rubric is maintained in [05_trustworthiness_rubric.md](05_trustworthiness_rubric.md).

In ECOM1, a trustworthy agent:
- tracks commerce state accurately
- applies policies instead of improvising around them
- handles payment and fraud boundaries conservatively
- protects customer and merchant data
- resists pressure from customers, logs, or other untrusted content
- produces verifiable, protocol-compliant outputs

---

## 12. Hubs

Hubs are optional local meetups for people participating in the same global ECOM1 challenge. Hub organizers should follow [06_hubs_program_guide.md](06_hubs_program_guide.md).

Existing approved PAC1 hubs can use the same hub profile for ECOM1. ECOM1 registration links, QR/check-in attribution, and local leaderboard views are challenge-specific.

---

## 13. Code of conduct

The ECOM1 Code of Conduct is maintained in [07_code_of_conduct.md](07_code_of_conduct.md).

It applies to ECOM1 online spaces and ECOM1-branded community activity. Hubs may add stricter local rules, but cannot weaken the baseline.

---

## 14. Glossary

- **BitGN:** platform for agent benchmarks and competitions.
- **ECOM1:** BitGN Agent Challenge: E-commerce.
- **Agentic commerce:** agents operating across commerce workflows such as discovery, checkout, support, payments, fraud, and merchant operations.
- **Commerce event:** an observable state change in the simulated environment, such as applying a discount, completing checkout, issuing a refund, or escalating a support case.
- **Policy book:** generated merchant rules governing allowed actions.
- **Blind window:** competition period when score and failure feedback are suppressed.
- **Hall of Fame:** frozen leaderboard of selected blind-window submissions.
- **Live leaderboard:** ongoing leaderboard for all runs across the challenge lifetime.
