---
title: "Google's $12.2B Marvell Deal Cracks Open the TPU Supply Chain"
description: "Google can now buy up to $12.2B of Marvell stock, vesting as it buys custom chips for its TPUs — a financing structure that dents Broadcom's near-monopoly."
tags: [news]
---

Marvell Technology disclosed on August 19 that it has given Google the right to buy up to $12.2 billion of Marvell stock — nearly 59 million shares at $206.58 each, close to 7% of the company. Marvell's stock jumped almost 8% on the news. Broadcom, which has been Google's main TPU chip-design partner, fell more than 5% the same day. Neither move is an accident: this deal is Google buying its way into a second major supplier for the chips that make its custom AI processors work.

## What was actually signed

The two companies struck a commercial agreement on July 29, made public through an SEC filing three weeks later. It's not one big chip order — it's a warrant, a financial instrument that gives Google the option to buy Marvell shares over time, but only as it actually pays Marvell for chips. The mechanics: an initial batch of about 1.36 million shares vests quarterly over the first year regardless, and after that, roughly 240,000 more shares vest every time Google's cumulative purchases from Marvell cross another $500 million. Do that 240 times and Google would own the whole $12.2 billion stake, tied to $120 billion of chip spending running through fiscal 2033.

The chips themselves aren't the TPU's main processing die — Google still designs and sources that core piece separately. What Marvell is building is everything that "attaches" to it: inference accelerators, storage controllers, network interface chips, memory interface controllers, and near-memory compute. Analysts at Futurum Group describe it as Marvell taking over the supporting cast around the TPU rather than the lead role.

## Why a stock warrant instead of just a purchase order

Nvidia has been doing something structurally similar all month — we covered its [$500 billion Wall Street financing platforms](https://eltacolibre.github.io/nvidia-500-billion-wall-street-ai-financing/) earlier in August, where outside asset managers front the capital for AI infrastructure instead of it sitting on one company's balance sheet. The Google-Marvell warrant runs the same logic in the other direction: instead of a supplier financing its customer, the customer is taking equity exposure to its supplier, paid for in the very purchases that make the supplier more valuable.

For Google, the appeal is that the discount effectively grows with scale. Morningstar analyst William Kerwin described it as building in an "effective rebate" on each $500 million tranche of purchases, one that gets richer if Marvell's stock price rises — meaning Google's own buying, if it helps validate Marvell as a serious AI supplier, feeds back into a cheaper effective price on the chips it just bought. For Marvell, it converts what would otherwise be modeled revenue guidance that analysts have to take on faith into contractually disclosed, quarter-by-quarter proof that the orders are real.

## What it means for Broadcom

Broadcom isn't being replaced. Its contract to design Google's core TPU compute die reportedly runs through 2031, and Kerwin's read — echoed by Futurum's analysts — is that this is Google growing the number of vendors it buys from, not swapping one out for another. But it does end the arrangement where Broadcom was effectively the only company Google trusted with TPU-adjacent silicon. Marvell already had components built for Amazon's Trainium chips and Microsoft's Maia chips; Futurum notes this deal makes Marvell the only merchant chip designer with signed programs across all three hyperscalers' custom silicon efforts. MediaTek is reportedly also picking up cost-optimized variants in the same ecosystem. The result looks less like a single dominant TPU supply chain and more like a disaggregated one, with different vendors owning different slices.

## Why this matters beyond one stock move

Custom AI silicon — chips hyperscalers design themselves rather than buying off-the-shelf GPUs — has been pitched as the industry's way of controlling AI inference costs long-term, since a chip built for one company's specific workloads can be cheaper to run at scale than a general-purpose GPU. Google, Amazon, and Microsoft are all deep into their own custom-chip programs for exactly that reason. What this deal shows is that even inside "custom silicon," no hyperscaler is building the whole stack alone. Google still needs outside partners for packaging, memory interfaces, and networking silicon, and it's now paying for that access with equity stakes rather than pure cash, tying its supplier's fortunes to its own chip demand more tightly than an ordinary purchase order would.

Whether that's a durable model or a one-off is worth watching. If it works, expect more of these warrant-for-volume structures showing up across the AI hardware supply chain — a quieter, more targeted cousin of the massive financing platforms Nvidia has been assembling with Wall Street this month.

Sources: [CNBC via Yahoo Finance](https://finance.yahoo.com/technology/articles/marvell-grants-google-12-2-123812695.html), [Futurum Group](https://futurumgroup.com/insights/marvell-attaches-across-googles-tpu-stack-with-a-warrant-vesting-toward-120b/), [Bloomberg](https://www.bloomberg.com/news/articles/2026-08-19/marvell-gives-google-right-to-buy-up-to-12-2-billion-in-shares), [TrendForce](https://www.trendforce.com/news/2026/08/20/news-marvell-amd-reportedly-shake-up-google-tpu-race-putting-broadcom-mediatek-under-pressure/).
