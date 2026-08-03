# Claims vs. Evidence Checker

<p>
  <img alt="Status: Working tool" src="https://img.shields.io/badge/status-working%20tool-2563eb">
  <a href="LICENSE"><img alt="Licence: MIT" src="https://img.shields.io/badge/licence-MIT-lightgrey"></a>
</p>

Check whether a tracked status, a project's "on track", a task's "done", is actually supported by the evidence held, separate from what the tracker records.

## Why

A status field is a claim, not a fact. Left unchecked, it drifts: something marked "done" that still needs a check, something marked "in progress" that has not moved in months, all reading as fine at a glance because the field says so. This holds the record and the evidence apart so it is clear where they actually agree.

![Recorded status compared with the evidence-supported state.](assets/diagrams/06-claims-vs-evidence-checker.svg)

## Use It

Copy [SKILL.md](SKILL.md) and paste it into your AI tool (ChatGPT, Claude, Gemini, or similar), then paste in your tracker and whatever notes exist for each item. It produces, per item:

- The recorded status next to what the evidence actually supports
- Any conflict between them, named specifically
- What to confirm before trusting or updating the status

See [the worked example](example/): a fictional home renovation punch list, catching a false "done" and a stale "in progress" that looked fine at a glance, while correctly leaving two genuinely healthy items alone, including one whose status label alone ("Blocked") could itself read as a concern. [The second worked example](example-two/) tests a harder case: two genuine notes on the same item that flatly contradict each other.

Use [the blank template](templates/status-check-template.md) for your own tracker, and [the review checklist](checks/checklist.md) before acting on anything it flags.

<details>
<summary><strong>See exactly what it produces</strong></summary>

1. Recorded status and evidence-supported state, shown side by side for every item
2. Any conflict, named specifically, not just flagged as "off"
3. What to confirm before trusting or updating the record
4. Genuinely healthy items called healthy, not buried under manufactured concerns

</details>

No installation, project, or coding required to try it once.

## Before You Use It

This flags gaps, it does not act on them. Every status update stays a deliberate action you make yourself.

## Licence

MIT.

## Feedback

Used it on a real tracker? [Start a discussion](https://github.com/shaunmarsden/claims-vs-evidence-checker/discussions) if it missed something or flagged a false positive.

## Part of a Family

This is one of a family of free tools generalising [practical-ai-sales-workflows](https://github.com/shaunmarsden/practical-ai-sales-workflows) patterns beyond sales. See [sibling-projects](https://github.com/shaunmarsden/sibling-projects) for the rest, or use [the router](https://github.com/shaunmarsden/sibling-projects/blob/main/ROUTER.md) if you are not sure which one actually fits.
