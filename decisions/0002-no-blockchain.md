# 0002 — No blockchain in v1

**Status:** Accepted · 20 August 2026

## Context

The design calls for a tamper-evident record of contributions, and "smart
contract" appeared in early framing of the trust layer. A chain was considered
seriously.

## Decision

No blockchain. Contribution records are hash-chained rows in D1, with chain roots
published at intervals so that anyone can verify history independently.

## Why

The property actually required is **tamper-evidence** — that a rewrite is
detectable by someone who did not write the record. A hash chain with published
roots delivers exactly that.

A chain would additionally bring wallet onboarding friction for non-technical
members, gas costs, a key-loss support burden nobody has staffed, securities
exposure the moment anything resembling a token exists, and a permanent "crypto
project" framing that changes which conversations are available. That is a
substantial cost for a property already obtained by cheaper means.

## When to revisit

If federation to independently operated instances requires trustlessness between
parties who have no reason to trust our published roots. That is a genuinely
different problem from the one we have, and a far easier case to make when it
actually arrives.

## Consequences

**Verification depends on us publishing honestly.** A hash chain proves internal
consistency; it does not prove we published every entry. Mitigate by publishing
roots to at least one venue outside our control, so that suppressing a root
requires cooperation we do not have.

**No trustless federation.** Another community forking the constitution cannot
verify our ledger without trusting our roots. Acceptable while there is one
instance; the trigger for revisiting.

**We forgo the fundraising narrative** that a token would offer. Deliberate. It
would attract the wrong capital for a project whose stated purpose is returning
value to people rather than to financial intermediaries.
