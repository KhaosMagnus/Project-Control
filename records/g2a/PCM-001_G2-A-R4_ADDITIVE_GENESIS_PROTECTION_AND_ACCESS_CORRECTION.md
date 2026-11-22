# PROJECT CONTROL MASTER — G2-A-R4 Additive corrective design

**ID:** `PCM-G2A-R4-GENESIS-PROTECTION-ACCESS-DES-001`  
**Date:** 2026-11-15  
**Author:** `PCM-001 / PROJECT_CONTROL_MASTER PROVISIONAL`  
**Status:** `DRAFT FOR FOCUSED INDEPENDENT QA / DOCUMENTARY ONLY / NO EXECUTABLE AUTHORITY`  
**Supersession:** additive clarification of three incomplete controls; does **not** rewrite or supersede frozen R3 source documents, original reviews or Owner decisions.  
**Base R3 contract SHA-256:** `c8789106252618549052e25a4dc43eb0b36f3d8bc15ab7d8bdbda0e1fa7ffaeb`  
**Owner R3 design-acceptance SHA-256:** `f23a9c66d1c5166c6645540d305afefa8a514a2eac75189a2355c59ab84eee40`  
**Received focal review (one unique ChatGPT report) SHA-256:** `42e12c2f9c7cf002a7a3cba18b71aabb7518c412de0d5f73bf8246b1368c53c4`  
**Decision still withheld:** `D-R3-APP / G2-B / G3 / G4 / G5`.

## 0. Frozen elements, no reopened architecture

- Provider: `GitHub Free`; destination proposal: `KhaosMagnus/Project-Control`; PUBLIC for both branches and histories, Owner-accepted **as design**, not as an executive push authorization.
- Topology `T-A`: **two distinct zero-parent Git roots**, no common ancestor; no cross-branch merge or indiscriminate tree copy.
- `main` genesis only `README.md` (414 bytes): SHA-256 `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340`; Git blob `56fd6d6560434e067c126c152ab86298bd57d61f`.
- `meta/project-control` genesis only `README.md` (400 bytes): SHA-256 `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0`; Git blob `2b30688846710fe73b89a537bb5a8cfb21e738eb`.
- No G2-B import of YU3DOH contracts, software, PP-002 material or historical authority. Genesis annex classification **`NONE`**, because no confidential attachment is necessary for these two neutral READMEs; this does NOT dispense with separately controlled evidence during later phases.
- Personal GitHub account Owner (to be confirmed for the future executable gate). Manual human operator, non-shared credential, no automatic repository creation through installation `162412374`.

## 1. F-R3-01 — Guard before first publication and partial-state containment

### 1.1 Proposed *fail-closed* provisioning sequence

**This is a proposed future procedure, not permission to perform it.** Exact GitHub UI/API availability and effective protection on a previously empty repository remain `NOT VERIFIED` until a separately authorized gate.

1. `P0 / PRECONDITIONS`: Confirm a separate Owner-approved `D-R3-APP` transition to `selected`, with post-change readback. Obtain an administrative snapshot and exact selected ID set. Verify the selected set excludes the not-yet-created destination by identity and, after manual creation, by its actual ID.
2. `P1 / EMPTY REPO`: Owner-authorized human creates a **public, empty** repo with **no generated README, license or gitignore**. Freeze actual repo ID, visibility, owner, empty refs, default branch target and exclusion from the app. STOP on any foreign ref or unexpected access.
3. `P2 / PRE-PUSH GUARD`: **Before the first commit is pushed**, configure and read back an **ACTIVE** branch ruleset `PCM-GENESIS-SAFETY` explicitly covering `refs/heads/main` and `refs/heads/meta/project-control`. Its *initial* requirements are **block force pushes** and **restrict deletions**. Set **no bypass** for this safety ruleset, to the extent the selected GitHub Free public feature allows. Do not set a branch-creation restriction, required pull request or non-existent status check at this stage, because doing so may reject the two zero-parent genesis pushes. Prove the target patterns and rule application to the proposed branches from authorized administrative evidence. **If an empty GitHub repository cannot have this guard configured/read back, STOP BEFORE THE FIRST PUSH and return to Owner for a revised design. No implicit unprotected fallback.**
4. `P3 / LOCAL OBJECTS`: A single separately authorized operator prepares two independent workspaces. Verify README bytes/paths, file mode `100644` unless expressly approved otherwise, author and committer identities, commit messages, zero parents, and Git trees. Freeze both local commit SHAs **before** touching remote refs. Do not reuse a YU3DOH ancestor. Any differing author/committer metadata or tree contents is STOP and requires refreeze.
5. `P4 / FIRST ROOT`: Push `main` non-force once. After the response **or an ambiguous timeout**, independently read back `main`, `meta/project-control`, the expected commit SHA, the tree and active safety rules. If the state matches `main=expected`, `meta=absent`, move only to `P5`; otherwise follow the recovery table.
6. `P5 / MAIN WORKFLOW PROTECTION`: **Before attempting the second push**, activate and verify the future-update workflow protection for `main` (profile `R-MAIN` in §2), in addition to the safety guard. If this is not possible or effective, STOP with `PARTIAL GENESIS / MAIN CONTAINED BY SAFETY GUARD`, preserve evidence and request authorized resolution. Do not push `meta`.
7. `P6 / SECOND ROOT`: Push `meta/project-control` non-force once. After success, error or ambiguous response, read back **both refs**, actual commit/tree IDs and safety guard. If `main` or its protection differs from the approved snapshot, STOP. Only then advance.
8. `P7 / META WORKFLOW PROTECTION`: Activate and verify future-update profile `R-META` for `meta/project-control`. Read back both profiles and safety guard, app exclusion, repository settings and ref names. STOP on mismatch.
9. `P8 / INFRASTRUCTURE QA`: Independent read-only QA validates two distinct root commits, zero parents, exact byte manifest and modes, no common ancestor (with both objects accessible), metadata, refs, rules, installation exclusion and audit trail. Owner acceptance of G2-B requires its **own** separate decision; G3/G4 remain deferred.

**Security nuance:** pre-push safety guard stops force-push/deletion but does not itself forbid every *ordinary fast-forward* update during bootstrap. Reduce this residual window through a single identified operator, no shared app grant, explicit freeze, immediate per-ref workflow lock and STOP on any unexpected event. Do not describe this as perfectly atomic or absolutely isolated. The Owner/admin can edit rules, so even a no-bypass guard is not an immutable control plane.

### 1.2 Partial and ambiguous remote states

| Readback after any command or ambiguous response | Required disposition |
|---|---|
| Repo not created, or two refs confirmed absent | `NO GENESIS / STOP` unless the exact phase remains within authorized re-entry; do not assume a timed-out command failed |
| `main=expected` and `meta=absent`, safety guard ACTIVE, `R-MAIN` ACTIVE | `PARTIAL PROTECTED / STOP` if second root failed; preserve first root, send snapshot to Owner; no force/delete/reset |
| `main=expected` and `meta=absent`, safety guard ACTIVE but `R-MAIN` not ACTIVE | `PARTIAL GUARD ONLY / STOP`; no second push and no new writes; Owner decides recovery/permission to activate profile |
| Both refs equal frozen expected SHAs and all required profiles ACTIVE | `GENESIS PRESENT / VERIFY` — proceed to independent infrastructure QA, **not** automatically to G3 |
| `meta` present while `main` absent; foreign refs; unexpected SHA, tree, visibility or app inclusion | `UNEXPECTED STATE / STOP`; freeze evidence and require separate Owner recovery decision |
| Any required configuration/readback inconclusive or access denied | `UNKNOWN / STOP`; do not classify as success or authorize blind retry |

Recovery may authorize only evidence-preserving completion with **the same frozen objects**, after rechecking the actual remote state. Replacing any file, changing history, deleting refs, force-pushing, relaxing protections or broadening installation access is **not** a permitted automatic rollback. Require a new exact Owner authorization.

## 2. F-R3-02 — Exact branch profiles and subsequent update route

The following profiles are **proposed configurations** for G2-B acceptance; they are not reported as deployed. The future administrator must record actual rule IDs, enforcement mode and effective ref matches. Where GitHub plan/role restrictions prevent an option, **STOP** rather than silently weaken it.

| Rule | `refs/heads/main` | `refs/heads/meta/project-control` |
|---|---|---|
| Phase P2: common `PCM-GENESIS-SAFETY` | ACTIVE before first push; block force pushes; restrict deletions; no safety bypass | Same coverage before first push |
| Phase P5/P7: workflow profile | `R-MAIN` ACTIVE after `main` root, before `meta` push | `R-META` ACTIVE immediately after `meta` root |
| Subsequent publication | PR into `main` from **main-lineage candidate** | PR into `meta/project-control` from **meta-lineage candidate** |
| Human approval | Require at least 1 eligible independent GitHub review (not merely a GPT/Grok report) when available under this personal-account plan; if none can be configured, STOP for Owner decision | Same; distinct eligible GitHub reviewer required or STOP |
| History | Require linear history; only supported squash/rebase route after reviewed resulting tree and commit identity | Same; no cross-lineage merge |
| Required checks | NONE at genesis; may only be required after a named check and source have been validated and separately approved | Same |
| Bypass for workflow restrictions | Proposed NONE by default. Any temporary necessity: explicit Owner, actor, duration, exact scope and readback. Never grant bypass to common safety prohibitions as an expedient | Same |
| Content and PR audit | Inspect full candidate tree and diff; no foreign project authority/history; validate frozen protocol version only in later G3 | Only new governance records; no product code or tests; no content copied from `main` without an authorized reference contract |
| Merge/integration | Authorized integrator checks base HEAD again, PR state, approving review, scope and resulting commit before final promotion; readback remote head | Same, in separate lineage |

**Bypass and permissions:** Do not equate `admin` in a GitHub connector response to the identity that actually writes, do not assume a reviewer model account can approve a PR, and do not assume that restricting updates to bypass actors leaves deletion and force-push blocked if the same bypass applies to all rules. Keep `PCM-GENESIS-SAFETY` separate from the workflow profile and record each ruleset’s bypass list and admin editability. If GitHub's personal Free feature cannot support the above exact configurations or a usable independent approver, report `NOT READY`; do not claim technical enforcement from a documentary intention.

**First subsequent change:** the only contemplated route is an authorized branch created from the corresponding protected ref, candidate content and evidence reviewed, a pull request to the same-lineage target, an eligible GitHub approval plus any separate GPT/Grok QA and explicit Owner/integrator authorization, followed by an approved integration method and independent readback. This **design path is not a live test**. If GitHub generates a different squash/rebase commit than the candidate, QA and authorized integrator must check the resulting SHA/tree and determine whether a new acceptance is required. A linear Git graph alone does not prevent copying files between histories.

**CAS:** Atomic expected-SHA updates and failure discrimination remain `NOT VERIFIED`; do not use this design to authorize autonomous writers. Future experimentation requires its own isolated scope and permission. No PP-002/ONLINE-1C restart is implied.

## 3. F-R3-03 — Correct installation selection acceptance

**Observed (read only):** installation `162412374`, account `KhaosMagnus`, `repository_selection=all`. Eleven repo IDs returned by the connected identity. This is a **scoped observation**, not the approved administrative inventory.

Let `S_admin(t)` be the entire ID set seen in a dated, directly authorized installation administrator snapshot; let `S_connector(t')` be the observed connector-returned set (currently 11); let `S_approved` be the **Owner-approved exact reconciled ID set**. The executable gate must compare these sets and record deltas. `|S_connector|=11` is **not** an invariant or success criterion.

1. Owner/operator obtains administration snapshot for installation `162412374`: account, timestamp, mode, actual permissions, complete accessible repositories/IDs, and UI/API provenance. This is a future **read-only administrative** action, not performed here.
2. Reconcile `S_admin` against the earlier eleven-ID connector observation and identify any new, missing, renamed or inaccessible ID. Keep `UNKNOWN` dependencies in the proposed retained set until competent project authorities authorize exclusions. Confirm priority functions, minimum READ paths and authorized WRITE operations by coordinator; never run exploratory writes to test continuity.
3. Publish to the Owner a **restricted** exact `S_approved` plus an authorized operator, window, STOP criteria and **ID-specific** recovery. If discrepancy unresolved, STOP. A proposed conservative first wave is all existing reconciled IDs, which limits automatic access to newly created repos without claiming least privilege over retained ones.
4. **Only** after `D-R3-APP: GRANTED`, Owner/operator changes the setting from `all` to `selected`, then reads back `selected`, the entire **exact** `S_approved`, permissions, and priority-flow availability. An extra ID, missing ID or ambiguous readback is STOP. Restore individual IDs only under the approved response scope; returning to `all` is a separate privilege expansion requiring explicit Owner authorization.
5. Future repository creation under G2-B happens **later**, manually outside the shared app. Verify actual new repo ID is **not** in the installation selection. An anonymous read of a public repo is not proof of app exclusion; inspect the authorized administrative configuration. Other user tokens and any independent GitHub App authorizations remain untested.

**No G2-B grant** can be inferred from completion or PASS of the selection change. Keep `D-R3-APP` and `G2-B` distinct executable decisions.

## 4. Executive objects still to freeze after conditional design QA

- Exact Owner authorization for the installation change (`D-R3-APP`), with `S_approved`, actor, date/window and approved recovery; no write prior to that decision.
- Exact future G2-B authorization: repository identity and `PUBLIC`, target branch names, two approved README digests/byte sources, `100644` file mode, authorship and committer identity rules, commit message strings, permitted metadata, authorized operator/credential type, reference SHA capture, stage-by-stage STOP, phase profiles and approved recovery.
- Screenshots/API evidence from the administration channel documenting availability of early rulesets, rule IDs and actual effective matches; can only be collected **in the authorized gate** after an empty repo exists. If no active pre-push guard is possible, STOP; new design/Owner decision required.
- G2-B QA appointment and evidence readback; independent reviewers cannot modify the repo to inspect it. Subsequent protocol import, builder adaptation, release, CAS test and pilot adoption are all out of scope.

## 5. Disposition requested from independent R4 reviewers

Examine whether F-R3-01/02/03 are `CLOSED DESIGN`, `PARTIAL`, or `OPEN`. Separate design-level soundness from real-world platform checks that only an authorized gate can execute. Do **not** count two identical submitted R3 files as separate independent reviews. Provide one verdict per truly distinct reviewer: `DESIGN PASS (CONDITIONAL) / DESIGN REVISE / DESIGN FAIL / INCONCLUSIVE`. A conditional design PASS does not override the final `GRANTED` reserved to the Owner.

**END STATE:** `R4 DOCUMENTARY CORRECTION DRAFT / NO GITHUB MUTATIONS / D-R3-APP,G2-B,G3,G4,G5 DEFERRED / PCM-001 PROVISIONAL`.

**Reference docs**: https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets ; https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository ; https://docs.github.com/en/apps/using-github-apps/reviewing-and-modifying-installed-github-apps .
