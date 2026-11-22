# PROJECT CONTROL MASTER — TRANSFERENCIA ACOTADA P5

**SOURCE:** PROJECT_CONTROL_MASTER / PCM-001 (PROVISIONAL)  
**TARGET:** SECOND_INSTANCE_GITHUB_REVIEWER_ELIGIBILITY / provisional independent read-only reviewer  
**ASSIGNMENT:** `PCM-G2B-P5-REVIEWER-ELIGIBILITY-001`  
**MODE:** AUTHORIZED READ-ONLY / IDENTITY + PERMISSION FEASIBILITY REVIEW / REPORT ONLY  
**DATE:** 2026-11-20  
**REPOSITORY:** `KhaosMagnus/Project-Control` — PUBLIC — GitHub repository ID `1465064417`  
**OWNER GRANT:** `PCM-G2B-INFRA-GENESIS-001 — GRANTED`, limited to Owner-operated infrastructure genesis P0–P8. This delegation is strictly investigative and does not transfer the Owner's operational authority.

## 1. Purpose

Determine whether the **separate GitHub account linked to this second ChatGPT instance** can technically serve as an eligible reviewer for future PRs to protected `main` and `meta/project-control`. Produce a verifiable evidence-based report to the Owner for forwarding to PCM-001. **Do not perform a GitHub review, approve a PR, create any PR, invite any collaborator, or modify any permission.**

The difference between a separate ChatGPT account, a distinct GitHub identity, a GitHub account with effective reviewer permissions, and an independent human reviewer must be kept explicit. Two accounts controlled by the same human do **not**, by themselves, establish human independence.

## 2. Frozen state provided by source (reconfirm independently)

- `main`: published root commit `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`, zero parents; tree `04bff84a661781fb8f3982235c6c93f668a658ed`; only `README.md` blob `56fd6d6560434e067c126c152ab86298bd57d61f` mode `100644`.
- `meta/project-control`: NOT CREATED. Local candidate root SHA `cac838940e0e824a1f828ff660e422a6441a1da7`, but **must not be published** under this assignment.
- Common branch ruleset `PCM-GENESIS-SAFETY`, ID `27708103`: ACTIVE; targets both branches; deletion + non-fast-forward forbidden; bypass list empty.
- `R-MAIN`, ID `27709862`: ACTIVE, target exactly `refs/heads/main`, `pull_request.required_approving_review_count = 1`, `required_linear_history`, no bypass. API currently reports allowed PR merge methods `merge`, `squash`, `rebase`; the approved operational contract permits only squash or rebase. Assess effective feasibility, but DO NOT change rules. `R-MAIN` also reports deletion/non-fast-forward rules (redundant with common guard).
- Shared installation `162412374` has `repository_selection=selected`, retains the 11 previously authorized IDs, and does not contain master repository ID `1465064417`.
- Current stage: P4 readback PASS; P5 configuration VERIFIED; reviewer eligibility NOT VERIFIED; P6/P7/P8 NOT STARTED. G3/G4/G5, CAS tests, permissions changes, and other repository operations are outside scope.

## 3. Authorized investigative steps (all GET/read-only)

1. Retrieve identity of **the GitHub principal actually attached to this ChatGPT instance** from the connected GitHub app, if exposed (`get_profile`/authenticated user). Report only public login, not private email, tokens, or other identifying data. If identity is not exposed, classify `NOT VERIFIED`; do not assume that the ChatGPT account and GitHub user are the same identity.
2. Re-read repository metadata, `main`, and rulesets `27708103` and `27709862` from GitHub; compare their IDs, state, branch-targeting, review count, linear history, and bypass entries against §2. Read any unexpected difference as a finding, not an invitation to repair.
3. Check **effective permissions for that specific GitHub principal on `KhaosMagnus/Project-Control`**, using a read-only authorized collaborator-permission endpoint or an authenticated GitHub UI indication where available. Distinguish authenticated account `read`/`triage`/`write`/`maintain`/`admin` from permissions granted to a GitHub App installation. Public repository readability by itself does not prove write/reviewer eligibility. If read-only tooling cannot establish the permission conclusively, record `NOT VERIFIED` and what evidence the Owner would need to collect.
4. Determine whether the GitHub login differs from the `main` genesis author account `KhaosMagnus`, and whether that login would be eligible to contribute an approval that **counts** for the required review on a future PR. Base the judgment on up-to-date official GitHub documentation and effective permissions; distinguish permission-level eligibility from an actual approved PR (none exists in this stage). Do not perform test approvals.
5. Assess prerequisites to make the route usable in the future: accepted repository invitation if one exists, minimum access role, separation from PR authorship and who would merge. **Do not issue, accept, or request invitations, or change collaborators or rulesets**. If a permission grant is required, prepare a separate Owner decision request; do not execute it.
6. Confirm that the report does not reveal secrets, private email addresses, connection tokens, or internal credential details.

## 4. Explicit prohibitions and STOP

- No POST/PATCH/PUT/DELETE to GitHub; no PR/issue/comment/review/approval creation; no branch, commit, ruleset, repository, user, app-installation, or permission modification; no test push or experimental CAS.
- Do not open or request access to private repositories, including YU3DOH-Carder / Bot MO-SHI / Respaldo; this task concerns only the public master.
- Do not impersonate the Owner or assert authority to execute P6. No G2-B P6 push or P7 ruleset creation under this assignment.
- If tooling reports ambiguous or contradictory identity/permissions, **STOP and report `INCONCLUSIVE`**; do not guess or repair access.

## 5. Exact report to return

Return a self-contained text report with:

- `ASSIGNMENT`, review time and source GitHub account login (if observable); tool/method used; links to GitHub API/documentary references or precise readback.
- Repository ID, `main` tip, `meta` absence, and both ruleset IDs, targets, enforcement, approval count, and bypass.
- Permission evidence for the secondary GitHub identity. State separately: **(a) login distinct**, **(b) role sufficient for a required approval**, **(c) human independence** (not established by account separation), **(d) whether a real approval was tested** (NO).
- **VERDICT:** `ELIGIBLE BY PERMISSIONS (NOT LIVE-TESTED)` / `NOT ELIGIBLE` / `INCONCLUSIVE`.
- If not eligible or inconclusive: exact missing permission/evidence and a proposed **Owner-only decision**, without any action.
- Attestation of strictly read-only work and the limitations of the finding.

Send the report to the Owner, who will transfer it to `PCM-001`. It grants no execution authority and does not close P5 on its own.

## 6. Source references

- Owner GRANT `PCM-G2B-INFRA-GENESIS-001`; executive request SHA-256 `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349`.
- Frozen R5 design SHA-256 `9c329b3c4be0dca6cf60bc27e92bd586a931c9236bd786f402ce508f952562e8`.
- P4 readback contract `PCM-001_G2-B_P4_READBACK_PASS_AND_P5_OPERATOR_GATE_2026-11-20.md`; hash must be independently verified when available.
- Official documentation: https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets ; https://docs.github.com/en/pull-requests/how-tos/review-pull-requests/approving-a-pull-request-with-required-reviews

**END OF HANDOFF**
