---
title: "Claude Opus 5 Launches at Half the Price of Anthropic's Own Flagship"
description: "Anthropic's new Opus 5 claims frontier-level coding and agent performance without the price hike, undercutting even its own top model, Fable 5."
tags: [news]
---

Anthropic shipped Claude Opus 5 on July 24, and the headline isn't really the model's capabilities — it's the price tag attached to them. Opus 5 costs $5 per million input tokens and $25 per million output tokens, the exact same rate as its predecessor, Opus 4.8. That's half of what Anthropic charges for Fable 5, the company's actual top-of-the-line model released back in June. Anthropic is, in effect, telling the market that its second-tier model now does most of what the flagship does, for half the money.

## What changed

Opus 5 rolled out immediately across every Anthropic surface — Claude.ai, the API, Claude Code, Claude Cowork, and both the Pro and Max subscription tiers, where it's now the default model. There's also a "fast mode" option that runs about 2.5 times quicker at double the base price, aimed at latency-sensitive coding and agent workloads where waiting on a response is the actual bottleneck, not the cost per token.

The performance claims center on a few areas. On Frontier-Bench v0.1, an evaluation that tests whether a model can turn engineering specifications into working software, Opus 5 reportedly scored 43.3%, more than double Opus 4.8's result and ahead of Fable 5's 33.7%. On ARC-AGI 3, a benchmark designed to resist memorization and test genuine novel problem-solving, Anthropic says Opus 5 scores roughly three times higher than the next-best competing model. On OSWorld 2.0, which measures how well a model can operate a real computer — clicking, typing, navigating software the way a person would — Opus 5 reportedly leads the field at around a third of Fable 5's cost per task.

Third-party reactions, for what they're worth, lean toward corroborating the "cheaper but almost as good" framing rather than the "outright better" one. Devin's CEO described it as approaching Fable-level performance at half the cost; Cursor's co-founder used almost identical language. Zapier's CEO said it topped their AutomationBench without burning more tokens per run. None of these are neutral parties — they're partners with products built on Anthropic's API — but the consistency of the message across separate companies is at least suggestive that the price-to-performance ratio is the real story, not a marketing framing layered on top of an ordinary upgrade.

## Reading the benchmark claims skeptically

A few caveats are worth keeping in mind before taking any of this at face value. First, essentially all of these numbers come from Anthropic itself or from companies with a commercial relationship to Anthropic. Independent, apples-to-apples third-party benchmarking of Opus 5 against Fable 5 and competing models from other labs hadn't caught up to the launch at time of writing, which is normal — it takes days to weeks for outside evaluators to run their own numbers — but it means the "half the cost, nearly the same quality" narrative is currently coming almost entirely from the company that benefits from you believing it.

Second, benchmark scores like Frontier-Bench and ARC-AGI 3 measure specific, narrow capabilities under specific test conditions. A model that doubles its predecessor's score on a coding-from-specs benchmark is not the same as a model that is twice as good at software engineering in general. These evaluations are useful signals, not full pictures, and progress on them doesn't necessarily transfer evenly to the kind of messy, underspecified work most people actually do with these tools.

Third, Anthropic's own writeup notes that Opus 5 remains behind an internal model called Mythos 5 specifically on cybersecurity exploitation tasks — a detail worth noting mainly because it's an unprompted admission of a weakness inside a launch announcement that is otherwise all upside. That kind of disclosure is a decent sign of at least some restraint in how the results are being presented, even if it doesn't tell you much on its own.

## The alignment angle

Anthropic also reported that Opus 5 posted its lowest score yet on the company's automated behavioral audit — a measure of "misaligned behavior" like deception or rule circumvention — beating out Opus 4.8, Sonnet 5, and Fable 5. That claim is worth reading alongside [our earlier coverage of the Future of Life Institute's AI safety index](/ai-safety-index-nobody-gets-an-a/), where every major lab, Anthropic included, scored somewhere between weak and failing on independent safety grading. An internal audit showing improvement over your own prior models is a real data point, but it's not the same thing as an outside body confirming the model is safe by some external standard. Anthropic grading Anthropic is useful information; it isn't independent verification.

## Why the pricing move matters more than the specs

The more interesting business story here is what this does to the rest of the market. Anthropic now has four models released in roughly two months — a cadence that would have been unusual even a year ago — and each release seems designed to compress the price-performance curve rather than just push the ceiling higher. That's a different competitive strategy than chasing the biggest possible benchmark number: it's an attempt to make the "good enough" tier cheap enough that fewer customers feel a need to reach for the most expensive option at all. Whether that holds up depends on how Opus 5 performs in the messier, non-benchmark reality of actual coding agents, customer support bots, and research assistants over the coming weeks — the kind of real-world testing that, unlike a launch-day benchmark chart, nobody controls the framing of.

Sources: [Anthropic](https://www.anthropic.com/news/claude-opus-5), [VentureBeat](https://venturebeat.com/orchestration/anthropic-launches-claude-opus-5-a-cheaper-ai-model-for-coding-agents-and-enterprise-workflows), [MarkTechPost](https://www.marktechpost.com/2026/07/24/meet-the-new-claude-opus-5-frontier-class-agentic-coding-and-computer-use-at-unchanged-opus-pricing/)
