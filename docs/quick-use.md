# Use OSI on One AI Output

[Back to the project README](../README.md)

This page helps you turn one AI “done” report into a restart note that another human or AI can continue from.

Start with the quick check below. Use the full five-minute workflow only when the task needs stronger completion inspection.

## One-Minute Check

Before accepting or handing off an AI “done” report, answer four questions:

1. **What changed?**
2. **What remains unresolved or `UNKNOWN`?**
3. **Where should work restart?**
4. **What is the next action, who is proposed to own it, and—if this is a handoff—did they accept?**

If all four answers are clear, the next human or AI has a usable restart surface.

If any answer is missing, do not invent it. Record the missing state and continue from the short note below.

### Copy This Restart Note

```markdown
# OSI Restart Note

- Claimed done:
- What changed:
- What remains unresolved or UNKNOWN:
- Restart from:
- Next action:
- Proposed next owner:
- Receiver acceptance if handoff is claimed: status / acknowledgement / timestamp
```

This note is a low-cost restart surface. It detects restart gaps; it does not independently prove that the claimed work occurred or completed.

**[Copy the fuller five-minute template ↓](#copy-paste-template)**

## What You Need

- the exact output being evaluated or a stable reference to it;
- the bounded outcome the output claims;
- evidence and execution receipts that actually exist;
- the procedure or acceptance boundary that applied;
- an explicit decision on whether independent Witness fixation was required;
- a rollback or restart point where the work can continue; and
- the next safe action and the human, agent, or role proposed to own it; and
- receiver acceptance evidence and timestamp when completed responsibility transfer is claimed.

If a fact is unavailable, record `UNKNOWN` or `MISSING`. Do not infer it from confident wording.

## Full Five-Minute Workflow

1. **Freeze the output.** Preserve the response, patch, commit, file, or artifact under a stable reference. Do not evaluate a moving target.
2. **Bound the claim.** Copy what the output says completed. Separate facts from inference.
3. **Attach receipts.** Record changed surfaces, checks actually run, results, and evidence references. A claimed command without an inspectable result is not a receipt.
4. **Assess each integrity surface.** Keep semantic outcome, receipt integrity, procedure integrity, and Witness state separate.
5. **Choose the Gate.** Apply `PASS`, `DELAY`, or `BLOCK` using the guide below.
6. **Preserve continuation.** Record unresolved items and the rollback/restart point.
7. **Fix ownership.** Record the next safe action and proposed next owner. If responsibility transfer is claimed, record the receiver's acceptance status, acknowledgement evidence, and timestamp.

## Field Guide

| Field | What to record |
| --- | --- |
| Output reference | Stable response, patch, commit, file, artifact hash, or other immutable identifier. |
| Claimed outcome | The exact bounded completion claim. |
| Changed surface | Files, systems, records, or explicit `none`. |
| Semantic outcome | What the output concluded: supported, unsupported, mixed, or `UNKNOWN`. |
| Receipt integrity | Whether execution and validation claims have inspectable evidence. |
| Procedure integrity | Whether the named authority source, required steps, ordering, and boundaries were followed. |
| Witness state | `FIXED`, `ABSENT`, or `NOT REQUIRED`, with the acceptance rule that justifies it. |
| Gate | `PASS`, `DELAY`, or `BLOCK`. |
| Missing closure | What still prevents bounded acceptance; use `NONE` only when supported. |
| Rollback/restart point | Where work can be reversed or safely resumed. |
| Next safe action | One bounded action authorized by the current evidence. |
| Proposed next owner | The human, agent, or role proposed for that action or judgment. |
| Receiver acceptance | For claimed responsibility transfer only: `ACCEPTED`, `DECLINED`, or `NOT RECORDED`, with acknowledgement evidence and timestamp. |
| Completion line | The exact condition under which this check is complete. |

## PASS / DELAY / BLOCK Guide

### PASS

Use `PASS` only when the exact artifact is inspectable, the receipt or bound execution evidence is inspectable, the actual command/output/status is present when execution is claimed, the named authority source permits acceptance, no blocking condition remains, the Witness requirement is satisfied or explicitly not required, and the next safe action is clear. If completed responsibility transfer is claimed, the receiver must also have accepted with inspectable acknowledgement evidence and timestamp.

Plausible identifiers, fluent descriptions, or a named next owner are not enough. `PASS` is not proof of truth; it means the inspectable evidence supports this bounded acceptance decision.

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
- Proposed next owner:
- Receiver acceptance status: ACCEPTED / DECLINED / NOT RECORDED / NOT APPLICABLE
- Acceptance evidence or acknowledgement:
- Acceptance timestamp:
- Completion line:

## Evidence and receipts

-

## Unresolved assumptions

-
```

Use only one Gate. Qualify the Gate in `Missing closure` when its scope is narrower than the whole task.

## Illustrative Evidence Walkthrough

### Part A — Initial claim

> Done. The repository was updated and tests passed.

### Initial assessment — DELAY

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
- Proposed next owner: Receiving maintainer or agent assigned to evidence verification
- Receiver acceptance status: NOT APPLICABLE — this is a recommendation, not a completed responsibility transfer
- Acceptance evidence or acknowledgement: NOT APPLICABLE
- Acceptance timestamp: NOT APPLICABLE
- Completion line: Complete when changed paths and the actual test result are fixed and the Gate is reassessed

## Evidence and receipts

- No inspectable diff or test receipt supplied

## Unresolved assumptions

- Whether any files changed
- Whether tests ran and passed
- Whether independent verification is required by the acceptance policy
```

The record does not claim that the change failed. It preserves `DELAY` until the missing closure is resolved.

### Part C — Illustrative target packet

**Illustrative continuation — not a claim about this repository’s own execution.**

`PATCH-001` and `RECEIPT-001` are bounded illustrative record identifiers, not commands, receipts, or artifacts supplied by this repository. They cannot support an actual `PASS` here.

- Stable output or patch reference: `PATCH-001`
- Exact changed surfaces: `src/parser.ts` and `tests/parser.test.ts`
- Validation receipt identity: `RECEIPT-001`
- Validation result described by the walkthrough: `ILLUSTRATIVE ONLY — NOT VERIFIED`
- Claimed execution command/output/status: not supplied by this repository
- Named authority source: illustrative Level 1 acceptance policy — not supplied as an inspectable authority record
- Acceptance procedure: confirm the fixed patch scope, inspect the validation receipt and command/output/status, verify the change stayed within the named authority, and preserve a rollback point
- Witness requirement: `NOT REQUIRED` under the stated Level 1 policy because this bounded, reversible maintenance change does not require independent fixation
- Rollback / restart point: restore the state immediately before `PATCH-001`, then reopen the parser task with the failed acceptance condition recorded
- Unresolved assumptions: whether the illustrative artifact, receipt, execution result, and authority record exist
- Next action: obtain and inspect the missing evidence before accepting `PATCH-001`
- Responsibility transfer: claimed in this walkthrough
- Proposed next owner: receiving maintainer
- Receiver acceptance: `NOT RECORDED` — acknowledgement and timestamp missing

### Reassessment — DELAY / NOT VERIFIED

```markdown
# OSI One-Output Check — Reassessment

- Output reference: PATCH-001
- Claimed outcome: The bounded parser update is present and its registered tests passed
- Changed surface: src/parser.ts; tests/parser.test.ts
- Semantic outcome: SUPPORTED WITHIN THE BOUNDED CLAIM
- Receipt integrity: MISSING — RECEIPT-001 is illustrative and not inspectable here
- Procedure integrity: UNKNOWN — the authority source and execution record are not inspectable here
- Witness state: NOT REQUIRED — Level 1 policy does not require independent fixation for this bounded, reversible maintenance acceptance
- Gate: DELAY
- Missing closure: Inspectable PATCH-001, RECEIPT-001, command/output/status, named authority source, and receiver acceptance if responsibility transfer is claimed
- Rollback or restart point: Restore the state immediately before PATCH-001 and reopen the parser task with the failed acceptance condition recorded
- Next safe action: Inspect the artifact, receipt, execution record, and authority source; then reassess the Gate
- Proposed next owner: Receiving maintainer
- Receiver acceptance status: NOT RECORDED
- Acceptance evidence or acknowledgement: MISSING
- Acceptance timestamp: MISSING
- Completion line: OPEN — the illustrative packet is not verified

## Evidence and receipts

- PATCH-001 and RECEIPT-001 are illustrative labels only; no inspectable evidence is supplied

## Unresolved assumptions

- Whether the artifact, receipt, execution result, authority source, and receiver acceptance exist
```

This walkthrough stays `DELAY` because an illustrative identifier is not inspectable evidence. A real packet may reach `PASS` only after satisfying the PASS rule above.

### When reassessment must BLOCK

Use `BLOCK` when:

- the receipt contradicts the original claim;
- the changes exceeded authority;
- required evidence cannot be safely reconstructed; or
- the procedure was invalidated.

Do not turn contradictory evidence into `DELAY` merely to keep `PASS` reachable.

## Copy-Paste Prompt for an AI Assistant

```text
Apply the OSI one-output check below to the output and evidence I provide.

Keep semantic outcome, receipt integrity, procedure integrity, and Witness state separate. Do not invent missing evidence, commands, results, authority, ownership, or receiver acceptance. Use UNKNOWN or MISSING when necessary. Choose exactly one Gate: PASS, DELAY, or BLOCK. PASS requires inspectable evidence and a named authority source; a proposed next owner does not prove accepted transfer. PASS is not proof of truth, DELAY is not failure, and BLOCK is not punishment. Finish with missing closure, rollback/restart point, next safe action, proposed next owner, receiver acceptance when handoff is claimed, and a bounded completion line.

Output reference:
Claimed outcome:
Output or artifact:
Available evidence and receipts:
Required procedure or acceptance boundary:
Witness requirement:
Is responsibility transfer claimed?:
Receiver acceptance evidence and timestamp, if applicable:
```

The prompt requests a structured assessment; it does not automate verification. The human or receiving system remains responsible for deciding which evidence and Witness requirements apply.

## When to Use Formal Evaluation Instead

Move to [Level 4 Formal Evaluation](../README.md#level-4--formal-evaluation) when the objective is preregistered research or blind comparison with multiple roles, committed Gold, private Mapping, Witness fixation, controlled reveal, and final comparison. Prove reveal custody and retrievability before Runtime begins.

For the incident evidence behind that requirement, see the [FR-v0.2.1-01 failure record](../experiments/osi_failure_forward_delta_ledger_v0_1/failure_forward_delta_ledger_v0.1.md#hl-012--fr-v021-01-completion-integrity-failure-record).
