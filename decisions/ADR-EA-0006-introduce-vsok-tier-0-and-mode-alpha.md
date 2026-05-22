# ADR-EA-0006 — Introduce VSOK at Tier 0 and rename Tier 1 to Mode Alpha

- **Status:** Accepted
- **Date:** 2026-05-22
- **Author:** JD Longmire
- **Reviewers:** @jdlongmire
- **Amends:** [cross-ai #40 Refinement B](https://github.com/ologos-corp/cross-ai/issues/40) (Strategy classification + canon tier shape)
- **Ratification note:** Comment-out period waived by explicit maintainer ratification (JD Longmire, 2026-05-22). Basis: sole-maintainer status, substantive deliberation captured in cross-ai #40 plus the in-session conversation that generated this ADR, and the ADR being a refinement-grade follow-up to a recently-ratified parent (cross-ai #40 Refinement B). enterprise-ai is also slated for archival as part of the cross-ai #40 canon stand-up; this ADR's content travels with the migration to `ologos-repos/aide-canon/decisions/`.

## Context

The canon structure ratified in [cross-ai #40](https://github.com/ologos-corp/cross-ai/issues/40) established a four-tier hierarchy for `ologos-repos/aide-canon`:

- **Tier 1 — Master Thesis:** AI-centric Digital Ecosystem (synthesis)
- **Tier 2 — Foundation:** HCAE, AIDK, RLEG
- **Tier 3 — Constructs:** DEA, OrdSA, MxM, OAgents
- **Tier 4 — Enterprise Platforms:** Strategy, AEON, AIDEX, OAAD (HCAE moved to Foundation per Refinement B)

The AIDE Architecture Overview infographic (`ologos-repos/aide-canon/infographics/AIDE-Architecture-Overview.png`, v1 published 2026-05-22) surfaced two structural issues with the ratified shape on review:

1. **Strategy is not a platform peer.** AEON, AIDEX, and OAAD are buildable software targets. *Enterprise Agentic AI Platform Strategy* is umbrella positioning — a CIO/CTO-altitude artifact arguing for the platforms beneath it. cross-ai #40 Refinement B addressed this by flagging Strategy `buildable: false` in `MANIFEST.yaml` while leaving it co-located with the platforms. The flag acknowledged the altitude mismatch without resolving it; an agent reading the canon's tier structure still sees Strategy as a Tier 4 peer.

2. **"Master Thesis" reads narrow.** The Tier 1 label connotes academic-degree framing. The artifact it points to is the corpus's primary synthesizing orientation, not a degree submission. A naming consistent with the corpus's own architectural vocabulary is preferred.

The infographic also displayed HCAE in both Tier 2 (Foundation) and Tier 4 (Enterprise Platforms) — a duplication inconsistent with cross-ai #40 Refinement B. That correction is captured here alongside the structural amendments below.

## Decision

### 1. Introduce Tier 0 — VSOK

Add a new top-level tier above Tier 1, named **VSOK** — the corpus's enterprise-strategic frame:

- **V**ision — long-horizon outcome the corpus advances toward (artifact reserved)
- **S**trategy — *Enterprise Agentic AI Platform Strategy* paper (migrated from Tier 4 enterprise-platforms)
- **O**bjectives — strategic goals deriving from Vision (artifact reserved)
- **K**ey Results — measurable outcomes anchoring Objectives (artifact reserved)

VSOK names the strategic umbrella under which the corpus operates. Vision and the two reserved slots (Objectives, Key Results) are placeholders the canon commits to populating over time.

### 2. Rename Tier 1 — Master Thesis → Mode Alpha

The synthesizing artifact at Tier 1 remains *AI-centric Digital Ecosystem*. The tier label changes from **Master Thesis** to **Mode Alpha** — the corpus's primary orientation mode (α).

The naming aligns with Greek-letter precedent already present in the corpus's deliberations (cross-ai #40 ADR-prefix decision used Pattern α). It scales naturally: Mode Beta, Mode Gamma reserved for future orientation modes if the corpus's intellectual surface broadens.

### 3. Tier 4 — Enterprise Platforms shrinks to three

Tier 4 becomes the buildable-software trio: **AEON, AIDEX, OAAD**.

- *Strategy* lifts to Tier 0 (VSOK / Strategy)
- *HCAE* was already migrated to Foundation per cross-ai #40 Refinement B; the prior infographic erroneously showed it in both tiers. This ADR corrects the visual record alongside the structural amendments.

### 4. Repository surface

The canon's directory layout changes as follows (relative to the cross-ai #40 ratified shape):

```
aide-canon/
├── vsok/                          # NEW — Tier 0
│   ├── vision/                    # reserved (artifact TBD)
│   ├── strategy/                  # Enterprise Agentic AI Platform Strategy (relocated)
│   ├── objectives/                # reserved (artifact TBD)
│   └── key-results/               # reserved (artifact TBD)
├── mode-alpha/                    # RENAMED from thesis/ (Tier 1)
│   └── ...                        # AI-centric Digital Ecosystem synthesis (forthcoming)
├── foundation/                    # unchanged (Tier 2 — HCAE, AIDK, RLEG)
├── constructs/                    # unchanged (Tier 3 — DEA, OrdSA, MxM, OAgents)
├── enterprise-platforms/          # unchanged shape, three subdirs only (Tier 4)
│   ├── aeon/
│   ├── aidex/
│   └── oaad/
├── related-work/                  # unchanged
│   └── theseus/
├── infographics/                  # unchanged
└── decisions/                     # unchanged
```

`enterprise-platforms/strategy/` is **not** created. `enterprise-platforms/hcae/` is **not** created (HCAE lives in `foundation/hcae/` only).

Sequencing: this ADR lands before OlogosAI's canon stand-up PR, so the migration produces the corrected shape directly rather than landing the cross-ai #40 shape and then patching.

## Consequences

**Positive:**
- Strategy's altitude becomes structurally honest — umbrella positioning at Tier 0, not a software peer at Tier 4.
- The canon gains an explicit strategic frame (VSOK) above its intellectual content. Enterprise-architecture-native shape; reads correctly to readers familiar with VSOK / OKR conventions.
- *Mode Alpha* reads forward — the corpus's first orientation mode, with room for siblings if future work warrants.
- Infographic structure becomes correct (HCAE no longer appears in two tiers).
- MANIFEST.yaml's `buildable: false` flag for Strategy becomes unnecessary; Strategy's non-buildability is now structurally evident from its placement in VSOK rather than declared as an exception within enterprise-platforms.

**Negative:**
- Tier renumbering touches references to "Tier 1 — Master Thesis" in any pending artifacts. Mitigated because `ologos-repos/aide-canon` is not yet populated beyond the README + initial infographic; no published downstream artifact cites the prior tier numbering as load-bearing.
- VSOK at Tier 0 adds reserved-but-unpopulated surfaces (Vision, Objectives, Key Results) the corpus commits to populating over time. Empty tiers are an explicit IOU.
- The canon directory layout diverges from cross-ai #40 Refinement B's `MANIFEST.yaml` flag approach; OlogosAI's stand-up PR must reflect the amended shape.

**Neutral:**
- Foundation (HCAE, AIDK, RLEG) and Constructs (DEA, OrdSA, MxM, OAgents) tiers unchanged.
- ADR-EA-NNNN prefix continuity holds per cross-ai #40's ratified (α) prefix decision.
- *Mode Alpha* relabeling does not change the synthesizing artifact itself — the master thesis paper, when authored, lives at Tier 1 under the new label.

## Alternatives considered

1. **Keep Strategy in `enterprise-platforms/` with `buildable: false`** (cross-ai #40 Refinement B's ratified position). Rejected. The flag acknowledges the altitude mismatch without resolving it. An agent traversing the canon's tier structure still encounters Strategy as a Tier 4 peer to AEON/AIDEX/OAAD; the MANIFEST flag is meta-information that requires a second pass to apply. Naming Strategy at Tier 0 inside VSOK makes the altitude explicit at first contact.

2. **Promote Strategy to Tier 1 as a peer of Master Thesis.** Rejected. Strategy and the AIDE synthesis paper are at different altitudes — Strategy is the enterprise-strategic frame (the *why and what* at corpus level); the synthesis is the integrative architectural argument (the *how the parts cohere*). Treating them as Tier 1 peers blurs the umbrella/synthesis distinction.

3. **Name Tier 1 "Mode 0" instead of "Mode Alpha".** Rejected. The combination *Tier 0 / Mode 0* reads as a numeric clash and visually suggests redundancy. *Mode Alpha* aligns with the corpus's existing Greek-letter convention (Pattern α from cross-ai #40's prefix discussion).

4. **Defer the structural amendment; keep cross-ai #40 Refinement B as-is and patch only the infographic.** Rejected. The infographic surfaced a structural problem in the ratified shape; patching the visual without correcting the structure would leave the canon's directory layout misaligned with its own positioning. Better to amend once than to ship with a known-wrong shape and patch later.

5. **Place VSOK inside `decisions/` rather than as a top-level tier.** Rejected. VSOK is not a decision artifact — it is the corpus's strategic frame. Burying it inside `decisions/` would make it discoverable only to readers who already know to look there. Top-level surfacing matches its load-bearing role.

## Related

- [cross-ai #40](https://github.com/ologos-corp/cross-ai/issues/40) — Canon structure proposal; this ADR amends Refinements A and B.
- [ADR-EA-0004](ADR-EA-0004-add-mx-modes-as-spine-construct.md) — Mx-Modes as spine construct (Greek-letter Pattern α precedent).
- [ADR-EA-0005](ADR-EA-0005-clarify-mxm-archetype.md) — MxM archetype clarification.
- [ADR-ORDSA-0007](https://github.com/osa-ai-org/ordsa-ai/) — Provenance promotion (pending OlogosAI execution; independent of this ADR).
- [`infographics/AIDE-Architecture-Overview.png`](https://github.com/ologos-repos/aide-canon/blob/main/infographics/AIDE-Architecture-Overview.png) — visual that surfaced the structural issues this ADR resolves; will be regenerated to reflect the amended shape.
