# PCM-001 — G2-B / P4 readback PASS and P5 execution gate

**Date:** 2026-11-20 (America/Mexico_City)  
**Mode:** documentary evidence + authenticated GitHub **GET only**; no GitHub writes by PCM-001.  
**Authorizing decision:** `PCM-G2B-INFRA-GENESIS-001 — GRANTED` (Owner only as provisioning operator); frozen request SHA-256 `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349`.  
**Source procedure:** `02_PCM-001_G2-B_OPERATOR_MANUAL_RUNBOOK_2026-11-16.md` and R5 SHA-256 `9c329b3c4be0dca6cf60bc27e92bd586a931c9236bd786f402ce508f952562e8`.

## 1. P4: Owner's command and independent readback

Owner reported one non-force `git push origin HEAD:refs/heads/main`, returned `* [new branch] HEAD -> main` and stopped writes.

Authenticated GitHub GET readback of `KhaosMagnus/Project-Control` yielded:

| Invariant | Observed readback | Disposition |
|---|---|---|
| Repository | `KhaosMagnus/Project-Control`, GitHub ID `1465064417`, PUBLIC, default `main` | MATCH |
| `refs/heads/main` tip | `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb` | MATCH frozen P3 |
| Git commit parent array | `[]`, exactly zero parents | MATCH |
| Commit message | `chore(genesis): reserve portable standard branch` | MATCH |
| Tree | `04bff84a661781fb8f3982235c6c93f668a658ed` | MATCH |
| Tree content | One `100644 blob README.md`, blob `56fd6d6560434e067c126c152ab86298bd57d61f` | MATCH |
| `refs/heads/meta/project-control` | HTTP 404 NOT_FOUND; branch list contains only `main` | EXPECTED ABSENCE |
| Safety ruleset | ID `27708103`, `PCM-GENESIS-SAFETY`, `active`; ref patterns `refs/heads/main`, `refs/heads/meta/project-control`; rules `deletion`, `non_fast_forward`; bypass actors `[]` | CONFIGURATION MATCH |
| Shared GitHub App installation `162412374` | `repository_selection=selected`, 11/11 approved IDs unchanged, master ID `1465064417` not among selected | MATCH |
| Workflow rulesets | Only common safety ruleset present at readback; `R-MAIN` not yet activated | EXPECTED POST-P4 |

**Formal disposition:** `P4 READBACK PASS / EXPECTED POST-P4`. The first root is published. Proceed **only to P5** within the existing Owner G2-B grant. Ruleset readback proves configuration, not adversarial enforcement. No P6 push is authorized until P5 is read back effective and the independent reviewer route is shown viable.

## 2. P5: Authorized Owner-only configuration

In repository Settings → Rules → Rulesets, create one **new branch ruleset**:

- Name exactly `R-MAIN`; target `branch`; enforcement `Active`.
- Bypass actors: **empty** (no exceptions).
- Branch target: exact inclusion `main` **only**; do not target `meta/project-control` or all branches.
- **Require a pull request before merging**: enabled; **required approving reviews: 1**; GitHub reviewer must be a separate eligible person/account with actual write/review eligibility (not documentary GPT/Grok QA); do not add collaborators or change repo permissions without separate authority.
- **Require linear history**: enabled; verify at least squash or rebase is an available merge method; merge-commit is not an authorized workflow path.
- Leave creation restrictions, direct update restrictions, deployments, signed commits, required checks, code-scanning and code-coverage requirements **disabled** in this profile; preserve the unchanged common safety ruleset. Do not invent status checks or install CI.
- No unapproved auxiliary constraints; no code or branch content changes; no test PR, no push, no bypass.
- Save the new ruleset through Owner UI, record its rule ID and displayed settings. PCM-001 must independently query `GET /repos/KhaosMagnus/Project-Control/rulesets/<ID>`, verify `active`, exact main target, `pull_request` rule requiring one review, `required_linear_history`, and no bypass; verify the safety ruleset is unchanged and meta remains absent.

**STOP:** if required review count cannot be configured, no eligible distinct GitHub reviewer exists, force/deletion protections disappear, a bypass is required, the target is not exactly `main`, GitHub plan prevents a required rule, or readback is inconclusive. Preserve published `main` root and evidence; **do not publish meta** or weaken the ruleset. Any permissions grants or expanded actors require separately approved Owner disposition.

## 3. Pending gates

- **P5:** Await actual Owner UI save and readback, no push permitted yet.
- **P6:** Only after P5 verified, attempt the single approved meta root push (frozen local commit `cac838940e0e824a1f828ff660e422a6441a1da7`) under G2-B; independent readback immediately after.
- **P7:** Protect meta with `R-META`; **P8:** dual independent QA and separate Owner acceptance.
- **G3/G4/G5, app installation changes, CAS, cross-project writes:** Not authorized.
