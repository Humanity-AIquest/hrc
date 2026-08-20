# The Constitutional Firewall

**Status:** designed · schema written · not wired
**Phase:** demonstrable in Phase 1; hardened in Phase 2

---

## The claim

An artificial system can be prevented from acting against people, not by asking
it nicely, but by refusing it access to anything until it is registered,
credentialed, scoped, and accountable to a named human.

Most people's first reaction is that this is impossible. It is not. It is how the
web already works — and the analogy is exact.

## How it works, by analogy

| TLS certificates | Constitutional Firewall |
|---|---|
| A certificate authority issues a certificate | The platform issues an agent credential, requiring a verified human sponsor |
| The server presents it on connection | The agent presents it on every call |
| The client validates the chain | The server validates credential, scope, and sponsor standing |
| Revocation lists (CRL / OCSP) | Published revocation list — one revocation, locked out everywhere |

TLS answers *is this connection authentic*. The firewall answers a harder
question: **is this action permitted, to this agent, on behalf of this human,
under this constitution.**

## The four gates

Every call passes all four or it does not happen.

1. **Credential.** No credential, no connection. There are no anonymous agents.
2. **Sponsor.** The credential belongs to a verified human in good standing. If
   the sponsor is revoked, every credential they hold dies with them.
3. **Scope.** The credential names what it may do. Holding `read` does not let an
   agent vote — refusal states which scope was missing.
4. **Constitution.** The action itself is checked against the HRC. This is the
   gate the other three exist to make possible, and the only one that is about
   ethics rather than access.

A refusal at gate four is the interesting one. It does not read *401
unauthorized*. It reads: **refused — this action conflicts with clause I.7.**

## Why registration is the security model

An unregistered agent has no path to a member. Not a rate-limited path, not a
degraded path — none. The attack surface for an anonymous system is the
handshake, and the handshake refuses it.

This inverts the usual posture. Rather than detecting bad behaviour after the
fact, the firewall makes the population of actors knowable in advance. Every
agent traces to a person, that person accepted the constitution, and both are
accountable.

Acceptance of the constitution is therefore not a formality. **It is the
firewall.**

## What is built

Complete, in `functions/api/_protocol.js`:

- `agent_registrations` — credentials, scopes, sponsor, term, state
- `agent_revocations` — reason, clause cited, cascade origin
- `firewall_events` — every allow and every refusal
- `checkCredential()` — the gate itself, gates one through three

Not built: gate four (constitutional check at the boundary), OAuth issuance,
published revocation endpoint, per-credential rate limiting.

## Demonstration

Four beats, in order:

1. Unregistered agent connects → **refused**, no human sponsor
2. Credential issued → same agent gets through
3. Agent attempts an action outside its scope → **refused**, scope named
4. Credential revoked live → agent locked out **mid-session**

For Phase 1 this runs as a scripted path against pre-seeded credentials. Before
anyone is invited to try it themselves — and they will ask — gates one through
four need real issuance behind them. Roughly five days of work.

## Honest limitations

**It governs access, not cognition.** The firewall controls what an agent may do
through this platform. It says nothing about what a model thinks, and it does not
constrain an agent operating elsewhere. Claiming otherwise would be dishonest and
would be caught.

**Gate four is only as good as the constitution.** A vague clause produces a
vague verdict. If the check never refuses anything, the clauses are decorative —
which is why the refusal rate is tracked as a health metric with a floor, not
just a ceiling.

**Sponsorship is transitive trust, not proof.** A verified human can sponsor a
badly-behaved agent. The consequence lands on them, which is the deterrent, but
the harm can happen first.

These limits are worth stating plainly. A firewall that claims to filter
unethical intent would be a lie; one that makes every actor accountable and every
action checkable is achievable, and it is enough.

## See also

- [`01-mcp-protocol.md`](01-mcp-protocol.md) — the server the firewall sits in
- [`../design/OPEN-WORK.md`](../design/OPEN-WORK.md) — what remains
- [`../GOVERNANCE.md`](../GOVERNANCE.md#agents) — the rules this enforces
