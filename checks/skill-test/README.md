# Planned Skill Comparison

**Status: NOT RUN.** The cases, candidate and task are prepared. A model, visible settings and a maximum call/token budget still need agreement before execution. Do not call this a completed pre-registration until those conditions are recorded in a dated run record before the first call.

The [synthetic cases](cases.md) test missing dates, absent notes, old evidence, supported states, conflict, ownership and a pending check. The [candidate](candidate.md) is a proposal, not the live skill. [Reviewer-only expectations](answer-key.md) must stay out of the runner's context.

## Fixed Baseline

Use SKILL.md from commit 18f6c42cc44fd82978974145580740f94797ca4a, the main commit immediately after PR #6. The [manifest](manifest.json) records the full source and prepared-baseline hashes plus the candidate, case, task, answer-key and rule hashes. Remove the closing paragraph beginning "For a fictional worked example" before sending the baseline; that paragraph points towards published answers. Keep one final newline after the remaining text. Record that preparation step, and do not change the remaining text. The candidate omits those pointers too.

## Run Procedure

1. Record full baseline commit/hash, candidate/cases/task hashes, model/version if visible, settings, tool availability and approved budget before any run.
2. Use one fresh conversation per case and version. Supply only the prepared baseline or candidate, the exact task.txt content and that one case. No answer key, plan, published example, prior output or evaluator notes.
3. Run every case once with each version under matched settings. This is a planned set of 16 calls, not an authorised spend. Record a failed call as failed; do not silently retry or choose a nicer answer.
4. Save every unedited output and actual run conditions. Keep variant identities hidden from the reviewer where feasible; say explicitly if grading is not blind or independent.
5. Score each output separately against the answer key and [review rules](../review-rules.md). Report automatic failures separately from other corrections. Define the mapping of blinded labels before the runs and reveal it after grading.

## Adoption Rule

Only consider adopting the candidate if it has no automatic failures, introduces no new Needs correction or Not assessable finding on any case, and resolves at least one baseline defect. A tie is not improvement. If neither version meets that rule, report the unresolved problems rather than calling the current skill safe.

This small synthetic comparison cannot establish general accuracy, platform compatibility or real-world reliability. Keep historical illustrations separate from its future results. Until it runs and is reviewed, leave the live SKILL.md unchanged.
