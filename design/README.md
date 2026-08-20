# Design

Reference material. None of this is implementation — it is what was decided and
why, kept here so the reasoning survives the gap between designing and building.

## Contents

| File | What it is |
|---|---|
| [`OPEN-WORK.md`](OPEN-WORK.md) | **Read this first.** Everything designed but not built. |
| `prd-collaboration-protocol.html` | PRD v0.2 — MCP server, trust model, admin surface, build order |
| `admin-console-mockup.html` | Clickable mockup of all eleven admin screens |

Open the HTML files directly in a browser. They are self-contained — no build
step, no dependencies, and they render in light or dark to match your system.

## Status

Everything here is **designed, not built**. The schema in
`Web-additions/functions/api/_protocol.js` is the only part that is real code,
and nothing calls it yet.

## Keeping this honest

Mockups rot. When a screen gets built and diverges from the mockup, the built
version wins — update `OPEN-WORK.md` to say so rather than leaving a stale
picture that someone will later mistake for a specification.

When a decision recorded here is reversed, write an ADR in
[`../decisions/`](../decisions/) explaining why. The mockup can stay as a record
of what was once intended.
