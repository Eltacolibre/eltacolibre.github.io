---
title: "Why Anthropic Won't Sign the Open-Weight AI Letter"
description: "25+ companies signed a letter opposing AI restrictions after China's Kimi K3 was accused of copying Anthropic's model. Anthropic itself didn't sign. Here's why."
tags: [news]
---

Over the past week, a fight has been playing out in Washington over how the US should respond to Chinese AI models, and the most interesting thing about it isn't the policy fight itself. It's who's missing from one side of it.

## How we got here

On July 21, Treasury Secretary Scott Bessent said the US has "the ability to sanction" Chinese AI companies over what he called IP theft. The next day, White House AI adviser Michael Kratsios named names: he said Moonshot AI's Kimi K3, the 2.8-trillion-parameter open-weight model [we covered when it launched](https://eltacolibre.github.io/kimi-k3-open-weight-model-explained/), was built by distilling Anthropic's Claude models. Distillation, in this context, means training a smaller model on the outputs of a bigger one — effectively using a rival's model as a free teacher instead of building your own training data from scratch. If true, it would mean K3's benchmark-beating performance was partly borrowed rather than earned.

Kratsios's claim hasn't been independently verified — Moonshot denies it, and "distillation" is genuinely hard to prove from the outside, since a model trained partly on another model's outputs looks similar to one that just learned similar patterns from similar data. But the accusation was enough to put a very specific question on the table in Washington: should the US restrict access to open-weight models, or crack down on the distillation techniques that let anyone fine-tune off a stronger model's outputs?

## The industry's answer, mostly

On July 24, a coalition of 25 companies led by Nvidia and Microsoft published an open letter arguing against broad restrictions. The list included Meta, IBM, Palantir, Hugging Face, Mozilla, the Linux Foundation, Dell, CrowdStrike, ServiceNow, Perplexity, Mistral, and Andreessen Horowitz. Their argument: open-weight models — ones where anyone can download the parameters and run them locally — are a genuine public good, used far beyond any single bad actor, and sweeping rules aimed at stopping one alleged theft would end up choking off a whole ecosystem of legitimate research and product-building. They asked for "targeted legal and commercial frameworks" instead of blanket bans on distillation as a technique.

By July 26 the signatory list had roughly doubled to 50, and OpenAI's name had quietly appeared on it — added after commentators on social media pointed out it wasn't there at launch, with Sam Altman reposting supportive commentary on open-source AI shortly after. Google and Amazon still hadn't signed as of this writing.

Neither had Anthropic. Which is the strange part, because Anthropic is the company that's supposedly the victim here.

## Why the alleged victim isn't defending open weights

Dario Amodei addressed it directly in a CNBC interview on July 27: Anthropic is not pushing for a ban on open-weight models, he said, and does support targeted testing and safeguards over broad restrictions — which sounds close to what the letter asks for. But he's also been consistent for months that he doesn't think "open source" is the right frame for this technology at all. In his words, it's "a red herring": traditional open-source software lets you read the actual source code, but an open-weight AI model just gives you a giant file of numbers you can run — you still can't see how it works inside, and the "many hands make the work better" logic that made open source valuable for software doesn't transfer cleanly to model weights. Anthropic's preferred alternative is closer to controlled access: its Project Glasswing program gives vetted security researchers early use of its models to find flaws, without publishing weights for anyone to download.

That philosophical stance means Anthropic can't easily co-sign a letter built around defending open weights as a category, even when doing so might look self-serving given it's the company that says it was copied. It's a case where being the injured party and being an ideological match with the people rallying around you turn out to be two different things.

## Why this matters beyond the letter

Step back from the specific fight, and the letter's signatory list is basically a map of who currently benefits from open-weight distribution. Nvidia sells more chips to more people who deploy their own models; Meta's whole strategy runs on Llama being open; Hugging Face's entire business is hosting downloadable weights; Microsoft and IBM sell services around a wider ecosystem of models companies can run themselves. None of that changes because one Chinese model may have been trained on borrowed Anthropic outputs. Anthropic, by contrast, sells access to its own closed models and has argued since [before the China alliance story](https://eltacolibre.github.io/china-waico-ai-alliance-without-us/) that the safety case for keeping frontier weights closed is separate from any single country's behavior.

What happens next is genuinely unclear. Congress hasn't proposed specific legislation yet, and Bessent's sanctions talk is still just talk. But the letter is a useful marker for how this debate will likely keep splitting: not cleanly along "US vs. China" lines, but along whether a company's business model depends on models staying open or staying closed — with the theft allegation as the occasion, not really the cause, of where everyone lined up.

Sources: [TechCrunch](https://techcrunch.com/2026/07/24/as-us-weighs-response-to-chinese-ai-industry-urges-against-broad-open-weight-restrictions/), [TechCrunch on the distillation claim](https://techcrunch.com/2026/07/22/treasury-threatens-sanctions-after-white-house-claims-moonshot-distilled-anthropics-fable/), [CNBC on Bessent](https://www.cnbc.com/2026/07/21/bessent-china-ai-sanctions.html), [CNBC on Amodei](https://www.cnbc.com/2026/07/27/anthropic-ceo-dario-amodei-isnt-advocating-open-weight-model-ban.html), [Forbes on signatory count](https://www.forbes.com/sites/sandycarter/2026/07/25/huangs-open-weights-letter-doubled-to-50-without-amazon-and-anthropic/), [The Register](https://www.theregister.com/ai-and-ml/2026/07/23/senior-white-house-official-claims-chinas-k3-model-stolen-from-anthropic/5276804/).
