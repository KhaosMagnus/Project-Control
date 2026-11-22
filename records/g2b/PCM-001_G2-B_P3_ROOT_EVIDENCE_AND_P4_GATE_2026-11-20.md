# PCM-001 — G2-B P3 root evidence and P4 gate

**Status:** `P3 LOCAL STRUCTURAL PASS / P4 PENDING OWNER EXECUTION`  
**Mode:** Documentary reconciliation; no GitHub mutations by PCM-001.  
**Authority:** Owner GRANTED `PCM-G2B-INFRA-GENESIS-001`, executive request SHA-256 `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349`.  
**Evidence level:** Local Git outputs were supplied by Owner and not directly inspected from their computer; GitHub state was independently read via the connector.

## 1. Owner local evidence (reported)

| Field | `main` | `meta/project-control` |
|---|---|---|
| Root commit SHA | `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb` | `cac838940e0e824a1f828ff660e422a6441a1da7` |
| Tree SHA | `04bff84a661781fb8f3982235c6c93f668a658ed` | `3e39ae46b9e1690604387452ee7283062a79e182` |
| `rev-list --parents` | Only root SHA, zero parents | Only root SHA, zero parents |
| `git ls-tree -r` | `100644 blob 56fd6d6560434e067c126c152ab86298bd57d61f README.md` | `100644 blob 2b30688846710fe73b89a537bb5a8cfb21e738eb README.md` |
| Exact message | `chore(genesis): reserve portable standard branch` | `chore(genesis): reserve local governance branch` |
| README SHA-256, Owner local hash | `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340` | `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0` |

The Git log and trees as reported match the frozen genesis constraints. Unrelated zero-parent roots ensure no shared ancestry **provided the actual local objects correspond to the reported outputs**. Author and committer identities and timestamps have **not** been shared or independently audited; Owner must privately confirm public attribution and preserve metadata before push.

## 2. Fresh remote preflight (read-only)

- Destination: `KhaosMagnus/Project-Control`, repository ID `1465064417`, visibility `public`, `size=0`, no branches.
- Ruleset ID `27708103`, `PCM-GENESIS-SAFETY`, `active`, target includes `refs/heads/main` and `refs/heads/meta/project-control`; rules `deletion` and `non_fast_forward`; bypass list `[]`.
- Shared installation `162412374`, `repository_selection=selected`, 11 existing repositories; destination repository ID not returned among selected IDs.
- These are connector observations, **not** proof of the independently required Owner administrative UI readback or enforcement tests for future branches.

## 3. Outstanding Owner-held conditions before P4

1. Confirm locally actual commit author and committer identities, timestamp metadata, messages, and that public attribution is approved; do not disclose email or token in chat. Preserve output privately.
2. Confirm in GitHub **administrative installation settings** that destination ID `1465064417` is excluded from the selected access list; the eleven approved repository IDs remain present. Discrepancy -> `STOP` before push.
3. Only the authorized Owner operator uses separately verified owner credentials, not app installation credentials, for the push.
4. Confirm local `main` HEAD remains `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`; no additional tracked changes or rewritten commits.
5. If any remote ref, ruleset, installation membership, metadata, or identity has changed: `STOP`, preserve evidence and reconcile before remote mutation.

## 4. P4 authorized action / checkpoint

Under the standing G2-B Owner GRANT, and **only if all above conditions are confirmed**, add the HTTPS GitHub remote to `P3-WORK-MAIN` and perform **one** non-forced push of the frozen local `HEAD` to `refs/heads/main`.

Immediately after the attempt **STOP ALL WRITES**, regardless of success/timeout/error. Read back ref, commit ID, parent count, tree, README blob, other ref absence, ruleset state, selected-set exclusion. If ambiguous, `UNKNOWN / STOP`; no automatic retry. P5 is not authorized to start by successful command output alone; the independent remote readback must confirm the P4 expected state.

**Forbidden:** force-push, branch deletion, reset, changing installation permissions, changing frozen commits, publication of meta before P5, G3/G4/G5.

## 5. Next evidence needed

- Owner local attribution approved (a PASS/STOP result is enough in chat; keep email private).
- Owner administrative selected list excludes new destination ID (PASS/STOP).
- Exact output of the **single P4 push** once conditions confirmed; omit tokens and private identity data.
