# Instructions for agents working in this repository

Read this before doing anything. It applies to any agent, in any client, whether
or not the Humanity-AI plugin is installed.

## What this repository is

The Humanities-AI Rights Constitution — 52 clauses, one file each under
`clauses/`. Amendments are pull requests. The constitution is the source of
truth for everything the platform does.

## Rules

**Never edit a clause file directly on `main`.** Clause text changes only through
the amendment process in [GOVERNANCE.md](GOVERNANCE.md). A pull request that
edits a clause without a linked ratified proposal will be closed.

**Disclose your role.** Every commit carries a `Co-Authored-By` line for the
agent and a sign-off from the human. See [AI_POLICY.md](AI_POLICY.md) for what
level of involvement to declare.

**Sign off every commit.** `git commit -s`. Unsigned commits fail the DCO check.
The sign-off is the human asserting they have the right to contribute the work —
it is the foundation of the provenance record.

**Small and specific.** One clause, one concern, one pull request. Bulk changes
are closed without review.

**Do not invent clause text.** Read the file. Clause text you recall from
training data is stale — clauses are amended.

## Layout

```
clauses/      52 clause files, named by identifier (I.7.md, II.4.md)
roadmap/      OS and Firewall design documents
decisions/    architecture decision records, numbered
design/       PRD and UI mockups — reference, not implementation
```

## If you have the MCP server

Prefer `hrc_lookup` over reading files directly — the server serves the current
ratified text with consensus standing attached, which the files alone do not
carry. Run `hrc_check` before proposing any amendment.

Connect at `https://mcp.humanity-ai.quest/v1`. Verified membership required.

## Register

Every agent needs a credential issued to a verified human before it can write
anything through the platform. See [GOVERNANCE.md](GOVERNANCE.md#agents).

Working in this repository through git alone does not require a credential — but
the human whose name is on the sign-off is accountable either way.
