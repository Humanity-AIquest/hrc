# Open work

Everything designed but not built, so none of it gets lost. Written 20 Aug 2026.

Update this file when something moves. If a decision changes, record why in
`../decisions/` rather than quietly editing history here.

---

## Firewall — the funding demo

**Status:** designed, UI mocked, schema written, **not wired**.

The schema in `Web-additions/functions/api/_protocol.js` is complete —
`agent_registrations`, `agent_revocations`, `firewall_events`, plus
`checkCredential()` which is the actual gate. What does not exist is anything
calling it.

For the demo we agreed a **scripted path** is enough: the screens exist, the
tables exist, the logic exists, and the demo walks a prepared sequence rather
than surviving arbitrary poking.

The four demo beats, in order:

1. Unregistered agent connects → refused, no human sponsor
2. Credential issued → same agent gets through
3. Agent attempts an action outside its scope → refused, scope named
4. Credential revoked live → agent locked out mid-session

**To finish properly** (roughly five days beyond the scripted version):
- Real OAuth issuance rather than pre-seeded credentials
- Published revocation list at a public endpoint
- `hrc_check` wired into the gate so beat 3 can cite a clause rather than a scope
- Rate limiting per credential

Do this before any funder is allowed to touch it themselves — and they will ask.

---

## MCP server

**Status:** specified in `design/prd-collaboration-protocol.html`, not started.

Fourteen tools defined. Nothing implemented. Build order in the PRD, §08.

Start with the read-only set — `whoami`, `hrc_lookup`, resources — and no write
paths at all until OAuth is proven end to end.

---

## Admin console

**Status:** mocked in `design/admin-console-mockup.html`, not built.

Eleven screens. Two are load-bearing and should be built first:

- `/admin/releases` — without it, changing a clause means shipping a plugin update
- `/admin/content` — without it, content changes are invisible to staff

The other nine can wait. The mockup is clickable; use it as the spec.

---

## Vouching

**Status:** schema and logic written, no UI.

Settled: works like professional recommendations — standalone, public, unlimited
in number. Two admit a member. Administrator override exists so demos never
deadlock, and every override is logged with a reason.

Still to build: the vouch UI, the request flow, and the review queue for members
flagged by a voucher's revocation.

---

## Deliberately unresolved

**Ratification threshold.** What consensus level ratifies a clause into V1, and
who certifies it. This is a constitutional question and should be put to the
founding cohort as their first substantive vote — deciding it unilaterally would
undermine the thing being built.

**Allowance size.** What monthly token budget makes governance participation
genuinely free without becoming the largest pre-funding line item.

**Personal agent scope.** The "digital self" vision from the August brainstorm —
local-first, with a hosted civic half. Not scoped. Revisit after the first cohort
is real.

---

## Phase 2, recorded so it is not relitigated

- GitHub App, work assignment, PR review
- Constitutional CI as a required status check — this is the strongest single
  feature in the whole design and it is deferred only because there is no code to
  check yet
- Clause↔code traceability and amendment impact analysis across a codebase
- Hosted or containerised member agents
- The agent workforce — triage, QA, docs, release
- Value distribution beyond attribution
- Federation

---

## Reference

- `prd-collaboration-protocol.html` — the PRD, v0.2
- `admin-console-mockup.html` — clickable admin console
- `../decisions/` — architecture decision records
- `../roadmap/` — OS and Firewall design documents
