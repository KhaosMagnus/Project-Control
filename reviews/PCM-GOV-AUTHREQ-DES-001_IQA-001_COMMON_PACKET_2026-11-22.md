# PCM-GOV-AUTHREQ-DES-001-IQA-001 — Paquete común para QA independiente documental

**PROJECT:** Project Control Master / `KhaosMagnus/Project-Control`
**COORDINATOR:** PROJECT_CONTROL_MASTER / PCM-002 (provisional)
**REVIEWERS:** ChatGPT independent instance (QA1) and Grok independent instance (QA2), separately
**DATE:** 2026-11-22
**AUTHORITY:** `PCM-GOV-AUTHREQ-DES-001-IQA-001 — OWNER GRANTED`, mensaje observado directamente en conversación PCM-002 después de la solicitud expresa para preparar y remitir paquete a dos evaluadores; esta constancia es `SECONDARY_ATTRIBUTED` para revisores externos sin export original.
**MODE:** STRICT READ-ONLY / INDEPENDENT DOCUMENTARY DESIGN REVIEW / REPORT ONLY
**PACKET STATUS:** PREPARED FOR OWNER-MEDIATED DISPATCH / NO QA VERDICT / NO OWNER ACCEPTANCE
**CONTROL BASE WHEN PACKET AUTHORED:** `meta/project-control@7067be93d2ebf0b5ac8622a1e12a797b62973545`
**PRODUCT/DEV REF:** `dev/portable@e022aee2dfcba6f13bba4d0f4ac57ba4a59154e6`
**MAIN REF:** `main@6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`

## 1. Exact pinned source inventory

The original files remain the source of truth, not the paraphrases in this packet. Reviewers must inspect the **actual pinned bytes** and cite their exact paths, sections and Git blob SHA. If any source cannot be opened or verified, classify the affected criteria `INCONCLUSIVE` rather than inventing a PASS.

| ID | Source | Git ref / blob |
|---|---|---|
| S1 — CANDIDATE | `planning/PCM-GOV-AUTHREQ-DES-001_AUTHORIZATION_REQUEST_GATE_DESIGN_2026-11-22.md` | `Project-Control@7067be93d2ebf0b5ac8622a1e12a797b62973545` / blob `332ab4813413cc2c317d33c4ed984cb82395dab4` |
| S2 — PROPOSAL | `proposals/PCM-GOV-AUTHREQ-001_EXPLICIT_AUTHORIZATION_REQUEST_GATE_2026-11-22.md` | `Project-Control@7067be93d2ebf0b5ac8622a1e12a797b62973545` / blob `bb58d83874f662a4640a303557982d3ff2a1db0f` |
| S3 — FROZEN PROTOCOL | `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/protocol/GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0.md` | `Project-Control@e022aee2dfcba6f13bba4d0f4ac57ba4a59154e6` / blob `1ac3689c1e811d1594291afee6b2c1c6efd093d0` |
| S4 — LOCAL PROVENANCE R3 | `records/provenance/PCM-GOV-PROV-DES-003_ATTRIBUTION_CONTRACT_R3_CORRECTIVE_DRAFT_2026-11-20.md` | `Project-Control@7067be93d2ebf0b5ac8622a1e12a797b62973545` / blob `9ed659715a47a199df4b21005382c68678958dc8` |
| S5 — LOCAL R3 ACCEPTANCE RECORD | `records/provenance/PCM-GOV-PROV-R3-ACCEPTANCE-001_LOCAL_OWNER_DECISION_RECORD_2026-11-21.md` | `Project-Control@7067be93d2ebf0b5ac8622a1e12a797b62973545` / blob `107aab1f7332849385737655bb171da1b712980a` |
| S6 — PROJECT LOCAL ROLE STATE | `ROLE_REGISTRY.md`, `REQUEST_LEDGER.md` | `Project-Control@7067be93d2ebf0b5ac8622a1e12a797b62973545` / blobs `624e1efa155e9e731fd1dbf2f064a0b5055c5aae`, `1b56efe8be470b74341793237b820955e2ceaa15` |

Primary online paths (pinned, no mutable HEAD fallback):
- S1: https://github.com/KhaosMagnus/Project-Control/blob/7067be93d2ebf0b5ac8622a1e12a797b62973545/planning/PCM-GOV-AUTHREQ-DES-001_AUTHORIZATION_REQUEST_GATE_DESIGN_2026-11-22.md
- S2: https://github.com/KhaosMagnus/Project-Control/blob/7067be93d2ebf0b5ac8622a1e12a797b62973545/proposals/PCM-GOV-AUTHREQ-001_EXPLICIT_AUTHORIZATION_REQUEST_GATE_2026-11-22.md
- S3: https://github.com/KhaosMagnus/Project-Control/blob/e022aee2dfcba6f13bba4d0f4ac57ba4a59154e6/bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/protocol/GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0.md
- S4: https://github.com/KhaosMagnus/Project-Control/blob/7067be93d2ebf0b5ac8622a1e12a797b62973545/records/provenance/PCM-GOV-PROV-DES-003_ATTRIBUTION_CONTRACT_R3_CORRECTIVE_DRAFT_2026-11-20.md
- S5: https://github.com/KhaosMagnus/Project-Control/blob/7067be93d2ebf0b5ac8622a1e12a797b62973545/records/provenance/PCM-GOV-PROV-R3-ACCEPTANCE-001_LOCAL_OWNER_DECISION_RECORD_2026-11-21.md
- S6: https://github.com/KhaosMagnus/Project-Control/blob/7067be93d2ebf0b5ac8622a1e12a797b62973545/ROLE_REGISTRY.md

**Access limitation:** this is a locator-and-contract review packet, not a byte-containing offline archive of all six sources. If the reviewer lacks internet/GitHub access to verify exact bytes, they must request the pinned source artifacts through the Owner and not declare an independent completed QA.

## 2. Purpose

Review whether S1 correctly strengthens the distinction:
`RECOMMENDATION ≠ AUTHORIZATION_REQUEST ≠ AUTHORIZATION_DECISION ≠ EXECUTION_RECORD ≠ VERIFICATION_RETURN`,
without creating redundant approval friction, inferring authority from prose, weakening frozen v1.0 or claiming unsupported cross-provider enforcement. Evaluate the *design* and proposed controls—not the functioning of a future implementation.

**Independence:** QA1 and QA2 must assess the same candidate independently; no sharing of the other QA report before submission. Distinct LLM products do not imply independent humans, and two favourable reports do not automatically authorize publication or implementation.

## 3. Required acceptance matrix — AR-AC01–AR-AC14

| ID | Verify | Expected evidence |
|---|---|---|
| AR-AC01 | A recommendation cannot be mistaken for an emitted authorization request | Explicit type separation, negative case |
| AR-AC02 | A draft grant cannot become an Owner decision | Issuer/source gate, negative case |
| AR-AC03 | Acceptance of design is not a publication/implementation grant | Differentiated scopes and examples |
| AR-AC04 | Material prepared but unpublished files have explicit request or existing grant | Candidate/target/closure rule |
| AR-AC05 | Clear direct Owner grant progresses without redundant request | Scope, exclusions, existing-grant case |
| AR-AC06 | Ambiguous generic “adelante” does not authorize unrelated writes | STOP or bounded inference |
| AR-AC07 | One-shot grants cannot silently become standing authority | Grant consumption/scope |
| AR-AC08 | Attribution roles remain separate | R3 compatibility of actors/events |
| AR-AC09 | Rollover carries pending/OPEN request with revision and authority | Rollover case |
| AR-AC10 | Publication is only completed after exact readback | Ref/commit/blob verification rule |
| AR-AC11 | Trivial advice is not subject to unnecessary approval bureaucracy | Materiality negative case |
| AR-AC12 | Portable standard remains versioned and adoption explicit | No cross-project auto-adoption |
| AR-AC13 | Enforcement claims match actual adapter capabilities | Tier boundaries, limitations |
| AR-AC14 | Frozen v1.0 and G2-B/R3 historical records are not altered or retroactively accepted | Pinned SHA/ref and scope checks |

**Required per criterion:** `VERIFIED / PARTIAL / FAILED / INCONCLUSIVE`, exact source reference, reasoning, materiality and remedy. Do not silently substitute opinion for evidence.

## 4. Candidate design test cases — AR-T01–AR-T18

These are **documentary stimulus/expected-behavior tests to inspect for adequacy**; no implementation exists to execute them.

| ID | Stimulus | Expected contractual classification |
|---|---|---|
| AR-T01 | Agent recommends deleting file X | Recommendation, no request or grant |
| AR-T02 | Agent explicitly requests deletion permission | Request only, no permission |
| AR-T03 | Agent drafts an Owner GRANTED message | AGENT_DRAFT, no Owner emission |
| AR-T04 | Owner accepts only design | No execution authority |
| AR-T05 | Owner grants only paths A,B in meta | A,B only; not C/main |
| AR-T06 | Agent prepares local reports requiring repo publication | Actual request or authority blocker |
| AR-T07 | Owner directly directs well-bounded next design stage | Continue design; no invented request |
| AR-T08 | Owner says “adelante” amid materially different options | Only supported scope; STOP ambiguity |
| AR-T09 | Owner rejects proposal | No implied grant |
| AR-T10 | Owner defers | DEFERRED with re-open trigger |
| AR-T11 | A one-shot grant was already consumed | Separate new grant required |
| AR-T12 | Coordinator changes chat to successor | Preserve pending and actual grant source |
| AR-T13 | Target branch HEAD moves before guarded update | STOP, reconcile, no blind retry |
| AR-T14 | Agent has admin GitHub technically, no Owner scope | BLOCKED_AUTHORITY |
| AR-T15 | Agent gives incidental advice | No artificial request |
| AR-T16 | Agent claims universal LLM enforcement without gateway | Reject unsupported assertion |
| AR-T17 | Owner grants archive of a draft only | Published, not QA/release/adopted |
| AR-T18 | Owner accepts design, defers release in one message | Two scope-specific dispositions |

Review **coverage, expected dispositions, contradictions and omissions** of all eighteen cases. Do not label any test `EXECUTED/PASS` merely because it is listed in S1.

## 5. Cross-cutting risk questions

1. Is the trigger `material action` precise enough to avoid false positives and silent omission?
2. How does the system detect prepared-but-unpublished artifacts in an agent response? Is a close-of-turn duty enough, and if not what integration would be needed?
3. Are direct Owner grants distinguished from recommendation acceptance, and how is authority authenticated for readers outside the original chat?
4. Is the accepted local R3 contract reused without silently changing its frozen/source metadata?
5. Does the proposal avoid attributing absolute enforcement to prompt instructions, SHA checking or GitHub roles?
6. Are roles, decisions, exceptions and scope unambiguously separated for single-human operations?
7. Is the versioning impact properly described as contingent, not prematurely labelled MAJOR or MINOR?
8. Does the design specify STOP on contradictory policies and preserve G2-B P5→P6 historic nonconformity?

## 6. Verdict and return contract

Return **one independent Markdown QA report**, authored in the reviewer’s own session, addressed to Owner / PCM-002:

- Assignee identity (model/service if known), input candidate commit and blob exact, reviewed source list and limitations.
- Compact overall verdict: `DESIGN PASS`, `DESIGN PASS (CONDITIONAL)`, `DOCUMENTARY REVISE` or `INCONCLUSIVE`.
- Matrix AR-AC01–AR-AC14 with per-item `VERIFIED/PARTIAL/FAILED/INCONCLUSIVE`, evidence and risk.
- Matrix AR-T01–AR-T18 indicating `DESIGN COVERED/PARTIAL/MISSING/INCONCLUSIVE`; NOT technical test results.
- Material defects ranked by severity, suggested corrections and whether they alter design scope.
- Distinguish evidence read directly from GitHub vs Owner-supplied transcripts, vs inferences.
- Confirm **NO GITHUB WRITES / NO TECHNICAL TESTS / NO NORMATIVE ADOPTION**.
- SHA-256 of the submitted report or explicit `NOT CALCULATED` if hashing unavailable; never fabricate digest.
- Return via Owner for reconciliation. Do not amend the source or the other reviewer’s results.

No reviewer may merge to main, rewrite source, change permissions, activate a new gate or issue an Owner acceptance. The coordinator will reconcile independent reports and request a separate decision on any revised candidate or later acceptance.

**END OF SHARED QA PACKET — SUBJECT TO INDEPENDENT REVIEW; NO QA VERDICT CLAIMED.**
