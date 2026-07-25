---
title: "Prompt Caching, Explained: Why Your Second AI Message Is Cheaper Than Your First"
description: "Prompt caching can cut the cost of long AI conversations by 90% and cut latency dramatically — but only if the reused part comes first. A plain-English guide to how it works and when it doesn't."
tags: [explainers, how-ai-works]
---

Here is a fact about AI assistants that surprises almost everyone who learns it: **every time you send a message, the model re-reads your entire conversation from the beginning.**

Not a summary. Not an index. The whole thing — your first message, its first reply, the 40-page document you pasted, all of it — processed again, from scratch, on every single turn.

That is enormously wasteful, and it's the problem prompt caching exists to solve.

## Why the model re-reads everything

This follows directly from how [context windows](/what-is-a-context-window/) work. A language model has no memory between turns. Its entire knowledge of your conversation is the block of text it's handed each time you hit send. There is no stored "session" inside the model — the illusion of continuity is produced by re-sending the transcript, every time.

For a short chat, fine. But consider a realistic working case: you paste a 60-page contract and ask fifteen questions about it. Without caching, that contract is processed fifteen times. You are billed for it fifteen times. And you wait for it fifteen times.

## What caching actually does

When a model processes text, it produces internal intermediate results — the expensive part of the work. Prompt caching stores those results for a chunk of text so that identical text, sent again shortly after, doesn't need to be recomputed.

The provider hashes the beginning of your request. If it matches something processed recently, it loads the saved state instead of redoing the math, and only processes the genuinely new part — your latest question.

The savings are not marginal. Typical published figures across providers land around:

- **Cost:** cached input tokens bill at roughly 10% of the normal input rate
- **Latency:** commonly 50–80% faster time-to-first-token on large cached prefixes
- **Cache lifetime:** minutes by default, with longer durations available at a premium

There's usually a small surcharge to *write* the cache in the first place. So caching pays off when you read it back more than once — and is a slight net loss if you never do.

## The one rule: the stable part goes first

This is the whole thing, and it's the part people get wrong.

Caching matches on **prefixes** — the text from the start of your request forward. The cache holds up to the first point where anything differs. One changed character early in the prompt invalidates everything after it.

So the structure that works is:

```
[ system instructions      ]  ← never changes
[ reference documents      ]  ← never changes
[ examples / tools         ]  ← rarely changes
──────────────────────────── cache boundary
[ conversation so far      ]  ← grows
[ this turn's question     ]  ← always new
```

And the structure that quietly destroys your savings:

```
[ today's date and time    ]  ← changes every request
[ system instructions      ]
[ reference documents      ]
```

That second version caches nothing. A timestamp, a session ID, a randomized greeting, or a user's name interpolated at the top will invalidate the entire prefix on every call. It's one of the most common and most expensive mistakes in production AI applications — and it's invisible, because everything still works. It just costs ten times more than it should.

If you need volatile values, put them at the **end**, next to the user's question.

## Where it helps most

Caching's value scales with how much text is repeated and how often. The clearest wins:

- **Long documents, many questions.** A contract, codebase, or research paper you interrogate repeatedly. This is the canonical case.
- **Coding assistants.** Large, stable system instructions plus project context, hit constantly.
- **Customer support bots.** The same product knowledge base in front of every conversation, thousands of times a day.
- **Any agent that loops.** Agentic systems re-send their full instruction set and tool definitions on every step. Uncached, this is brutally expensive.

And where it doesn't help: short one-off questions, conversations where the early content genuinely changes every time, and anything spaced far enough apart that the cache has expired between uses.

## What it is not

Two clarifications worth making, because both get muddled.

**It isn't answer caching.** The model still generates a fresh response every time. Caching skips re-reading the *input*, not re-doing the *thinking*. Ask the same question twice and you'll still get two different answers, and you'll still pay full price for both outputs.

**It isn't memory.** A cache expires in minutes and holds no meaning for the model — it's an optimization at the infrastructure layer, not a place where the model "remembers" you. Products that recall your preferences across sessions are storing text somewhere and re-inserting it into the prompt. That's a database, not a cache.

## Why this ends up in the news

Caching sounds like plumbing, but it shapes stories you'll actually read about.

When a lab announces a dramatic price cut, some of it is usually caching-related rather than a fundamentally cheaper model. When someone reports that an AI agent "cost $200 to run a simple task," the failure is often a cache-hostile prompt structure re-processing the same instructions hundreds of times. And the broader shift toward AI agents that run in long loops only became economically sensible *because* of this optimization — an agent that re-reads its instructions two hundred times per task is a research demo at full price and a product at a tenth of it.

That's the pattern worth noticing: the frontier of what AI can do is set by capability, but the frontier of what AI actually gets *deployed* to do is set by cost per run. Boring infrastructure optimizations move that second line more than most model announcements do.

---

*Related: [What is a context window?](/what-is-a-context-window/) — the limit that explains most of AI's odd behavior. New here? Start with the [plain-English glossary of AI terms](/ai-terms-in-headlines-explained/).*
