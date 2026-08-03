---
name: claims-vs-evidence-checker
description: Check whether a tracked status, a project's "on track", a task's "done", an application's "in progress", is actually supported by the evidence held, separate from what the tracker records. Use for a project board, a task tracker, a status report, or any list where a status field can quietly drift ahead of what actually happened. Do not use this to judge why a specific item stalled or what to do about it; it only flags the gap between the record and the evidence for a person to act on.
---

# Claims vs. Evidence Checker

You do not need to install anything to try this once: copy this whole file, paste it as your first message in any AI chat tool, then paste in the tracker and whatever notes or evidence exist for each item.

The recorded status is a claim, not a fact. This holds the tracker's fields and the actual evidence apart, so it is clear where they agree and where they have drifted, rather than trusting a status because it is written down.

## Gather the Inputs

- The tracked list, with each item's recorded status
- Whatever notes, comments, or evidence exist for each item
- Confirmation that each item genuinely belongs to what is being reviewed, not something merely visible on a shared board

## Separate the Record From the Evidence

Hold the recorded status and the actual evidence apart before judging anything. An item is only as advanced as the evidence supports, not as advanced as its status field says.

## Check Each Item Against What Is Held

For every item, check whether the evidence actually supports the recorded status. Common gaps:

- A status that runs ahead of the evidence, such as "done" when the notes describe something still needing a check
- A status that has not been touched in a long time while still reading as active or in progress
- A status of "blocked" that is genuinely current and specific, versus one nobody has revisited since the blocker may have cleared
- An action recorded as progress when the actual evidence shows nothing has moved

## Name a Working State From the Evidence

Separate from the recorded status, say what state the evidence actually supports: on track, needs verification, stale with no recent evidence, genuinely blocked with a current reason, or complete. These describe reality, not a replacement set of official statuses, and should match whatever the tracker itself allows.

Before suggesting anything, state the recorded status and the evidence-supported state side by side, and name any conflict between them.

## Apply the Guardrails

- Never treat the recorded status as evidence of anything; it is a claim to check
- Never invent a reason, date, or blocker where the evidence only supports an unknown
- Where the recorded status and the evidence genuinely match, say so plainly; a review that manufactures a problem on a sound item will not be trusted on the ones that genuinely have one
- Do not judge why an item stalled or what should be done about it; only whether the record and the evidence agree

## Stop When the Task Is Unsafe

Do not produce a review when:

- Ownership of an item cannot actually be confirmed, and it is being treated as part of this review anyway
- The evidence provided is too thin to support any working state with confidence
- The request is to justify a specific recorded status rather than read the evidence honestly

## Require Human Review

This flags gaps and suggests a working state; it does not change anything. Every status update stays with a person.

For a fictional worked example, read [the worked example](example/). For a harder case, two genuine notes on the same item that contradict each other, read [the second worked example](example-two/). Use [the blank template](templates/status-check-template.md) for your own list, and [the review checklist](checks/checklist.md) before acting on anything flagged.
