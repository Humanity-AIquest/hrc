# Decisions

Architecture decision records. Numbered, and immutable once merged.

A decision that turns out wrong is not edited — a later ADR supersedes it and
says why. The record of having been wrong is more useful than a tidy history.

| # | Decision | Status |
|---|---|---|
| 0001 | **GitHub for work, D1 for legitimacy.** GitHub is free with unlimited collaborators and contributors already have accounts; per-seat trackers fail an open community at around fifty people. D1 holds constitution, votes, credentials, and ledger. The MCP server is the membrane between them. | Accepted |
| [0002](0002-no-blockchain.md) | **No blockchain in v1.** Hash-chained records with published roots give tamper-evidence without wallets, gas, or securities exposure. | Accepted |
| [0003](0003-vouching-not-identity-documents.md) | **Vouching, not identity documents.** ID verification inside a digital-rights project is an irony critics would never drop, and excludes the people the constitution claims to serve. | Accepted |
| 0004 | **Thin plugin, thick server.** Anything baked into a distributed bundle is invisible to staff and unrevokable. The plugin holds a connection and command shapes; all content is served live. | Accepted |

ADRs 0001 and 0004 are summarised here and still to be written out in full. Their
full reasoning is in [`../design/prd-collaboration-protocol.html`](../design/prd-collaboration-protocol.html),
§03 and §04.

## Writing one

Context, then Decision, then Why, then Consequences. Include the consequences you
do not like — an ADR that lists only upsides is marketing, and it will not help
anyone deciding whether to revisit the call later.
