---
title: "Google Shuts Down Imagen 4 API Models Today"
description: "Google retires three Imagen 4 model IDs on August 17, 2026, pushing developers to gemini-3.1-flash-image with a different API and higher per-image cost."
tags: [news]
---

Google is turning off three Imagen 4 model IDs today, August 17, 2026: `imagen-4.0-generate-001`, `imagen-4.0-ultra-generate-001`, and `imagen-4.0-fast-generate-001`. Any application still calling these endpoints in the Gemini API will start failing. Google's own deprecations page lists today as the earliest possible shutdown date, and the replacement path is not a simple find-and-replace of a model name.

## What developers have to change

The recommended replacement is `gemini-3.1-flash-image`, but it does not sit behind the same method call. Imagen 4 used a dedicated `generate_images()` function. The new model runs through `generate_content()`, the same general-purpose call used for text and chat. That means teams cannot just swap a string constant. They have to rewrite the request shape, update response parsing, and retest anything downstream that expected the old output format.

The practical checklist for anyone still on Imagen 4 looks like this:

- Move image requests from `generate_images()` to `generate_content()`.
- Re-test prompt adherence, since a differently trained model will not always follow the same prompt the same way.
- Recheck aspect ratio handling and output resolution options.
- Confirm SynthID watermark behavior still matches compliance needs.
- Re-measure latency and quota limits under production load, not just a quick test call.

None of these are exotic problems, but each one takes real engineering time, and Google is giving developers a hard date rather than an open-ended window.

## The cost is going up, not down

The part of this migration that will surprise some teams is price. Imagen 4 generated images at roughly $0.02 to $0.06 per image depending on the tier. A 1,000-image batch on `gemini-3.1-flash-image` runs about $0.067 per image, noticeably more than even the higher end of the old Imagen 4 range. For a hobby project this is a rounding error. For a product generating thousands of images a day, it is a real line-item increase, and it lands at the same time as the forced code change, which leaves no gap to plan around.

This is a small but clear example of a pattern that shows up across the AI industry: new models often come with better benchmark scores, but "better" does not automatically mean "cheaper" or "drop-in compatible." Anyone treating an AI API like a stable utility, the way you'd treat a database connection, is going to be surprised at some point by a forced migration with cost implications attached.

## Why Google is doing this now

Google has been consolidating its image and video generation into the broader Gemini model family rather than keeping separate, narrowly scoped models like Imagen running in parallel. `gemini-3.1-flash-image` folds image generation into the same multimodal model that also handles text and, per Google's release notes, improves prompt following and detail accuracy over the Imagen 4 line. From Google's side, maintaining fewer, more capable general models is cheaper and simpler than keeping a family of single-purpose models alive indefinitely.

That consolidation logic is common across the industry right now. We covered a similar dynamic when [Claude Opus 5 launched at half the previous price](/claude-opus-5-launch-half-the-price/): labs are constantly trading off model count, capability, and cost, and today's frontier price or feature is not a stable target. The Imagen 4 shutdown is the same forcing function, just aimed at image generation instead of text.

## The broader lesson for anyone building on these APIs

Model deprecation notices are becoming a routine part of building AI products, not an edge case. If your product calls a foundation model API directly, you are implicitly agreeing to keep pace with that provider's release and retirement schedule, on their timeline, not yours. That is a different maintenance burden than most software dependencies, where a library can sit untouched for years without breaking.

Teams that want to reduce this risk have a few practical options: build a thin abstraction layer between your application code and the specific model API, so a model swap touches one file instead of a dozen call sites; subscribe to the provider's deprecation feed instead of finding out from a failed request in production; and budget migration time into your roadmap the same way you'd budget for a major library upgrade, because for Imagen 4 users, that bill is coming due today whether they planned for it or not.

None of this is unique to Google. Every major lab, including Anthropic and OpenAI, retires older model versions on a schedule, and the pattern will keep repeating as the pace of model releases stays fast. Understanding how these APIs are billed and versioned, which we've touched on before when explaining [how prompt caching works](/prompt-caching-explained/), is quietly becoming as important to shipping AI features as understanding the models themselves.

Sources:
- [Google Imagen 4 API shutdown window: August 17, 2026](https://kingy.ai/ai-launch-tracker/google-will-shut-down-three-imagen-4-api-models-august-17/)
- [Google Model Retirements: Gemini 2.5 Shutdown, Imagen 4 Dates, Vertex vs Gemini API](https://vorplabs.com/models/google-model-retirements)
- [Imagen 4 Shutdown August 17 — Migrate to Gemini Image API Now](https://byteiota.com/imagen-4-shutdown-august-17-migrate-to-gemini-image-api-now/)
- [Google Deprecates Imagen 4 and Veo Models in Gemini API](https://www.narracomm.com/google-deprecates-imagen-4-and-veo-models-in-gemini-api/)
