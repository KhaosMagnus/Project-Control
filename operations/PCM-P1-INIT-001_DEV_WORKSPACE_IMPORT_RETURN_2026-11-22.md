# PCM-P1-INIT-001 — Retorno de ejecución del workspace portable
**SOURCE:** DEVELOPMENT / PROJECT_CONTROL_MASTER / PCM-001 provisional.  
**TARGET:** Owner / PCM-001 governing instance; QA independiente por asignación futura.  
**ACTIVITY:** Owner-approved creation of isolated work branch and byte-preserving historical import.
**AUTHORITY:** `decisions/PCM-BRANCH-STRATEGY-001_OWNER_APPROVAL_2026-11-22.md` published in control commit `0431e24aca2c1ef29add5f32e7942aef39267b8a`.
**DATE:** 2026-11-22. **MODE:** publish candidate to development branch ONLY; no main changes, QA acceptance, merge, release or protocol adoption.
**RESULT:** `WORKSPACE INITIALIZATION DONE / FROZEN v1.0 IMPORTED BYTE-EXACT / NEXT WORK CANDIDATE UNDEFINED`.

## Exact Git identities

- Repository: `KhaosMagnus/Project-Control`, public.
- Historical source repository: `KhaosMagnus/YU3DOH-Carder` @ `056adb5097b7ce067082782e8d8c92b42db9082a`.
- Development branch: `dev/portable`, created at main HEAD `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`; then moved by an expected-head guarded, non-force fast-forward commit.
- Dev snapshot commit / current result: `e022aee2dfcba6f13bba4d0f4ac57ba4a59154e6`.
- Dev snapshot tree: `47de9df8b5e8151d90db8f552bc6814024015d29`.
- Frozen v1.0 protocol Git blob: `1ac3689c1e811d1594291afee6b2c1c6efd093d0`; SHA-256 `586cb4d8740e33ac8a3a6db65a5ce1506fe855ca1968adacd3034352106c70e3`.
- Frozen v1.0 ZIP blob: `13eae102d5aed553d4fb3a023ab77b71601306b2`; SHA-256 `c3c5cb0c896d7e11696948e7677d74ea077a87d27350064b1ad6d521ceb74f6e`.
- Distribution checksum sidecar blob: `43d6943b5ac7a6df421f08e78bd993ce400164f1`.
- Legacy YU3DOH builder (archived as `bootstrap/legacy/build_package_yu3doh_v1.py`) blob: `83a580f9d2339e566ea2a2ceddfa98b39f9ef07f`.
- Historical distribution files: 11 originals `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/`; 11/11 source blob SHAs identical after transfer.
- Main branch remains at `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`; no changes. Control branch remains its own history, not merged with product.
- Root `README.md` Git blob `56fd6d6560434e067c126c152ab86298bd57d61f` preserved.

## Observed QA-like technical checks, not formal acceptance

- **PASS:** branch creation verified from exact current main.
- **PASS:** 14 original blob hashes (11 distribution source files, ZIP, checksum sidecar, builder) byte-identical to historical source.
- **PASS:** dev commit parent is prior main HEAD; guarded update used `expected_sha` and `force=false`; readback confirmed.
- **PASS:** `main` unchanged; product HEAD separate from control HEAD.
- **NOT EXECUTED:** independent QA of release, real adopter bootstrap, functional portability test, rebuilt ZIP in new repo, PR reviewer eligibility/integration method.
- **KNOWN LIMIT:** legacy builder invokes historical YU3DOH commit; snapshot notes label it **not a master builder**. The v1.0 package remains unchanged and no newly versioned successor was issued.

## Return and next route

- `PCM-P1-PREP-001` anticipated import to main; **superseded for destination only** by explicit Owner `PCM-BRANCH-STRATEGY-001`. Historical PREP remains intact; no retrospective statement of main import.
- **Next stage:** design vNext successor requirements and a new portable builder in `dev/portable` without changing frozen v1.0, determine version after compatibility analysis, create tests and QA path. This describes future work; no automatic product scope or release approval beyond actual authorization.
- **Gate for main:** Owner exact integration decision with valid QA and method/target before SHA; R-MAIN rules remain active and are not bypassed.

**Durable recoverability:** retrieve the fixed control revision containing this record, then resolve current `meta/project-control`, `dev/portable` and `main` refs independently. Names are locators; the full SHAs above are identities of this operation.
