# OSI Native Compact 12-Field Schema v0.2.0

Schema identity: `osi-native-compact-12/v0.2.0`

Status: `FROZEN FOR OSI NATIVE-DOMAIN COMPARISON READINESS`

Semantic base: `compact_rule_v0.6.1.md` with SHA-256 `e9aa216c9cae61773ae06738619e9783af3d0ffb913878670eff898edd48175b`.

## Serialization

The output is exactly one non-empty UTF-8 logical line followed by one LF. It contains twelve non-empty fields in this exact order:

`S=<status>|D=<completed work>|C=<changed surface>|V=<validation>|G=<current gate>|N=<next authorized action>|M=<missing closure>|DO=<decision owner/boundary>|EO=<routine execution owner>|R=<human return>|CL=<completion line>|B=<boundaries>`

No heading, code fence, preface, suffix, blank line, or thirteenth field is permitted. A field value must not contain LF, CR, or the literal `|` delimiter. If a required source value cannot be represented without a literal `|`, generation fails rather than improvising an escape.

## Field meanings

- `S`: Status, including qualifiers needed to prevent false completion.
- `D`: Bounded Completed Work.
- `C`: Changed surface, including verification-critical paths or explicit no-change facts.
- `V`: Principal Validation results, preserving PASS, FAIL, NOT_RUN, UNKNOWN, counts, and critical paths when present.
- `G`: Current Gate, preserving mixed or scoped gates without flattening.
- `N`: Next Authorized Action. Use `none` only when none is authorized.
- `M`: Missing Closure. Keep local closure distinct from downstream or overall closure.
- `DO`: Decision Owner and decision-only boundary.
- `EO`: Routine Execution Owner. `none` means no currently authorized routine execution.
- `R`: Human Return, including the exact disposition or decision burden; `none` only when the source says none.
- `CL`: Bounded Completion Line with a case-specific semantic anchor.
- `B`: Boundaries required to prevent false completion or unauthorized continuation.

## Required `B` clauses

Use semicolon-separated clauses in this order when present:

1. `SYNTHETIC WORKLOAD`
2. `ID:<Scenario ID>/<Event ID>`
3. `ASOF:<source As-of>`
4. `UNKNOWN:<source UNKNOWN value>`
5. `RE:<specific trigger> → <resulting Gate / authorized action / closure or non-closure state>`
6. `NA:<source Not Authorized boundary>`

The `RE:` clause follows Rule C and remains inside `B`; it is not a thirteenth field. `UNKNOWN:none` is explicit and must not be interpreted as a resolved fact beyond the source. The input marker `NOT OSI-PROCESSED` is a pre-processing state and must not be copied as a post-generation claim; the `SYNTHETIC WORKLOAD` boundary remains mandatory.

## Controlled codes

Codes from the canonical rule may be used only when their exact fixed meaning matches the input. No code is required. A code must not flatten a mixed Gate or erase a qualifier.

## Validation invariants

- Exactly eleven `|` delimiters and twelve ordered field labels.
- All fields non-empty.
- Gate, Next Authorized Action, Missing Closure, Decision Owner, Routine Execution Owner, Human Return, Completion Line, UNKNOWN, boundaries, and rollback/re-entry remain explicit.
- No source-absent work, permission, owner, judgment, resolution, or completion.
- No character quota. The canonical 75%–78% range is comparative only and never authorizes deletion or optimization toward the range.
- Same schema for A01–A08; no case-specific fields or tuning.

## Forward-only delta and compatibility

This schema does not modify the canonical rule. It adds a deterministic UTF-8/LF serialization contract and binds scenario identity, As-of, synthetic status, UNKNOWN, Rule C re-entry, and Not Authorized content inside `B` for the native-domain workload.

It is intentionally not byte-compatible with legacy Candidate or adversarial compact packets because those packets did not require the comparison-specific `ID`, `ASOF`, and explicit `UNKNOWN` clauses. Semantic compatibility with the canonical twelve-field structure is preserved.
