# Is Your AI Operation Ready to Scale?

If your current AI workflow is already strong, you may not need to change it.

You do not need to understand OSI first.
You do not need to trust the author first.
You do not need to adopt a new framework first.

## Start in under three minutes

1. Open an AI session that already has access to the work history you want to assess.
2. Paste the public OSI repository URL and the prompt below.
3. Treat the OSI repository as reference material only.
4. Treat only your accessible work history as evidence about your workflow.

Public reference:

`https://github.com/shin4141/output-surface-integrity`

If your AI cannot access enough real work history, the result should remain `UNKNOWN`.

## Ask your own AI

Copy the prompt below.

```text
Using only the work history you can actually access, assess whether my current AI operation is likely to compound as 1.01, 0.99, or UNKNOWN when the number of projects, agents, handoffs, collaborators, and model changes increases.

Use the OSI repository only as reference material for what operational state may matter.
Do not treat the repository as evidence about my own workflow.

Do not use generic accident rates, imagined events, or unsupported assumptions.
Use evidence from my actual accessible history.
When evidence is missing, write UNKNOWN.

Start with what is already working.

Then identify:

1. Current operating practices that are already effective
2. Strengths that are likely to remain useful under scale
3. Re-explanation, re-verification, supervision, handoff, ownership, and recovery costs that may repeat under scale
4. The actual history supporting each judgment
5. Important conditions that cannot currently be evaluated
6. The minimum conditions that should be checked before expanding

Choose one final classification:

1.01 — The current operation is likely to compound useful structure under scale

0.99 — The current operation is likely to compound recovery, supervision, or coordination costs under scale

UNKNOWN — The available history is insufficient to determine the direction

If the result is 1.01:
Do not recommend replacing the workflow. Explain which conditions must not be lost during expansion.

If the result is 0.99:
Do not recommend a full framework rollout. Propose only one reversible change for the next real task.

If the result is UNKNOWN:
Specify only what should be recorded during the next real task to make the operation diagnosable.
```

`1.01` and `0.99` are directional labels, not measured productivity multipliers.

## Why check before scaling?

A workflow that works for one project, one model, or one operator may behave differently when you add:

- more projects;
- more AI agents;
- more handoffs;
- more collaborators;
- more model changes;
- more files, customers, and operational dependencies.

Scale may amplify the operating structure already present.

When accessible history does not show a reliable direction, the result should remain `UNKNOWN`.

If the current operation is effectively **1.01**, scaling may increase leverage:

- restart state remains reusable;
- decisions remain inspectable;
- evidence and unresolved items stay visible;
- the next human or AI can continue without rebuilding the full history.

If the current operation is effectively **0.99**, scaling may also increase:

- re-explanation;
- repeated verification;
- human supervision;
- lost restart state;
- unclear ownership;
- recovery work after mistakes.

## How to use the result

### If the result is 1.01

Do not replace a workflow that is already working.

Preserve the conditions that make it scale:

- evidence continuity;
- restartability;
- clear unresolved state;
- bounded ownership;
- receiver acceptance when responsibility transfer is claimed.

### If the result is 0.99

Do not redesign everything.

Apply the single reversible change identified by the diagnosis to the next real task.

When the diagnosed weakness concerns restart or handoff state, a minimal OSI restart note can record:

- what changed;
- what remains unresolved or `UNKNOWN`;
- where work should restart;
- the next action;
- the proposed next owner;
- receiver acceptance when handoff is claimed.

Continue to the [one-minute restart check](quick-use.md#one-minute-check) only when that matches the diagnosed weakness.

### If the result is UNKNOWN

Do not force a conclusion.

Use the next real task to record only the missing information needed to classify the operation.

## What this does not claim

This page does not claim:

- that every current AI workflow is 0.99;
- that OSI is required for every user;
- that the labels are measured productivity multipliers;
- universal token, time, safety, or productivity gains;
- that an AI diagnosis replaces human judgment;
- independent validation of your specific workflow.

The purpose is narrower:

> Determine whether the structure you scale is likely to amplify useful continuation, amplify recovery cost, or remain unknowable because the operational record is missing.

## About OSI

Output Surface Integrity is a manual restart-oriented compression and completion-integrity method for long-running human–AI work.

You can inspect:

- the [project README](../README.md);
- the [one-minute restart check](quick-use.md#one-minute-check);
- the [claim boundary](../CLAIM_BOUNDARY.md);
- the [published adverse evidence](../evaluation/osi_rtk_native_domain_v0.2/comparison_interpretation_packet_v0.1/measured_score_facts.json);
- the [terminal Formal Run `BLOCK`](../experiments/osi_failure_forward_delta_ledger_v0_1/failure_forward_delta_ledger_v0.1.md#hl-012--fr-v021-01-completion-integrity-failure-record).

OSI does not make trust automatic.

It makes the basis for continuation inspectable.
