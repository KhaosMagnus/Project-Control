# PROJECT CONTROL MASTER — G2-A PREPARACIÓN Y AUDITORÍA PRELIMINAR

**Artifact ID:** `PCM-001-G2A-D2D3-PRELIM-20261115`  
**Date:** 2026-11-15 (America/Mexico_City)  
**Author/role:** `PROJECT_CONTROL_MASTER / PCM-001` (PROVISIONAL)  
**Mode:** READ-ONLY OBSERVATION / DESIGN / ROUTING ONLY  
**Status:** PRELIMINARY — NOT INDEPENDENT QA, NOT AN EXECUTABLE AUTHORIZATION

## 1. Authority and scope

Owner selected GitHub Free and agreed to continue preparation. G2-B creation, settings, permission mutation, G3 import/bootstrap, G4 activation and G5 adoption remain **DEFERRED** absent separate exact Owner approval. The proposed public visibility is CONDITIONAL on explicit publication acceptance and content review. The historical source is `KhaosMagnus/YU3DOH-Carder` at control commit `056adb5097b7ce067082782e8d8c92b42db9082a` (pinned extraction source, not necessarily HEAD). No source repository writes are authorized.

This packet is a local conversation artifact, not a GitHub control commit. Do not post it unredacted to a public repository: it includes the names of other private repositories and a future private pilot candidate.

## 2. Observations from GitHub (read-only)

| Locator | Observed value | Interpretation |
|---|---|---|
| Proposed target `KhaosMagnus/Project-Control` | `404 NOT_FOUND` to current connection | Not visible/accesssible; **does not prove name availability** |
| GitHub App installation | `162412374`, account `KhaosMagnus`, `repository_selection=all` | Installation covers current and potentially future repos; not a security boundary for master |
| YU3DOH `meta/project-control` HEAD | `d43c8095f7889e4c620795dd160ef20ccc9e64d1` | Live observation; not an alteration of frozen extraction input |
| YU3DOH `main` HEAD | `54cc3aad246c89a29f2a18be63c539db68cae041` | Product control remains at the observed revision |
| YU3DOH source protocol | `protocols/GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0.md`, Git blob `1ac3689c1e811d1594291afee6b2c1c6efd093d0` | Frozen v1.0; no implicit adoption |
| Source bootstrap tree | `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/`, Git tree `a70242dd0827c3ee978a4b9a50d04176b6b71c50` | Payload candidate; not independently QA-passed |
| Source metadata | `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/PACKAGE_METADATA.md`, Git blob `95233ecfb1afd9004eabc07ecd8e7e9b84b05b4b` | Metadata says independent QA not yet declared |
| Source portability review | `protocols/PROJECT_CONTROL_PORTABILITY_REVIEW-v1.0.md`, Git blob `25a5bb4629481562bdd0b3739c66e6933d0bbdc8` | Historical review, not live authority |
| Source builder | `bootstrap/build_package.py`, Git blob `83a580f9d2339e566ea2a2ceddfa98b39f9ef07f` | Contains historical source PIN; do not silently adapt frozen distribution |
| Source local Git policy | `protocols/GIT_CONTROL_POLICY.md`, Git blob `8e00dd5ae7a153a09ce88c2614fbea2ce3f2393d` | YU3DOH-specific; **reference only** |
| Source federated architecture | `control/PROJECT_CONTROL_FEDERATED_ARCHITECTURE_DIRECTION.md`, Git blob `fb2ee2ffd44415a1a049de433b4e1fe005d89103` | Strategic direction, not infrastructure authorization |
| ONLINE-1C checkpoint | `runs/PP-002_ONLINE-1C_SUPPORT_HUMAN_ESCALATION_RECOVERY_CHECKPOINT.md`, Git blob `b2e64984be77e5884b25993a44ea937c93623e64` | Keep local; A1 INCONCLUSIVE/A2 NO-GO |

**Limit of evidence:** This was a bounded documentary audit of identified inputs, not an exhaustive QA of every file in the source repository or proof of any future target protection.

## 3. D2 — Dependency / installation inventory: initial population

Eleven repositories currently appear under the `all` installation. Visibility alone is **not evidence of operational dependency**. Keep `dependency=UNKNOWN` until a competent project actor confirms the last use, required operations, permission level, effect of removal, and recovery method.

| Repo | Visibility | Current app coverage | Operational dependency | Owner disposition |
|---|---|---|---|---|
| `KhaosMagnus/PLXMonitor` | private | all | UNKNOWN | PENDING |
| `KhaosMagnus/YU3DOH-Model-Showcase` | private | all | UNKNOWN | PENDING |
| `KhaosMagnus/YU3DOH-LoRA-Profiler` | private | all | UNKNOWN | PENDING |
| `KhaosMagnus/NazarickBot` | private | all | UNKNOWN | PENDING |
| `KhaosMagnus/YU3DOH-Carder` | public | all | Historical usage observed; current requirement UNKNOWN | PENDING, coordinate PC-004 |
| `KhaosMagnus/Orgizador-Biblioteca` | private | all | UNKNOWN | PENDING |
| `KhaosMagnus/YU3DOH-PromptKit` | private | all | UNKNOWN | PENDING |
| `KhaosMagnus/certificador-aoi` | private | all | UNKNOWN | PENDING, future pilot separate |
| `KhaosMagnus/YU3DOH-Aspect-Ratio-Visualizer` | private | all | UNKNOWN | PENDING |
| `KhaosMagnus/Bot-MO-SHI` | private | all | UNKNOWN | PENDING, coordinate active control |
| `KhaosMagnus/Respaldo` | private | all | UNKNOWN | PENDING |

**Matrix contract, add per repo:** owner/contact; criticality; operations needed (READ/WRITE/ADMIN); last verified usage + evidence; required GitHub App and signer's identity; future KEEP/REMOVE/UNKNOWN decision; allowed validation; rollback recipient; independent readback; authorization SHA. Unknown dependency **blocks removal**, not the whole documentary study.

**Recommended transition:** before G2-B create a separate Owner-approved permission change plan: take authoritative installation snapshot; identify dependencies; select at least all verified active dependencies; migrate `all → selected`; confirm relevant reads and already-authorized operations; leave the master out of the selected scope initially; if regression appears, STOP and request a separately authorized recovery. **No change is approved by this report.** App visibility and per-call issuer remain distinct proof questions.

## 4. D3 — Extraction & topology: preliminary outcomes

### Content classification

- **PORT EXACT to master `main` at G3 only:** frozen Generic Protocol v1.0; bootstrap payload and included templates as a candidate requiring integrity and independent QA. Preserve precise path, commit SHA, blob SHA, SHA-256 and provenance. `main` also will host newly authored generic compatibility/release material under later authorization.
- **REVIEW/TRANSFORM at G3 only:** GitHub adapter; `build_package.py` with historical source PIN; concurrency/forward-control patterns; portability review used as non-normative evidence. Never silently replace the frozen original.
- **REFERENCE by immutable links:** federated architecture rationale, YU3DOH-local Git policy, PP-002 conclusions, supporting historical decisions.
- **KEEP LOCAL:** YU3DOH state and request ledgers, CR/RUN history, PP-002 files, Carder/Workspace product and local Owner authorizations.
- **CREATE NEW MASTER-LOCAL in `meta/project-control` at G2/G3 as authorized:** state, role and instance registry, request ledger, decision records, publication/QA/recovery policy. No PC-004/YU3DOH authority import.

### Branch topology alternatives

**T-A — Two independent Git roots:** preferred design if an authorized CLI/technical path can reliably create and prove separate genesis roots. Feature branches must derive from their own lineage; never merge `meta/project-control` into `main` or vice versa. Requires before/after SHA, ancestry proof, protection rules and recovery test.

**T-B — Shared historical parent, distinct trees:** fallback only with explicit Owner `REVISE/GRANTED` after audit; replace the complete control tree, enforce no-cross-merge convention and controls, acknowledge shared ancestry. Easier with currently available GitHub app but weaker historical separation; not equivalent to T-A by assertion.

**Observed connector constraint:** `create_branch` takes an existing SHA/base ref; `create_commit` requires `parent_sha`. Thus T-A cannot be claimed supported via those actions alone. A Git CLI actor is a separate separately authorized route; never create it as a side effect of audit. There is no proof here of working protected-branch conditional update for the future repository; ONLINE-1C remains unresolved.

### Pre-publication gates for public GitHub Free

1. Express Owner acceptance of public visibility of **all branches**, PRs/issues/comments and retained history (GitHub Free alone does not imply permission to disclose).
2. Exact G2-B allowlist of neutral minimal genesis files. **No protocol/bootstrap import until G3.**
3. Before first push: public-classification, secrets/PII, private-repo names, embedded credentials, license/attribution and identity provenance review on full byte content.
4. Separate privileged configuration/readback by an authorized actor; use public rules and prove enforcement rather than inferring from REST `403` or design alone.
5. Controlled rollback and STOP on HEAD mismatch, policy gap, unexpected public content, permission scope mismatch or recovery uncertainty. No force and no retroactive purge as a substitute for prepublication review.

## 5. Delegation and independent QA

**Author/coordinator:** PCM-001 prepares audited candidate dossier and common frozen acceptance packet, consolidates but does not self-certify independent QA.

**Design/read-only review now (G2-A):** two independent reviewers: `INDEPENDENT_QA_GPT / PROPOSED` and `INDEPENDENT_QA_GROK / PROPOSED`, each receiving the identical frozen packet. They must inspect original GitHub sources at exact refs and issue separate documentary verdicts (`PASS / REVISE / FAIL / INCONCLUSIVE` with scope, methods, omissions, observations). No repositories, branches, comments, PRs, permissions or settings changes; no unapproved test actions. Submit reports to Owner/PCM by transfer, not GitHub publication. Do not share one reviewer's conclusions with the other before completion.

**G2-B after separate exact Owner authorization:** authorized installer creates minimum repo and applies policies; reviewers independently audit actual newly created repo at exact candidate SHA and compare before/after. A G2-A design PASS is not G2-B infrastructure PASS.

**G3 after separate exact authorization:** author imports allowed generic candidates with provenance; independent GPT + Grok QA validate byte integrity, publication classification, adopted governance, protected refs and recovery. QA PASS is not Owner acceptance or integrator permission.

**G4 activation:** Owner only, after bootstrap accepted, recorded and verified. No authority transfer to other projects.

**G5 external adoption:** a separate project Owner approves a bounded pilot, independent actor runs it and independent QA verifies. One adopter does not prove global portability.

## 6. Formal requests, NOT permissions

- `D2-A`: authorize independent documentary dependency discovery via affected project Owners; no installation mutation. Current disposition: PROPOSED.
- `D3-A`: authorize or recognize the two proposed independent documentary design QA appointments/mandates; no code changes. Current disposition: PROPOSED (Owner's general continuation does not name actors, accounts or tool scopes).
- `D3-B`: choose topology T-A vs T-B after independent reports, and approve exact provisioning method in later G2-B. Current disposition: PENDING.
- `D1-PUBLIC`: confirm public accessibility of both branches and publication allowlist, not just GitHub Free plan selection. Current disposition: PENDING.
- `G2-B`: create repository, refs, policies: DEFERRED. `G3`: DEFERRED. `G4`: DEFERRED. `G5`: DEFERRED.

**STOP:** This report authorizes no GitHub mutation, installation, configuration, import, bootstrap, new privileged identity, product pilot or cross-project delegation. PCM-001 remains PROVISIONAL.
