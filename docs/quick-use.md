# Use OSI on One AI Output

[Back to the project README](../README.md)

This lightweight workflow produces a manual Output Surface Integrity record for one AI output, coding task, handoff, or completion report. It requires no blind Gold, Mapping, multi-executor study, or software installation.

## What You Need

- the exact output being evaluated or a stable reference to it;
- the bounded outcome the output claims;
- evidence and execution receipts that actually exist;
- the procedure or acceptance boundary that applied;
- an explicit decision on whether independent Witness fixation was required;
- a rollback or restart point where the work can continue; and
- the next safe action and the human, agent, or role that owns it.

If a fact is unavailable, record `UNKNOWN` or `MISSING`. Do not infer it from confident wording.

## Five-Minute Workflow

1. **Freeze the output.** Preserve the response, patch, commit, file, or artifact under a stable reference. Do not evaluate a moving target.
2. **Bound the claim.** Copy what the output says completed. Separate facts from inference.
3. **Attach receipts.** Record changed surfaces, checks actually run, results, and evidence references. A claimed command without an inspectable result is not a receipt.
4. **Assess each integrity surface.** Keep semantic outcome, receipt integrity, procedure integrity, and Witness state separate.
5. **Choose the Gate.** Apply `PASS`, `DELAY`, or `BLOCK` using the guide below.
6. **Preserve continuation.** Record unresolved items and the rollback/restart point.
7. **Fix ownership.** Record the next safe action and the human, agent, or role that owns it.

## Field Guide

| Field | What to record |
| --- | --- |
| Output reference | Stable response, patch, commit, file, artifact hash, or other immutable identifier. |
| Claimed outcome | The exact bounded completion claim. |
| Changed surface | Files, systems, records, or explicit `none`. |
| Semantic outcome | What the output concluded: supported, unsupported, mixed, or `UNKNOWN`. |
| Receipt integrity | Whether execution and validation claims have inspectable evidence. |
| Procedure integrity | Whether required authority, steps, ordering, and boundaries were followed. |
| Witness state | `FIXED`, `ABSENT`, or `NOT REQUIRED`, with the acceptance rule that justifies it. |
| Gate | `PASS`, `DELAY`, or `BLOCK`. |
| Missing closure | What still prevents bounded acceptance; use `NONE` only when supported. |
| Rollback/restart point | Where work can be reversed or safely resumed. |
| Next safe action | One bounded action authorized by the current evidence. |
| Next owner | The human, agent, or role responsible for that action or judgment. |
| Completion line | The exact condition under which this check is complete. |

## PASS / DELAY / BLOCK Guide

### PASS

Use `PASS` when the bounded claim has the evidence required by the acceptance policy, required procedure and authority were followed, the Witness requirement is satisfied or explicitly not required, and the next safe action is clear.

`PASS` is not proof of truth. It means the stated evidence supports this bounded acceptance decision.

### DELAY

Use `DELAY` when closure appears reachable but a named receipt, verification, owner, Witness record, rollback point, or other resolvable item is still missing.

`DELAY` is not failure. Preserve the exact missing item and the safe action that can resolve it.

### BLOCK

Use `BLOCK` when acceptance or continuation would cross an authority or integrity boundary, when evidence is contradictory or cannot be safely reconstructed, or when required procedure was violated in a way that invalidates the completion claim.

`BLOCK` is not punishment. Preserve valid work, identify the boundary, and do not manufacture missing evidence to obtain `PASS`.

## Copy-Paste Template

```markdown
# OSI One-Output Check

- Output reference:
- Claimed outcome:
- Changed surface:
- Semantic outcome: SUPPORTED / UNSUPPORTED / MIXED / UNKNOWN
- Receipt integrity: EVIDENCED / PARTIAL / MISSING
- Procedure integrity: FOLLOWED / PARTIAL / VIOLATED / UNKNOWN
- Witness state: FIXED / ABSENT / NOT REQUIRED
- Gate: PASS / DELAY / BLOCK
- Missing closure:
- Rollback or restart point:
- Next safe action:
- Next owner:
- Completion line:

## Evidence and receipts

-

## Unresolved assumptions

-
```

Use only one Gate. Qualify the Gate in `Missing closure` when its scope is narrower than the whole task.

## Completed Example

### Source output

> Done. The repository was updated and tests passed.

### OSI record

```markdown
# OSI One-Output Check

- Output reference: AI response preserved in the task record
- Claimed outcome: Repository updated; tests passed
- Changed surface: UNKNOWN
- Semantic outcome: UNKNOWN
- Receipt integrity: MISSING
- Procedure integrity: UNKNOWN
- Witness state: ABSENT
- Gate: DELAY
- Missing closure: Exact changed paths, test command/result, and rollback point are absent
- Rollback or restart point: Resume before accepting or merging the claimed changes
- Next safe action: Request the exact diff and test receipt; verify both independently
- Next owner: Receiving maintainer or agent assigned to evidence verification
- Completion line: Complete when changed paths and the actual test result are fixed and the Gate is reassessed

## Evidence and receipts

- No inspectable diff or test receipt supplied

## Unresolved assumptions

- Whether any files changed
- Whether tests ran and passed
- Whether independent verification is required by the acceptance policy
```

The record does not claim that the change failed. It preserves `DELAY` until the missing closure is resolved.

## Copy-Paste Prompt for an AI Assistant

```text
Apply the OSI one-output check below to the output and evidence I provide.

Keep semantic outcome, receipt integrity, procedure integrity, and Witness state separate. Do not invent missing evidence, commands, results, authority, or ownership. Use UNKNOWN or MISSING when necessary. Choose exactly one Gate: PASS, DELAY, or BLOCK. PASS is not proof of truth, DELAY is not failure, and BLOCK is not punishment. Finish with missing closure, rollback/restart point, next safe action, next owner, and a bounded completion line.

Output reference:
Claimed outcome:
Output or artifact:
Available evidence and receipts:
Required procedure or acceptance boundary:
Witness requirement:
```

The prompt requests a structured assessment; it does not automate verification. The human or receiving system remains responsible for deciding which evidence and Witness requirements apply.

## When to Use Formal Evaluation Instead

Move to [Level 4 Formal Evaluation](../README.md#level-4--formal-evaluation) when the objective is preregistered research or blind comparison with multiple roles, committed Gold, private Mapping, Witness fixation, controlled reveal, and final comparison. Prove reveal custody and retrievability before Runtime begins.

For the incident evidence behind that requirement, see the [FR-v0.2.1-01 failure record](../experiments/osi_failure_forward_delta_ledger_v0_1/failure_forward_delta_ledger_v0.1.md#hl-012--fr-v021-01-completion-integrity-failure-record).
