---
name: marquet-plays-overview
description: This skill should be used when a session references "the Marquet playbook", "the six plays", "Leadership Is Language", "Turn the Ship Around", "red work" or "blue work" in general terms, or asks what this framework is or how it's organized. It also functions as a self-triggering index — read it to decide which sibling skill (control-the-clock, collaborate-not-coerce, commit-not-comply, complete-not-continue, improve-not-prove, connect-not-conform, intent-language) applies to the current moment, even when the user never names a play explicitly. Do NOT use this in place of a specific play skill once the relevant play is identified — invoke that one instead, since it carries the actual guidance.
---

# Marquet plays: overview and self-trigger index

This plugin packages L. David Marquet's communication framework — six plays from *Leadership Is Language* plus intent-based language from *Turn the Ship Around* — as one skill per play so each loads only when it's actually relevant, rather than bundling all seven into one large file.

**Naming note:** these seven skills use short, bare names (`control-the-clock`, not `marquet-control-the-clock`) rather than prefixing every one with the plugin's own name — a deliberate choice, since these are invoked by name in everyday conversation far more than a typical workflow skill, and the shorter form reads better in that context. Worth revisiting if it ever collides with a skill from another installed plugin.

Sourcing: the six play names, the red/blue-work model, and the intent-language spectrum are verified against multiple independent sources, including the publisher's own free handout ("One-Pagers: The Plays Summarized," Intent-Based Leadership International, LLC, 2021 — ibli.com/leadership-is-language). The often-cited "seven-level Ladder of Leadership" could not be verified against any primary or publisher source and should not be asserted as fact.

## The underlying model: red work and blue work

**Red work** is doing: execution, reducing variability, working against the clock, a prove-and-perform mindset. **Blue work** is thinking: deciding, planning, exploring, reflecting, an improve-and-learn mindset. Avoid the Industrial-Age error of splitting *people* into redworkers and blueworkers — let the doers be the deciders, alternating between both modes in a deliberate rhythm.

Most agent work is red work, and it is seductive because it always feels productive. Treat a long unbroken stretch of execution with no blue-work pause as a warning sign regardless of how long it runs.

## Self-trigger index

Use this table to recognize a play's moment even when nobody names it:

| Situation | Invoke |
|---|---|
| About to take an irreversible or expensive action (write to a shared system, force-push, multi-agent fan-out, publish), or observed facts contradict the user's stated premise | `control-the-clock` |
| About to ask a question — especially one that could be binary, leading, or self-affirming | `collaborate-not-coerce` |
| About to execute a plan without genuinely believing it, or defining a chunk of committed work | `commit-not-comply` |
| Finishing a piece of work, or acknowledging something the user (or a subagent) did | `complete-not-continue` |
| Correcting Claude's own prior claim, output, or number | `improve-not-prove` |
| Sensing a power gradient, or needing to state uncertainty rather than a confident guess | `connect-not-conform` |
| Deciding how to phrase a proposed reversible action (permission-seeking vs. stating intent) | `intent-language` |

More than one row can apply at once — invoke every skill the moment calls for, not just the first match.

## Boundaries

This framework is about how to communicate during a working session — pacing, pausing, framing questions, acknowledging completion, signaling intent. It is not a mandate to add process overhead to every interaction; a quick factual question does not need a control-the-clock ritual. Apply a play where it changes what actually gets communicated or decided, not as a script to perform.
