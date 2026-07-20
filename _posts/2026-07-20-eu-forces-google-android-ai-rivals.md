---
title: "The EU Just Told Google: Share Android and Search With AI Rivals"
description: "The European Commission ordered Google to open Android's AI features and share search data with competitors under the DMA. Here's what changes, and when."
tags: [news]
---

On July 16, 2026, the European Commission handed Google two binding orders under the Digital Markets Act, and together they aim at the two things Google has leaned on hardest to keep its Gemini assistant ahead of the pack: privileged access to Android itself, and the mountain of search data nobody else gets to see at Google's scale.

Neither order is a fine. They're specification measures — the Commission telling a designated "gatekeeper" exactly how it must change its product to comply with a law it's already found in violation of the spirit of. That distinction matters, because it means this isn't a one-time penalty Google can absorb and move past. It's an operational rewrite of how Android and Search are allowed to work in the EU going forward.

## What actually changes

The first order targets Android. Right now, if you have a Pixel or Samsung phone, "Hey Google" gets system-level treatment that a rival assistant — say, one built on ChatGPT or Perplexity — simply doesn't get. Under the new rules, users will be able to trigger a third-party AI assistant by voice the same way they trigger Google's own, let that assistant act inside other apps on their behalf (book a taxi, draft a reply in a chat app, look up a place you just visited), and have it work with the same depth of access Gemini currently gets by default. Google has to make this available starting July 2027.

The second order hits Search. Competing search engines and AI chatbots with search features will be entitled to anonymized data drawn from the same signals Google uses to keep improving its own results — the kind of data advantage that's arguably done more to keep Google's search quality ahead of challengers than any single algorithm change. That sharing is scheduled to start in January 2027.

Both timelines give Google roughly six months to a year of runway, which is either a reasonable compliance window or a long time for a company with every incentive to slow-walk implementation, depending on how charitably you read Google's track record with prior DMA orders.

## Google's objection isn't unreasonable on its face

Google's response, delivered through general counsel Kent Walker, was blunt: "Today's decisions risk undermining vital privacy and security guardrails for millions of Europeans." The company argues it offered alternative compliance paths that would have protected users without the level of access the Commission ultimately mandated, and that opening system-level Android permissions to outside apps bypasses hardware-level vetting that device makers normally control.

That's not pure spin. Deep OS-level access for third-party AI assistants is a real attack surface — an assistant with permission to act inside your banking app or read your messages to draft replies is exactly the kind of capability that, done carelessly, turns into a privacy incident. The Commission's order does include stated safeguards, but "safeguards" is doing a lot of work in a press release, and the actual technical spec is what will determine whether this is manageable or a mess.

At the same time, "security" has been the standard first line of defense every gatekeeper platform reaches for when a regulator tries to open a moat — Apple made a nearly identical argument about sideloading before the DMA forced its hand there too. Google's specific complaints deserve to be evaluated on the merits, but the pattern of the objection is not new, and it's worth noticing that the underlying business problem for Google is the same for either objection: whether the security argument survives scrutiny or not, this order chips away at exactly the two advantages — being the default assistant on the world's dominant mobile OS, and holding a search-data monopoly no competitor can independently rebuild — that made Gemini's position on Android close to unassailable.

## Why this is bigger than one product

Assistant switching costs have always been artificially high partly because of exactly this kind of default-and-access asymmetry. If a rival assistant can genuinely act inside your apps the way Gemini can, "just use a different assistant" stops being a hypothetical and starts being a real option for hundreds of millions of Android users in the EU. Search data sharing is the slower-burning change, but arguably the more structural one: search quality compounds on scale of usage data, and that's been close to impossible for anyone but Google to replicate organically.

It's also a useful data point on how differently the US, EU, and China are approaching AI governance right now. We wrote last week about [China assembling 29 countries into a new AI cooperation body outside Western frameworks](/china-waico-ai-alliance-without-us/) — a governance model built around cooperation and state coordination. The EU's approach here is the opposite instinct: force interoperability and break up data advantages through binding, product-specific mandates, the same playbook it's used on Apple's App Store and iMessage. Both are bets about what actually produces a healthy AI market. Neither has fully proven out yet.

## What to watch

The real test isn't the order itself, it's the implementation. Watch whether Google's actual technical specification, due before the July 2027 deadline, matches the spirit of "equal access" or arrives narrowed by exactly the kind of safeguards Google is currently arguing for. Watch whether any AI assistant maker — OpenAI, Perplexity, Microsoft — actually ships something that uses this access meaningfully, since a right to interoperate is worthless if nobody builds against it. And watch whether the Commission opens a nonconformance case if Google's rollout falls short, which is exactly what happened with several of Apple's earlier DMA compliance attempts.

Sources: [European Commission — Digital Markets Act](https://digital-markets-act.ec.europa.eu/commission-provides-guidance-google-ai-interoperability-android-and-sharing-google-search-data-under-2026-07-16_en), [Unite.AI](https://www.unite.ai/eu-compels-google-to-share-android-and-search-data-with-rival-ai-assistants/), [Tech Times](https://www.techtimes.com/articles/320760/20260716/eu-gives-rival-ai-assistants-system-level-android-access-google-reserved-gemini.htm), [MediaNama](https://www.medianama.com/2026/07/223-eu-orders-google-open-android-search-data-ai-rivals/), [Android Authority](https://www.androidauthority.com/eu-android-ai-google-search-mandates-3688186/)
