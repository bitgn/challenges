# Competition Rules & Fair Play
**BitGN Agent Challenge: E-commerce** (ECOM1)  
**Audience:** participants, observers, community organizers  
**Version:** 0.2  
**Last updated:** 6 May 2026 (Vienna time)  

This doc is the canonical source for ECOM1 participation rules, fair play, and valid competition submissions. For scoring formulas, penalties, Hall of Fame, and leaderboard behavior, see [04_scoring_penalties_leaderboards.md](04_scoring_penalties_leaderboards.md).

## Eligibility

Open to all worldwide, subject to the BitGN Terms of Service. Participation is free and remote-first. Google login is required to obtain an API key.

The BitGN Terms of Service include restrictions on participation by sanctioned persons or entities.

## Teams and collaboration

- Solo participants are allowed.
- Teams are allowed.
- Collaboration and open-source sharing are allowed and encouraged.

## During-run rule: no human-in-the-loop

No human intervention is allowed inside a run. Once a run starts, the agent must complete the task autonomously:

- no manual selection of tool calls
- no manual writing of the final answer
- no operator steering mid-run
- no human override for commerce decisions such as discounts, refunds, payment recovery, fraud review, replacement, or escalation
- no manual correction of commerce state during the run

Between runs, you may modify your agent, prompts, tools, code, configuration, and local test harnesses.

## Allowed tooling

- Any LLMs, cloud or local
- Any programming language
- External tools, wrappers, orchestration frameworks, and local runtimes
- Local logging, debugging, evaluation, and observability outside the active benchmark run

Allowed tooling must still follow the challenge API contract and fair-play rules.

## Baseline disallowed behavior

- Exploiting platform bugs or security vulnerabilities
- Bypassing intended limits, abusing rate limits, or degrading platform reliability
- Attempting to extract hidden tasks, hidden evaluation data, scoring internals, or leaderboard internals
- Manual answering or human-in-the-loop operation inside a run

## ECOM1-specific fair-play boundaries

ECOM1 is about safe action inside business constraints. Agents should not treat simulated business controls as obstacles to bypass.

Disallowed ECOM1 behavior includes:

- forcing unauthorized discounts, coupons, refunds, replacements, credits, or installment approvals
- bypassing payment safety controls, fraud-review boundaries, risk checks, or checkout constraints
- inventing policy exceptions that are not supported by the policy book
- leaking customer, account, order, payment, merchant, or benchmark-sensitive data
- manipulating logs, warehouse evidence, order history, customer files, or support records to make an invalid action appear valid
- completing checkout, support, refund, replacement, escalation, or merchant-operation actions through unintended platform behavior
- using real-world commerce systems, real customer data, or real payment flows as part of a benchmark run

## Competition window mechanics (blind scoring)

During the competition window:
- you may execute multiple runs
- you may submit one run to Hall of Fame
- detailed feedback is suppressed

After the window closes, results and breakdowns are revealed where supported by evaluation design.

## What counts as a valid competition submission

A valid Hall of Fame entry is one completed run during the competition window that is:
- explicitly selected via **"Submit to Hall of Fame"**, or
- auto-submitted as the last completed run before cutoff

## Enforcement approach

Violations may result in:

- Hall of Fame disqualification for affected runs
- leaderboard removal for severe or repeated abuse
- platform access restrictions to protect integrity and uptime
