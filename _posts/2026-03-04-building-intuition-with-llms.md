---
title: "Building Engineering Intuition in an LLM World"
date: 2026-03-04
tags: [career, learning, llm, software-development]
excerpt: "LLMs don’t replace experience—they compress feedback loops. You still build intuition through debugging scars, mental models, and deliberate reps."
---

If you’re new to software engineering, this question is completely valid:

“If companies expect AI to be used from here on out, how do I build the years of experience and intuition that used to come from manually writing code and building systems?”

Here’s the core truth:

**LLMs don’t replace experience. They compress feedback loops.**

The risk for early engineers isn’t using LLMs. The risk is using them *passively*—copying outputs without building the reasoning and debugging muscle underneath.

This post is a practical framework for building real engineering intuition *with* LLMs, not *instead of* it.

## The Mental Model: What “Intuition” Actually Is

Engineering intuition is not a magical senior-engineer superpower. It’s mostly pattern recognition built from repetition and failure.

One simple way to think about it:

**Intuition = Scars (Debugging) + Models (Reasoning) + Reps (Deliberate Practice)**

### 1) Scars (Debugging)

The fastest way to learn is to ship something that breaks and then fix it calmly.

LLMs can generate code, but they don’t give you the “scar tissue” from:

- A flaky test that fails only in CI
- A retry storm that melts your downstream dependency
- A timeout that silently turns into data inconsistency
- A memory leak that takes hours to surface

Those scars build reflexes that no tutorial can replace.

### 2) Models (Reasoning)

Models are your internal explanations of how systems behave:

- latency vs throughput
- cache hits vs staleness
- retries vs idempotency
- consistency vs availability
- blast radius vs rollout strategy

LLMs can *suggest* trade-offs, but your intuition grows when you can **predict** what will happen before running the system.

### 3) Reps (Deliberate Practice)

Reps are not “writing more code.” Reps are building end-to-end:

- requirements → design → implementation → testing → deployment → monitoring

Most early engineers stall because they only practice *snippets* (a small function, a small feature) but not the full lifecycle.

## How to Work with an LLM (Without Losing Your Brain)

Treat the LLM as a **sparring partner**, not an author.

Here’s the workflow that compounds skill quickly:

**Try solo (30–60 min) → Ask for critique → Refactor yourself → Write what you learned**

### Step 1: Try Solo First (30–60 minutes)

You need a little struggle. Not weeks of struggle—just enough to form a hypothesis.

Before prompting:

- What is the problem?
- What are the constraints?
- What are likely failure modes?
- What trade-offs am I making?

Even a rough design is better than none, because it gives you something to compare against.

### Step 2: Ask the LLM to Critique, Not Create

Copy/paste prompt templates (use exactly like this):

- “Here is my design and constraints. What edge cases did I miss?”
- “Find the weakest assumption in this approach and challenge it.”
- “List 5 failure modes. For each: detection signal + mitigation.”
- “Review this like a strict senior engineer. Ask questions, don’t rewrite it.”
- “What would break at 10x traffic? Be specific.”

This keeps you in the driver’s seat.

### Step 3: Refactor Yourself (No Blind Copy-Paste)

If the LLM gives you a better approach, great—but rewrite it in your own words and code.

This is the difference between:

- learning a concept
- renting a solution

### Step 4: Write a Mini Post-Mortem

After you finish, write 10 lines:

- what you tried
- what failed
- what surprised you
- what you would do differently

That reflection is how experience becomes intuition.

## Non-Negotiables for Early Engineers

These are rules that protect your growth:

- **Never ship code you can’t explain line-by-line.**
- **Always run the code.** (LLM output is untrusted until executed.)
- **Break it intentionally.** (bad inputs, timeouts, concurrency, load)
- **Read real code.** (open source + production codebases)

If you do these consistently, you will build intuition quickly—even while using LLMs every day.

## The Biggest Traps (Anti-Patterns)

If you avoid these, you’re already ahead:

- **Prompting before thinking:** you outsource the most important part.
- **Copy-paste programming:** you ship things you don’t understand.
- **Skipping debugging:** you lose the main path to intuition.
- **Treating LLM output as truth:** you stop verifying assumptions.

LLMs accelerate people who think. They expose people who don’t.

## A 2-Week Training Plan (Practical Reps)

If you want to build “years of intuition” faster, do this:

### Week 1: Build a Small System End-to-End

**Day 1:** Build a simple HTTP API (CRUD for a single resource).
Focus: request/response shape, basic validation.

**Day 2:** Add persistence.
Focus: schema design + error handling.

**Day 3:** Add tests.
Focus: unit tests for business rules + one integration test for the API.

**Day 4:** Add structured logging and request IDs.
Focus: debugging in production-like conditions.

**Day 5:** Add a basic performance check.
Focus: measure latency at p50/p95 and understand where time goes.

**Day 6:** Add one reliability feature.
Pick one: retries + idempotency, or rate limiting, or circuit breaking.

**Day 7:** Break it on purpose and write a post-mortem.
Introduce: timeouts, bad inputs, partial failures. Document what happened.

### Week 2: Operate It Like Production

**Day 8:** Add monitoring signals.
Focus: error rate, latency, saturation.

**Day 9:** Add a safe rollout mechanism.
Pick one: feature flag or canary rollout conceptually (even if simulated locally).

**Day 10:** Practice a rollback.
Focus: rollback steps, data safety, and verification.

**Day 11:** Read an open source project in your stack.
Ask: why is it structured this way? what trade-offs were chosen?

**Day 12:** Ask the LLM to do a “senior review” of your system.
Focus: biggest risks, missing tests, missing observability.

**Day 13:** Refactor one subsystem.
Focus: code clarity, modularity, maintainability.

**Day 14:** Write a final summary post.
What changed in your mental model? What would you build next?

This plan works because it forces you to build *scars*, *models*, and *reps*—not just features.

## A Quick Note for Seniors (Mentors)

LLMs can generate options. Seniors still teach judgment:

- what to ignore
- what to measure
- where the risk really is
- how to recover when things break

If you’re mentoring juniors, a powerful practice is to ask them to explain:
**“Why is this the right design, and what would make it fail?”**

## Closing

If you’re early in your career, don’t worry that you “missed” the pre-LLM era.

You can grow faster than previous generations if you use LLMs correctly:

- to critique your thinking
- to surface failure modes
- to shorten feedback loops

And you keep your fundamentals strong by refusing to ship what you can’t explain.

That’s how you build intuition in an LLM world.

