# Claims vs. Evidence Checker

<p>
  <img alt="Status: Working tool" src="https://img.shields.io/badge/status-working%20tool-2563eb">
  <a href="LICENSE"><img alt="Licence: MIT" src="https://img.shields.io/badge/licence-MIT-lightgrey"></a>
</p>

Check whether the evidence you hold backs up a status in your tracker, such as a project's "on track" or a task's "done".

## Why

A status field is a claim, not a fact. If nobody checks it, it can drift. Something marked "done" still needs a check. Something marked "in progress" hasn't moved in months. Both look fine at a glance because the field says so. This keeps the record and the evidence apart, so you can see where they agree.

[![Recorded status compared with the evidence-supported state.](assets/diagrams/06-claims-vs-evidence-checker.svg)](SKILL.md)

**Not what you need?** This checks the status fields in a tracker you already have against the evidence for each item. If you're turning a meeting into a written record, you probably want [Evidence-Labelled Meeting Notes](https://github.com/shaunmarsden/evidence-labelled-meeting-notes). If you have two records, kept separately, that should both show the same thing, rather than one record and its evidence, [Do These Actually Match?](https://github.com/shaunmarsden/do-these-actually-match) fits better.

## Use It

Copy [SKILL.md](SKILL.md) and paste it into your AI tool (ChatGPT, Claude, Gemini or similar). Then paste in your tracker and any notes you have for each item. For each item you get:

- The recorded status next to what the evidence supports
- Any conflict between them, named precisely
- What to confirm before you trust or update the status

[The worked example](example/) is a made-up list of home renovation jobs. The tool catches a false "done" and a stale "in progress" that looked fine at a glance. It leaves two healthy items alone, including one whose label ("Blocked") might look like a problem in itself. [The second worked example](example-two/) is harder: two real notes on the same item that contradict each other.

Use [the blank template](templates/status-check-template.md) for your own tracker, and [the review checklist](checks/checklist.md) before you act on anything it flags.

<details>
<summary><strong>See exactly what it produces</strong></summary>

1. The recorded status and what the evidence supports, side by side for every item
2. Any conflict, named precisely, not just flagged as "off"
3. What to confirm before you trust or update the record
4. Healthy items called healthy, not buried under made-up concerns

</details>

You don't need to install anything or write any code to try it once.

## Before You Use It

This flags gaps. It doesn't act on them. You make every status update yourself.

## Feedback

Used it on a real tracker? [Start a discussion](https://github.com/shaunmarsden/claims-vs-evidence-checker/discussions) if it missed something or flagged a false positive.

## Part of a Family

This is one of a family of free tools that take patterns from [practical-ai-sales-workflows](https://github.com/shaunmarsden/practical-ai-sales-workflows) and use them outside sales. The rest are in [sibling-projects](https://github.com/shaunmarsden/sibling-projects). Not sure which one fits? Try [the interactive picker](https://shaunmarsden.github.io/sibling-projects/), or paste a description of your problem into an AI chat with [the router](https://github.com/shaunmarsden/sibling-projects/blob/main/ROUTER.md).
