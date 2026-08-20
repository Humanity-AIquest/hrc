# 0003 — Vouching, not identity documents

**Status:** Accepted · 20 August 2026

## Context

Every downstream guarantee — attribution, the agent firewall, one member one vote
— rests on knowing that a member is a distinct human being. Options considered:
government identity documents, proof-of-personhood protocols, phone
verification, and social vouching.

## Decision

Vouching, seeded by an invite-only founding cohort that is verified by hand.

Two vouches from members in good standing admit a member. Vouches work like
professional recommendations: standalone, public, unlimited in number, each
optionally carrying a statement. Additional vouches beyond two confer no extra
rights — they are signal.

Administrators may override, with a reason recorded in the public audit trail.
The override exists so the process cannot deadlock during demonstrations or at
the founding edge. It is not meant to be routine.

## Why

Requiring identity documents inside a digital-rights project is an irony critics
would never let go of, and it would be fair of them. It also hard-excludes people
without documents and people in exactly the regions this constitution most claims
to serve. Proof-of-personhood protocols carry their own political baggage with
precisely this audience.

Vouching is cheap, consistent with the mission, and it builds the social graph
the platform needs later anyway.

## Consequences

**Accepted weaknesses.** Vouching is gameable at small scale. A determined group
could admit each other. The mitigation is that vouchers stake their own standing:
if a member is revoked for cause, everyone they vouched for is flagged for review.
That is reactive, not preventive, and we accept it.

**Growth is bounded by the graph.** A feature early — it keeps the founding
cohort coherent — and a constraint later.

**Flagged is not revoked.** A cascade marks members for review rather than
removing them. A bad voucher does not prove a bad member, and treating it that
way would punish people for someone else's conduct.

**Everything rests on the founding cohort.** Their integrity determines the
integrity of every chain that descends from them. Invite carefully; there is no
technical fix for a bad root.
