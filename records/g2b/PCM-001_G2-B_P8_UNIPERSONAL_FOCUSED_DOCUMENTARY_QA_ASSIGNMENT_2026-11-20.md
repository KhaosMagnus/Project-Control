# PROJECT CONTROL MASTER — Asignación de QA focalizada del modelo unipersonal

**Assignment:** `PCM-G2B-P8-UNI-IQA-001`  
**Mode:** `STRICT READ-ONLY / INDEPENDENT DOCUMENTARY QA / NO EXECUTABLE AUTHORITY`  
**Owner decision enabling design:** `PCM-G2B-P8-P5-DISPOSITION-001 — GRANTED DESIGN ONLY — OPTION B`  
**Candidate:** `PCM-001_G2-B_P8_UNIPERSONAL_AUTHORITY_AND_REVIEW_AMENDMENT_DRAFT_2026-11-20.md`  
**Input:** el **mismo ZIP** con manifiesto y fuentes congeladas entregado individualmente a ChatGPT y Grok. No reutilizar el informe del otro como respuesta propia.

## Alcance exacto

Revisar el **delta de autoridad y procedimiento**, no repetir QA general de las dos raíces Git:

| Criterio | Comprobación requerida | Resultado |
|---|---|---|
| U1 | La aceptación final y la revisión humana decisoria siguen reservadas al Owner, sin imposición implícita de segunda persona. Diferenciar aceptación Owner y `Approve` GitHub | VERIFIED/PARTIAL/FAILED/UNKNOWN |
| U2 | Dos cuentas GitHub del mismo Owner **no** constituyen separación entre personas. Autor del PR y aprobador deben ser cuentas técnicamente elegibles y diferentes; no afirmar ruta live-test no hecha | mismo |
| U3 | QA GPT/Grok verdaderamente separado como revisión documental; no sustituto de aprobación GitHub ni de la persona Owner | mismo |
| U4 | Secuencia para futuras PR conserva linaje, `B/H/D/T_expected`, método squash/rebase, readback, STOP por discrepancias y decisiones separadas de preparar/integrar/aceptar | mismo |
| U5 | Identifica limitaciones actuales de `R-MAIN/R-META`: una aprobación; `require_extra_approval_for_unattributed_changes=true`; autoría por Copilot no cubierta; elegibilidad y fork **NOT TESTED** | mismo |
| U6 | P5→P6 continúa no conforme a contrato histórico; no hay convalidación retroactiva ni reclasificación silenciosa de QA1/QA2 P8 | mismo |
| U7 | Precedencia prospectiva precisa; conserva contrato, README, SHAs, reglas, QA histórico, G2-B no aceptado y G3/G4/G5 diferidos | mismo |
| U8 | Distingue qué requiere nueva decisión Owner y qué falta para aceptación G2-B (Q5/Q7/Q8/Q9 y regla histórica de dos `PASS`) | mismo |

## Límites

- Solo lecturas de ZIP y documentación oficial de GitHub; comprobaciones GitHub GET si están disponibles. Prohibida toda escritura, PR, review, fork, rama, commit, instalación, permiso, ruleset, test destructivo o fusión.
- Identificar evidencia **OBSERVED / SOURCE CONTRACT / INFERENCE / PROPOSED**, con fecha y SHA del candidato. No tratar `JormungandrMagnus` como persona independiente.
- La comprobación del primer PR y de la elegibilidad efectiva se reserva a otro gate; no hacerla ahora.
- No aceptar ni activar la enmienda; QA devuelve recomendaciones al Owner. Si un criterio no es acreditable, declarar `UNKNOWN` o `INCONCLUSIVE`.
- Clasificación global: `DESIGN PASS (CONDITIONAL) / DESIGN REVISE / DESIGN FAIL / INCONCLUSIVE` y U1–U8 individuales.
- Registrar SHA-256 del ZIP recibido, digest del candidato, integridad de miembros, citas puntuales a cláusulas y límites de herramientas; atestación explícita de solo lectura.

**Producto:** informe autocontenido para el Owner, con veredicto, matriz U1–U8, defectos materiales, riesgos residuales y disposición. El Owner lo transferirá a PCM-001. Sin publicación GitHub.
