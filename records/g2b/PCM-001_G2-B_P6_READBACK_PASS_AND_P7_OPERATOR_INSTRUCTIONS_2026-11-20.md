# PCM-001 — G2-B: P6 remote readback PASS and P7 operator instructions

**Date:** 2026-11-20 (America/Mexico_City). **Assignment:** PCM-G2B-INFRA-GENESIS-001. **Authority:** Owner GRANTED for the manual G2-B sequence P0–P8; Owner is the only authorized mutating operator. PCM-001 performed READ ONLY checks. **Status:** P6 PASS; P7 NOT YET EXECUTED. G3/G4/G5 NOT AUTHORIZED.

## 1. Observed P6 readback

GitHub live REST readback on repository `KhaosMagnus/Project-Control`, repository ID `1465064417`, public, default `main`:

| Check | Readback |
|---|---|
| `refs/heads/main` | `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb` |
| `refs/heads/meta/project-control` | `cac838940e0e824a1f828ff660e422a6441a1da7` |
| `meta` commit parents | `[]` (zero) |
| `meta` commit tree | `3e39ae46b9e1690604387452ee7283062a79e182` |
| `meta` tree entries | One: `100644 blob 2b30688846710fe73b89a537bb5a8cfb21e738eb README.md` |
| `PCM-GENESIS-SAFETY` | Ruleset `27708103`, active, exact targets `refs/heads/main`, `refs/heads/meta/project-control`, rules `deletion`, `non_fast_forward`, bypass `[]` |
| `R-MAIN` | Ruleset `27709862`, active, target `refs/heads/main` only, PR/one approval/linear history, methods squash and rebase, bypass `[]` |
| `R-META` | Not listed at this P6 readback |
| GitHub installation `162412374` | `selected`, 11/11 approved repo IDs, excludes `1465064417` |

P6 user-reported single push succeeded; these independent readbacks confirm the expected remote objects and protection state. Two zero-parent commits with distinct trees remain on separate branch tips. No GitHub mutation was performed by PCM-001. The user interface's `Compare & pull request` suggestion must not be used to merge the unrelated branches.

## 2. P7, Owner manual action only

Navigate to `https://github.com/KhaosMagnus/Project-Control/settings/rules` and create a new **branch ruleset** named `R-META`. Configure:

- Enforcement **Active**.
- Bypass list **empty**.
- Exact target branch **`meta/project-control` only**, no wildcards that include `main`.
- Require a pull request before merging **ON**; require **1** approving review.
- Require linear history **ON**.
- Block force pushes **ON**, restrict deletions **ON**, as on `R-MAIN` (the independent common safety rule also remains active).
- Restrict creations **OFF**; restrict updates **OFF**; status checks **OFF** until separately authorized and actually provisioned; no required deployment or code-scanning checks.
- Keep merge methods consistent with `R-MAIN` and the R5 contract: **squash/rebase only**; never merge `meta/project-control` into `main`.
- Do not add collaborators, modify `R-MAIN` or `PCM-GENESIS-SAFETY`, alter the GitHub App installation, commit files, or issue test pushes.

**STOP** if any required rule or no-bypass setting cannot be configured, if the selector targets a different ref, or if GitHub reports a configuration ambiguity. Preserve both branch commits unchanged. The actual availability of an independent eligible reviewer for future PRs remains an explicit condition for those PRs, not proven by the Owner's P5 configuration review; do not call it proven.

After the Owner saves `R-META`, PCM-001 must independently read back its ID, active enforcement, target, rules and no bypass, recheck all three rulesets, both commit tips, branch lineages and installation selection. Only after P7 PASS prepare P8 independent read-only QA with two separate reviewers. Do not ask for the already given G2-B grant again. Owner acceptance of G2-B is separate from QA and never automatically permits G3/G4/G5.

## 3. References

- G2-B executive authorization SHA-256 `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349` (Owner GRANTED).
- R5 corrective specification SHA-256 `9c329b3c4be0dca6cf60bc27e92bd586a931c9236bd786f402ce508f952562e8` (Owner accepted design).
- Local runbook `02_PCM-001_G2-B_OPERATOR_MANUAL_RUNBOOK_2026-11-16.md`, P6/P7; QA contract `03_PCM-001_G2-B_INFRASTRUCTURE_INDEPENDENT_QA_CONTRACT_2026-11-16.md`.
- GitHub URLs: `https://api.github.com/repos/KhaosMagnus/Project-Control/branches`, `/git/commits/cac838940e0e824a1f828ff660e422a6441a1da7`, `/git/trees/3e39ae46b9e1690604387452ee7283062a79e182`, `/rulesets/27708103`, `/rulesets/27709862`.

**Disposition:** `P6 PASS / P7 OWNER ACTION NEXT / P8 NOT STARTED / NO AUTO-AUTHORITY`.
