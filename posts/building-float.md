---
title: "Building float"
date: "2026-05-05"
tags: ["float", "codex", "development"]
readTime: "5 min read"
summary: "How float is being built as a testbed for agentic development, and what that changes about iteration speed and architecture work."
status: "scheduled"
---

## float's goals

float is intended, first and foremost, to be a testbed for agentic development. This comes with the caveat that any goals I set will (and have, many times) adjust with the course of AI & open source development. The long-shot goal is to create an independent, DIY Artificial General Intelligence (AGI) that shapes itself to the needs of its given workspace, deliberately scoped to an achievable program. AGI is not well defined or agreed upon as of yet - and I am taking advantage of that ambiguity here - for some this means running a business, others require physical intelligence, others might only care about intelligence and not agency. In order to have a concrete target, I set my working definition as:

- Persistence (not just an ephemeral response)
- Agency (ability to affect its environment)
- Ability to learn (memory and training)
- Perception (ability to observe itself and its environment)

What has landed so far is best described as a personal knowledge agent, with simple API tools and filesystem-based workspaces. I don't expect to out-scale any large organizations, but I see the path to AGI less as a race that one person wins and more like a labyrinth we are navigating together. For float specifically, this means something that you can live and work with, that can exist passively or actively and does not demand all of your attention. The initial intent was simply an autonomous workspace, but I realized it could be generalized just as easily: treat float as an exo-cortex, a personal journalist, a space to test models, or a project to build off (float is open-sourced under the AGPL license, please share anything you make based on it).

## Before agents

float, as it exists, has been constructed almost entirely alongside Codex, from the early CLI tools to highly structured spec-driven design with parallel GPT5.5 agents. My early days working with LLMs towards the nebulous goal of "local AGI" came long before Codex - I have fond memories of the comically doomed AutoGPT, quantized Llama leaks, and using Huggingface endpoints to wrap my head around API conversations. One of my first glimpses of agency happened by accident: by editing a message in LMstudio, removing the stop token, adding a `<user>` token, then simply asking it to continue, it spooled off into strange corners of its latent space. Functionally, I believe this was closer to accidentally distilling Llama than any kind of agency or real intelligence, but I quickly learned two things:

1. tinkering with these tools can lead to emergent behaviour, seemingly from nowhere
2. predicting the next token gets a *lot* more interesting when your tokens include more than just text

A few months later, CLI agents started being published, and I was quick to try them out. Actual structure started to be introduced in two lanes: actual inference tools like [Smolagents](https://github.com/huggingface/smolagents) and [openai-realtime-agents](https://github.com/openai/openai-realtime-agents) were central to my early prototypes; Codex CLI, Zed, and Cursor were my preferred tools to build with. By now, float has been built almost entirely with Codex, with blind feedback from Claude and Gemini when something gets stuck.

## Staying focused

Vibe-coding has caught on for a good reason, it's a ton of fun to throw a few lines into Codex and get a workable prototype, but if you want a consistent program, you need production-grade code. Specification-driven development and observability-based evaluation have been absolutely essential to getting float to a presentable state. There are descriptions available for the implemented and planned in the float repo's docs folder; in addition to this I've been using internal markdown files for issue tracking, QA, agent work logs, and to-do lists. float is an ambitious project by design, which has scaled well as the tools have gotten better, but this means that there is a LOT to keep track of, check, and build. Development is still largely vibes-first since everything is made from scratch, but I go through cycles of expansion and contraction, cleaning as I go.

## Building with Codex

Recent tools like [Codex skills](https://github.com/CherryResearch/float-codex-skills) enable a much tighter dev loop: troubleshooting, logs, live testing, managing servers, verifying sync, and evaluations can happen *inside* of the coding agent. Supervision is still very important - I have found that the most important improvements have not been to just raw intelligence but the integrations. Shorter feedback loops mean improvements happen faster, bugs get caught quicker, and the next feature gets attention sooner, which has been compounding so quickly that I am back to the same unapproachable chaos as before.

## What next?

float has been open-sourced, not just to give users agency, but in hopes of getting even more feedback so that float can be as excellent as possible. I have begun experimenting with work on fine-tuning, reinforcement learning and evaluating models and tool-call pipelines to fully realize the vision of a local-first general agent. Regardless of the final outcome, the process has taught me more about technical software development and the things I need and want in my own life than any other project I've taken on before this. Cherry Research as a whole will be used to document my process in (machine) learning and share other projects that I plan on making. Feel free to poke around the files to see what's going on under the hood. I would encourage you to be ambitious, and try the same: find something that would make your life better and simply build it - but be ruthless when it comes to quality. Maybe float can help you do that.
