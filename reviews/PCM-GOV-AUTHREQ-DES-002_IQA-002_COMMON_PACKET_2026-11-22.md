# PROJECT CONTROL MASTER — PCM-GOV-AUTHREQ-DES-002-IQA-002: paquete común de re-QA documental R2

**Project:** `KhaosMagnus/Project-Control`
**Assignment:** `PCM-GOV-AUTHREQ-DES-002-IQA-002`
**Coordinator:** PROJECT_CONTROL_MASTER / PCM-002 (provisional)
**Reviewers:** QA1 ChatGPT (sesión separada) y QA2 Grok (sesión separada)
**Date:** 2026-11-22
**Authorization source:** mensaje efectivo del Owner en esta conversación, `OWNER DECISION — PCM-GOV-AUTHREQ-DES-002-IQA-002: GRANTED`, únicamente para **preparar y publicar** un paquete común y dos encargos en `meta/project-control`. `PRIMARY_OBSERVED LOCAL` para PCM-002; para evaluadores externos sin mensaje original, `SECONDARY_ATTRIBUTED`. La autorización de creación del paquete NO acredita su entrega ni resultados de QA.
**Mode of requested QA:** STRICT READ-ONLY / FOCUSED INDEPENDENT DOCUMENTARY DESIGN QA / REPORT ONLY.
**Package status:** `PREPARED FOR OWNER-MEDIATED DISPATCH / NO R2 QA PERFORMED / NO OWNER ACCEPTANCE`.
**Packet drafting control base:** `meta/project-control@48b558caaf989e6952b42265890d60d7b75d2790`.

## 1. Candidate identity and documentary authority

**Exact subject of review (R2 only):**
- Path: `planning/PCM-GOV-AUTHREQ-DES-002_R2_AUTHORIZATION_GATE_CORRECTIVE_CANDIDATE_2026-11-22.md`
- Full immutable commit: `48b558caaf989e6952b42265890d60d7b75d2790`.
- Exact Git blob SHA: `3e817012a1207eec3fe20a058333724b13b20506`.
- SHA-256: `fcf3acab3927731b61e6c7ca3a8f4ab4ca9b1b0fe27b19a3be152fd369fdfc15`.
- Source size: 23,117 UTF-8 bytes; original candidate 221 lines.
- Source: https://github.com/KhaosMagnus/Project-Control/blob/48b558caaf989e6952b42265890d60d7b75d2790/planning/PCM-GOV-AUTHREQ-DES-002_R2_AUTHORIZATION_GATE_CORRECTIVE_CANDIDATE_2026-11-22.md

**Temporal note:** R2's internal heading says `PREPARED OFF-REPO / NOT PUBLISHED`. This accurately describes drafting time. The subsequent publication is evidenced by the immutable commit above. Do not silently edit those frozen candidate bytes or treat its historical header as an assertion about the present branch state.

**Review baseline and precedent:**

| Ref | Purpose | Exact revision and Git blob |
|---|---|---|
| S1 — R2 candidate | Review subject | `Project-Control@48b558caaf989e6952b42265890d60d7b75d2790` / `3e817012a1207eec3fe20a058333724b13b20506` |
| S2 — R1 design | Superseded candidate for comparison, not overwritten | `Project-Control@7067be93d2ebf0b5ac8622a1e12a797b62973545` / `332ab4813413cc2c317d33c4ed984cb82395dab4` |
| S3 — original improvement proposal | Original scope | `Project-Control@c31de29ae616fd0ee34f2963b18aaf62cc188006` / `bb58d83874f662a4640a303557982d3ff2a1db0f` |
| S4 — generic v1.0 FROZEN | Historical protocol precedence (not amended) | `dev/portable@e022aee2dfcba6f13bba4d0f4ac57ba4a59154e6` / `1ac3689c1e811d1594291afee6b2c1c6efd093d0` |
| S5 — local provenance R3 | Roles, issuer and event source grading | `Project-Control@48b558caaf989e6952b42265890d60d7b75d2790` / `9ed659715a47a199df4b21005382c68678958dc8` |
| S6 — R3 later local acceptance record | Historic decision and limits, secondary as to Owner source | `Project-Control@48b558caaf989e6952b42265890d60d7b75d2790` / `107aab1f7332849385737655bb171da1b712980a` |
| S7 — ROLE_REGISTRY snapshot | Current record limitations; does not alone activate PCM-002 | `Project-Control@48b558caaf989e6952b42265890d60d7b75d2790` / `624e1efa155e9e731fd1dbf2f064a0b5055c5aae` |
| S8 — local document discovery guidance | Separate improvement, **outside** F1–F3 scope | `Project-Control@48b558caaf989e6952b42265890d60d7b75d2790` / `3b83f096e4d5f2f534db116239fae6bdc76902b2` |

**Pinned navigation:**
- S2: https://github.com/KhaosMagnus/Project-Control/blob/7067be93d2ebf0b5ac8622a1e12a797b62973545/planning/PCM-GOV-AUTHREQ-DES-001_AUTHORIZATION_REQUEST_GATE_DESIGN_2026-11-22.md
- S3: https://github.com/KhaosMagnus/Project-Control/blob/c31de29ae616fd0ee34f2963b18aaf62cc188006/proposals/PCM-GOV-AUTHREQ-001_EXPLICIT_AUTHORIZATION_REQUEST_GATE_2026-11-22.md
- S4: https://github.com/KhaosMagnus/Project-Control/blob/e022aee2dfcba6f13bba4d0f4ac57ba4a59154e6/bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/protocol/GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0.md
- S5: https://github.com/KhaosMagnus/Project-Control/blob/48b558caaf989e6952b42265890d60d7b75d2790/records/provenance/PCM-GOV-PROV-DES-003_ATTRIBUTION_CONTRACT_R3_CORRECTIVE_DRAFT_2026-11-20.md
- S6: https://github.com/KhaosMagnus/Project-Control/blob/48b558caaf989e6952b42265890d60d7b75d2790/records/provenance/PCM-GOV-PROV-R3-ACCEPTANCE-001_LOCAL_OWNER_DECISION_RECORD_2026-11-21.md
- S7: https://github.com/KhaosMagnus/Project-Control/blob/48b558caaf989e6952b42265890d60d7b75d2790/ROLE_REGISTRY.md
- S8: https://github.com/KhaosMagnus/Project-Control/blob/48b558caaf989e6952b42265890d60d7b75d2790/planning/PCM-GOV-RECOVERY-SOURCE-001_PROJECT_LIBRARY_DISCOVERY_CONTROL_2026-11-22.md

**Independent historical QA1 / QA2 reports (only referenced, not reproduced nor uploaded to the public GitHub repository):**
- QA1: `PCM-GOV-AUTHREQ-DES-001_IQA-001_CHATGPT_REPORT.md`, SHA-256 `e5e8b04d89ce73fa48a5144fa1dde91d983036648d20ef8c4348c7e72979bed7`; `DOCUMENTARY REVISE` / 12 verified, 1 partial, 1 failed; 14 design-covered, 4 partial scenarios.
- QA2: `PCM-GOV-AUTHREQ-DES-001_IQA-001_GROK_REPORT.md`, SHA-256 `fbdc203ba5bd8ba8a37653fbab009d9bd6b63b2add2c8b05dd6eeeb45e0f8dbe`; `DESIGN PASS (CONDITIONAL)`.
- The full original QA reports may be available in the Owner's ChatGPT Library / existing custody; **not** guaranteed accessible to either independent reviewer. R2 §1 summarizes findings, but this is a coordinator-authored secondary summary, not the primary independent report. If verification of source-report bytes is essential and they cannot be retrieved, mark the specific evidentiary limitation; do not pretend to have opened them. Do not ask for duplicate upload before checking accessible Project/Library surfaces.

## 2. Mission of focused re-QA

Determine whether R2 has **closed all three findings** from QA1 on R1 without reintroducing regressions, weakening a historic frozen rule or claiming operational enforcement that has not been implemented.

- **F1 / HIGH:** `DEFERRED_WITH_OWNER` in R1 §2.2 allowed deferral without actual Owner/delegate decision, bypassing the duty in G-AR-05 to issue a request when a material required action lacks a grant.
- **F2 / MEDIUM:** R1 lacked explicit correspondence across decision, request status and closure, notably `REJECT` distinct from `DEFER/REVISE/NONE`, and mixed Owner decisions.
- **F3 / MEDIUM:** R1 did not fully specify traceability for one-shot grants through attempt, readback, result uncertainty, recovery and reuse.

These are documentary contract defects. Re-QA is not a test of a deployed checker, adapter, LLM prompt enforcement or GitHub CAS capability.

**Independence rule:** QA1 and QA2 must each evaluate R2 using S1–S8 independently and must not consume the other's new R2 QA report prior to return. Two LLM products are not automatically two independent humans or credential boundaries. Coordinator self-review does not count as independent QA.

## 3. Mandatory focused findings matrix

For each finding report `CLOSED / PARTIAL / OPEN / INCONCLUSIVE`, exact source+section, proof, residual risk and corrective proposal:

| Finding | Mandatory documentary checks |
|---|---|
| F1 | S1 §§2–3 and G-AR-05 in §6.1: `DEFERRED_BY_AUTHORITY` requires valid decision with source and reopen condition; a recommendation cannot be converted to deferral; `PREPARED_NOT_REQUESTED` is not a material closure; `BLOCKED_AUTHORITY` must include request/clarification; AR-N01 rejects "recommend and defer". Check direct Owner grant does not require fabricated earlier request. |
| F2 | S1 §§3–4: separate decision/request/closure domains; explicit `REJECTED_BY_AUTHORITY`, `DECIDED_REJECTED`, `DEFERRED_BY_AUTHORITY`; `ACCEPT_MODIFIED`; mixed outcomes per clause; user-supplied options are never the limit of Owner authority. |
| F3 | S1 §5 and G-AR-04/07/09/10: grant ID, issuer, scope, mode, operation and attempts/readback; `UNKNOWN/PARTIAL/CONFIRMED_APPLIED/CONFIRMED_NOT_APPLIED`; prohibition on blind retries; documentation of when original authority still covers a recovery versus when a **new** grant is needed. Test `AR-N05/N06`. |

**Failure policy:** one material OPEN finding means `DOCUMENTARY REVISE`; an unverifiable source central to a material claim means `INCONCLUSIVE` for that claim, not a fabricated `PASS`. If a finding is only PARTIAL, justify whether it is material enough to block acceptance.

## 4. Full regression matrix — AR-AC01–AR-AC14

Report a separate verdict for **each**: `VERIFIED / PARTIAL / FAILED / INCONCLUSIVE`, with exact S1 section, reference baseline (S2–S6), and risk.

| ID | Requirement |
|---|---|
| AR-AC01 | Recommendation and actual authorization request remain distinct; no automatic issuance |
| AR-AC02 | Draft decision labelled Owner is not an emitted Owner act |
| AR-AC03 | Design acceptance does not authorize publication/implementation |
| AR-AC04 | A material prepared but unpublished deliverable cannot close via self-deferral; requires effective grant or actual express request/clarification |
| AR-AC05 | Bounded direct Owner instruction can authorize the specified stage without redundant request |
| AR-AC06 | Ambiguous broad instruction stops materially uncertain writes |
| AR-AC07 | One-shot grant cannot be reused without scope/readback/consumption determination |
| AR-AC08 | Recommender, drafter, issuer, authorizer, operator and QA remain distinct with R3 provenance |
| AR-AC09 | Rollover recovers open requests, exact control/role state, grant and uncertainty |
| AR-AC10 | Publication requires confirmed readback of exact ref/commit/blob to claim completion |
| AR-AC11 | Incidental nonmaterial advice does not force artificial approval |
| AR-AC12 | Portable successors require explicit versioned adoption; no automatic cross-project effect |
| AR-AC13 | Prompt/ledger/checker/gateway limits are accurately characterized; no unfounded universal enforcement |
| AR-AC14 | No rewriting of frozen v1.0, local R3 or historical G2-B QA; R1 remains preserved |

Particular attention: R2's §7 self-labelled `Diseñado` and `Corregido propuesto` are **author assertions**, not independent evidence of QA PASS.

## 5. Full scenario coverage — original AR-T01–AR-T18

For **each** stimulus, give `DESIGN COVERED / PARTIAL / MISSING / INCONCLUSIVE`, S1 evidence, reasoning and correction if needed. This assesses contract consistency; **DO NOT CALL THESE EXECUTED TESTS**.

| ID | Scenario |
|---|---|
| AR-T01 | "Recomiendo borrar X" → recommendation only |
| AR-T02 | "Solicito autorización para borrar X" → emitted request, not grant |
| AR-T03 | Agent drafts `OWNER GRANTED` → agent draft only |
| AR-T04 | Owner accepts only design → no execution |
| AR-T05 | Owner grants A,B in meta, not C/main → only A,B |
| AR-T06 | Local repo-bound reports with no publication grant → request, not invented deferral |
| AR-T07 | Direct Owner instruction for bounded design → proceed design without invented request |
| AR-T08 | Ambiguous "adelante" among material options → STOP uncertain write |
| AR-T09 | Owner rejects → `REJECTED_BY_AUTHORITY`, not DEFER |
| AR-T10 | Owner explicitly defers → `DEFERRED_BY_AUTHORITY`, proof required |
| AR-T11 | Consumed one-shot permission → verify consumption and grant applicability before another action |
| AR-T12 | Chat rollover → transfer request, grant, attempts, uncertainty |
| AR-T13 | HEAD changed before write → reconcile without blind retry |
| AR-T14 | GitHub admin access but no Owner grant → BLOCKED_AUTHORITY |
| AR-T15 | Pure incidental advice → OUT_OF_SCOPE_NO_ACTION |
| AR-T16 | Universal LLM enforcement claimed without gateway → reject |
| AR-T17 | Owner only permits archiving a draft → published if verified, not accepted/released |
| AR-T18 | Owner accepts design but defers release → separate dispositions by clause |

## 6. Additional adversarial scenarios — AR-N01–AR-N06

Report **each** separately, using the same `DESIGN COVERED/PARTIAL/MISSING/INCONCLUSIVE` fields.

| ID | Scenario |
|---|---|
| AR-N01 | Agent recommends publishing and declares "deferred" without Owner decision → INVALID_CLOSURE + real request |
| AR-N02 | Agent shows its own GRANTED button and assumes approval → draft/pending, never grant |
| AR-N03 | Owner rejects although only GRANTED/DEFERRED/REVISE suggested → REJECTED_BY_AUTHORITY |
| AR-N04 | Owner approves A but rejects B in same message → two distinct decisions/scopes |
| AR-N05 | Tool returns ambiguous write error under one-shot grant → EXECUTION_UNCERTAIN, readback before retry |
| AR-N06 | Readback shows the write was already applied despite error → CONFIRMED_APPLIED, do not repeat or invent new grant |

**Cross-check:** if the result of an adversarial case conflicts with closure table or G-AR-05, classify as PARTIAL/FAILED with exact citation even if S1's own scenario table lists the correct expected behavior.

## 7. Required risk/limitation checks

- Detect inconsistencies between S1 §§3,4,5,6 and the matrices (§§7–8), especially `REVISE_REQUIRED` self-labeling, `BLOCKED_AUTHORITY` versus request emission and conditions to reopen a rejected/expired action.
- Distinguish recovery of an interrupted operation under a still-effective original grant from performing a **new effect**; do not demand redundant fresh authorization for read-only reconciliation.
- Classify evidence per claim, not per file. Git blob and SHA-256 identify bytes but do not authenticate the original Owner chat message. `SECONDARY_ATTRIBUTED` authority must not become `PRIMARY_OBSERVED` outside the originating session.
- Frozen R1 and v1.0 not amended. No adoption into other projects, no `main` integration, no version choice or automatic release.
- Check if any assertion in S1 relies on an unavailable QA1/QA2 original; the reviewer must distinguish directly opened sources from report summaries and constraints.
- Tool-capacity claims remain documentary only; no claim that `expected_sha`, `force=false` or a prompt universally prevents race conditions or unauthorized writes.
- The local source discovery guide (S8) has its own approval status; do not silently merge it into R2 QA as a fourth finding.

## 8. Return format and decision boundaries

Deliver **one Markdown report per reviewer** to the Owner, for delivery to PCM-002. Use the following sections:

1. Reviewer identity, mode, exact candidate commit/blob/SHA-256 if independently verified and list of original sources actually opened (and unavailable sources).
2. Executive verdict: `DESIGN PASS` / `DESIGN PASS (CONDITIONAL)` / `DOCUMENTARY REVISE` / `INCONCLUSIVE` with explicit materiality basis.
3. Focused F1, F2, F3 outcome matrix `CLOSED/PARTIAL/OPEN/INCONCLUSIVE`.
4. **14-row** AR-AC01–AR-AC14 matrix with exact evidence and remedies.
5. **24-row** scenarios matrix AR-T01–18 + AR-N01–06 with separate coverage grades and evidence; no summarizing all 18 into one undocumented PASS.
6. Findings ordered by severity, residual risks and precise corrections.
7. Version/compatibility/authority scope; list limitations clearly.
8. SHA-256 of the **final report bytes** if actually calculated; else `NOT CALCULATED`. Never invent a hash.
9. Explicit `NO GITHUB WRITES / NO TECHNICAL TEST EXECUTION / NO NORMATIVE ACCEPTANCE / NO RELEASE` declaration.

**A QA report is neither a new Owner decision nor permission to change source files.** Reviewers may not update GitHub, publish findings, request/activate another QA or modify any frozen candidate. They return their reports to the Owner, who can relay both for reconciliation. The coordinator will then propose the next gate; acceptance/implementation/versioning remain reserved Owner acts.

**Transport note:** GitHub publication of this packet does not mean ChatGPT QA1/Grok QA2 have received or executed the assignment. Owner-mediated handoff remains necessary. The public packet references existing private QA materials only by identity/hash; it contains no private report bytes.

**END OF SHARED R2 FOCUSED DESIGN RE-QA PACKET — NO QA VERDICT CLAIMED.**
