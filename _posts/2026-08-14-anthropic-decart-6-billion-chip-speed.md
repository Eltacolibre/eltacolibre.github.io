---
title: "Anthropic's $6 Billion Bet on Faster Chips, Not Better Video"
description: "Anthropic is reportedly in talks to buy Decart AI for about $6 billion, its largest deal yet, mainly for software that makes AI chips run faster."
tags: [news]
---

Anthropic is in talks to acquire Decart AI, an Israeli startup, for around $6 billion, according to a Bloomberg report on August 13. If the deal closes, it would be Anthropic's largest acquisition to date. Multiple outlets, including Fortune and TechRepublic, confirm the broad terms, though the talks are still early and could still fall through.

Decart is best known to the public for Lucy, a model that edits live video streams in real time, and for Oasis, a model that generates simulated environments for training robotics and self-driving systems. Those products explain the headlines, but they are not the main reason Anthropic wants the company.

## The real prize is a speed trick, not a video model

The part of Decart that matters most to Anthropic is a piece of software called the Decart Optimization Stack, or DOS. DOS is an inference and training optimizer that, by industry estimates, lets AI models run up to eight times faster on the same hardware. It works across Nvidia GPUs, Google's TPUs, and Amazon's Trainium chips, so it is not locked to one supplier.

That hardware-agnostic design is the point. Anthropic runs Claude across a mix of chip types already, and a tool that squeezes more throughput out of whichever chips it has on hand is worth more to Anthropic than a single flashy consumer app. If Decart's team joins Anthropic's inference and performance organization, as reported, the acquisition reads less like a product purchase and more like a hire of an entire engineering team plus its best tool.

## Why Anthropic needs this now

Anthropic has spent 2026 racing to secure enough computing capacity to keep up with demand for Claude. In May, the company closed a $65 billion funding round at a $965 billion valuation, with chipmakers Micron, Samsung, and SK hynix among the investors. In August, Anthropic confirmed it is building its own custom AI inference chips, with Samsung reported as a manufacturing partner. Earlier this month, we covered how Anthropic set up [Theseus Infrastructure](/anthropic-theseus-data-center-joint-venture/), a joint venture with Macquarie and Singapore's GIC that lets outside investors build and own the data centers while Anthropic signs on as the long-term tenant.

Theseus and the Decart talks are two different answers to the same problem: there is not enough AI computing capacity in the world, and building more of it is slow and expensive. Theseus adds capacity by getting someone else to finance new buildings. Decart, if the deal closes, would let Anthropic pull more performance out of the chips it already has, whether those chips sit in a Theseus-financed data center or anywhere else. One lever is about renting more space; the other is about using each square foot better.

## The context this deal doesn't erase

The interest in efficiency software is not unique to Anthropic. Every major AI lab is confronting the same math: demand for AI inference is growing faster than the supply of advanced chips, and Nvidia GPUs remain the most expensive line item on most labs' budgets. A tool that reliably delivers a multiple of extra throughput on existing hardware is, in effect, free compute. That is why reports put a $6 billion price tag on a three-year-old startup whose consumer products, while interesting, do not obviously justify that number on their own.

It is also worth noting what is still unconfirmed. Neither Anthropic nor Decart has made an official announcement, and the reported terms come from people described as familiar with the discussions rather than a signed agreement. Deal talks at this stage change or collapse regularly, and the $6 billion figure could move before anything is finalized. We will treat this as a developing story rather than a done deal.

## What it would mean if it closes

For Anthropic, a completed deal would mean owning both a compute-optimization stack and the team that built it, rather than licensing similar technology from a third party or building an equivalent in-house from scratch. For Claude's users, the practical effect of better inference efficiency, if it materializes at the scale claimed, would likely show up indirectly: lower per-token costs that Anthropic can pass through as pricing changes, or faster response times at the same cost. Neither is guaranteed. Efficiency claims made before an acquisition closes have a way of shrinking once they meet production workloads at scale.

The bigger signal is about where AI labs think the next competitive advantage lives. A year ago, the story was mostly about who could sign the biggest chip supply deals. Now labs are also paying billions for the software that decides how much value they extract from each chip they already have.
