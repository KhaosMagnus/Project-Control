# PCM-001 — P7 Readback PASS / P8 Independent Infrastructure QA Dispatch

**Date:** 2026-11-20  
**Project:** Project Control Master — PCM-001 (PROVISIONAL)  
**Gate:** `PCM-G2B-INFRA-GENESIS-001` (Owner GRANTED; only P0–P8 manual establishment)  
**Current disposition:** `P7 CONFIGURATION & READBACK PASS / P8 QA PREPARED / OWNER G2-B ACCEPTANCE PENDING`  
**Modifications by PCM-001:** none; all checks were GET/read-only.

## A. Evidence observed from GitHub

| Control | Evidence | Disposition |
|---|---|---|
| Repository | `KhaosMagnus/Project-Control`, ID `1465064417`, `public`, default `main` | VERIFIED |
| `main` | `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`, root, tree `04bff84a661781fb8f3982235c6c93f668a658ed` | VERIFIED |
| `meta/project-control` | `cac838940e0e824a1f828ff660e422a6441a1da7`, root, tree `3e39ae46b9e1690604387452ee7283062a79e182` | VERIFIED |
| `main` README | sole file `README.md`, `100644`, blob `56fd6d6560434e067c126c152ab86298bd57d61f` | VERIFIED |
| `meta` README | sole file `README.md`, `100644`, blob `2b30688846710fe73b89a537bb5a8cfb21e738eb` | VERIFIED |
| `PCM-GENESIS-SAFETY` | ruleset `27708103`, ACTIVE, both refs, deletion + non-fast-forward, bypass `[]`; created `2026-11-20T01:09:59.320-06:00` | VERIFIED configuration |
| `R-MAIN` | ruleset `27709862`, ACTIVE, only main, PR required, 1 approval, linear history, squash/rebase, bypass `[]` | VERIFIED configuration |
| `R-META` | ruleset `27717600`, ACTIVE, only meta, PR required, 1 approval, linear history, squash/rebase, bypass `[]`; created `2026-11-20T04:15:23.475-06:00` | VERIFIED configuration |
| App selection | installation `162412374` `selected`, 11 historical IDs observed, master repo ID absent | VERIFIED as connector-side readback; admin screenshot not included |
| No common ancestor | Each final commit reports `parents=[]` and is a distinct SHA, consistent with disconnected roots | Structural inference supported; formal `git merge-base` check belongs to QA |

Both README SHA-256s were checked against source ZIP bytes: main `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340`, meta `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0`. Git blob/tree object checks matched those source bytes. Reviewers must independently verify the remote content.

## B. Open acceptance questions (do not conceal)

- **Future GitHub review path:** `R-MAIN` and `R-META` demand one approval. The Owner confirmed that `JormungandrMagnus` is another account controlled by the same human; it was not a registered collaborator when checked, and secondary public read access reported `push:false`. The Owner accepted P5 rule configuration personally. This does **not** establish a separate human reviewer. A future PR authored by another account may be reviewed by Owner under GitHub constraints, but the independently governed reviewer route needs explicit QA disposition and, if material, Owner decision. Do not modify collaborators or rulesets implicitly.
- **App selection administrative evidence:** the installed-app enumeration verified `selected` with 11 original IDs and master excluded. The actual administrative page with that post-creation set has not been attached in this P8 packet. This is an evidence limitation, not proof of inclusion.
- **Ruleset operation:** readbacks show active configurations, not a destructive-write negative test; such tests are not authorized.
- **Event history:** Owner provided CLI success messages for single pushes P4 and P6, but current refs alone do not prove every historical operation's absence; an independent reviewer should classify accordingly.

## C. Traceability and authority

- R5 accepted as DESIGN ONLY, candidate SHA-256 `9c329b3c4be0dca6cf60bc27e92bd586a931c9236bd786f402ce508f952562e8`; dual QA PASS conditional.
- D-R3-APP manually changed from all to selected with 11/11 readback PASS (limited), separate from G2-B.
- Owner expressly GRANTED `PCM-G2B-INFRA-GENESIS-001`, with exact executive request SHA-256 `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349`.
- P1 Owner-created empty public repo, P2 guard readback, P3 frozen local roots, P4 main publication, P5 branch profile+Owner review, P6 meta publication, P7 meta profile activated. Evidence and exact objects detailed above.
- Next: two independent P8 read-only QA reports, consolidation, **separate Owner acceptance of G2-B**. No G3/G4/G5, code migrations, release, app changes, CAS, or PCM activation authorized.
