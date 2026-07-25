---
title: "What Is a Context Window? The AI Limit That Explains Most of Its Weird Behavior"
description: "Why AI assistants forget the start of long conversations, why they slow down, and why 'one million tokens' doesn't mean what the marketing implies. A plain-English guide to context windows."
tags: [explainers, how-ai-works]
---

If you use an AI assistant regularly, you have probably run into some version of this: forty messages into a productive conversation, the model suddenly forgets a detail you established at the beginning. Or you paste a long document and get a summary that's oddly thin on the middle section. Or a coding assistant that was doing great work starts making changes that contradict something it wrote an hour ago.

These all have the same cause, and it isn't a bug. It's the **context window** — the single most useful concept for understanding why AI systems behave the way they do.

## The short version

A context window is the maximum amount of text a model can consider at one time. Everything the model knows about your specific conversation — your instructions, your pasted documents, the model's own previous replies — has to fit inside it.

The critical thing most explanations skip: **a model has no memory outside its context window.** It doesn't remember your last conversation. It doesn't remember the first message of this one unless that message is still inside the window. Every single time you hit send, the entire conversation is re-read from scratch, and anything that no longer fits has been dropped or compressed.

That's it. That one fact explains most of the strange behavior.

## What's actually being measured

Context windows are measured in **tokens**, not words. A token is a chunk of text — often a whole common word, sometimes a fragment of a longer or unusual one, sometimes a space or punctuation mark.

The rough conversion for English:

- 1 token ≈ 0.75 words
- 1,000 tokens ≈ 750 words ≈ 1.5 pages
- 100,000 tokens ≈ a 300-page book
- 1,000,000 tokens ≈ several long novels, or a mid-sized codebase

Code, non-English languages, and text full of numbers or unusual formatting tokenize less efficiently — sometimes dramatically so. A 10,000-word Python file will eat noticeably more of your window than a 10,000-word essay.

## Why bigger numbers keep appearing in the marketing

The trend line here is real. Early consumer chatbots had windows of a few thousand tokens — a few pages. Current frontier models advertise hundreds of thousands to over a million.

That growth is genuinely useful. It's the difference between "summarize this chapter" and "here is the entire contract, the entire prior version, and our internal notes; find every clause that changed." Whole categories of work only became possible once documents stopped needing to be chopped up.

But the advertised number is a *ceiling*, not a promise about quality, and three things routinely go unmentioned.

**First, the window is shared.** It holds your input *and* the model's output *and* the system instructions the provider added before you ever typed anything *and* every previous turn of the conversation. A "200,000-token window" is not 200,000 tokens of room for your document.

**Second, performance is not flat across the window.** Researchers have documented a "lost in the middle" effect: models reliably attend to information at the beginning and end of a long context, and are measurably worse at retrieving things buried in the middle. Put the instruction that matters most at the very start or the very end. This is one of the highest-return prompting habits there is, and it costs nothing.

**Third, filling the window has real costs.** Long contexts are slower and more expensive — you are billed for input tokens, and every turn re-sends the whole conversation. A long chat gets progressively pricier per message even if your messages stay short. This is also why providers cache: **prompt caching** stores the unchanging front portion of a context so it doesn't have to be reprocessed, which is why a long-running session can suddenly get faster and cheaper after the first message.

## What happens when you run out

Different products handle overflow differently, and the choice matters more than most users realize:

- **Hard stop.** The API refuses the request. Blunt, but at least it's honest.
- **Truncation.** The oldest messages are silently dropped. This is the classic "why did it forget?" experience.
- **Summarization / compaction.** Older turns are compressed into a summary that stays in context. Better, but lossy — specifics become generalities, and the model can't recover a detail that got summarized away.

Most consumer chat products do some version of the last two, usually without telling you. So when an assistant "forgets," it typically hasn't malfunctioned. It has been shown a lossy summary of a conversation you remember in full — and it has no way of knowing what was in the part it lost.

## What this means for actually using these tools

A handful of practical consequences follow directly:

**Start a new conversation more often than feels natural.** A fresh chat with a clean, well-written setup message usually outperforms a sprawling one where your original instructions are twenty thousand tokens back — or gone. Long threads feel like accumulated understanding. Often they're accumulated noise.

**Restate what matters.** If a constraint is important ("keep responses under 200 words," "we decided against the Postgres option"), repeat it. You're not being redundant; you're keeping it inside the window.

**Front-load and back-load your instructions.** Documents in the middle, instructions at the edges.

**Don't treat a big window as a filing cabinet.** Pasting eight documents so the model "has everything" measurably degrades its performance on the one document that mattered. Relevance beats volume, consistently.

**Expect context limits to explain most complaints.** When someone says an AI tool "got worse over a long session," "ignored my instructions," or "contradicted itself," the context window is the first thing to check — usually before anything about the model itself.

## The part that's easy to miss

There is a genuine philosophical oddity buried in all this. The model doesn't experience a conversation as a continuous thing at all. Each turn, it receives a block of text and produces the next chunk. The sense of an ongoing relationship — that it *knows* you, that you're building something together — is constructed entirely out of text being re-fed to it every single time.

Which means the context window isn't a technical footnote about capacity. It's closer to the boundary of what the system is, at any given moment. Everything inside it exists for the model. Everything outside it does not.

That's worth keeping in mind the next time an AI assistant forgets something you told it. It didn't forget. It was never shown.

---

*New here? Start with our [plain-English glossary of the 15 AI terms in every headline](/ai-terms-in-headlines-explained/), or the [seven questions that cut through AI hype](/how-to-read-ai-news-without-the-hype/).*
