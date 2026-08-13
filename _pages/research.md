---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

The question I keep returning to is **how much central control a system of language-model agents actually needs**.

The default answer in deployed systems is: all of it. One planner model decomposes the task, assigns subtasks, and integrates results. This is easy to reason about and easy to debug, and it breaks in a specific, predictable way — the planner must hold the entire task in context, so as horizons grow it becomes simultaneously the accuracy ceiling, the cost centre, and the single point of failure. Scaling the planner is the obvious fix and an expensive one.

My work has been on the alternative: distributing coordination across the agents themselves.

Agent-to-agent communication
======

In **[Anemoi](/publication/2025-08-23-anemoi)** (NeurIPS 2025 LAW Workshop) we replaced the all-knowing planner with structured agent-to-agent (A2A) communication over an MCP server. Because worker agents can talk to each other directly, plans get refined by the agents that can actually see execution state, rather than dictated up front by a planner that cannot. On GAIA this reached 52.73% with GPT-4.1-mini as the planner and beat the OWL baseline by 9.09 points under identical LLM settings.

The result I found most interesting was not the headline number but what it implied: a *smaller* planner in a better-coordinated system outperformed a larger planner in a centralized one. Coordination structure, not model capacity, was the binding constraint.

**[Beyond Rule-Based Workflows](/publication/2026-01-14-beyond-rule-based-workflows)** approaches the same question from the other side. Here we kept a central orchestrator but removed the fixed workflow graph, letting an information-flow orchestrator adapt coordination dynamically while agents communicate in natural language. That reached 63.64% pass@1 on GAIA, +8.49 over the workflow-based baseline at comparable token cost.

Taken together the two results suggest the rigidity of predetermined workflows, rather than centralization as such, is what limits these systems. I do not think that is settled, and it is the thread I would most like to pull on in graduate work.

Trustworthy code generation
======

At the University of New Brunswick I am working on a narrower but related problem: whether we can trust what these models emit. I am benchmarking security vulnerabilities in LLM-generated code — measuring at scale whether frontier models follow secure coding patterns or reproduce known anti-patterns.

The connection to the agent work is direct. Multi-agent systems increasingly write and execute their own code, which means a vulnerability rate that is tolerable in a human-reviewed setting becomes something else entirely when the code path is autonomous. Evaluation has to catch up with autonomy.

Agent security
======

I am also part of a collaborative, in-progress project on **defending LLM agents against indirect prompt injection** — the setting where an attacker plants instruction-like text in content the agent has to read, and the agent treats it as a command rather than as evidence. The interesting part, to me, is that this is an *authority* failure rather than a knowledge failure: the model knows what the user asked for, and still lets untrusted text override it.

The work is unpublished, so I am keeping specifics off this page. I am glad to discuss it directly.

What I want to work on next
======

- **Evaluation that survives contact with long horizons.** GAIA is a good benchmark and an insufficient one. Agentic evaluation currently rewards systems that are good at benchmarks rather than systems that degrade gracefully, and I would like to work on measurement that distinguishes the two.
- **Coordination under uncertainty.** When agents cannot verify each other's claims, what communication structures remain robust? This is where multi-agent LLM work seems to me to meet older questions from distributed systems and mechanism design.
- **Safety properties of autonomous code execution.** Extending the UNB benchmarking work from static generation to agents that write, run, and revise their own code.

I am applying for **thesis-based MSc programs in Canada for Fall 2027**. If any of the above overlaps with your lab, I would welcome the conversation — [ahsentahir007@gmail.com](mailto:ahsentahir007@gmail.com).
