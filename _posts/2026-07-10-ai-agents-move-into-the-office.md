---
title: "OpenAI and Anthropic Are Now Racing to Be Your AI Coworker"
description: "ChatGPT Work and Claude Cowork's mobile launch land days apart. Anthropic's own usage data shows the fight isn't really about coding — it's about spreadsheets and reports."
tags: [news]
---

This week gave us a genuinely busy stretch of AI news: OpenAI shipped a new three-tier model family, xAI put Grok 4.5 in front of the public, and both OpenAI and Anthropic launched competing products aimed at the same target — turning their chatbots into something that does your job with you, not just answers your questions. The model releases will get most of the headlines, but the more interesting story is the coworker one, because the data behind it cuts against the industry's own favorite narrative.

## Two launches, three days apart

On July 7, [Anthropic expanded Claude Cowork](https://techcrunch.com/2026/07/07/the-coding-agent-wars-are-spilling-into-the-rest-of-the-office-claude-cowork/) from a desktop-only app (it launched in January) to mobile and web, starting in beta for Max subscribers. Cowork is built on the same idea as Claude Code — hand it a task and let it work autonomously — but aimed at general office work instead of programming. The pitch is that you can kick off a task on your laptop, let it run in the background while you're away, and check in from your phone once it's done.

Two days later, on July 9, [OpenAI launched ChatGPT Work](https://www.infoworld.com/article/4195478/openai-launches-chatgpt-work-as-it-broadens-gpt-5-6-rollout.html), a new agent built into ChatGPT for Pro, Enterprise, and Edu accounts (Plus and Business are getting it "in the coming days"). It's explicitly pitched as an AI coworker: pull context from Google Drive, Calendar, Slack, Outlook, SharePoint, and Gmail, then produce a finished report, spreadsheet, presentation, or even a built website. For organizations, it plugs into the same admin controls — spend limits, tool permissions, network access — that ChatGPT Enterprise already offers.

Same week, same pitch, same target customer. That's not a coincidence; it's two companies converging on the same bet at the same time because they're seeing the same signal in their own usage data.

## The bet: it's not about coding

Here's the part worth sitting with. Anthropic published its own breakdown of what people actually do with Cowork, and software development was the smallest category — just 8.7% of usage. The largest chunk, at 33.4%, was what Anthropic called "business process operating": pulling scattered updates into one report, building onboarding checklists, reconciling spreadsheets. The unglamorous, high-volume back-office work that every company has and nobody enjoys doing.

That matters because the public conversation about AI agents has been dominated by coding — Claude Code, Codex, Cursor, GitHub Copilot's agent modes. Coding is where agents got good first, in part because code has clear pass/fail feedback (does it compile, do the tests pass) that makes it an easier problem to train and evaluate against. But Anthropic's own numbers suggest that once you hand the same underlying agent a general "do this task across my tools" capability, most people don't point it at code. They point it at the reporting and reconciliation grind that eats hours out of finance, HR, and admin roles. That's a different economic story than "AI replaces programmers" — it's closer to "AI replaces the least interesting three hours of an analyst's Tuesday."

## The model underneath

Both products are riding on new model releases from the same week. OpenAI moved [GPT-5.6](https://www.marktechpost.com/2026/07/09/openai-releases-gpt-5-6-a-three-tier-model-family-with-programmatic-tool-calling/) to general availability as three separate models rather than one: Sol (flagship, $5/$30 per million input/output tokens), Terra (mid-tier, $2.50/$15, pitched as GPT-5.5-class performance at half the price), and Luna (cheapest, $1/$6, aimed at high-volume pipelines rather than one-off complex reasoning). Splitting a release into three price points instead of shipping one model is itself a signal — OpenAI is explicitly optimizing for the economics of running agents at scale, where most individual steps in a long task don't need frontier-level reasoning and paying frontier prices for every one of them adds up fast.

xAI's Grok 4.5, which went public on July 8, is competing in the same general-purpose space but currently ranks behind Fable 5, GPT-5.5, and Opus 4.8 on Artificial Analysis's Intelligence Index — a reminder that "just released" and "best available" aren't the same claim, however the launch post frames it.

## Why this is worth tracking, not just noting

None of this means office admin work is about to disappear. Early-innings agent products routinely overpromise — the coding-agent wars of the last two years produced plenty of demos that looked cleaner than the tools turned out to be in daily use, and "reconciling spreadsheets" covers a huge range of tasks from trivial to genuinely judgment-heavy. What's actually notable here is the shift in where two well-resourced labs are choosing to point their agents next, and the fact that Anthropic's own data undercuts the assumption that agentic AI is primarily a programmer's tool. If you want a grounding in the vocabulary this kind of coverage leans on — agent, context window, tool calling — [our explainer glossary](/ai-terms-in-headlines-explained/) covers the terms plainly. And if the pattern of "AI lab ships enterprise-facing agent product, promises time saved" feels familiar, it's worth applying the same read we gave [Chinese open-weight model adoption](/chinese-ai-models-us-enterprise-adoption/) last week: watch what people actually pay for and actually use, not what the launch post claims.

Sources:
- [TechCrunch: Claude Cowork expands to mobile and web](https://techcrunch.com/2026/07/07/the-coding-agent-wars-are-spilling-into-the-rest-of-the-office-claude-cowork/)
- [VentureBeat: Claude Cowork usage data](https://venturebeat.com/technology/anthropic-brings-claude-cowork-to-mobile-and-web-as-usage-data-shows-most-users-arent-coding)
- [InfoWorld: OpenAI launches ChatGPT Work](https://www.infoworld.com/article/4195478/openai-launches-chatgpt-work-as-it-broadens-gpt-5-6-rollout.html)
- [MarkTechPost: GPT-5.6 Sol, Terra, Luna](https://www.marktechpost.com/2026/07/09/openai-releases-gpt-5-6-a-three-tier-model-family-with-programmatic-tool-calling/)
