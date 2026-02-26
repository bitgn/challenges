# Participant Quickstart
**BitGN Agent Challenge: Personal & Trustworthy** (BitGN PAC)  
**Audience:** participants (builders)  
**Goal:** first successful run  
**Version:** 1.1  
**Last updated:** 26 Feb 2026 (Vienna time)

## Prerequisites
- Google account (sign-in via Google)
- Local runtime to run an agent (laptop/VM)
- Access to your chosen LLM(s) (cloud or local)
- Basic ability to run a sample agent (Python samples provided; API is language-agnostic)

## Key dates (Vienna time)
- March 2026: API access smoke test / minimal sandbox goes live — confirm your setup and run the sample agent
- At least two weeks before 11 Apr 2026: full API + practice task set available — integrate and iterate
- 11 Apr 2026: main competition day (blind scoring window opens)
- After the event: challenge continues with live feedback and ongoing runs

## The 4-step path (available after the sandbox is released)
1) **Register** on BitGN  
2) **Create an API key**  
3) **Run the sample agent** on the practice tasks  
4) **View your results** on the live leaderboard

## Practice vs competition mode
**Same:**
- agent interface contract
- tool schemas and API surface
- deterministic simulation + outcome-based scoring

**Different:**
- the task set (competition tasks are unseen until the event)
- during the competition blind window, detailed feedback is suppressed

## Product definitions
- **Task:** one unit of work with deterministic success criteria
- **Run:** one attempt on one task instance (one task = one run)
- **Session:** executing across all tasks in a task set (practice or competition)

## Submissions and Hall of Fame
- You can run multiple sessions.
- To submit to the **Hall of Fame** (frozen leaderboard), select **one** completed session during the blind window via **“Submit to Hall of Fame”**.
- If you don’t select one, the **last completed session before cutoff** is auto-submitted.

All sessions still contribute to the **live leaderboard**.

## Where to get help
- Status: check the status page first
- Technical support: email
- Updates + Q&A: newsletter (comments)

## What to prepare before 11 Apr 2026
- Agent runs end-to-end on practice tasks
- Tool schemas understood and implemented correctly
- Injection resistance: refuse/flag malicious instructions
- Constraint compliance and safe tool use
- Output protocol compliance (required flags/references)
- Runtime under control (ballpark ~30 minutes for ~100 tasks with limited parallelization)
