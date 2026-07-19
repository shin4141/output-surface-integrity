# Responsibility-Weighted OSI / RTK Positioning

## Status

`INTERNAL POSITIONING HYPOTHESIS — NOT A BENCHMARK RESULT`

## Core question

Do not ask only:

> “Which system reduces more tokens?”

Ask:

> “Is reducing context cost worth lowering the guarantees that responsibility-bearing state remains traceable, reconstructable, and transferable?”

## Core position

> Responsibility-bearing operations should default to OSI.
> RTK is appropriate only where the operator can rationally prioritize lower context cost over responsibility-preservation guarantees.

Responsibility itself cannot be deleted. What can be weakened is the structure that makes responsibility traceable and restartable, including Owner, Gate, Next Authorized Action, Missing Closure, Completion Line, UNKNOWN, rollback, and re-entry.

## Default selection rule

### OSI default

Use OSI from the beginning when the workflow affects any of:

- company operations;
- customers;
- production;
- publication;
- financial assets;
- permissions or execution authority;
- audit evidence;
- handoff between people, chats, agents, or systems;
- rollback or incident recovery; or
- legal, contractual, or reputational responsibility.

The cost of one ownership, Gate, completion, or re-entry failure can exceed the saved context cost.

### RTK-permitted lane

RTK may be sufficient only when all of the following are true:

- impact is low;
- the work is highly reversible;
- Raw evidence remains readily accessible;
- no responsibility or authority transfer depends on the compressed output;
- failure does not alter Owner, Gate, rollback, release, or completion state; and
- the expected loss from omitted context is lower than the saved processing cost.

## Reversed decision framing

> The burden of proof is not on OSI to justify its additional cost.
> In responsibility-bearing work, the burden is on the lower-cost path to justify why responsibility-preservation guarantees may safely be reduced.

> OSIの追加コストを正当化するのではなく、責任を伴う運用では、責任保全の保証を下げてまで低コスト化する合理性があるかを、低コスト側が証明する。

## Decision table

| Work condition | Default | Reason |
|---|---|---|
| Disposable personal test log | RTK may be sufficient | Low impact and disposable when no later authority or recovery depends on it. |
| Production incident log | OSI | Owner, Gate, rollback, recovery, and closure must remain traceable. |
| Company/customer workflow | OSI | Responsibility and downstream impact outweigh context-cost savings. |
| Public release decision | OSI | Authorization, evidence, completion, and release boundaries must remain explicit. |
| Reversible local exploration with retained Raw | RTK may be sufficient | Raw remains available and an omission does not transfer authority or change a Gate. |
| Multi-agent or multi-session handoff | OSI | Responsibility-bearing state must remain reconstructable and transferable across context boundaries. |

## Supported evidence from current work

- Operational corpus: `77.70%` reduction with complete rubric reconstruction.
- Synthetic adversarial corpus: `56.44%` reduction with complete rubric reconstruction.
- The higher-complexity corpus retained more information while preserving all tested judgment-critical fields.

This is consistent with responsibility-sensitive information retention. It does not establish universal superiority over RTK, lower total cost than RTK, an identical-workload benchmark victory, product readiness, independent third-party validation, or general proof across all workflows.

## Comparative hypothesis

> As accountability-bearing state increases, the value of preserving Owner, Gate, closure, rollback, and re-entry should increase faster than the value of maximizing token reduction.

This is a hypothesis for future identical-workload testing, not a completed result.

## Falsifier

> If RTK preserves the same responsibility-critical state, supports the same correct delta updates, and produces equal or lower total continuation cost under identical accountability-bearing workloads, the claim that OSI should be the default for those workloads must be revised.

## Future comparison question

Any future comparison must use an identical workload, an identical next-agent task, and the same Raw source, then compare:

- responsibility-state preservation;
- correct Gate and Owner reconstruction;
- correct delta application;
- false-completion rate;
- unauthorized-next-action rate;
- re-read, clarification, and recovery cost; and
- total token and tool cost.

No comparison is started or authorized by this note.

## Current Gate

- Internal positioning note: `GO`
- Identical-workload comparison: `HOLD pending protocol authorization`
- RTK superiority / OSI superiority claim: `HOLD`
- Public or market positioning: `HOLD`

## Completion Line

`COMPLETE`

The default is responsibility-weighted rather than beginner/advanced or simple/complex. OSI is the default for responsibility-bearing operation; RTK is bounded to cases where reduced responsibility-preservation guarantees are rational; current evidence and the future hypothesis remain separate; and no benchmark or superiority claim is introduced.
