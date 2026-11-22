# PCM-GOV-AUTHREQ-DES-001-IQA-001 — Encargo QA2

**SOURCE:** PROJECT_CONTROL_MASTER / PCM-002 (provisional)
**TARGET:** INDEPENDENT_QA / Grok (separate chat/instance)
**DATE:** 2026-11-22
**ASSIGNMENT:** `PCM-GOV-AUTHREQ-DES-001-IQA-001` / QA2
**MODE:** STRICT READ-ONLY / DOCUMENTARY DESIGN QA / REPORT ONLY
**OWNER AUTHORITY:** `GRANTED` para preparar y remitir revisión por ChatGPT y Grok, no implementación/release/aceptación.
**COMMON PACKET:** `reviews/PCM-GOV-AUTHREQ-DES-001_IQA-001_COMMON_PACKET_2026-11-22.md`, en `meta/project-control` (usar commit de publicación fijado en el mensaje de transferencia).
**FROZEN REVIEW CANDIDATE:** `planning/PCM-GOV-AUTHREQ-DES-001_AUTHORIZATION_REQUEST_GATE_DESIGN_2026-11-22.md` en control commit `7067be93d2ebf0b5ac8622a1e12a797b62973545`, blob `332ab4813413cc2c317d33c4ed984cb82395dab4`.
**EXPECTED OUTPUT:** `PCM-GOV-AUTHREQ-DES-001_IQA-001_GROK_REPORT.md` (Markdown, hash SHA-256 si se calcula efectivamente).

## Instruction

Read the **full common packet** and all accessible primary sources at their pinned commits and blob identities. Perform an independent design review of AR-AC01–AR-AC14 and AR-T01–AR-T18, using their exact IDs and evidence. Classify any inaccessible source as an evidence limitation. Do not rely on the other reviewer’s report; do not treat the coordinator’s self-review as independent QA. Check recommendation/request/grant separation, materiality, direct Owner instruction, rollover, traceability, R3 compatibility, frozen v1.0 preservation and realistic enforcement boundaries.

Produce the structured independent QA report described in Section 6 of the common packet, including overall verdict, evidence matrix, design-only test coverage, defects, limits and return route.

**STOP:** no writes to GitHub, no execution of technical tests or code, no alteration of candidate files, no QA dispatch to other agents, no acceptance of the normative standard, no release, no permission changes. **Return the report to the Owner**, to be relayed to PCM-002. If source verification is not possible, report `INCONCLUSIVE` in affected checks.

**Independence note:** a distinct LLM session can supply an independent analytical viewpoint but not necessarily an independently controlled human identity.

**Transport:** this is a prepared handoff. Its existence in GitHub does not establish that INDEPENDENT_QA / Grok (separate chat/instance) has received it or completed QA.
