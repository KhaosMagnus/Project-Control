# Project Control Master — G2-B Executive Authorization Request

**Document:** `PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_REQUEST_2026-11-16.md`  
**Request ID:** `PCM-G2B-INFRA-GENESIS-001`  
**Prepared by:** `PCM-001 PROVISIONAL`  
**Status:** `READY FOR OWNER DECISION / NOT GRANTED / NO EXECUTION`  
**Destination:** `KhaosMagnus/Project-Control`; GitHub Free; PUBLIC  
**Scope:** infrastructure genesis only. No protocol adoption, product content, code, QA report publication, CAS experiment, downstream adoption, or activation of PCM-001.

## 1. Authority and observed prerequisites

- Owner already accepted R5 design only: SHA-256 `9c329b3c4be0dca6cf60bc27e92bd586a931c9236bd786f402ce508f952562e8`; two independent QA `DESIGN PASS (CONDITIONAL)`; fixes `F-R3-01/02/03 CLOSED DESIGN`.
- Authority chain: R3 contract `c8789106252618549052e25a4dc43eb0b36f3d8bc15ab7d8bdbda0e1fa7ffaeb`; R4 correction `bcacf7ed0d36454459c7a6f7846658f40b948b56149271a66dbe762ee3b12725`; R5 corrects phase state P4–P7 and pre/post merge verification. Frozen reports and Owner's grants are preserved.
- `D-R3-APP` already authorized and **performed by Owner**: installation `162412374` changed to `selected`, approved set of 11 existing repos. Post-save readback record `4604228b41da94967e3bacdceaaaa789f612ebfda1739048e4bce275001e8b98`, verdict `PASS (LIMITED)`. The connector returned 11/11 approved name+ID pairs, zero extras/missing, and individual 11/11 repository metadata reads. No write continuity tests; this is not a proof of cross-repo isolation.
- Destination was `404 NOT_FOUND` **from connected context** before issuance; this is not global availability proof. Confirm in owner admin UI immediately before creation. Current selected set must be freshly inspected before G2-B begins.
- Historical source for later G3 remains `KhaosMagnus/YU3DOH-Carder` at `056adb5097b7ce067082782e8d8c92b42db9082a`; **zero YU3DOH bytes** are to be imported at G2-B.

## 2. Exact authorized object scope requested

| Object | Exact allowed state | No other objects |
|---|---|---|
| New GitHub repo | `KhaosMagnus/Project-Control`, under Owner account, **public**, empty at creation; initial default-branch name `main` | No auto-generated README, license, .gitignore, CI, issues/PR/comments, release, or import. Repository default branch must resolve to `main` after P4. |
| `refs/heads/main` | Independent zero-parent commit, single `README.md` **414 bytes**, file mode `100644`; SHA-256 `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340`; Git blob `56fd6d6560434e067c126c152ab86298bd57d61f` | No additional tracked files or shared ancestor |
| `refs/heads/meta/project-control` | Independent zero-parent commit, single `README.md` **400 bytes**, mode `100644`; SHA-256 `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0`; Git blob `2b30688846710fe73b89a537bb5a8cfb21e738eb` | No merge with `main`, no copied project governance |
| Rules | ACTIVE `PCM-GENESIS-SAFETY` before any first push; then ACTIVE `R-MAIN` at P5, `R-META` at P7 | No unprotected fallback. No bypass on safety rules. No new non-existent CI/status checks |
| Installation | `162412374` remains `selected`, approved existing repositories retained; new repo **excluded from selected set** by admin readback before first push | No change to its existing selections or permissions |

**Git commit messages proposed for approval in this grant** (two distinct, exact strings):

- `chore(genesis): reserve portable standard branch`
- `chore(genesis): reserve local governance branch`

**Operator and Git attribution:** the **Owner personally** (authenticated as `KhaosMagnus`) is the sole nominated provisioning operator. The *actual* Git author/committer name and email must be read from the Owner's approved private local Git configuration, preferably a GitHub-verified no-reply address, and frozen with date/time, file mode, tree SHA and both commit SHAs at P3 **before any push**. The Owner must validate that attribution and public email exposure locally. It is prohibited to invent an email or write a secret to Git. If attribution cannot be approved, **STOP before first push**; this grant cannot be used to delegate execution to another operator.

## 3. Exact sequence and automatic STOP gates

**P0:** Verify grant and immutable SHA references, `D-R3-APP selected` readback, ApprovedSet unchanged, Owner credential/actor, local Git version and reviewer eligibility plan; do not write to other repos.  
**P1:** Owner creates exactly one **empty public** repo `KhaosMagnus/Project-Control` manually in GitHub. Freeze actual repo ID and account, verify zero refs/default branch target, current public exposure, and app **not** in selected set. Unexpected object/permissions -> STOP.  
**P2:** Before any commit is sent, create and **read back ACTIVE** branch ruleset `PCM-GENESIS-SAFETY` explicitly matching `main` and `meta/project-control`. It must block force pushes and restrict deletions, with **no bypass**, but must NOT require PR for the two initial creations, prohibit new refs, or require nonexistent checks. If GitHub Free cannot apply/read back the effective guard to an empty repo -> STOP, no push.  
**P3:** In two clean, unrelated local Git workspaces (not cloned from YU3DOH), use the exact README files from this packet. Inspect byte SHA-256, Git blob SHA, tracked paths/modes, independent parentless commits, both commit SHAs, author/committer identity and commit messages. Freeze the output. Different bytes, unexpected refs or identity -> STOP.  
**P4:** Push only `main` non-force once; read back ref, root parent count, tree, README, guard and app exclusion. Expected state `H_main=C_main`, `H_meta=absent`, `G=true`, `A=true` -> advance **only P5**, despite `R-MAIN` not yet attempted. Error/timeout -> read back; never blind retry.  
**P5:** Enable/read back ACTIVE `R-MAIN` (PR + 1 eligible independent **GitHub** review, linear history, no force/delete by safety guard, no status checks at genesis). If not demonstrably viable -> STOP with protected main only; do not publish meta.  
**P6:** Push only `meta/project-control` non-force once. Read back both tips, trees, `G`, `R-MAIN`, exclusion. Expected both roots correct, `R-META` not yet attempted -> advance **only P7**. Any missing/ambiguous or foreign state -> STOP per R5.  
**P7:** Activate/read back ACTIVE `R-META` with the same workflow restrictions appropriate to this ref. If not verifiable -> STOP, preserve both objects, no G3.  
**P8:** Two independent, strictly read-only infrastructure QA reports (GPT and Grok through Owner), then separate Owner acceptance. Neither QA performs writes. No acceptance/activation is inferred from the commits.

**Transition authority:** P1–P7 only under this future explicit GRANTED. Any STOP or ambiguity freezes writes, captures refs, rule IDs, identity, logs and current public state; recovery beyond an already-verifiable expected transition requires a **new exact Owner authorization**. Never delete repo/refs, force-push, reset, relax the guard, broaden installation access or change the operator as an implicit repair. Creation of a public repo is externally visible even on partial failure.

## 4. Ruleset invariants and first later publication

- `PCM-GENESIS-SAFETY`: both ref names explicitly matched, ACTIVE before P4; restrict deletions and block force pushes; bypass list empty. Absence or ineffective coverage -> STOP. Ordinary fast-forward moves during the short initial window remain residual risk.
- `R-MAIN` / `R-META`: ACTIVE per branch in P5/P7, require PR and at least one eligible independent GitHub reviewer (not GPT/Grok documentary signoff), require linear history; candidate must originate from same independent lineage. Restrict bypasses; any required bypass needs separate approval. No CI checks not yet provisioned.
- In a future separately authorized change, approve inputs (`B`, `H`, `D`, `T_expected`, method, reviewer) **before** squash/rebase; verify resulting commit SHA `C`, tree and delta **after** merge. CAS and autonomous publisher remain `NOT VERIFIED` and **not permitted** by G2-B.
- Enabling a rule and observing `ACTIVE` is configuration evidence, not an adversarial security test. Do not perform a destructive test or forbidden write to verify.

## 5. Independent QA and acceptance gate

For each of two distinct reports: inspect repository ID and visibility; selected set excluding new repo ID; exactly the two expected refs; both commits zero parents; distinct roots/no common ancestor (`git merge-base` exit 1 only with both histories fully accessible); each tree consists of a single `README.md` mode `100644` and verified exact content digests; exact commit messages and publicly approved metadata; default `main`; ruleset IDs/patterns/ACTIVE statuses and bypasses; effective PR+review/linear-history rule configurations; list of refs and extraneous surface objects. Compare before/after readbacks and inspect unexpected writes. A read-only evaluator must have public GET plus separately authorized **read-only administrative evidence** if needed.

**Success:** two separate QA reports `PASS` within bounded scope + Owner `ACCEPT` explicitly after inspecting evidence. Even then G3/G4/G5 stay deferred and PCM-001 stays provisional until a separate activation record.

## 6. Owner decision requested (not issued)

**`OWNER DECISION — PCM-G2B-INFRA-GENESIS-001`**  
`GRANTED / REVISE / DEFERRED`

**Exact proposed GRANTED:**

> Authorize **only** the Owner as operator to create empty PUBLIC `KhaosMagnus/Project-Control` manually; configure/read back the common pre-push safety ruleset; prepare two exact frozen README root commits with approved Git attribution and the two specified messages; push `main`, protect it, push `meta/project-control`, protect it, and collect independent read-only infrastructure QA according to P0–P8 and STOP/recovery constraints of this request and approved R3/R4/R5. Approve no unprotected fallback, no deletion/force-push, no source import, no changes to shared installation `162412374`, no other projects, no G3/G4/G5, no CAS experiments or autonomous publication. Actual Owner acceptance of G2-B after QA is separate.

**Not yet authorized:** any action listed above until the Owner issues `GRANTED` referencing the exact SHA-256 of this request after it is frozen. 
