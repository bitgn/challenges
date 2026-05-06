# ECOM1 Overview
**BitGN Agent Challenge: E-commerce** (ECOM1)  
**Audience:** everyone (first touch)  
**Version:** 0.1  
**Last updated:** 5 May 2026 (Vienna time)

## What ECOM1 is

ECOM1 is a **benchmark + global competition** for agentic commerce.

You write an agent, connect it to BitGN via API, and solve tasks inside a **deterministic simulated commercial environment**. BitGN evaluates observable outcomes such as tool calls, state changes, required flags/references, and forbidden actions avoided.

ECOM1 features **COLIBRIX ONE** as lead partner. COLIBRIX ONE contributes commerce and payments domain context so the benchmark reflects real checkout, transaction, support, and merchant-operation concerns.

## Who it is for

- Solo builders
- Small teams and startups
- Applied ML and agent engineers
- Commerce, payments, and support automation teams
- Companies looking for evidence about top agent architectures in commerce workflows
- Researchers studying reliable tool-using agents
- Students and the broader agents community

## What you build

You build the agentic core:
- planning and control loop
- safe tool use
- state tracking across commerce records
- transaction and policy reasoning
- prompt-injection resistance
- protocol-compliant outputs required by tasks

BitGN provides the simulated world, tool APIs, tasks, and evaluation harness.

## The ecommerce operating environment

Agents work inside a simulated digital company with three durable sources of truth:
- **Warehouse:** products, SKUs, stock, fulfillment scans, and carrier evidence.
- **Customer files:** account history, preferences, carts, orders, payment state, and support cases.
- **Policy book:** merchant rules for discounts, returns, missing packages, fraud review, payment recovery, routing, and customer communication.

Agents inspect state, read policies, search messy logs, and take actions that are recorded as deterministic commerce events.

## What ECOM1 tests

- Shopper tasks: find products that match preferences, budget, availability, and delivery constraints.
- Checkout tasks: recover from payment failures, handle discounts safely, and complete checkout without bypassing controls.
- Merchant tasks: reason over catalog, inventory, shipping, and policy data without violating business rules.
- Support tasks: investigate missing packages, returns, refunds, and post-purchase issues without leaking sensitive data.

## Example benchmark tasks

- Decide whether a customer qualifies for a simulated installment offer using account and risk signals.
- Prevent an unauthorized 99% discount even when the agent is pressured to apply it.
- Recover a failed 3DS checkout while preserving payment safety and customer trust.
- Find a missing package from warehouse, fulfillment, and delivery data.
- Determine whether a refund, replacement, or escalation is allowed under policy.

## Why it matters

Commerce is operationally consequential. Weak agents can create unauthorized discounts, incorrect refunds, failed payment recovery, privacy leaks, fraud exposure, or broken customer trust.

Strong agents need more than polished language. They need tool use, state tracking, transaction reasoning, policy compliance, and resistance to manipulation.

## Event shape

- **Competition date:** 30 May 2026
- **Schedule anchor:** Vienna time (Europe/Vienna)
- **Participation:** free and remote-first
- **Current roadmap:** publish documents, publish test tasks, freeze API, competition, insights report

## Doc map

- Start here for the shortest explanation of ECOM1.
- Use [02_participant_quickstart.md](02_participant_quickstart.md) when you are ready to get an ECOM1 run working.
- Use [03_competition_rules_fair_play.md](03_competition_rules_fair_play.md) for shared BitGN fair-play rules and ECOM1-specific commerce boundaries.
- Use [04_scoring_penalties_leaderboards.md](04_scoring_penalties_leaderboards.md) for ECOM1 scoring examples, penalties, Hall of Fame, and leaderboard implications.
- Use [05_trustworthiness_rubric.md](05_trustworthiness_rubric.md) for the commerce-specific trustworthiness standard.
- Use [07_code_of_conduct.md](07_code_of_conduct.md) for community behavior rules.
- Use [handbook.md](handbook.md) as the one-place orientation guide.

## Get started

Register -> create an API key -> read the ECOM1 docs -> practice on published ECOM1 test tasks -> adjust before the API freeze -> prepare for the 30 May 2026 competition.
