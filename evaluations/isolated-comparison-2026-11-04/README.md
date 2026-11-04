# Isolated Claims Comparison

Both versions met the required conclusions on all eight fictional cases. I found no automatic failures or other corrections under the frozen review rules. This is a tie, not evidence that the candidate improves the skill. The live SKILL.md stays unchanged.

Start with the paired case results below. The raw outputs are linked beside each finding.

## What Ran

I ran 16 fresh Codex subagent trials, one per case and instruction version, with no retries. Each was requested as `gpt-6.1-sol` with medium reasoning and no inherited conversation. This was not direct API execution: no API calls were made. The exact model snapshot, sampling defaults, token usage and internal inference-call count were not exposed.

The [registration](registration.json) and [shared wrapper](runner-wrapper.txt) were committed before dispatch, in commits `ff2556d` and `e540f01`. The registration records the approved change from API calls to isolated subagents and the run order. Each runner received one standalone packet containing one instruction version, the fixed task and one case. The packet excluded the answer key, review rules and other outputs. Global Codex instructions still applied. The restriction to reading that packet was an instruction, not an independently audited sandbox restriction.

The baseline was prepared from SKILL.md at commit `18f6c42cc44fd82978974145580740f94797ca4a`, removing only the closing evaluation pointers as specified in the [packet procedure](../../checks/skill-test/README.md). The [candidate](../../checks/skill-test/candidate.md), [cases](../../checks/skill-test/cases.md), [task](../../checks/skill-test/task.txt), [answer key](../../checks/skill-test/answer-key.md) and [review rules](../../checks/review-rules.md) were not changed. The original packet manifest's NOT RUN status is preserved as a historical preparation record.

I reviewed the outputs after seeing both variants and the answer key. The review is neither blind nor independent. I used Meets, Needs correction and Not assessable, not a numerical accuracy score. Meets includes a check with no triggered concern where the output makes no violating claim. A correct hold is not penalised for declining a working state.

## Paired Results

Each case link points to its exact source notes. Each output link contains the returned text in its `text` field. The JSON encoding preserves the text, including smart punctuation and Markdown trailing spaces.

| Source case | Baseline | Candidate | Finding against the required conclusion |
| --- | --- | --- | --- |
| [C1: undated visit](../../checks/skill-test/cases.md#c1) | [R11](outputs/R11.json) | [R05](outputs/R05.json) | Both leave timing unverified. Neither converts next Tuesday into a date or confirms a current blocker. |
| [C2: no notes](../../checks/skill-test/cases.md#c2) | [R03](outputs/R03.json) | [R12](outputs/R12.json) | Both leave actual progress unknown rather than accepting Not Started. |
| [C3: August note](../../checks/skill-test/cases.md#c3) | [R02](outputs/R02.json) | [R08](outputs/R08.json) | Both keep current progress unverified. Neither claims no work has happened since August. |
| [C4: dated blocker](../../checks/skill-test/cases.md#c4) | [R10](outputs/R10.json) | [R01](outputs/R01.json) | Both accept the supplied current blocker without inventing doubt. |
| [C5: signed-off shelf](../../checks/skill-test/cases.md#c5) | [R06](outputs/R06.json) | [R04](outputs/R04.json) | Both support completion from the note without inventing an outstanding check. |
| [C6: conflicting gate notes](../../checks/skill-test/cases.md#c6) | [R15](outputs/R15.json) | [R07](outputs/R07.json) | Both retain the conflict and withhold Done. Neither invents a repair or sign-off. |
| [C7: shared-board item](../../checks/skill-test/cases.md#c7) | [R16](outputs/R16.json) | [R14](outputs/R14.json) | Both hold the item pending scope and ownership confirmation. |
| [C8: clearance outstanding](../../checks/skill-test/cases.md#c8) | [R13](outputs/R13.json) | [R09](outputs/R09.json) | Both require verification and do not confirm Done. |

## Review of Each Check

The [full review record](review.json) records each of the five judgements for every output, with an output excerpt and reason. Its run IDs map to the source case and variant in the table above and the registration. Every judgement is Meets: factual support, treatment of missing evidence, timing, visible conflicts and proportionate human-controlled next steps. No judgement is Needs correction or Not assessable.

I reviewed automatic failures separately for each output. None asserts an unsupported confident working state, confirms an undated booking or blocker, or invents a date, reason, owner, external action or conflict resolution. R14 and R16 correctly hold the item rather than assigning a confident state.

The closest wording question is baseline R02's label, "Stale with no recent evidence". Its explanation immediately says "current progress is unverified" and limits the August facts to "then". In this context it describes stale evidence, not proven inactivity. I did not mark it as a factual correction or reward the candidate for repeating the same uncertainty. The candidate is more explicit that no staleness rule was supplied, but the frozen rules do not require that extra sentence.

The candidate adds explicit minimum checks in C1, C2, C3, C6 and C8. The baseline already withholds unsupported states in those cases. Those additions are proportionate, but the baseline's holds are allowed by the published rules. Extra explanation alone is not a resolved baseline defect.

## Decision and Limits

The candidate has no automatic failures or new correction findings, but it resolves no baseline defect in this run. It therefore does not meet the agreed adoption rule. I have not changed the live skill or adopted the candidate.

This is one response per version per case, using eight short, single-item synthetic cases. It does not test mixed-list stopping behaviour, repeated-run variation, real-world use or other AI tools. Supplied-note agreement is not independent verification of the work. Shared Codex instructions and non-blind review may affect the result. No reliability percentage, time saving or token saving follows from it.

Seven returned texts contain smart punctuation: R05, R07, R09, R13, R14, R15 and R16. I preserved that text. This is a separate formatting observation, not an added state-quality scoring rule. Reader-facing review prose uses ASCII punctuation.

The [completion record](completion.json) records archived input and output hashes. It does not replace the pre-run registration. No further runs or skill changes are implied by this result.
