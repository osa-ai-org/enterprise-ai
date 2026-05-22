# Mx-Modes — Meta-Harness Framework

This subdirectory holds a **co-authored architectural construct** bundled alongside the main AI EA corpus as an allied artifact. The main corpus in the parent repository is sole-authored by James D. Longmire; this subdirectory carries a two-author construct under its own framing.

## What's here

| File | What it is |
|---|---|
| [`Mx-Modes-Technical-Reference.docx`](Mx-Modes-Technical-Reference.docx) / [`.pdf`](Mx-Modes-Technical-Reference.pdf) | The full technical reference — framework purpose, the five governing surfaces (MIND / MORALS / MISSION / MEMORY / MEANS), lifecycle, precedence rules, example modes |
| [`Mx-Modes-Construct-Infographic.jpg`](Mx-Modes-Construct-Infographic.jpg) | Construct overview infographic — five surfaces, foundational rule, precedence model, lifecycle, sample modes |

## What Mx-Modes is

Mx-Modes (architecturally designated **MxM**) is a meta-harness framework that structures AI operation through explicit *mode orientation*. A root `mode.md` file activates a governing posture that resolves five surfaces — **MIND** (reasoning discipline), **MORALS** (permission boundaries), **MISSION** (purpose and scope), **MEMORY** (continuity and reference), **MEANS** (execution surface: tools, skills, workflows) — *before* execution begins.

The architectural claim the framework rests on:

> **AI behavior should be oriented before it is executed.**

Most AI implementations begin with capability — models, tools, APIs, plugins, automations — and try to constrain that capability afterward. Mx-Modes inverts the order: orientation first, then capability is loaded against an established posture. The posture is governed by four discipline-bearing surfaces (Mind / Morals / Mission / Memory) and *implemented* by a fifth (Means). Means does not grant permission; it executes within the envelope the other four establish.

The framework is deliberately not a model architecture, not a safety standard, not a compliance framework, and not a substitute for enterprise policy. It is a categorical-separation pattern into which any of those things can be loaded.

## Relation to this corpus

Mx-Modes operates at the **agent-orientation layer** — how an individual AI instance is structured before it executes. That is a different altitude from the rest of the corpus:

| Construct | Altitude | What it governs |
|---|---|---|
| **DEA** | Enterprise | Three-baseline coherence across capability/technical/operational disciplines |
| **AEON / AIDEX / HCAE / OAAD** | Enterprise AI control plane | The four-plane operating model for enterprise-scale agentic AI |
| **OrdSA** | Layered authority within an agent's lifecycle | Seven ordinal layers (O0–O6) ordering intent, authority, evidence, outcome |
| **Mx-Modes** | Agent orientation | Five governing surfaces that orient a single AI instance before it executes |

Mx-Modes is conceptually compatible with OrdSA — an OrdSA-conformant agent at O3 can carry an Mx-Modes envelope as its operating structure. The two are orthogonal: Mx-Modes says *what posture is active*; OrdSA says *what authority and evidence ordering governs the run*.

A reader working through the AI EA corpus benefits from having Mx-Modes at hand because the governance discipline it formalizes (Mind / Morals / Mission / Memory) is the same categorical separation that AEON, AIDEX, and HCAE assume at the enterprise scale. Mx-Modes is what that separation looks like when collapsed onto a single agent instance.

## Why bundle Mx-Modes here rather than in the corpus spine

The corpus README positions the work as sole-authored by JD Longmire, with the four AI-specialization constructs (AEON / AIDEX / HCAE / OAAD) and the general-EA foundation (DEA) as that single author's research program. Mx-Modes is a different shape — a joint construct co-authored with Micah Longmire — and absorbing it into the corpus spine would either:

1. Change the corpus's stated sole-author identity (a positioning-change ADR), or
2. List Mx-Modes as JD-only and underrepresent Micah's contribution.

The allied-subdirectory pattern (precedent: [`docs/theseus-thesis/`](../theseus-thesis/)) is the established way to bundle research that sits in the corpus's intellectual neighborhood without subordinating it to the corpus's authorship identity. Mx-Modes inherits that pattern.

The framing decision to bundle this way (rather than absorb into the spine or split into a separate repo) is recorded in [ADR-EA-0004](../../decisions/ADR-EA-0004-bundle-mx-modes-as-allied-subdirectory.md).

## Authorship and rights

| | |
|---|---|
| **Authors** | JD Longmire ([ORCID 0009-0009-1383-7698](https://orcid.org/0009-0009-1383-7698)) — Northrop Grumman Fellow<br>Micah Longmire ([ORCID 0009-0006-7608-9322](https://orcid.org/0009-0006-7608-9322)) — Sr. AI Architect |
| **Disclaimer** | Both authors conduct this research independently and in personal capacity. Their employer affiliations are listed for identification only and do not endorse, sponsor, or own this work. |
| **License** | CC BY 4.0 — consistent with the parent corpus. Attribution form: cite both authors with their ORCIDs. |
| **Citation** | "Longmire, JD; Longmire, M. *Mx-Modes: A Meta-Harness Framework for Multi-Mode AI Operation.* 2026. ORCID 0009-0009-1383-7698 / 0009-0006-7608-9322." |
| **Status** | Technical Architecture Reference — first published version. |

## How this differs from the AI EA corpus

The AI EA corpus develops constructs at the **enterprise** altitude — how an organization composes its AI control plane and architects its digital ecosystem. Mx-Modes develops a construct at the **agent** altitude — how a single AI instance is oriented before it executes. The two altitudes inform each other (the enterprise control plane is, at the limit, a population of oriented agents) but they are distinct levels of architectural analysis, and bundling Mx-Modes here is a convenience for readers, not a claim that the two are the same kind of artifact.
