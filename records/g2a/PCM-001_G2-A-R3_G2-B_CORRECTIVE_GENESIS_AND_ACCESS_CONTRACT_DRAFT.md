# PROJECT CONTROL MASTER — G2-A-R3 CORRECTIVE DESIGN FOR G2-B

**Status:** `DRAFT / NOT APPROVED / NON-EXECUTABLE`  
**Date:** 2026-11-15  
**Prepared by:** `PCM-001 PROVISIONAL`  
**Review basis:** QA GPT and QA Grok, assignment `PCM-G2A-IQA-DES-001`, both `DESIGN REVISE`.  
**Source reference:** `KhaosMagnus/YU3DOH-Carder` commit `056adb5097b7ce067082782e8d8c92b42db9082a`. Historical source is cited, not copied.  
**Gate:** `G2-B DEFERRED`; G3/G4/G5 remain deferred.

## 1. Architecture decisions and assumptions

- **Git provider:** GitHub Free, Owner-selected.
- **Proposed destination:** `KhaosMagnus/Project-Control`. The name currently returned `404` via the connected app; this is **not** proof of global name availability.
- **Visibility:** `PUBLIC`, still requiring Owner's **separate, specific** acceptance of both branch histories and public GitHub surfaces. No branch-level confidentiality.
- **T-A recommendation:** one **independent zero-parent root** for `main` and one for `meta/project-control`. No shared ancestor, no cross-branch merges. Do not silently substitute T-B.
- **Genesis:** only two newly authored neutral READMEs, one on each branch. No source-protocol, bootstrap, historical governance, private repo inventory, QA report, script, CI workflow, token, license or release in G2-B.
- **Confidential evidence needed at G2-B genesis:** proposed `NONE`. This narrow disposition does not cover G3 or later governance; a future restricted annex must have authorized custodian, recovery, integrity and access for QA.
- **Authority:** Owner retains all reserved decisions; **no** automatic PCM-001 activation.

## 2. Exact proposed genesis allowlist (draft bytes, not authorized)

Both proposed files use UTF-8, LF-only and final newline; they are held locally for QA and shall not be pushed without explicit Owner approval.

| New branch | Path within branch | Size | SHA-256 of bytes | Git SHA-1 blob |
|---|---|---:|---|---|
| `main` | `README.md` | 414 | `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340` | `56fd6d6560434e067c126c152ab86298bd57d61f` |
| `meta/project-control` | `README.md` | 400 | `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0` | `2b30688846710fe73b89a537bb5a8cfb21e738eb` |

**Proposed `main:README.md` exact bytes rendered as text:**

```markdown
# Project Control

This repository is reserved for the development of the portable Project Control standard.

Status: PROVISIONAL — INFRASTRUCTURE GENESIS ONLY.
No protocol, bootstrap package, adapter, or release is adopted or published by this commit.
This repository does not govern any other project by implication.

Local documentary governance is maintained separately in the `meta/project-control` branch.
```

**Proposed `meta/project-control:README.md` exact bytes rendered as text:**

```markdown
# Project Control Master — Local Governance

This branch is reserved for the documentary governance of Project Control Master.

Status: PROVISIONAL — NO EXECUTABLE AUTHORITY.
No new authority, release, or adoption is activated by this genesis.
This branch holds documentary governance only; product files and tests belong on `main`.
Do not merge `meta/project-control` into `main` or vice versa.
```

The final approved byte manifest must also freeze Git commit messages, acceptable author/committer identity and rules for dates/metadata, plus the two branch names. Because commit SHA incorporates metadata, future commit IDs are read back at execution; they are not fabricated at design time. Any change of README bytes invalidates the above digests and requires renewed review.

## 3. T-A provisioning method — proposed manual two-repository Git genesis

A **single authorized human operator** will use **two distinct clean local Git initializations**, one per root, to avoid accidentally carrying the first tree into the second. No commands are executed by this document. Proposed operational sequence:

1. **Precondition:** authorized installation transition `all → selected` completed and independently verified; existing dependent repo access retained; future Project-Control repo not in the selected set. Freeze an exact installation screenshot/API inventory and the Owner-authorized repository ID set. No client of the shared installation may create the target repo.
2. **Precondition:** Owner accepts PUBLIC exposure, the two exact README digests, T-A, operator and approved Git identity; verify no confidential data in paths, content, commit messages and author metadata. Owner approves a STOP/partial-state recovery method.
3. **Creation:** Owner/identified operator creates **empty** GitHub public repository manually (disable README/license/gitignore auto-generation). Prove repository owner, ID, visibility, no refs, current app-exclusion by an authoritative route. If a race creates unexpected files/refs, STOP.
4. **Two roots:** prepare two **independent new local `git init` workspaces**, one targeting `refs/heads/main`, the other targeting `refs/heads/meta/project-control`; each contains only the respective approved README and a root commit (zero parents). Use a vetted, narrowly scoped Owner credential, not an app writer token from another project. A local `git switch --orphan` route is an alternative only under reviewed step-by-step instructions; never use an inherited YU3DOH history.
5. **Publish:** push `main` first and then `meta/project-control` using ordinary non-force Git pushes. **These two pushes are not atomic as a pair.** If the second fails, mark `PARTIAL GENESIS / STOP`, retain the first branch and its evidence, do not reset/force-push/delete without Owner's separate recovery authorization.
6. **Protect promptly:** authorized Owner applies and inspects protections/rulesets for both refs: force-push/deletion denied, writer and bypass lists recorded, PR/review rules configured to match future authorized publication. Avoid impossible status checks. Confirm restrictions for the actual account/roles; initial unprotected window is a residual risk, never claim retroactive protection.
7. **Read back:** independent auditors verify the two refs/commit IDs, parent array empty for each, trees, exact README SHA-256 and Git blob SHA, full list of public refs and remote repository files, **no common ancestor** by `git merge-base` (distinguish exit code 1 from command failure), no import from YU3DOH, effective rulesets, and installation exclusion. They review the control plane through an appropriately authorized read channel if API returns 403.
8. **Accept:** Owner accepts G2-B only after independent infrastructure QA. G3 and activation remain separate decisions. Future branch writers must have an authorized route that can operate under the resulting protections before G3 is initiated.

**STOP conditions:** target repo present unexpectedly; app still `all`; target unexpectedly included in selected installation; selected set differs from approval; wrong repo ID/visibility; foreign refs/files/history; unexpected Git identity; missing protection; wrong hashes; mismatched branch root; incomplete QA access; unauthorized write capability; inability to restore/reconcile an intermediate state. Do not broaden privileges, use force, or silently downgrade T-A to T-B.

## 4. App installation `162412374` — separate authorized precondition

**Observed snapshot:** `repository_selection=all`; 11 repositories were returned by a connector search. This is a **visible candidate population**, not verified inventory completeness, not dependency proof, and not the approved selected set. The migration may be performed **only after a separate Owner authorization**.

| Field required **for each repo** | Interpretation |
|---|---|
| GitHub repo ID and full name | Authoritative and reconciled with installation configuration |
| Visibility / active owner or coordinator | May require restricted handling for private repos |
| Dependency state | `CONFIRMED / NONE / UNKNOWN` with dated evidence |
| Necessary app operations | `READ / WRITE / ADMIN`; app credential kind and issuer verified separately |
| Keep/exclude disposition | Owner-approved, never remove `UNKNOWN` automatically |
| Post-transition verification | Confirm needed flows and effective selected set |
| Recovery | Owner, trigger, exact access to restore, STOP and escalation |

**Conservative proposal:** choose `selected` with the **entire reconciled authorized existing set** at first, not arbitrarily dropping the 11 observed. This prevents automatic coverage of future repositories without pretending to reduce privileges over the retained ones. Removing unneeded repos is a **later** independent decision. Rely on authorized GitHub settings and installation-owner evidence; the connector search alone is insufficient. A rollback to `all` is privilege expansion and requires authorization, not an automatic response to incident.

## 5. Branch protection and QA architecture

- Rules apply per ref. Require no deletion, no force push and reviewed modification path. Enumerate actors who can bypass, including Owner/admin, plus disable/override conditions. A policy of linear history alone does **not** prevent copying or cherry-picking files across lineages.
- Require QA GPT and Grok to inspect the same frozen G2-B evidence independently. Use read-only credentials or public GET wherever appropriate; server policy inspection may require elevated **read** access, which must be separately controlled.
- Distinguish `initial genesis (manual human)`, `future protected authoring/PR`, `integration by authorized actor` and `autonomous publication CAS`. No claimed capability at one phase proves another.
- Protected-ref atomic conditional write semantics remain `NOT VERIFIED`. Gate any future unattended author/installer on its own documented experiment and authority; do **not** reopen PP-002/ONLINE-1C.
- Attestation of no writes is limited to the reviewers' actual identities/actions; a stable HEAD alone does not prove complete absence of mutations.

## 6. G3 extraction manifest — separate, not part of G2-B

| Source candidate | Proposed treatment at G3 | Explicit caveat |
|---|---|---|
| Frozen Generic Protocol v1.0, blob `1ac3689c1e811d1594291afee6b2c1c6efd093d0` | `PORT EXACT` conditional | Rights, attribution, byte identity and QA before adoption |
| Frozen bootstrap v1.0, tree `a70242dd0827c3ee978a4b9a50d04176b6b71c50` | `PORT EXACT` candidate, not already adopted | Complete manifest, rights and QA; maintain source bytes |
| Github adapter included within frozen bootstrap | Keep frozen original as part of PORT EXACT | New adapter version is additive, never overwrite the frozen artifact |
| `bootstrap/build_package.py`, blob `83a580f9d2339e566ea2a2ceddfa98b39f9ef07f` | `TRANSFORM` under new version if actually needed | Hard-coded historical source PIN cannot define master build |
| Portability Review v1.0, blob `25a5bb4629481562bdd0b3739c66e6933d0bbdc8` | `REFERENCE` as review history by default | Do not import YU3DOH-local evidence as universal policy |
| `CONCURRENT_PUBLICATION_POLICY.md`, blob `9b7c4dfed7b25b98b61e73f342592359b846e490` | `REFERENCE`, evaluate generic `TRANSFORM` later | Local policy is not implicitly the master policy |
| Federated direction and local Git policy | `REFERENCE` immutable GitHub URLs | Preserve roles and local authority distinction |
| All YU3DOH RUN/CR/PP-002/ONLINE-1C operational records | `KEEP LOCAL` | External support state unchanged |
| Master governance state and role ledger | `CREATE NEW MASTER-LOCAL` upon separate G3 authorization | No automatic PCM activation |

Disposition per path is **proposed** and will be frozen with content digests, provenance and publication rights under G3. It does not authorize copying/rewriting the frozen protocol or bootstrap in the present gate. This table eliminates the contradictory `PORT / REFERENCE` status of the portability review in earlier drafts by making `REFERENCE` the default unless Owner expressly supersedes it.

## 7. Decisions still required

- `D-R3-PUB`: Owner explicitly approves PUBLIC for **both** `main` and `meta/project-control`, complete future history and public GitHub surfaces; approves proposed bytes/metadata of G2-B genesis. If not, STOP and revise architecture.
- `D-R3-TOPO`: Owner explicitly selects T-A independent roots and named provisioning method/actor, or specifies a documented T-B exception. No automatic substitute.
- `D-R3-APP`: Owner approves a separately gated and reversible `all → selected` change with exact repository IDs (none presumed) and qualified operator after inventory confirmation. This is **not** covered by design GRANTED.
- `D-R3-G2B`: Only after preconditions, Owner may GRANT creation of the exact new repository/refs and protection configuration with recovery and post-QA. Current state: **DEFERRED**.

This document is a **corrective design draft** for focused independent re-QA. The earlier two QA reports remain immutable; their `DESIGN REVISE` does not convert automatically into PASS. No public repository, branch, settings, credential or release has been changed.
