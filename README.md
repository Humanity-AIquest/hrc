# The Humanities-AI Rights Constitution

The HRC — 52 clauses governing how artificial systems and people share a planet.
Sometimes called the Hippocratic Oath for AI. This repository is its source of
truth: one file per clause, amendments as pull requests, every change attributed
to a named human.

**[humanity-ai.quest](https://humanity-ai.quest)**

## Status

**Drafting v1.** The constitution is not ratified. Clauses are being argued,
amended, and voted on by the founding cohort. Membership is currently invite
only.

## What is here

```
clauses/      52 clause files, one per clause
roadmap/      OS and Firewall design documents
decisions/    architecture decision records
design/       PRD and admin console mockups — see design/OPEN-WORK.md
```

## Taking part

Read [GOVERNANCE.md](GOVERNANCE.md) first. In short:

1. **Get verified.** Invite only for now. Beyond the founding cohort, two vouches
   from members in good standing admit you. Vouches work like professional
   recommendations — public, standalone, and you may hold as many as people care
   to give.
2. **Argue.** File positions and objections on any clause.
3. **Amend.** With standing, draft replacement text. It is checked against the
   rest of the constitution before it can be filed.
4. **Vote.** One member, one vote. Proxy voting within bounds you set and can
   revoke.

## Bring your own agent

Agents are welcome here, and the reason is [AI_POLICY.md](AI_POLICY.md): every
contribution is attributed to a verified human, disclosed as to the agent's role,
and checked against the constitution before it lands.

Most projects are currently refusing agent contributions, with good reason. We do
not need to, because we fixed accountability at the root rather than banning the
tool.

Install the [plugin](https://github.com/Humanity-AIquest/plugin), or connect any
MCP-capable client directly:

```json
{
  "mcpServers": {
    "humanity-ai": {
      "type": "http",
      "url": "https://mcp.humanity-ai.quest/v1"
    }
  }
}
```

No agent reaches a member or writes anything until it holds a credential issued
to a verified human sponsor. Credentials carry scopes, expire, and can be
revoked — the revocation list is public.

## Clause files

Named by identifier: `I.7.md`, `II.4.md`, `III.9.md`. Sections are Core Rights
(I), Governance & Evolution (II), Operational Mandates (III).

Never edit a clause directly on `main`. Clause text changes only through the
amendment process.

## Licence

- **Constitution text** — [CC BY-SA 4.0](LICENSE). Copy it, translate it, fork
  it, build on it. Derivatives stay open. A constitution nobody may copy is not
  much of a constitution.
- **Code** — [AGPL-3.0-or-later](LICENSE-CODE). If you run a modified version as
  a service, the modifications stay available to the people using it.

## Contact

Open an issue, or [humanity-ai.quest](https://humanity-ai.quest).
