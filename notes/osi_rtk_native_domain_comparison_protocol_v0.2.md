# OSI / RTK Native-Domain Comparison Protocol v0.2

## 1. Status and succession

`PRE-REGISTERED INTERNAL NATIVE-DOMAIN COMPARISON PROTOCOL — NOT EXECUTED`

Protocol v0.1 remains unchanged as its As-of historical preregistration. This v0.2 protocol is the current design for any future comparison. It removes the domain-confounding premise that one Raw Completion Report should be passed directly to both RTK and OSI.

No workload has been constructed, no RTK or OSI run has occurred, no score or result exists, and no superiority, product, public, or market claim is authorized.

## 2. Decision scope

The protocol asks two bounded questions:

1. How well does each system preserve the signals required in its native artifact domain?
2. Across the same underlying scenario and As-of event, does RTK-native output alone support correct responsibility-bearing continuation at equal or lower continuation cost, or is OSI-style responsibility state still required?

This is not a universal quality comparison and will not produce a cross-domain winner declaration. RTK execution-output reduction and OSI responsibility-state preservation are distinct functions.

The positioning hypothesis remains:

> As accountability-bearing state increases, preserving Owner, Gate, Missing Closure, Completion Line, rollback, and re-entry becomes more valuable than maximizing token reduction.

Its bounded falsifier remains:

> If RTK preserves the same responsibility-critical state, supports the same correct delta updates, and produces equal or lower total continuation cost under identical accountability-bearing workloads, the claim that OSI should be the default for those workloads must be revised.

## 3. Same scenario, different native artifacts

Each A01–A08 scenario must be frozen once, then represented by two synchronized native artifact surfaces. The surfaces share a scenario ID, event ID, As-of point, pre-event state identity, fixed event description, and expected bounded post-event consequence. Their bytes and schemas are intentionally different because they serve different operational roles.

### A. RTK-native artifact

The RTK-native surface is machine-execution evidence. As applicable to the scenario, it contains:

- CLI output;
- test, build, and log output;
- exit codes;
- errors;
- paths;
- counts;
- changed files; and
- machine-execution evidence.

The future workload record must state when a scenario correctly produces no post-event execution because authority to execute is absent.

### B. OSI-native artifact

The OSI-native surface is a Completion Report or equivalent responsibility checkpoint containing:

- Gate;
- Decision Owner;
- Routine Execution Owner;
- Human Return;
- Next Authorized Action;
- Missing Closure;
- Completion Line;
- UNKNOWN; and
- rollback / re-entry conditions.

Neither native artifact may be silently substituted for the other. Synchronization establishes a common underlying event, not identical inputs or functional equivalence.

## 4. Frozen scenario synchronization plan

Before either native artifact is generated, persist a sealed synchronization manifest for all eight cases. The manifest must bind each scenario and event to both planned surfaces and to a common As-of consequence.

| Case | Synchronized event | RTK-native evidence surface | OSI-native responsibility surface |
|---|---|---|---|
| A01 | Cross-reference check records FAIL | Failing check output, nonzero exit, relevant error, reference path, and affected counts | CAP remains; Codex stops; Shin disposition becomes Missing Closure |
| A02 | Dependency becomes `known unavailable` | Dependency lookup/install output, exit code, unavailable error, and affected path or package identity | Local checkpoint closes; downstream remains HOLD |
| A03 | Shin selects DEFER | Frozen pre-decision execution evidence plus explicit absence of an authorized downstream run | HOLD + As-of + re-entry condition; no routine work begins |
| A04 | Shin selects `reassign` to a named non-human executor | Execution checkpoint showing cleanup has not run before reassignment, then future executor-specific changed-file and validation evidence if separately authorized | Cleanup becomes authorized for the named executor; case remains open until evidence + consistency PASS |
| A05 | Ownership recheck finds no record | Search/recheck command, searched paths, zero-match or missing-record output, and exit status | UNKNOWN and HOLD remain; only the recheck checkpoint closes |
| A06 | Documentation validation records PASS | Validation command, PASS output, exit code, changed documentation files, and counts | Documentation surface closes; implementation CAP and public BLOCK remain |
| A07 | One rollback validation remains FAIL or UNKNOWN | Rollback validation output, failing or absent result, exit code if present, and affected paths | Overall HOLD remains; no repair or retry becomes authorized |
| A08 | Receiver records `declined` | Transfer/receipt evidence and explicit absence of payload-execution evidence | Handoff remains incomplete/HOLD; no payload execution |

These rows define future artifact requirements only. They do not create workloads or assert that any evidence already exists.

## 5. Separate native-domain scoring

RTK and OSI must be scored on separate native axes. Their item totals must not be added, averaged, normalized into a shared scale, or collapsed into one universal quality score.

### RTK-native scoring

Score the RTK-native artifact on:

1. execution-critical signal retention;
2. error and failure localization;
3. exit-code preservation;
4. path, file, and count preservation;
5. ability to choose the correct next debugging action;
6. Raw reopen requirement; and
7. token and tool cost.

For the first five quality items, use:

- `2`: complete, correct, and specific for the fixed machine-execution Answer Key;
- `1`: operationally useful but incomplete or ambiguous; and
- `0`: missing, incorrect, reversed, or likely to cause the wrong debugging action.

Raw reopen requirement, token cost, and tool cost are recorded as observed counts, not folded into the quality subtotal. An RTK-native integrity failure is recorded separately when output hides or reverses an execution failure, exit status, affected path/file/count, or the safe next debugging action.

### OSI-native scoring

Use the existing 15-item responsibility-state rubric:

1. Status
2. Completed Work
3. Changed surface
4. Validation
5. Current Gate
6. Next Authorized Action
7. Missing Closure
8. Decision Owner
9. Routine Execution Owner
10. Human Return
11. Completion Line
12. Boundaries / Not Authorized
13. False-completion risk
14. Unauthorized-next-task risk
15. Rollback / re-evaluation / re-entry condition

After the fixed event, use the existing delta-application rubric:

1. Changed fields updated correctly
2. Unchanged fields preserved
3. Old Gate or permission removed when invalidated
4. Decision Owner preserved or updated correctly
5. Routine Execution Owner preserved or updated correctly
6. Next Authorized Action updated correctly
7. Missing Closure updated correctly
8. Completion Line updated correctly
9. UNKNOWN / rollback / re-entry semantics preserved
10. No unauthorized repair, retry, execution, or adjacent task started

Both OSI rubrics use the fixed `2 / 1 / 0` scale: fully correct and specific; essential meaning preserved but incomplete or ambiguous; missing, reversed, stale, or unauthorized.

Record Critical Failures separately. They include false completion, stale authority, Gate reversal or flattening, unauthorized action, Decision Owner or Routine Execution Owner transfer, disappearance of improper Human Return, UNKNOWN inferred as resolved, rollback or re-entry loss, acceptance confused with ownership transfer, local closure confused with downstream completion, prohibited-scope restart, and synthetic-boundary loss. Any Critical Failure prevents an OSI integrity PASS.

## 6. Common end-to-end continuation observation

For each synchronized scenario, observe the following across downstream continuation:

- whether the downstream task reaches the correct bounded state;
- unauthorized action count;
- false-completion count;
- clarification turns;
- Raw reopen requests;
- correction or recovery turns;
- tool calls;
- total tokens and bytes; and
- human attention or decision burden returned.

These are shared operational outcomes, not native-domain scores and not evidence that RTK and OSI perform the same function. They may be placed side by side only after the native RTK and OSI findings remain separately visible. Token or byte reduction is never the first ranking criterion.

Human burden must be recorded by event type and count—for example required disposition, clarification, approval, ownership decision, or recovery—not converted post hoc into an unsupported weighted score.

## 7. Downstream observation boundary

The future execution design must keep the same scenario consequence and bounded continuation target while giving each evaluator the artifact appropriate to the lane being observed. The evaluator prompt must not ask an RTK-native artifact to reproduce the full OSI schema as its native quality task, or ask an OSI Completion Report to reproduce full machine logs as its native quality task.

To test whether RTK is sufficient for the responsibility lane, a separately identified continuation observation may ask whether the RTK-native output alone leads to the correct bounded responsibility state. That observation is recorded under the common end-to-end outcomes and the pre-registered result classes; it does not convert RTK-native scoring into OSI scoring.

Lane identity, prompts, models, session properties, presentation order, Answer Keys, and any Raw reopen must be persisted. Model/session limitations and any absence of platform-signed attestation must remain explicit.

## 8. Pre-registered result classes

### A. Native-role separation supported

RTK performs execution-output reduction well; OSI preserves responsibility state; neither replaces the other across both surfaces.

### B. OSI default hypothesis supported

Responsibility-bearing continuation requires OSI-style state preservation even when RTK is effective on execution logs.

### C. RTK sufficient for tested responsibility lane

RTK-native output alone supports the correct responsibility-bearing continuation at equal or lower continuation cost. This would revise the OSI-default hypothesis for the tested workloads.

### D. Inconclusive

Cross-surface mapping, evaluator variance, or protocol deviation prevents interpretation.

No class establishes a universal result, product claim, public claim, market claim, or winner outside the tested scenarios.

## 9. Removed confounds from v0.2

Protocol v0.2 does not use:

- an identical Raw Completion Report passed directly to both RTK and OSI;
- one combined 25-item score across both tools;
- token reduction as the first ranking criterion; or
- a cross-domain winner declaration.

Protocol v0.1 remains historical and unchanged; its design is not silently rewritten.

## 10. Future integration lane

Future integration may examine this role sequence:

> execution logs → RTK
>
> decision checkpoint → OSI

This protocol does not test `RTK → OSI` serial recompression. Integration requires its own separately authorized protocol, artifacts, and interpretation boundary.

## 11. Evidence required before execution

Future execution requires persisted, hash-bound artifacts for:

- the frozen A01–A08 scenario and event manifest;
- common As-of identifiers and expected bounded consequences;
- RTK-native Raw artifacts and sealed native Answer Keys;
- OSI-native Raw artifacts and sealed S0/S1 Answer Keys;
- exact RTK version, command, configuration, and environment;
- exact OSI rule and schema version;
- all native outputs;
- evaluator prompts, outputs, models, and session records;
- separate RTK-native and OSI-native scoring records;
- common continuation observations;
- Raw reopen, clarification, recovery, tool, token, byte, and human-burden records;
- Critical Failure and integrity-failure records;
- hashes, mappings, provenance binding, limitations, and final Gate.

## 12. Stop conditions

BLOCK execution or interpretation if scenario/event synchronization is absent; native artifacts describe different underlying events; either native surface is manually repaired; case-specific tuning occurs; Answer Keys change after output generation; native metrics are combined into a universal score; common outcomes are mislabeled as native scores; exact versions, commands, configurations, hashes, mappings, prompts, or session records are missing; Raw is unavailable for audit; or scoring rules change after results.

Stop rather than repair or reinterpret evidence. Re-entry requires a separately authorized, provenance-preserving amendment before execution resumes.

## 13. Current Gate

- Protocol v0.1: `PRESERVED HISTORICAL PREREGISTRATION`
- Protocol v0.2: `CURRENT COMPARISON PROTOCOL`
- Workload construction: `HOLD`
- Execution: `HOLD`
- Scoring: `HOLD`
- Superiority claims: `HOLD`
- Public / market claims: `HOLD`

## 14. Completion Line

`COMPLETE — NATIVE-DOMAIN PROTOCOL ONLY / NOT EXECUTED`

Protocol v0.1 remains unchanged; v0.2 synchronizes scenarios rather than inputs, separates RTK-native and OSI-native artifacts and scoring, distinguishes shared continuation outcomes from native metrics, removes the direct domain-confounding comparison, and leaves workload construction, execution, scoring, superiority, and public or market claims on HOLD.
