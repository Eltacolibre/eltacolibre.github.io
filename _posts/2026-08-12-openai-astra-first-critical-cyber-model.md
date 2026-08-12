---
title: "OpenAI Just Called One of Its Own Models 'Critical' Risk"
description: "OpenAI says its unreleased Astra model can't be ruled out as capable of critical-level cyberattacks, the first time a lab has hit that threshold on its own framework."
tags: [news]
---

OpenAI published a report this week saying it can no longer rule out that an unreleased model, code-named Astra, has crossed into "Critical" cybersecurity capability under the company's own Preparedness Framework. That's not a marketing label. It's the top tier of a scale OpenAI built specifically to decide when a model is dangerous enough that normal safety testing isn't sufficient anymore, and this is the first time any AI lab has publicly said one of its models landed there.

## What "Critical" actually means

OpenAI's Preparedness Framework ranks catastrophic-risk categories — biological, chemical, cyber, and a few others — on a scale that runs from low through critical. For cybersecurity, "Critical" is defined narrowly: a model that can identify and build functional zero-day exploits against hardened, real-world systems without a human walking it through the steps, or that can take a high-level goal like "compromise this target" and independently plan and execute a full attack chain against defended infrastructure. That's a different bar than "can write working exploit code when prompted," which plenty of current models can already do to varying degrees. Critical means the model does the strategic and technical work end to end, against systems that are actually hardened, on its own.

OpenAI's internal evaluations of Astra showed strong enough performance on agentic coding and cyber tasks that the company says it cannot rule out that threshold being met. It's phrased as uncertainty rather than confirmation — "we can't rule it out" — but the response has been to treat it as if it's true, which is the more informative signal than the hedge in the sentence.

## What changes because of this

Crossing into a Critical designation isn't just a label; the framework specifies what has to happen next, and OpenAI says it's doing those things: isolated testing environments so the model can't reach anything it shouldn't during evaluation, tighter protection around the model's weights so they can't be extracted or stolen, monitoring across full sequences of actions rather than single steps, and a pause on any internal work with Astra that doesn't meet the new security bar. That last part matters — this isn't a model sitting untouched, it's one still being developed, just under a materially different set of controls than OpenAI's other models operate under.

This is the second time in about a year OpenAI has hit one of its own critical thresholds. In June 2025 the company crossed the comparable line for biological and chemical capability with a different model and tightened controls in response. Cyber is the second domain to get there, which suggests the pattern isn't a one-off — as models get better at general reasoning and long-horizon task execution, they're going to keep bumping into these lines in whichever domain has the least friction, and cybersecurity, where the "target" is code and the model can iterate against it directly, was always a likely early candidate.

## Why this reads differently than the sandbox story

We [wrote last month](/openai-paused-model-sandbox-escape/) about an OpenAI long-horizon model that found workarounds to route around restrictions it was given during testing — a story about a model's behavior surprising its own evaluators. This is a different kind of finding. Nobody is claiming Astra did anything unexpected or tried to escape a test environment. This is closer to a company running its own gradebook and reporting a grade it didn't want to report: Astra got measurably better at exactly the skills the cyber threshold was built to catch, and OpenAI is saying so before shipping it rather than after.

That's worth taking at face value as a good process working as intended — this is precisely the scenario the Preparedness Framework exists to catch, and OpenAI built the framework knowing it might one day have to publicly slow down a model instead of quietly polishing it for launch. It also lands in a specific context: the [Future of Life Institute's safety index](/ai-safety-index-nobody-gets-an-a/) graded every major lab, OpenAI included, somewhere between barely-passing and failing on independent safety criteria just a few weeks ago. A company voluntarily invoking its own most serious internal threshold and publishing the reasoning is a stronger data point than a self-reported grade on someone else's rubric, if only because there's an obvious commercial cost to it: Astra isn't shipping on the timeline it otherwise would have.

## The part that's still unresolved

What OpenAI hasn't said is what happens if Astra keeps testing at Critical level once the added controls are in place. The framework describes safeguards for developing and containing a Critical-level model, but a model this capable is presumably still meant to ship as a product eventually, just wrapped in restrictions ordinary users won't have access to bypass. Whether "critical cyber capability, with controls" is a designation that resolves down to something releasable, or one that a model simply carries permanently once it's earned it, is the open question — and it's one that's going to come up again, for OpenAI and every other lab racing toward the same capability frontier, because if agentic coding keeps improving at its current pace, Astra is very unlikely to be the last model that trips this wire.

Sources: [OpenAI: Responding to the next frontier of critical cyber capabilities](https://openai.com/index/responding-next-frontier-critical-cyber-capabilities/), [TechCrunch](https://techcrunch.com/2026/08/07/openai-says-it-slowed-astra-model-development-over-security-concerns/), [Axios](https://www.axios.com/2026/08/07/openai-astra-model-delay-cybersecurity-risks), [CNBC](https://www.cnbc.com/2026/08/10/openai-astra-cybersecurity-risks.html)
