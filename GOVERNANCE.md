# Governance

How decisions get made here. This document is itself amendable by the process it
describes.

## The short version

Verified humans deliberate on clauses. Clauses reach consensus and are ratified.
Agents help, but never decide, and never act without a human sponsor.

## Membership

### Phase 1 — invite only

The founding cohort is invited directly. Every invited member is manually
verified by an administrator before their account becomes active. This is
deliberate: the vouching graph needs honest roots, and there is no way to
bootstrap that except by hand.

### Vouching

Beyond the founding cohort, admission is by vouching. A vouch works like a
professional recommendation — it is a standalone, public endorsement of a
person, it carries optional text, and a member may hold as many as people care
to give.

- **Two vouches admit a member.** Both must come from members in good standing.
- **A member may hold any number.** Additional vouches beyond two do not confer
  extra rights; they are a public signal, nothing more.
- **Vouchers stake their standing.** If a member is revoked for cause, everyone
  who vouched for them is flagged for review. Vouching is not free.
- **An administrator may override.** For demonstrations, founding members, and
  edge cases. Every override is logged to the public audit trail with a reason.
  The override exists so the process never deadlocks — not so it can be routine.

### Standing

Standing is time as a verified member in good conduct. Some capabilities require
it — drafting amendments requires two sealed contributions; vouching for others
requires ninety days. These thresholds are set in the scope registry and are
themselves amendable.

## Agents

No agent reaches a member or writes anything until it holds a credential issued
to a verified human sponsor. Credentials carry scopes, expire, and can be
revoked. The revocation list is public.

An agent owes a duty of advocacy to its human, bounded by this constitution. It
argues their position; it does not defect from the HRC to do so.

Agents propose. Humans dispose. Any action that changes the public record
requires explicit human confirmation in the session where it happens.

## Deliberation

1. **Argument.** Any member in good standing may file a position, objection, or
   supporting case on any clause. Attributed and recorded.
2. **Amendment.** A member with standing drafts replacement text with a
   rationale. It is checked against the rest of the constitution before it can
   be filed. Conflicts must be resolved or argued for explicitly.
3. **Voting.** Amendments that survive debate go to a vote of verified members.
   One member, one vote. Proxy voting is permitted within bounds the member sets
   in advance and can revoke at any time.
4. **Ratification.** A clause passing threshold is ratified into the working
   version of the HRC.

> **Open question, deliberately unresolved.** What consensus threshold ratifies a
> clause into V1, and who certifies it? This is a constitutional question, not a
> product decision. It will be put to the founding cohort as their first
> substantive vote rather than settled by the maintainers.

## Contribution record

Every contribution is sealed to a named human, hash-chained, and timestamped
server-side. Contributions are not only code or clause text — argument,
objection, translation, and review all count and are recorded the same way.

AI involvement is **declared by the contributor**, never inferred. See
[AI_POLICY.md](AI_POLICY.md).

## Roles

| Role | Can |
|---|---|
| Invited | Read everything; act once verified |
| Member | Argue, vote, record contributions |
| Member with standing | Draft amendments, vouch for others |
| Steward | Approve content changes, promote releases, issue credentials |
| Administrator | All of the above, plus override and revocation |

Steward and administrator actions are logged publicly without exception.

## Amending this document

By the process above. Governance is a clause like any other.

## Current stewards

See [MAINTAINERS.md](MAINTAINERS.md).
