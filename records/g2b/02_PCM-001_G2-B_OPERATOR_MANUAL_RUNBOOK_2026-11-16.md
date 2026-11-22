# PCM-001 — G2-B Operator Manual Runbook (Future Authorized Gate)

**Status:** `INSTRUCTIONS ONLY — NEVER RUN WITHOUT G2-B GRANTED`.  
**Actor:** Owner only. **Environment:** Git CLI isolated workspaces; not YU3DOH repo.  
**Sources of authority:** R3 `c8789106252618549052e25a4dc43eb0b36f3d8bc15ab7d8bdbda0e1fa7ffaeb` / R4 `bcacf7ed0d36454459c7a6f7846658f40b948b56149271a66dbe762ee3b12725` / R5 `9c329b3c4be0dca6cf60bc27e92bd586a931c9236bd786f402ce508f952562e8` / D-R3-APP post-save `4604228b41da94967e3bacdceaaaa789f612ebfda1739048e4bce275001e8b98`.

## Before any remote mutation

- Confirm Owner `GRANTED` exact authorization request SHA-256. Verify identity and repository selection still `selected`, and its 11 existing repositories still match approved `(ID, name)` set. Do not change any existing repo or app grant.
- Confirm repository name `KhaosMagnus/Project-Control` availability from Owner UI (404 alone is insufficient). Confirm GitHub Free public branch rulesets are present in this account's UI. Confirm an eligible distinct GitHub reviewer exists for future PR approval, or record uncertainty and recognize that P5/P7 may be a STOP.
- Confirm public Git author/committer name+email selected by Owner locally (do **not** expose secrets in chat). Avoid accidental personal-email exposure; GitHub no-reply only when verified in Owner account settings. The two exact messages below are fixed.
- At P1 Owner creates GitHub repository **without** auto README, license or .gitignore. Capture `repo_id`, `owner`, `public`, and refs/branches (should be empty), and prove the new `repo_id` absent from the **administrative selected list**; public GET accessibility is not an exclusion test.
- P2 before any push: configure **branch ruleset** `PCM-GENESIS-SAFETY` with explicit exact targets `main`, `meta/project-control`, `ACTIVE`, block force pushes, restrict deletions, **no bypass**, no branch-creation restriction, no PR/status requirement. Record rule ID, screen, selector semantics, effective targeting. If unavailable/readback inconclusive: STOP before first push. Documentation: https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository

## Safe local object preparation (P3)

The reviewed README payloads are supplied in the controlled package as `genesis/main/README.md` and `genesis/meta-project-control/README.md`. Extract their *bytes* directly into two separate clean directories; do not retype or use a formatter. Verify before any git command:

```sh
sha256sum genesis/main/README.md genesis/meta-project-control/README.md
# EXPECT:
# e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340  genesis/main/README.md
# 326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0  genesis/meta-project-control/README.md
```

The following is an illustrative **future operator sequence**; no execution is authorized by the presence of commands. Use shell quoting suitable for the actual OS. Set Git identity from the Owner's **validated actual value**, not from placeholder examples.

```sh
# Workspace A; should contain only approved README.md
cd <PRIVATE_CLEAN_WORKSPACE_MAIN>
git init -b main
git config user.name "<OWNER_APPROVED_GIT_AUTHOR_NAME>"
git config user.email "<OWNER_VERIFIED_GITHUB_NOREPLY_EMAIL>"
git config core.autocrlf false
git add -- README.md
git diff --cached --name-status
git ls-files --stage
git commit -m "chore(genesis): reserve portable standard branch"
git rev-list --parents -n 1 HEAD            # exactly one SHA on the line
G2B_MAIN_SHA=$(git rev-parse HEAD)
git ls-tree -r HEAD                     # exactly 100644 blob README.md
# Check emitted Git blob SHA against 56fd6d6560434e067c126c152ab86298bd57d61f

# Workspace B; completely independent, NO cloning/fetching from workspace A or YU3DOH
cd <PRIVATE_CLEAN_WORKSPACE_META>
git init -b meta/project-control
git config user.name "<OWNER_APPROVED_GIT_AUTHOR_NAME>"
git config user.email "<OWNER_VERIFIED_GITHUB_NOREPLY_EMAIL>"
git config core.autocrlf false
git add -- README.md
git diff --cached --name-status
git ls-files --stage
git commit -m "chore(genesis): reserve local governance branch"
git rev-list --parents -n 1 HEAD            # exactly one SHA on the line
G2B_META_SHA=$(git rev-parse HEAD)
git ls-tree -r HEAD                     # exactly 100644 blob README.md
# Check emitted Git blob SHA against 2b30688846710fe73b89a537bb5a8cfb21e738eb
```

**Freeze metadata and object IDs now**: two commit SHAs, two tree SHAs, both author and committer ident strings/dates, file modes, Git object format (`sha1`), messages and exactly one path per tree. Do not publish if any check fails. If e-mail exposure is not approved, STOP at P3.

## Controlled remote sequence (P4–P7)

The Owner uses a *separately verified owner credential*, never app installation `162412374` for pushes. `git push` commands shown are **not** to be run until the UI readback and exact preconditions succeed.

```sh
# In workspace A, after P0–P3 PASS:
git remote add origin https://github.com/KhaosMagnus/Project-Control.git
git push origin HEAD:refs/heads/main
# P4: NOW STOP COMMANDS; read back both refs, tree, common guard and exclusion.

# P5 Owner activates and readbacks R-MAIN. If cannot, STOP: do not run workspace B push.

# In workspace B, only when P5 PASS:
git remote add origin https://github.com/KhaosMagnus/Project-Control.git
git push origin HEAD:refs/heads/meta/project-control
# P6 readback; expected both exact root commit SHAs.

# P7 Owner activates/readbacks R-META. Then P8 independent READ-ONLY QA.
```

Never add `--force`, delete refs, change author data post-freeze, rewrite commits, use auto-retry or perform an unreviewed fallback. Git commands use a credential manager: **never paste tokens into remotes, logs or chat**.

## Phase-specific STOP / expected state summary

| Phase | Expected remote state | Next action | If not verified |
|---|---|---|---|
| P0 | app selected, approved set retained, repo not created | P1 | STOP |
| P1 | new repo empty public, app excludes repo ID | P2 | STOP |
| P2 | safety ruleset ACTIVE targeting both future branches, no bypass | P3 | STOP BEFORE PUSH |
| P3 | two exact independent zero-parent local commits, metadata approved | P4 | STOP BEFORE PUSH |
| P4 | main exact, meta absent, safety active, R-MAIN **not yet required** | P5 | STOP / reconcile no blind retry |
| P5 | main exact, R-MAIN active, safety active, meta absent | P6 | STOP, retain first root |
| P6 | both tips exact, safety and R-MAIN active, R-META **not yet required** | P7 | STOP, preserve public refs |
| P7 | both tips exact; safety+R-MAIN+R-META active | P8 | STOP, recovery request |
| P8 | independent QA confirms roots and controls; Owner acceptance is separate | Await Owner | No G3 until explicit future grant |

All timeout/ambiguous outcomes require an independent remote readback; if unresolved => `UNKNOWN / STOP`. If P4 or P6 push returned success but readback shows objects absent or divergent, the run stops; a second push is **not** automatically permitted. If partial repo exists it must not be deleted to “reset” without a new Owner grant.

## Evidence to preserve for QA

Record repo ID, owner, visibility, exact refs, empty-parent status, commit IDs, tree IDs, `git ls-tree`, `sha256sum` of both blobs, branch parentage + no `merge-base`, rule IDs/targets/enforcement/bypass, default main, selected-set exclusion, operator and environment, timestamp+time zone, action/readback sequence and any errors. Avoid recording reusable credentials. Keep controlled operational logs **outside the public new repository**.
