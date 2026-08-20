# Contributing

Contribution here is mostly not code. Arguing a clause, translating one,
objecting to one, or reviewing someone else's amendment all count and are
recorded the same way.

## Before anything

Read [GOVERNANCE.md](GOVERNANCE.md) and [AI_POLICY.md](AI_POLICY.md). They are
short and they are the rules.

You need to be a **verified member**. Membership is invite only during the
founding phase.

## Sign off every commit

```bash
git commit -s -m "your message"
```

The `-s` adds a `Signed-off-by` line. This is the
[Developer Certificate of Origin](https://developercertificate.org/) — you are
asserting that you have the right to contribute the work. Unsigned commits fail
the check.

We use a DCO rather than a contributor licence agreement deliberately. A DCO is a
line in a commit; a CLA is a legal document you sign before you may participate.
The lower barrier is the point.

## Declare your agent's role

If an agent helped, say so:

```
Co-Authored-By: Claude <noreply@anthropic.com>
AI-Role: assisted
```

Roles: `drafted`, `assisted`, `reviewed`, `none`. See
[AI_POLICY.md](AI_POLICY.md). Spelling and formatting need no declaration.

Declare honestly. We would rather hold an accurate record of heavy AI use than a
flattering one that is false, and under-declaring costs you your credential.

## Amending a clause

1. Open an issue using the **Amendment proposal** template.
2. Argue it. Objections are the point, not an obstacle.
3. If it survives, it goes to a vote of verified members.
4. On ratification, a maintainer opens the pull request against the clause file,
   linking the ratified proposal.

**Never open a pull request that edits a clause file directly.** It will be
closed. The constitution changes by vote, not by merge.

## Roadmap and documentation

These take ordinary pull requests. Roadmap documents in `roadmap/` render
directly on the website, so improvements there are visible immediately.

## Scale

Small, specific, answerable. One clause, one concern, one submission.

Reviewer capacity is the binding constraint in open source, and it is the reason
most projects are currently refusing agent contributions altogether. We accept
them because provenance makes accountability clear — but that does not make
review free. If you would not read it yourself, do not file it.

Bulk submissions are closed without review. Repeated bulk submission costs you
your credential.

## Conduct

[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md). Argue positions, never people.

Serious disagreement is the mechanism working. Contempt is not.
