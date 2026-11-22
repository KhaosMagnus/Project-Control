# PROJECT CONTROL MASTER — G2-A INDEPENDENT QA CONSOLIDATION

**Disposition ID:** `PCM-G2A-IQA-DES-001 / PCM-001 CONSOLIDATION`  
**Date:** 2026-11-15 (America/Mexico_City)  
**Mode:** DOCUMENTARY / READ-ONLY / NO GITHUB MUTATIONS  
**Instance:** `PCM-001 PROVISIONAL`  
**Overall finding:** `DESIGN REVISE` — unanimous independent reviewer verdicts.  
**Authoritative effect:** none. Owner's reserved decisions, and `G2-B / G3 / G4 / G5`, remain deferred.

## 1. Evidence and integrity of transferred QA

| Artifact | SHA-256 calculated locally | Reviewer disposition |
|---|---|---|
| `PCM-G2A-IQA-DES-001_INFORME_QA_INDEPENDIENTE.md` | `69704fefbe32beac533c0be41d8aec506190ab4c820968b983551b1c959a550e` | `DESIGN REVISE`, detailed external/public-source rehash |
| `PCM-G2A-IQA-DES-001_GROK_INDEPENDENT_QA_REPORT.md` | `6208c452ae1e3a5644beae7be6949f1652bca2c5b9687e09ee062df7f486a407` | `DESIGN REVISE`, narrower independent source verification |
| `PCM-001_G2-A_INDEPENDENT_QA_SHARED_PACKET_2026-11-15.zip` | `d860ca78bc675eceac003ff1e7db5cf041483465960ccfe70f27ba7d52789033` | Shared frozen review packet |

The ZIP was re-opened locally, CRC checked and all eight manifest-listed documents matched their exact SHA-256. The manifest itself is the ninth ZIP member and its separately calculated digest is `90e6c4e821abd38d04f75d400ac0c367b2f0c989e5c46ab3a0c143e6750eb8ce`. There is no evidence of a material source hash discrepancy.

The independent ChatGPT reviewer performed extensive public source checks, including 9/9 declared Git references, frozen bootstrap bundle checks (11/11 ZIP members, 10/10 manifest entries); it did **not** perform an active proof of GitHub permissions or repo creation. The Grok review independently verified the packet and main protocol/source commit but expressly left some secondary blobs `PARTIAL`. These verification depths differ without contradicting one another.

Both reports attest read-only GitHub operations and no GitHub writes. These are **reviewer attestations**, not a forensic proof covering all time, all tokens or all users. The source commit and current application configuration were also independently read by PCM-001; do not infer from a stable HEAD that transient writes never occurred.

## 2. Reconciled findings

| Finding | QA GPT | QA Grok | PCM-001 disposition | Gate |
|---|---|---|---|---|
| T-A two independent Git roots | Preferred, exact genesis path missing | Preferred, path unproven | **ACCEPT; SPECIFY TWO SEPARATE LOCAL GIT ROOTS** | G2-B |
| Public GitHub Free scope | Prior acceptance of free insufficient for full-history disclosure | Same | **ACCEPT; REQUIRE EXPLICIT OWNER DISCLOSURE CONSENT** | G2-B |
| Pre-publication bytes | Exact allowlist/digests missing | Sanitization/custody pending | **ACCEPT; PROPOSE TWO NEUTRAL READMES; REVIEW BEFORE FIRST PUSH** | G2-B |
| `all → selected` | Incomplete authoritative inventory; preserve unknown dependencies | Same | **ACCEPT; SEPARATE PERMISSION CHANGE AUTHORIZATION** | Precondition to G2-B |
| Confidential annex custody | Explicit `NONE` or verified custody required | Same | **G2-B: PROPOSE `NONE` FOR TWO NEUTRAL GENESIS FILES; REASSESS G3** | G2-B / G3 |
| Portability review, adapter and builder | Ambiguous exact/reference/transform classification | Partially harmonized | **SEPARATE RECONCILED G3 MANIFEST; NO IMPORT IN G2-B** | G3 |
| Protected-branch authorizations and CAS | Actual behavior unknown | Actual behavior unknown | **REQUIRE DESIGN FOR FIRST PROTECTED WRITE; NO AUTONOMOUS PUBLISHER AUTH** | G2-B design, future execution |
| QA independence | Attested read-only | Attested read-only | **ACCEPT QA AS DOCUMENTARY, NOT EXECUTION** | Current |

There is **no material disagreement** between the two reports requiring a third tie-breaker. Independent corroboration is not equivalent to proving every assertion in the design.

## 3. Reinterpretation of material blockers (do not overblock G2-B)

G2-B is **infrastructure-only**: create a neutral repository and two separated minimal initial branches with protections, with *no* protocol or bootstrap import. Therefore license clearance, complete import-manifest reconciliation, builder transformation and release QA remain G3 prerequisites, not automatically G2-B blockers. Confidential archival infrastructure is not required at G2-B **if** the Owner formally approves the proposed exact neutral genesis bytes and documents no indispensable confidential annex (`NONE`) for this stage. Later confidential records need an authorized custody model or a redesigned privacy decision before publication.

The architecture remains dependent on real actions **not yet authorized**: permissions transition, creation, branch pushes and protection. A successful G2-B read-back cannot prove protected-ref CAS behavior without a specifically authorized test. Do not conflate protection of Git history with prevention of cross-branch content copying or independent QA on a PR.

## 4. Authority separation

- `PCM-001` authors the corrected contract and reconciles QA but may not self-certify independent QA or approve execution.
- Owner decides visibility, root topology, permission change, operator and each execution gate.
- Repo actors/installation permissions are not inferred from chat roles.
- QA GPT and Grok remain independent reviewers; their reports stay immutable; any re-QA is a new additive report.
- `YU3DOH / PC-004` and other adopters retain separate authority; `PP-002/ONLINE-1C` is not reopened.

## 5. Recommended disposition

**Accept both reports as documentary evidence with a consolidated `DESIGN REVISE`.** Approve *drafting* of `G2-A-R3` corrective material under existing documentary-only authorization. DO NOT APPROVE G2-B YET. Request only focused re-QA on the corrected design once the explicit permission evidence and Owner publication/topology decisions are available.

**Next material decision:** an explicit Owner statement accepting permanent public exposure of `main`, `meta/project-control`, their commits and GitHub surfaces; accepting T-A two independent roots as the intended design; choosing a qualified actor for an initial manual Git operation; and, in a separate gate, authorizing a bounded `all → selected` change after the full inventory is reconciled. This statement is not an authorization to execute.

## 6. Residual risks

Persistent public exposure on mistaken publication; administrator bypass; shared app permissions for retained repositories; unproven exact CAS semantics; first publication before protection; non-atomic publication of two branch refs; future confidential governance annexes. Residual risks must be visibly accepted or mitigated at the gate where they arise.

**STOP:** No remote writes, creation, branch/ruleset changes, credential changes, automatic integration or authority activation under this document.
