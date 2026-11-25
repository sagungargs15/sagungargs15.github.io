---
layout: post
title: "Nov2026 - Between Rules and Gradients: Why AI Keeps Relearning the Symbolic–Stochastic Split"
date: 2026-11-24 23:59:59 -0000
categories: symbolic stochastic rules learning
author: "Sagun Garg"
tags: symbolic stochastic rules learning
---


## Executive summary

The most useful question in building intelligent systems isn't "rules or learning?" It's "where does this problem sit between them?" Every few years the field forgets that, swings hard to one side, and pays for it.

- **The split.** Symbolic systems run on explicit rules and give exact, explainable answers. Stochastic systems learn from examples, follow gradients, and are usually right in ways no one fully specified.
- **The pattern.** AI has swung between the two at least three times: logic and search in the 1960s, expert systems in the 1980s, deep learning in the 2010s. Each swing looked like the final answer.
- **The narrow island.** Pure rules only win when the solution space is well defined, the answer is known to exist, and a small rule set covers it. That island is real, but very narrow.
- **The gap.** We still lack a disciplined way to navigate between the two. Most teams pick a camp, not a boundary.

My read: The durable skill isn't loyalty to a paradigm. It's knowing where a problem's boundary lies, and building the bridge across it on purpose.

## Primer: two ways to be intelligent

**Symbolic systems** encode knowledge as rules: if this, then that, provably. A compiler, a tax engine, and a chess move validator all work this way. Same input, same output, every time, and you can trace why.

**Stochastic systems** encode knowledge as weights learned from data. A spam filter, an image classifier, and a large language model all work this way. They handle messy, open-ended inputs that no one could write rules for, but their answers are probabilities, not proofs.

**Each camp has a story about the other.** To symbolists, neural nets are confident guessers that can't show their work. To connectionists, rule systems are brittle cages that shatter the moment reality wanders off the script. Both stories are true. That's the problem.

## History repeats, with better hardware

**The first swing: logic and search.** In the 1950s and 60s, symbolic AI promised that intelligence was logic plus search. When Minsky and Papert's *Perceptrons* (1969) exposed the limits of single-layer networks, attention and funding drained away from the neural approach.

**The second swing: expert systems.** In the 1980s, companies encoded specialists' knowledge as thousands of hand-written rules. Some worked well inside narrow walls. Then the walls moved. Every exception spawned three more rules, maintenance fell to scarce experts, and the systems couldn't learn. The market collapsed by the end of the decade.

**The third swing: gradients everywhere.** Backpropagation, popularized in 1986, made multi-layer networks trainable. With enough data and compute, the 2010s turned gradients into the default answer to almost everything. Rich Sutton's "bitter lesson" captured the mood: general methods that scale with computation eventually beat clever hand-built knowledge.

**And now, the echo.** In the LLM era we hear the old symbolist complaints in new clothes: hallucination, unreliable reasoning, no guarantees. The fixes look strangely familiar. Tool calls to calculators and code interpreters. Schemas and validators. Retrieval over curated knowledge. Formal verifiers checking generated proofs. We are rebuilding symbolic scaffolding around stochastic cores.

The lesson isn't that one side won. Each swing overcorrected, and the people who did best knew which tool fit which problem.

## The narrow island where rules win

Pure symbolic systems shine under three conditions, all at once:

1. **The solution space is well defined.** You can write down what a valid answer looks like.
2. **The solution is known to exist.** You're computing, not discovering.
3. **A small set of rules covers it.** The rulebook ends.

Tax calculation, compilers, move legality, unit conversion, access control, and double-entry accounting all live here. On this island, rules aren't a limitation; they're the point. You want determinism, and you want to prove it.

**Step off the island and the conditions erode one by one.** "Is this email urgent?" has no closed specification. Language, vision, and human intent have long tails no rulebook ever finishes. Drug discovery and design exploration require searching spaces no one has mapped.

The expert-systems era didn't fail because rules are bad. It failed because people kept pretending the island was a continent.

## Where gradients run out

The ocean around the island is where stochastic systems thrive, but they have their own coastline. Gradients need a smooth landscape and lots of examples. They struggle where:

- **One wrong answer is catastrophic.** A model that's right 99.5% of the time is excellent for search ranking and unacceptable for a medication dosage.
- **Correctness is binary and cheap to check.** It's wasteful to approximate arithmetic or a type checker when the exact version costs microseconds.
- **Data is scarce or the world shifts.** A new regulation lands tomorrow; no training set contains it yet.
- **You must explain the decision.** Auditors, courts, and engineers debugging an outage need a reason, not a probability.

**The failure modes are mirror images.** Rules break loudly at the edge of their coverage. Learned models fail quietly, producing fluent answers that are plausible and wrong. Quiet failure is often worse, because no one knows to look.

## A way to navigate between them

We still need a method for deciding, problem by problem, how much rule and how much gradient to use. Four questions do most of the work:

1. **Can you write down what "correct" means?** If yes, that definition belongs in code, even if something else generates the candidates.
2. **How expensive is a wrong answer?** The higher the cost, the more you want a symbolic check between the model and the world.
3. **How long is the tail?** If unanticipated cases keep arriving, rules alone will drown. Let a learned model cover the breadth.
4. **Is generating harder than verifying?** Often it is. That asymmetry is the most useful seam in the whole design.

The answers usually point to a hybrid. The hybrids that work tend to follow a few patterns:

| Pattern | Learned part does | Symbolic part does | Example |
| --- | --- | --- | --- |
| Propose and verify | Generates candidates | Checks them exactly | LLM writes code; tests and type checker gate it |
| Learned intuition, explicit search | Scores promising moves | Searches and enforces legal moves | AlphaGo pairing networks with tree search |
| Translate, then compute | Turns messy input into structure | Does the math or logic | Natural-language question parsed into SQL |
| Guardrails | Handles the open-ended bulk | Enforces hard constraints and policy | Model drafts; rules block forbidden actions |
| Rules as fallback | Covers the common case | Takes over when confidence is low | Fraud model plus deterministic escalation |

**The common thread:** let the stochastic system explore, and let the symbolic system decide what counts. Gradients are good at finding; rules are good at knowing.

## What I expect

The next pendulum swing is already visible. As learned systems take on more consequential work, demand for guarantees will grow, and rules will look fashionable again. The mistake would be to swing all the way back.

**Predictions:**

1. **Verification becomes the bottleneck, not generation.** The scarce resource shifts from models that can produce answers to systems that can certify them.
2. **"Neuro-symbolic" stops being a research label.** It becomes ordinary engineering practice, the way "client-server" did.
3. **Regulated industries lead the hybrid wave.** Finance, healthcare, and payments will demand explicit rule layers around every model in production.
4. **Some rule-based systems quietly come back.** Teams that replaced deterministic logic with a model will rediscover why it was deterministic in the first place.

**What builders should do:**

- Map each problem before choosing a tool: which part is island, which part is ocean.
- Put the definition of "correct" in code wherever you can write it down.
- Use models for breadth and candidate generation; use rules for gating and guarantees.
- Design for loud failure. Route low-confidence outputs to deterministic paths or humans.
- Revisit the boundary often. As models and data improve, the coastline moves.

Draw that line well, and you get systems that are both flexible and trustworthy. Draw it badly, and history will repeat once more.

## Further reading

- Marvin Minsky and Seymour Papert, *Perceptrons* (1969)
- David Rumelhart, Geoffrey Hinton and Ronald Williams, "Learning representations by back-propagating errors," *Nature* (1986)
- Rich Sutton, "The Bitter Lesson" (2019)
- David Silver et al., "Mastering the game of Go with deep neural networks and tree search," *Nature* (2016)
