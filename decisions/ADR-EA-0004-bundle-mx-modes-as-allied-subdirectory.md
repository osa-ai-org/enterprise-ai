# ADR-EA-0004 — Bundle Mx-Modes as an allied subdirectory under `docs/mx-modes/`

- **Status:** Proposed
- **Date:** 2026-05-22
- **Author:** JD Longmire
- **Reviewers:** @jdlongmire

## Context

On 2026-05-22 a new architectural construct, **Mx-Modes** (architecturally designated **MxM** — multi-mode meta-harness), was authored jointly by JD Longmire and Micah Longmire as a Technical Architecture Reference. The framework structures AI operation through five governing surfaces — **MIND, MORALS, MISSION, MEMORY, MEANS** — and rests on the architectural claim that *AI behavior should be oriented before it is executed*.

Mx-Modes sits at the **agent-orientation altitude**: it formalizes how a single AI instance is structured before execution begins. That altitude is different from the rest of this corpus, which operates at the **enterprise** altitude (DEA's three-baseline framework, the four-plane AI control plane via AEON / AIDEX / HCAE / OAAD).

Two facts about Mx-Modes make its addition to this repository non-trivial:

1. **It is the first co-authored architectural construct in the corpus's neighborhood.** Every prior construct in this repository (AEON, AIDEX, HCAE, OAAD, DEA) is sole-authored by JD Longmire. The corpus README positions the work as a single-author research program. Mx-Modes is co-authored with Micah Longmire, whose contribution is foundational, not editorial.

2. **It operates at a different altitude than the corpus's stated scope.** The corpus describes itself (per [ADR-EA-0003](ADR-EA-0003-expand-corpus-to-include-dea.md)) as developing "enterprise architecture, with AI specialization." Mx-Modes is not enterprise architecture — it is per-agent operating-envelope orientation. Absorbing it into the corpus spine would either broaden the corpus's stated altitude or misrepresent the construct's purpose.

The Theseus Agent Thesis ([PR #4](https://github.com/osa-ai-org/enterprise-ai/pull/4)) established a precedent for bundling adjacent research that does not fit the corpus's sole-author / enterprise-altitude spine: an allied `docs/<work-name>/` subdirectory with its own README, authorship table, and disclaimer. Mx-Modes is a natural match for that precedent.

Adding Mx-Modes touches a clause CONTRIBUTING.md flags as **non-waivable under the maintainer-prerogative waiver**:

- *Introduces a new architectural construct* (Mx-Modes itself)

The standard one-week comment-out period therefore applies, regardless of how the construct is bundled. This ADR records the bundling decision and the rationale.

## Decision

**Add Mx-Modes to this repository as an allied subdirectory at `docs/mx-modes/`, following the precedent established by `docs/theseus-thesis/`.** The corpus spine — its sole-author identity, its enterprise-altitude scope, its four-construct AI-specialization enumeration, its DEA foundation — remains **unchanged**.

Concretely:

1. **Directory:** `docs/mx-modes/` is created with the following contents:
   - `README.md` — directory framing, authorship table, relation to the corpus, license + disclaimer
   - `Mx-Modes-Technical-Reference.docx` — source document
   - `Mx-Modes-Technical-Reference.pdf` — rendered PDF for reading
   - `Mx-Modes-Construct-Infographic.jpg` — construct overview visual

2. **Top-level README is not modified.** Mx-Modes is not added to the corpus's reading order, document index, audience description, citation block, or four-construct enumeration. From the corpus README's perspective, the work in `docs/mx-modes/` is bundled-adjacent, not part of the corpus.

3. **Authorship:** Both authors are listed with ORCIDs in the subdirectory's README and in the construct's own attribution. Each author's employer affiliation appears for identification only, with the standard "research conducted independently and in personal capacity" disclaimer.

4. **License:** CC BY 4.0, consistent with the corpus license. Citation form is the joint-author pattern with both ORCIDs.

5. **Relation to allied constructs is documented in the subdirectory README**, not in the top-level corpus README. This keeps the corpus's stated scope clean.

### Scope: directory creation + ADR

This ADR's PR carries only:
- `docs/mx-modes/` directory with the four files described above
- `decisions/ADR-EA-0004-bundle-mx-modes-as-allied-subdirectory.md` (this ADR)
- `decisions/README.md` index entry for ADR-EA-0004

It does **not**:
- Modify the top-level corpus `README.md`
- Modify any other ADR
- Modify [`CONTRIBUTING.md`](../CONTRIBUTING.md) (including its sole-author waiver clause, which remains in effect for the corpus spine — the spine remains sole-authored after this change)
- Change the corpus's CC BY 4.0 license, citation pattern, or "independent research" disclaimer
- Introduce Mx-Modes content claims into the corpus's argumentation

## Consequences

- **Corpus identity preserved.** The corpus's stated scope, altitude, and sole-author identity all remain unchanged. The Theseus precedent now has a sibling precedent, reinforcing the allied-subdirectory pattern as the corpus's established mechanism for adjacent research.
- **Mx-Modes gains a stable home.** The construct can be cited from `docs/mx-modes/` with a durable URL, and the bundled PDF removes the need for readers to traverse external sites.
- **Multi-author work is now in the repository, but not in the corpus spine.** Future joint or multi-author constructs can follow this same pattern without requiring CONTRIBUTING.md changes. If Mx-Modes (or any future allied work) is later promoted into the corpus spine, that promotion is itself an ADR-bearing decision.
- **Cross-references can be added later.** If the corpus README's *Suggested reading order* eventually wants to recommend Mx-Modes to readers as a per-agent companion to the enterprise constructs, that recommendation lands as a separate content PR, not as part of this ADR. The decision to point at allied work is distinct from the decision to bundle it.
- **The non-waivable-clause precedent holds.** A new construct, even one bundled as allied-adjacent, still triggers the standard ADR period. This ADR is the second instance applying that rule (ADR-EA-0003 / DEA was the first), making the rule load-bearing rather than aspirational.

## Alternatives considered

1. **Absorb Mx-Modes into the corpus spine alongside DEA and the AI-specialization constructs.** Reframe the corpus as covering enterprise *and* agent-orientation altitudes, list Mx-Modes in the reading order and document index, and add a multi-author exception to the corpus's stated authorship. Rejected for three reasons: (1) it requires changing the corpus's stated audience, positioning, and authorship — three non-waivable triggers stacked — making the ADR materially heavier than needed; (2) it forces a revisit of CONTRIBUTING.md's sole-author waiver clause ([PR #3](https://github.com/osa-ai-org/enterprise-ai/pull/3)) immediately after that clause was installed; (3) the altitude difference is genuine — agent-orientation is not enterprise architecture, and stretching the spine to cover both would weaken the corpus's coherence.

2. **Publish Mx-Modes as a standalone repository at `osa-ai-org/mx-modes` (or similar).** Treat Mx-Modes as a parallel work with its own independent presence, not bundled here at all. Rejected because (a) Mx-Modes is operationally adjacent to OrdSA and the AI EA constructs — readers benefit from having it bundled with the corpus they're already reading rather than chasing an additional repository; (b) the Theseus precedent already established that allied adjacent work belongs *here, isolated*, not *elsewhere, separated*. Standing up a new repo for every allied work would proliferate surface area without proportionate benefit.

3. **Bundle under `docs/mx-modes/` but also add a "related work" section to the top-level README pointing at the subdirectory.** A middle path between absorption and isolation. Rejected for *this* ADR because the act of adding a Related Work section to the top-level README is itself a positioning change — it broadens what the corpus README presents to first-time readers — and would benefit from being a deliberate, separate decision rather than tucked into this ADR's scope. If the cross-reference is wanted, it lands as a separate content PR after this one merges. The bundling decision and the surface-it-in-the-spine decision are orthogonal and should be made independently.

4. **Defer bundling until Mx-Modes has a public canonical home (e.g., a published paper, a Substack mirror, an arXiv preprint).** Treat the docx as draft and wait for an external citable source before mirroring. Rejected because the docx is presented as a complete Technical Architecture Reference (v1), not a draft. Bundling now records the framework's first stable form in the corpus's neighborhood; any future canonical publication is additive.

## References

- [ADR-EA-0001](ADR-EA-0001-adopt-ordsa-development-process.md) — the governance process this ADR follows (PR-first + ADRs as PRs)
- [ADR-EA-0002](ADR-EA-0002-reframe-as-ordsa-exemplar.md) — the AI EA corpus as canonical enterprise-scale OrdSA deployment (unchanged by this ADR)
- [ADR-EA-0003](ADR-EA-0003-expand-corpus-to-include-dea.md) — DEA expansion (in flight as PR #5; this ADR does not depend on its merge state)
- [`CONTRIBUTING.md`](../CONTRIBUTING.md) — the waiver-exclusion clause that triggers the standard one-week period for new-construct ADRs
- [`docs/theseus-thesis/`](../docs/theseus-thesis/) — the precedent allied-subdirectory pattern this ADR adopts
- [`docs/mx-modes/`](../docs/mx-modes/) — the directory introduced by this ADR
- [`docs/mx-modes/README.md`](../docs/mx-modes/README.md) — subdirectory framing, authorship table, relation to corpus
- [`docs/mx-modes/Mx-Modes-Technical-Reference.docx`](../docs/mx-modes/Mx-Modes-Technical-Reference.docx) / [`.pdf`](../docs/mx-modes/Mx-Modes-Technical-Reference.pdf) — the construct's technical reference
- [`docs/mx-modes/Mx-Modes-Construct-Infographic.jpg`](../docs/mx-modes/Mx-Modes-Construct-Infographic.jpg) — construct overview infographic
