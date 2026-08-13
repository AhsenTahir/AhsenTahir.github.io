---
title: "Beyond Rule-Based Workflows: An Information-Flow-Orchestrated Multi-Agents Paradigm via Agent-to-Agent Communication from CORAL"
collection: publications
category: preprints
permalink: /publication/2026-01-14-beyond-rule-based-workflows
excerpt: 'A workflow-free multi-agent paradigm in which a centralized information-flow orchestrator coordinates agents communicating in natural language, reaching 63.64% pass@1 on GAIA — +8.49% over a workflow-based baseline at comparable token cost.'
date: 2026-01-14
venue: 'arXiv preprint'
paperurl: 'https://arxiv.org/abs/2601.09883'
bibtexurl: '/files/beyond-rule-based-workflows.bib'
citation: 'Xinxing Ren, Qianbo Zang, Caelum Forder, Suman Deb, <b>Ahsen Tahir</b>, Roman J. Georgio, Peter Carroll, Zekun Guo. (2026). &quot;Beyond Rule-Based Workflows: An Information-Flow-Orchestrated Multi-Agents Paradigm via Agent-to-Agent Communication from CORAL.&quot; <i>arXiv preprint arXiv:2601.09883</i>.'
---

Rule-based workflows are the standard way to make multi-agent systems reliable: fix the graph of who calls whom, and behaviour becomes predictable. The cost is that the system can only handle tasks whose shape someone anticipated in advance, and real long-horizon tasks rarely cooperate.

This paper drops the fixed workflow entirely. Agents communicate in natural language over an A2A protocol, and a **centralized information-flow orchestrator** monitors task state and adapts coordination dynamically instead of executing a predetermined graph.

Results on GAIA:

- **63.64% pass@1**, versus the workflow-based OWL baseline.
- **+8.49% improvement** at comparable token usage — the gain is not bought with extra inference budget.
- Notably better behaviour on edge cases and long-horizon task decomposition, which is exactly where fixed workflows fail.

Read together with *Anemoi*, the two papers bracket a design question I find genuinely open: how much central coordination does a multi-agent system actually need? Anemoi removes the central planner; this work keeps a coordinator but strips the fixed workflow. Both beat the rigid baseline, which suggests the rigidity — not the centralization — was the problem.

<!-- TODO (Ahsen): uncomment and describe what you ACTUALLY did on this paper.
     Left commented out so nothing unfinished renders publicly.

*My contribution:* ...
-->

