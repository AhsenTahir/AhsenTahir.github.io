---
permalink: /
title: "Ahsen Tahir"
seo_title: "Ahsen Tahir — Multi-Agent LLM Systems"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a final-year B.S. Computer Science student at [FAST NUCES](https://www.nu.edu.pk/), currently a **Mitacs Globalink Research Intern** at the [University of New Brunswick](https://www.unb.ca/) in Fredericton, Canada.

My research is on **multi-agent systems built from large language models** — specifically, how independent agents should communicate and coordinate when no single planner can hold the whole task. Most deployed agent systems route everything through one central planner, which becomes both a bottleneck and a single point of failure as tasks get longer. I work on the alternative: giving agents structured **agent-to-agent (A2A) communication** so that plans can be refined by the agents actually executing them. Two papers on this have come out of that line of work, and the results suggest the semi-centralized design beats workflow-based baselines while using a *smaller* planner model.

At UNB I am working on a different question with the same underlying concern — whether we can trust what language models produce. I am benchmarking **security vulnerabilities in LLM-generated code**, measuring whether frontier models follow secure coding patterns or reproduce known anti-patterns at scale.

Alongside that I am part of a collaborative project on **defending LLM agents against indirect prompt injection** (SASD), currently unpublished. I am happy to talk about it directly, but I am keeping the details off this page until the work is out.

I am applying for **thesis-based MSc programs in Canada for Fall 2027**, and I am looking for a supervisor working on LLM agents, multi-agent coordination, or evaluation and safety of language models. My [CV](/cv/) has the full record, and I am reachable at [ahsentahir007@gmail.com](mailto:ahsentahir007@gmail.com).

Research interests
======
- **Multi-agent LLM systems** — coordination, planning, and role delegation among autonomous agents
- **Agent-to-agent communication** — protocols and information flow as an alternative to rigid, rule-based workflows
- **Evaluation of agentic systems** — benchmark design and measurement on GAIA and similar long-horizon tasks
- **Agent security** — keeping agents faithful to the user's instruction when untrusted content tries to redirect them
- **Trustworthy code generation** — security properties of code produced by frontier language models

Selected publications
======
**Anemoi: A Semi-Centralized Multi-agent System Based on Agent-to-Agent Communication MCP server from Coral Protocol**
Xinxing Ren, Caelum Forder, Qianbo Zang, **Ahsen Tahir**, Roman J. Georgio, Suman Deb, Peter Carroll, Önder Gürcan, Zekun Guo
*NeurIPS 2025 Workshop on Language Agents and World Models (LAW)*
[arXiv:2508.17068](https://arxiv.org/abs/2508.17068) · [details](/publication/2025-08-23-anemoi)

**Beyond Rule-Based Workflows: An Information-Flow-Orchestrated Multi-Agents Paradigm via Agent-to-Agent Communication from CORAL**
Xinxing Ren, Qianbo Zang, Caelum Forder, Suman Deb, **Ahsen Tahir**, Roman J. Georgio, Peter Carroll, Zekun Guo
*arXiv preprint, January 2026*
[arXiv:2601.09883](https://arxiv.org/abs/2601.09883) · [details](/publication/2026-01-14-beyond-rule-based-workflows)

The [full list is here](/publications/).

News
======
- **Jun 2026** — Started as a Mitacs Globalink Research Intern at the University of New Brunswick, working on security benchmarking of LLM-generated code.
- **Feb 2026** — Co-founded Velton, building an embedded copilot layer for B2B SaaS products.
- **Aug 2025** — *Anemoi* accepted at the NeurIPS 2025 Workshop on Language Agents and World Models.
- **Feb 2025** — Joined CoralOS as an AI Engineer, working on production agent-to-agent communication infrastructure.
