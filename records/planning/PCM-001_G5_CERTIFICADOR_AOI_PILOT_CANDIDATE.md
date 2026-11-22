# PROJECT CONTROL MASTER — FUTURE ADOPTION PILOT CANDIDATE

**ID:** `PCM-G5-ADOPTER-AOI-CANDIDATE-001`  
**Status:** CANDIDATE ONLY / NOT AUTHORIZED / NO REPOSITORY WRITE  
**Owner-suggested project:** `KhaosMagnus/certificador-aoi` (official GitHub repo name; user may refer to it informally as 'certificador AUI')  
**Observed 2026-11-15:** PRIVATE; default branch `main` at `f23160204a4c0dd5cc79519a02eea803b062958e`; one observed branch `main`.

## Bounded observational intake

- `README.md` Git blob `df57bf05d3157b2cecb5e5e6c6c84dafc94120b2`: identifies local AOI inspector certification/training web app; reports frontend build and dotnet tests green. This is an author statement, **not independently reproduced QA**; deployment validation not established in this intake.
- `docs/AOI_V1_brief_bot_v1.2.0.md` Git blob `6a36930023615e748e9398d044cfda13dbff226d`: pre-existing product scope/acceptance requirements, not to reinterpret.
- `docs/AOI_V1_prompt_bot_v1.1.0.md` Git blob `4ad84c196d2763d9a229e274316bdd197b841eb3`: pre-existing implementation guidance.
- `docs/AOI_V1_github_protocol_v1.1.0.md` Git blob `1981db67cc25dda695d4c0d81f8613f1a90ce6ff`: **current local GitHub workflow** says private repo, development on `main`, no mandatory PR. Adoption of Project Control requires policy-conflict reconciliation by project Owner rather than silent substitution.
- GitHub rulesets GET returned `403` citing lack of support on Free for private-repo rulesets; do not infer any broader proof about protection or permissions from that alone.
- No canonical master release or master adoption version exists yet. Do not pretend this pilot can begin now.

## Pilot hypothesis and roles

Hypothesis: a Grok-based project coordinator can *adopt and operate* a pinned Project Control standard in an existing project with its own history and product contracts, preserving local authority and producing independently auditable evidence.

Grok may serve as **proposed adopter-side coordinator**, but does **not** automatically gain scope or writer privilege; if Grok also authors implementation, it cannot perform its own independent QA/acceptance/integration. PCM-001 is upstream supplier/evaluator of standard, **not** controller of AOI. The AOI Owner makes local adoption/integration decisions. Independent QA should be distinct from the actor that implemented adoption; a ChatGPT reviewer can assess if properly authorized and provided exact source evidence. A negative result is a legitimate portability finding, not a reason to erase reports.

## Conditions before any pilot write

1. Master `main` has a released, immutable candidate protocol/bootstrap with independent QA; master `meta/project-control` has an effective authorized PCM role after G4.
2. AOI Owner explicitly approves pilot scope, local control store/ref, Grok's exact role, authorized access, independent QA, integration method and recovery. No implicit 'Grok owns' assumption.
3. Freshly inspect AOI exact HEAD, pre-existing `AOI_V1_github_protocol_v1.1.0.md`, code and current work. Resolve conflict: previous direct-on-main/no-PR workflow versus proposed review/protection/branch governance. Do not silently rewrite frozen or current local contracts.
4. Since AOI repo is private under GitHub Free, do not claim that private-branch protection and mandatory reviews are enforced. Either use an Owner-approved compensating route, plan/policy change, or scope the pilot to documentary adoption without guarded product writes. Any public visibility change is a separate Owner decision and data exposure review.
5. Establish published input manifest and per-artifact SHA-256, exact source git refs, permitted paths and rollback plan. No shared personal credentials or broad write access for reviewers.
6. Run delegated adoption; independent GPT and (if distinct author role) Grok evaluations only within valid independence model. Report observation, deviations, failures and acceptance separately. No automatic promotion of AOI evidence to the master.

## Pilot deliverables after separate authorization

- `ADOPTION_PREFLIGHT`: existing authority conflict and repo SHA, role/permission plan, test cases and STOP.
- `ADOPTION_IMPLEMENTATION`: exact local governance artifacts and revision, separate from product code.
- `INDEPENDENT_QA`: test evidence, limitations and verdict on exact revision.
- `OWNER_ACCEPTANCE`: local project disposition.
- `UPSTREAM_FEEDBACK`: reusable lessons offered to PCM-001 as a proposal, never silently incorporated into master.

**STOP / NO G5 WRITES, NO AUTOMATIC ADOPTION OR ACTIVATION.**
