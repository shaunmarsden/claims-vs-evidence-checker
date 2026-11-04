# Claims vs. Evidence Checker

<p>
  <img alt="Status: Illustrative examples" src="https://img.shields.io/badge/status-illustrative%20examples-2563eb">
  <a href="LICENSE"><img alt="Licence: MIT" src="https://img.shields.io/badge/licence-MIT-lightgrey"></a>
</p>

Check whether the evidence you hold backs up a status in your tracker, such as a project's "on track" or a task's "done".

## Why

A status field is a claim to check. Something marked "done" may still need verification. An old "in progress" entry may no longer reflect what is happening. These instructions ask an AI to compare the record with the supplied notes, not to verify the work itself. No recent note is not proof that nothing has happened.

[![Recorded status compared with the evidence-supported state.](assets/diagrams/06-claims-vs-evidence-checker.svg)](SKILL.md)

These are possible findings, not fixed replacements for each status. "In progress" does not always mean stale, and a blocked item needs current evidence before it can be called confirmed.

**Not what you need?** This checks the status fields in a tracker you already have against the evidence for each item. If you're turning a meeting into a written record, you probably want [Evidence-Labelled Meeting Notes](https://github.com/shaunmarsden/evidence-labelled-meeting-notes). If you have two records, kept separately, that should both show the same thing, rather than one record and its evidence, [Do These Actually Match?](https://github.com/shaunmarsden/do-these-actually-match) fits better.

## Use It

Copy [SKILL.md](SKILL.md) and paste it into any AI chat. Then paste in an approved tracker and the notes you have for each item. The instructions ask for:

- The recorded status next to what the evidence supports
- Any conflict between them, named precisely
- What to confirm before you trust or update the status

[The first example](example/) uses four fictional home renovation jobs. Its output flags an outstanding cabinet check and a tiles entry with no update for three months. It also calls two other items healthy, but the [review](example/review.md) explains why the notes do not establish that the electrician booking is current or that the hallway work has not started.

[The second example](example-two/) uses two fictional notes that disagree about whether a fence is finished. The output surfaces that conflict, but the [review](example-two/review.md) notes that it overstates how specific the first note is.

Both examples are illustrations, not logged model tests. The repository does not record the model, exact run instructions or settings. It has no measured accuracy or tool-by-tool compatibility results.

The [later illustration review](evaluations/illustration-calibration.md) applies explicit rules to both saved outputs. The [planned skill comparison](checks/skill-test/README.md) prepares a separate test; it has not been run and the live skill is unchanged.

Use [the blank template](templates/status-check-template.md) for your own tracker, and [the review checklist](checks/checklist.md) before you act on anything it flags.

<details>
<summary><strong>See the requested output</strong></summary>

1. The recorded status and what the evidence supports, side by side for every item
2. Any conflict, named precisely, not just flagged as "off"
3. What to confirm before you trust or update the record
4. Healthy items called healthy, not buried under made-up concerns

</details>

You don't need to install anything or write any code to try it once.

## Before You Use It

This asks an AI to flag gaps. It does not inspect the work or change your tracker. Check its conclusions against the source, including dates, missing notes and unresolved conflicts. You make every status update yourself.

Use only material you are allowed to share with your chosen AI tool. Remove private details that the check does not need.

## Repository Checks

Pull requests and changes to main run offline checks for relative links, heading anchors, punctuation and SVG XML. These do not test AI output or external websites. With Python 3.11 or newer, run:

```sh
python3 -m unittest discover -s checks -p 'test_*.py' -v
python3 checks/check_repository.py
```

The checker reads Git-tracked files, so stage new documentation first. It supports the inline Markdown and HTML link forms used here, not all possible Markdown syntax.

## Feedback

Used it on a real tracker? [Start a discussion](https://github.com/shaunmarsden/claims-vs-evidence-checker/discussions) if it missed something or flagged a false positive.

## Part of a Family

This is one of a family of free tools that take patterns from [practical-ai-sales-workflows](https://github.com/shaunmarsden/practical-ai-sales-workflows) and use them outside sales. The rest are in [sibling-projects](https://github.com/shaunmarsden/sibling-projects). Not sure which one fits? Try [the interactive picker](https://shaunmarsden.github.io/sibling-projects/), or paste a description of your problem into an AI chat with [the router](https://github.com/shaunmarsden/sibling-projects/blob/main/ROUTER.md).
