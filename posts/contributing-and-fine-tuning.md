---
title: "Contributing and Fine-Tuning"
date: "2026-06-14"
tags: ["float", "contributing", "fine-tuning", "tinker"]
readTime: "2 min read"
summary: "How outside contributions can help float and why data provenance matters."
---

As an open-source, independent project, contributions are very valuable to the development of float. Contributing can be as simple as short feedback, feature requests, bug reports, or full pull requests. Anything helps: in order to make AGI as beneficial for the world as possible, open discussion and culture are highly important. You can find more details in the [Float contribution guide](https://github.com/CherryResearch/float/blob/main/CONTRIBUTING.md).

If you would like to fork the project or make a serious contribution, please do not hesitate to reach out. I am happy to discuss the development of float and work with interested people. float is licensed under the [GNU Affero General Public License v3.0](https://github.com/CherryResearch/float/blob/main/LICENSE), which means derivatives must use the same license, and larger contributions are covered by the repository's [contributor assignment agreement](https://github.com/CherryResearch/float/blob/main/CONTRIBUTOR_ASSIGNMENT_AGREEMENT.md).

float is an open interface and agentic workspace for working with models, tools, memory, and local context. That means the project needs more than code. It needs people testing edge cases, runtimes, and modules. 

We value all feedback, critique, and input. Some of the most useful contribution areas right now are:

- bug reports with exact setup, runtime mode, model/provider, expected behavior, actual actions, and sanitized reproduction notes;
- QA passes against chat flow, tool approval, local provider setup, model downloads, sync, memory/RAG, modules, and import/export paths;
- documentation that makes current behaviour easier to verify;
- focused code fixes with tests;
- modules, add-ons, skill docs, and sample workflows that are safe to publish;
- evaluation cases and data proposals with clean provenance.

Anything that helps make float more inspectable, adaptable, and useful is worth hearing about. 

## Training Direction

float relies heavily on open-source models like `gpt-oss` and Gemma. It is designed specifically for structured model interaction, including harmony format, channels, tools, memory, modules, and local or compatible runtimes. 

As float grows, one major goal is to develop fine-tuned models and evaluation sets that improve performance inside this environment. The main training direction is tool and agent behaviour: local-first privacy habits, approval behaviour, error recovery, argument repair, memory and retrieval judgment, and float-specific workflows. This requires thoughtfully curated training data, which we intend to develop and maintain so that it can be used to update future models if needed. We are also proposing the idea of an open-source, collaborative training set.

This process has to be considerate. A collaborative, open-source dataset for reasoning, tool behavior, or personality-focused multimodal data would be valuable, but only if the rights chain is clear. Permissively licensed, community-evaluated material is the right direction. Synthetic transformations for float-specific evaluations and tool calls are acceptable when labeled and evaluated, but distillation from non-permissively licensed models, datasets, or hidden reasoning traces is not acceptable.

The intent is to demonstrate the process of data curation, separation, training, and evaluation. The local fine-tunes should be transparent, transferable to future models, and replicable for evaluations and forks. A useful adapter should leave behind enough metadata for someone else to understand the dataset snapshot, source and license notes, training configuration, and evaluation prompts without guessing what happened.

If you are interested in contributing a dataset or evaluation set, (or if you have any other questions or comments) please email cherryresearch@pm.me first rather than sending files cold. We can consider storage solutions case by case; if there is a useful shared dataset later, something like Hugging Face may be a good home for it.

## Tinker Studio

To that end, we have also created [Tinker Studio](https://github.com/CherryResearch/tinker-studio), a dashboard for working with Thinking Machines Lab's Tinker API directly. This includes scripts and Codex/agent skills for managing data curation, separation, training, monitoring, checkpoint sampling, notebook recovery, and inference experiments. If there is interest, the same pattern could be generalized to other training backends like PyTorch, TensorFlow, or Hugging Face workflows. Please take a look, ask questions, make suggestions, or see what you can learn from it.

If you are interested in float, the most helpful thing is to try it, break it politely, and tell us what happened.
