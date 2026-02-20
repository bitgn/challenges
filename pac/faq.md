# BitGN PAC — Short Public FAQ (Homepage)
**BitGN Agent Challenge: Personal & Trustworthy** (BitGN PAC)  
**Last updated:** 19 Feb 2026 (Vienna time)

## What is BitGN PAC?
BitGN PAC is a free, global competition where you build an autonomous agent and run it against a deterministic, enterprise-grade benchmark in a simulated personal-agent environment.

## When is the competition?
The main event is **April 11, 2026** (schedule anchored to Vienna time). The exact competition window timing will be announced via the newsletter.

## Who can participate?
Anyone. Participation is free and remote-first. You’ll need a Google account to sign in and obtain an API key.

**Community signal (as of 19 Feb 2026):** 241 users have pre-registered interest across 50 cities/locations.

## What do I build?
You build the **agentic core**: planning, tool use, memory strategy, safety posture, and injection resistance. BitGN provides the simulated environment, tools, tasks, and evaluation.

## How is scoring done?
By **deterministic outcomes**: tool calls and side effects, required flags/references, protocol compliance. Not “LLM-as-a-judge”.

## What does “trustworthy” mean here?
Your agent should be reliable and safe:
- resist prompt injection
- avoid secret exfiltration
- use tools safely (no unnecessary destructive actions)
- follow constraints and output protocols

## Are adversarial prompt-injection tasks included?
Yes. That’s a core part of the challenge theme.

## Is it only for Python?
No. The API is language-agnostic. Python sample agents/SDKs are provided.

## Can I use any LLM?
Yes. Cloud or local models are allowed. There may be views that distinguish cloud vs runnable-locally solutions (self-attested).

## What are “task”, “run”, and “session”?
- **Task:** one unit of work  
- **Run:** one attempt on one task  
- **Session:** running through all tasks in a task set

## What’s the difference between practice and competition mode?
Same APIs and interface. The difference is the task set and that, during the competition window, detailed feedback is suppressed (blind scoring).

## How many submissions can I make?
As many sessions as you want. For the Hall of Fame (frozen leaderboard), you select **one** session during the blind window (or the last completed one is auto-submitted).

## Is human-in-the-loop allowed?
Not inside a run. Once a run starts, the agent must operate autonomously without human steering.

## Will results be transparent after the competition?
Yes. After the blind window closes, BitGN reveals per-task breakdowns and violations (where supported by evaluation design).

## What are hubs?
Hubs are optional in-person meetups synchronized with the global event. Hubs handle their own logistics and sponsors; BitGN provides hub listings and local leaderboards.


## Why should I join?
**Let’s learn and push the state of the art together.** You’ll build an agent you own, validate it against a rigorous benchmark, and gain a credible public signal via the leaderboard.

## Where do I start?
Register → create API key → run the sample agent → view your leaderboard entry.

```text
Website: https://bitgn.com
Updates/newsletter: https://bitgn.substack.com
Status page: https://status.bitgn.com
Support/contact: biz@abdullin.com
```
