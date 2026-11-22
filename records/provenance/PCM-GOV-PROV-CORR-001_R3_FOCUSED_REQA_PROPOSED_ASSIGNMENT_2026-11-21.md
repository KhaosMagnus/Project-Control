# PCM-001 — CORR-001 R3 / Re-QA focalizada propuesta

**ASSIGNMENT:** `PCM-GOV-PROV-CORR-001-IQA-002`
**MODE:** STRICT READ-ONLY / DOCUMENTARY DELTA QA / PROPOSED — NO OWNER QA GRANT YET
**CANDIDATE:** `PCM-GOV-PROV-CORR-001_R3_ATOMIC_PROVENANCE_CORRECTIVE_CANDIDATE_2026-11-21.md`
**SHA-256:** `f4317eaae4047086d32e00247e5e6f36e01c7e2d6a5c0b87f086eab524291d09`

El Owner todavía no ha aceptado R3 ni autorizado esta nueva revisión. La autorización anterior no debe extenderse automáticamente al candidato cambiado.

## Contrato de evaluación

- **H1:** CORR-05 separa `READBACK_DOCUMENT_TEXT` (primario para archivo) de CORR-05B `OWNER_PUSH_REPORTED` (secundario); eventos/actores correctos; número total de intentos UNKNOWN.
- **H2:** CORR-08 `links.adopts` enlaza candidato R3 exacto y `decision.scope` refleja aceptación prospectiva LOCAL; CORR-04/07 registran alcances diferentes; enlaces EXEC, P5 y R3 tienen destinos verificables por sección/SHA.
- **H3:** CORR-04 no afirma redacción GPT sin fuente primaria portable; verifica `drafter=UNKNOWN`, preservando propuesta previa GPT y acto Owner separado.
- **Regresión:** control C1–C9, preservación del STOP histórico P5→P6 y de los dos P8 `INCONCLUSIVE`, sin nueva imputación al Owner ni autorización de GitHub.

Recalcular hashes, reproducir diff R2→R3, leer ambos informes R2 y emitir `DOCUMENTARY PASS (CONDITIONAL)`, `DOCUMENTARY REVISE`, `DOCUMENTARY FAIL` o `INCONCLUSIVE`. Prohibidas escrituras GitHub, publicación, PR, permisos o aceptación normativa.
