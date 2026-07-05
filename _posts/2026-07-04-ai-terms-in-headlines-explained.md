---
title: "15 AI Terms You Keep Seeing in Headlines, Explained in Plain English"
description: "LLM, context window, RAG, hallucination, open weights — a no-jargon glossary of the AI vocabulary that shows up in every news story, so you can read past the buzzwords."
tags: [explainers]
---

Every AI news story leans on the same handful of terms, and most of them are never defined. Here is the vocabulary you actually need, explained the way you'd explain it to a smart friend — no math, no marketing.

## 1. Large language model (LLM)

A program trained on enormous amounts of text to predict what words come next. That one trick — predict the next word, at massive scale — turns out to produce systems that can write, summarize, translate, and reason through problems. ChatGPT, Claude, and Gemini are all built on LLMs.

## 2. Parameters

The internal dials the model tuned during training — billions of numbers that encode everything it "knows." Headlines use parameter counts as a shorthand for size ("a 70B model"), but bigger is not automatically better. Training data quality and technique matter as much as raw size.

## 3. Tokens

The chunks a model actually reads and writes. A token is usually a word fragment: "unbelievable" might be three tokens. Pricing, speed, and limits are all measured in tokens, which is why the word appears in every product announcement.

## 4. Context window

How much text a model can consider at once — its working memory. A bigger context window means the model can read whole books or codebases in one go. When a model "forgets" the start of a long conversation, it has run out of context window. (Yes, this site is named after it.)

## 5. Inference

Running the model to get an answer, as opposed to training it. Training happens once and costs a fortune; inference happens every time you ask a question. When companies talk about "inference costs," they mean the ongoing bill for serving users.

## 6. Fine-tuning

Taking a trained model and giving it extra training on a narrow dataset — a company's support tickets, legal documents, medical notes — so it gets better at one specific job.

## 7. RAG (retrieval-augmented generation)

Instead of relying only on what the model memorized during training, the system first *looks things up* — in a database, a document store, the web — and hands the results to the model to answer with. It's the standard fix for models that need current or private information.

## 8. Hallucination

When a model states something false with total confidence — an invented citation, a fake court case, a wrong date. It's not lying (there's no intent); it's the next-word predictor producing plausible-sounding text that happens to be untrue. Every model does it; the question is how often.

## 9. Multimodal

A model that handles more than text: images, audio, video, or all of them. "Multimodal" is why you can now show a chatbot a photo of your fridge and ask what to cook.

## 10. Agents

AI systems that don't just answer — they *act*: browsing, clicking, writing files, calling other software, working through multi-step tasks with limited supervision. Most of the current industry buzz (and much of the risk debate) is about agents.

## 11. AGI (artificial general intelligence)

The hypothetical point where AI matches or exceeds humans at most economically valuable work. There is no agreed definition, which is exactly why the term generates so many headlines — anyone can claim we're close or far, and no one can be proven wrong.

## 12. Alignment

The research problem of making AI systems reliably do what humans intend — and not do what we don't. It spans everything from "don't help build weapons" to deep questions about controlling systems smarter than their operators.

## 13. Open weights

When a company releases the trained model itself (the parameters) for anyone to download and run. Often mislabeled "open source" — true open source would also include the training data and code, which almost nobody releases. Open weights is why powerful models now run on ordinary laptops.

## 14. Benchmark

A standardized test used to score models — math problems, coding challenges, exam questions. Benchmarks make headlines ("model X beats model Y"), but they're gameable: models can be trained on material similar to the test. Treat benchmark wins as a claim, not a verdict.

## 15. Compute

Shorthand for the raw processing power — mostly specialized chips like GPUs — needed to train and run models. When you read about export controls, billion-dollar data centers, or chip shortages, that's the compute story. It's the physical bottleneck under the entire industry.

---

**The pattern to notice:** most AI headlines are really about one of three things — capability (what models can do), compute (who has the hardware), or control (alignment, policy, safety). Once you can sort a story into one of those buckets and translate its jargon, you're reading AI news, not being read to.

*Next up: [a practical filter for reading AI news without getting played](/how-to-read-ai-news-without-the-hype/).*
