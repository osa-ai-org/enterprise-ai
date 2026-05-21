# Contributing to enterprise-ai

Thanks for reading the corpus closely enough to want to contribute. A few notes on how contributions flow.

## Two kinds of change

enterprise-ai distinguishes between **framework changes** and **content changes**, because they have different reversibility profiles. The split mirrors the OrdSA development process this corpus has adopted (see [ADR-EA-0001](decisions/ADR-EA-0001-adopt-ordsa-development-process.md)).

**Framework changes** modify what the corpus *is*: adding or redefining one of the constructs (AEON, AIDEX, HCAE, OAAD), changing the audience or positioning, revising framework alignment claims (e.g., the relationship with OrdSA), changing the license or citation model, or adopting a methodology that affects how the corpus itself is governed. These flow through ADRs as **PRs**:

1. *(Optional)* If the change is contentious or you want community signal first, open a **Framework Q&A** discussion describing the question before authoring the ADR.
2. Draft an ADR in `decisions/ADR-EA-NNNN-<slug>.md` (numbering is sequential, append-only) using [`decisions/TEMPLATE.md`](decisions/TEMPLATE.md) as a starting point.
3. Open a PR with the ADR. Apply the **`adr`** label. Discussion happens on the PR — the PR is the deliberation record, the merge is ratification.
4. Ratification requires explicit sign-off from the maintainer (currently @jdlongmire) and a comment-out period of at least one calendar week, unless the ADR is purely editorial, part of a maintainer-batched founding set, or invoked under a **maintainer-prerogative waiver** (see below).
5. Merged ADRs are immutable. A later ADR may supersede an earlier one; the earlier one stays in the tree marked `Superseded by ADR-EA-NNNN`.

### Maintainer-prerogative waiver

The one-week comment-out period exists to gather community signal. While the corpus has a sole maintainer (the current state), no community signal is available and the period is procedural ceremony.

The maintainer may **explicitly waive** the comment-out period for a specific ADR by posting a comment in the PR thread stating the waiver and its basis. To remain a legitimate waiver — rather than silent rule-skip — the comment must:

- Identify the ADR being waived (PR number is sufficient).
- State the basis. Acceptable bases include: substantive deliberation documented elsewhere (in-session conversation, related Discussion thread, or the ADR's own References section); the corpus's current sole-maintainer status; or the ADR being a refinement-grade follow-up to a recently-ratified parent ADR.
- Be visible on the PR before the merge button is pressed, so the waiver is part of the durable record.

The waiver is intentionally narrow. It does **not** apply to:

- ADRs that introduce a new construct, deprecate a construct, or revise the four-construct enumeration.
- ADRs that change audience, positioning, license, or the "independent research" disclaimer.
- Any ADR the maintainer has reason to believe a contributor (current or prospective) would want to comment on.

This clause is itself revisable as the corpus's contributor surface changes; superseding it requires a future ADR-EA-NNNN, not just a CONTRIBUTING.md edit.

See [`decisions/README.md`](decisions/README.md) for the navigable index of ratified ADRs.

**Content changes** — new papers in the existing scope, prose refinements, infographic additions, README cleanup, typo fixes, errata — flow as ordinary PRs. No ADR needed.

### Why PRs (not Issues) for ADRs

The PR *is* the ADR's lifecycle. Discussion on the PR is the deliberation, reviews are the consensus signal, the merge commit is the ratification timestamp, and the file at `decisions/ADR-EA-NNNN-<slug>.md` is the durable record. Issues are reserved for **gaps**, **implementation work**, and **umbrella tracking of multi-PR programs** — not for the decisions themselves.

## What goes where

| Change | Path | Mechanism |
|---|---|---|
| Add a new construct alongside AEON / AIDEX / HCAE / OAAD | `README.md` + new paper in `docs/` | ADR + PR |
| Redefine an existing construct's scope or role | `README.md` + relevant paper in `docs/` | ADR + PR |
| Audience or positioning shift (who the corpus addresses, the "independent research" framing) | `README.md` | ADR + PR |
| Add, remove, or revise a framework alignment claim (currently: methodologically allied with OrdSA) | `README.md` (Relation-to section) | ADR + PR |
| Change license, citation pattern, or attribution model | `README.md` + `LICENSE` | ADR + PR |
| Adopt a new governance practice that affects how the corpus is itself governed | `decisions/` (the ADR is the artifact) | ADR + PR |
| Add a new paper within an existing construct's scope | `docs/` + README index | PR |
| Add an infographic | `infographics/` + README's Infographics section | PR |
| Companion deck for an existing paper | `docs/` | PR |
| Prose refinements, typos, errata | anywhere | PR |

## Branch flow

- `main` is the released, citable surface.
- `dev` is the working branch — feature branches off `dev` are welcome but `dev` is acceptable for small changes.
- All changes land on `main` via PR. No direct commits to `main`.

## Style

- Prose, not jargon. If a sentence requires a glossary to parse, rewrite it.
- Cite frameworks and constructs by full name on first mention; acronym thereafter.
- New papers carry the standard author block and the "independent research" disclaimer.
- Diagrams committed as PNG are acceptable for high-fidelity infographics; for line diagrams and architecture sketches, prefer SVG / Mermaid / PlantUML as committed source.

## What this corpus is not

- It is **not** a vendor product spec.
- It is **not** an exhaustive treatment of every enterprise AI question — it focuses on the control plane and its subdomains.
- It is **not** the position of any author's employer or institution; everything published here is independent research.

If you're unsure whether your idea fits, open a **Framework Q&A** discussion before writing the PR. Cheaper than a rewrite.

## Artifact roles at a glance

| Artifact | Use for |
|---|---|
| **PR** | Concrete changes (content edits, ADRs, new papers, infographic additions). The PR is the change's lifecycle and record. |
| **Issue** | Gaps in the corpus, implementation work for tooling, umbrella tracking of multi-PR programs. Not the place where decisions get made. |
| **Discussion** | Pre-PR brainstorming, Framework Q&A, adoption stories. Output may inform a PR but isn't itself a durable record. |
