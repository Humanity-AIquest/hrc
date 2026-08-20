# Clauses

One file per clause, named by identifier — `I.7.md`, `II.4.md`, `III.9.md`.

| Section | Range | Covers |
|---|---|---|
| I | I.1 – I.33 | Core Rights & Protections |
| II | II.1 – II.10 | Governance & Evolution |
| III | III.1 – III.9 | Operational Mandates |

## Status

`I.33.md` is present as a worked example of the format. The remaining 51 clauses
still live in `src/App.jsx` in the Web repository and need migrating here. That
migration is the first task in `../design/OPEN-WORK.md`.

## Editing

Do not edit a clause directly on `main`. Clause text changes only through the
amendment process in [GOVERNANCE.md](../GOVERNANCE.md). A pull request that edits
a clause without a linked ratified proposal will be closed.

The `consensus` field is written by the platform, not by hand.

## Why one file per clause

Amendments read as diffs. Every clause carries its own history. And `hrc_lookup`
can serve straight from the file rather than from a database that has to be kept
in sync with it.
