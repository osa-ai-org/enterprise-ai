# enterprise-ai

Independent research on enterprise architecture for the agentic era — by **James D. Longmire** (Northrop Grumman Fellow, Chief Architect – Digital Ecosystems; ORCID [0009-0009-1383-7698](https://orcid.org/0009-0009-1383-7698)).

This corpus develops the canonical **enterprise-scale deployment of [OrdSA (Ordinal Systems Architecture)](https://github.com/osa-ai-org/ordsa-ai)** — the layered authority and evidence construct for agentic systems. The thesis: the control plane should be **enterprise-owned**, not vendor-rented; the four planes (control, runtime, experience, capability) should be composed as one architecture.

> *This work presents independent research and reflects the views of the author. It does not represent the position of any employer or program.*

---

![NextGen Enterprise AI Architecture — four-plane platform](infographics/NextGen-Enterprise-AI-Architecture-Infographic.png)

*The four-plane architecture at a glance — Control (AEON) · Runtime · Experience (AIDEX) · Capability (OAAD). The full argument lives in the source documents below.*

---

## The four constructs

| Construct | Stands for | What it is |
|---|---|---|
| **AEON** | AI Enterprise Orchestration Nexus | The enterprise control plane for the agentic era. Six service planes — identity, authority, evidence, integration, capability composition, orchestration runtime. Enterprise IT-developed and sustained, not a vendor product. |
| **AIDEX** | AI Digital Experience | The worker-facing subdomain under AEON. The architecture that expresses HCAE operationally at the digital experience layer. One of nine peer subdomains. |
| **HCAE** | Human-Curated, AI-Enabled | The practice discipline AIDEX expresses. The practitioner curates AI-enabled output, remains the locus of judgment and accountability, contributes to institutional practice as an attributed and consenting participant. |
| **OAAD** | Open Source Software Agentic AI DevSecOps | A platform thesis: OSS + agentic AI + DevSecOps governance replaces the COTS business capability stack. The build-vs-buy calculus reframed by agentic AI. |

---

## Suggested reading order

1. **[Enterprise Agentic AI Platform Strategy](docs/Enterprise-Agentic-AI-Platform-Strategy.pdf)** — the umbrella. Read this first. Argues for an enterprise-owned, four-plane platform architecture with a staged maturity model. Addressed to CIO / CTO.
2. **[AEON white paper](docs/AEON-White-Paper.pdf)** — the control plane in depth. Six service planes specified; Enterprise IT operating model; multi-classification deployment; phased path; minimal coherent subset.
3. **[AIDEX white paper](docs/AIDEX-White-Paper.pdf)** — the experience subdomain. Eight-axis modularity (presentation, persona, role, authority, context, memory, modality, lineage); HCAE framework; multi-backend topology; Claude Cowork as deployed reference.
4. **[OAAD Strategic Brief](docs/OAAD-Strategic-Brief-v5.pdf)** — the OSS-replaces-COTS platform thesis. Addresses the build-vs-buy reframing under agentic AI.
5. **[The Next Shape of the IT Business Capability Model](docs/OAAD-The-Next-Shape-of-the-IT-Business-Capability-Model.pdf)** — extends OAAD into the broader business-capability-model question. Reframes the capability map around owned vs. rented substrate, develops the sovereignty-constrained application, and distinguishes the pattern from its architectural neighbors.
6. **Companion decks** — [Enterprise Agentic Platform Architecture](docs/Enterprise-Agentic-Platform-Architecture-Deck.pdf) · [AIDEX](docs/AIDEX-Deck.pdf) · [AIDEX / AEON](docs/AIDEX-AEON-Deck.pdf).

---

## Infographics

Visual companions to the corpus. The full argument lives in the source documents; these are for orientation and at-a-glance reference.

- **[NextGen Enterprise AI Architecture — landscape](infographics/NextGen-Enterprise-AI-Architecture-Infographic.png)** — the four-plane architecture in slide-friendly orientation (embedded above)
- **[NextGen Enterprise AI Architecture — portrait](infographics/EntAI-Architecture-Infographic.png)** — same architecture in tall format, expanded design principles, AEON core services, foundation layer, domain consumers, outcomes, and Longmire's AI Maxims
- **[Enterprise IT Agentic AI Platform Teams](infographics/EntAI-Platform-Team-Infographic.png)** — the four-platform operating model: AEON Control Plane Team, Enterprise AI Platform Team, AIDEX Experience Team, OAAD Capability Platform Team, and Domain AI Delivery Squads — with how the teams relate and the stand-up sequence
- **[OrdSA Construct](infographics/OrdSA-Construct.png)** — the methodologically-allied [Ordinal Systems Architecture](https://github.com/osa-ai-org/ordsa-ai) framework that orders this corpus: 7 ordinal layers (O0 Enterprise Intent → O6 Outcome/Audit/Feedback) with the four governance principles and alignment with TOGAF, ArchiMate, UAF, NIST AI RMF. Canonical home is the OrdSA repo; this copy is bundled here for navigability.

---

## Document index

| Document | Source | PDF |
|---|---|---|
| Enterprise Agentic AI Platform Strategy | [.docx](docs/Enterprise-Agentic-AI-Platform-Strategy.docx) | [.pdf](docs/Enterprise-Agentic-AI-Platform-Strategy.pdf) |
| Enterprise Agentic Platform Architecture Deck | [.pptx](docs/Enterprise-Agentic-Platform-Architecture-Deck.pptx) | [.pdf](docs/Enterprise-Agentic-Platform-Architecture-Deck.pdf) |
| AEON white paper | [.docx](docs/AEON-White-Paper.docx) | [.pdf](docs/AEON-White-Paper.pdf) |
| AIDEX white paper | [.docx](docs/AIDEX-White-Paper.docx) | [.pdf](docs/AIDEX-White-Paper.pdf) |
| AIDEX deck | [.pptx](docs/AIDEX-Deck.pptx) | [.pdf](docs/AIDEX-Deck.pdf) |
| AIDEX / AEON deck | [.pptx](docs/AIDEX-AEON-Deck.pptx) | [.pdf](docs/AIDEX-AEON-Deck.pdf) |
| OAAD Strategic Brief v5 | [.pptx](docs/OAAD-Strategic-Brief-v5.pptx) | [.pdf](docs/OAAD-Strategic-Brief-v5.pdf) |
| OAAD — The Next Shape of the IT Business Capability Model | [.docx](docs/OAAD-The-Next-Shape-of-the-IT-Business-Capability-Model.docx) | [.pdf](docs/OAAD-The-Next-Shape-of-the-IT-Business-Capability-Model.pdf) |

`.docx` and `.pptx` are the authoritative source; `.pdf` is provided alongside for browser-viewable rendering.

---

## Relation to OrdSA

enterprise-ai is the **canonical enterprise-scale deployment of [OrdSA (Ordinal Systems Architecture)](https://github.com/osa-ai-org/ordsa-ai)**. Where OrdSA specifies the layered authority, evidence, and execution-rights construct for agentic systems, this corpus develops the concrete enterprise-architectural shape — control plane (AEON), runtime, experience subdomain (AIDEX), capability platform (OAAD) — that an enterprise builds when it operationalizes OrdSA at platform scale.

The alignment runs in three dimensions:

- **Structural** — AEON's six service planes and the four-plane platform map cleanly onto OrdSA's seven ordinal layers (O0 Enterprise Intent → O6 Outcome/Audit/Feedback). A worked methodological appendix mapping the two is planned as a future companion paper.
- **Visual** — the [OrdSA construct infographic](infographics/OrdSA-Construct.png) is bundled in this corpus's infographic shelf alongside the four AI-EA infographics, since the AI-EA architecture cannot be read coherently without the construct it deploys.
- **Operational** — this corpus has adopted OrdSA's PR-first + ADR-as-PR governance ([ADR-EA-0001](decisions/ADR-EA-0001-adopt-ordsa-development-process.md)); the framing reflected here is ratified in [ADR-EA-0002](decisions/ADR-EA-0002-reframe-as-ordsa-exemplar.md).

For framework-builders evaluating OrdSA itself — read the [OrdSA construct repo](https://github.com/osa-ai-org/ordsa-ai) first. This corpus is the deployment view, not the construct.

---

## Governance

enterprise-ai operates under OrdSA-style governance: framework-level changes flow as **ADRs ratified by PR**; refinements, new papers within scope, and infographic additions flow as **ordinary PRs**. `main` is the released, citable surface; all changes land via PR from `dev` or a feature branch.

- [`CONTRIBUTING.md`](CONTRIBUTING.md) — the workflow, the framework-vs-content distinction, and what triggers an ADR
- [`decisions/`](decisions/) — the ADR index and ratified records ([ADR-EA-0001](decisions/ADR-EA-0001-adopt-ordsa-development-process.md) adopts this process)

---

## Audience

**Primary** — CIO, CTO, Chief Architect, CISO at defense and highly regulated enterprises: those running classified or mission systems, those bound to demonstrate first-party auditability of all agentic operations, those whose sovereignty posture makes vendor governance over their own operations unacceptable.

**Secondary** — enterprise architects, identity engineering, and the subdomain engineering functions that compose into AEON.

For an enterprise without those pressures, a rented vendor control plane may be the rational choice; the corpus says so explicitly rather than posing as a universal prescription.

---

## License

Licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE). You may share and adapt these works for any purpose, including commercial use, with appropriate attribution.

**Suggested citation:**

> Longmire, J. D. (2026). *[Document title]*. AEON / AIDEX / HCAE / OAAD architectural research corpus. https://github.com/osa-ai-org/enterprise-ai

---

## Contact

Correspondence: **jdlongmire@outlook.com** · ORCID [0009-0009-1383-7698](https://orcid.org/0009-0009-1383-7698)
