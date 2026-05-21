# Architectural Decision Records

This directory holds the **ratified ADRs** for enterprise-ai — append-only records of framework-level decisions and the reasoning behind them.

For the authoring process, see [`../CONTRIBUTING.md`](../CONTRIBUTING.md). For the ADR shape, see [`TEMPLATE.md`](TEMPLATE.md).

## Index

| ADR | Status | Date | Title |
|---|---|---|---|
| [0001](ADR-EA-0001-adopt-ordsa-development-process.md) | Proposed | 2026-05-21 | Adopt OrdSA-style development process for enterprise-ai |

## Conventions

- **Numbering** is sequential and never reused: `ADR-EA-0001`, `ADR-EA-0002`, etc. A retracted-before-merge draft does not consume a number; ADRs are numbered at PR-open time and the number is held until merge or withdrawal.
- **Filename** is `ADR-EA-NNNN-<slug>.md` where `<slug>` is lowercase-kebab-case (e.g., `ADR-EA-0001-adopt-ordsa-development-process.md`).
- **Status** values: `Proposed` (PR open), `Accepted` (PR merged), `Superseded by ADR-EA-NNNN` (a later ADR replaces this one). Withdrawn drafts don't enter the index.
- **Immutability**: once an ADR is merged, the file is not edited except for typo fixes and the addition of a `Superseded by` note in the header. Substantive revision happens by writing a new ADR that supersedes the old one.

## How to read this index

The entries here are durable claims. If you're citing or extending enterprise-ai, ADRs explain the *why* behind the corpus as it stands today — they tell you which framework alternatives were considered and rejected, so you can judge whether your context warrants reopening a question.

If an entry says **Superseded by**, follow the chain — the latest ADR in the chain is the active position. Earlier ADRs in the chain remain in the tree as history, but should not be cited as current.
