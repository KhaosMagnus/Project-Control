# PCM-GOV-PROV-CORR-001 — QA independiente focalizada del anexo R2

**ASSIGNMENT:** `PCM-GOV-PROV-CORR-001-IQA-001`  
**MODE:** STRICT READ-ONLY / DOCUMENTARY PROVENANCE QA  
**CANDIDATE:** `PCM-GOV-PROV-CORR-001_R2_ATOMIC_ADDITIVE_PROVENANCE_CANDIDATE_2026-11-21.md`  
**SHA-256:** `d68d6563c94e2141a76e5126ca1d513974b82df9bee3fd3358afde8d21256572`  
**STATUS:** PREPARED FOR OWNER DISPATCH; NO OWNER ACCEPTANCE OF CORR-001.

## Objetivo y fuentes

Inspecciona el candidato aditivo R2 frente al borrador R1, al contrato R3 aceptado documentalmente y a los documentos congelados G2-B, P5, P6 y P8 adjuntos. **No confundir un archivo que relata un mensaje del Owner con el mensaje original.** Las fuentes conversacionales originales no están exportadas en este ZIP, por lo que su grado para la QA es `SECONDARY_ATTRIBUTED`. La constancia de aceptación R3 es primaria del texto escrito por PCM-001 y secundaria de la emisión original del Owner.

## Matriz de evaluación C1–C9

| ID | Control requerido |
|---|---|
| C1 | Integridad ZIP/manifest y SHA exacto de R1, R2, R3 y fuentes; cualquier discrepancy es STOP |
| C2 | Los ocho registros R2 tienen IDs, actor, procedencia, source, `claims[]`, decision, effect, links y status coherentes con R3 §2 |
| C3 | `old_claim` no inventa una frase histórica no localizada y la rectificación tiene objeto acotado |
| C4 | Autoría GPT del handoff P5 y acto de revisión/ejecución Owner se representan por separado |
| C5 | La incompatibilidad EXEC §3 P5 vs P5 §2 se presenta como INFERRED_WITH_BASIS sin culpa o intenciones inventadas |
| C6 | Mensajes del Owner sin export primario quedan SECONDARY_ATTRIBUTED para este evaluador; evidencia local no se importa como primaria |
| C7 | Dos QA `INCONCLUSIVE`, STOP histórico, R3 local, UNI pendiente, G2-B no aceptado quedan intactos |
| C8 | `PROVENANCE_CORRECTION` es propuesta aditiva, sin superseding ni permiso de ejecución ni publicación |
| C9 | Referencias, SHAs, expresiones de autoría y eventos no generan contradicciones, ni una nueva falsa atribución de recomendación u orden |

## Salida

Entrega tabla C1–C9 (`VERIFIED / PARTIAL / FAILED / UNKNOWN`), hallazgos por severidad, rutas/hashes y verdict `DOCUMENTARY PASS (CONDITIONAL) / DOCUMENTARY REVISE / DOCUMENTARY FAIL / INCONCLUSIVE`. Describe los errores del propio R2 si los encuentras, incluso si provienen de PCM-001. Declara límites de acceso a los originales. No asumas aceptación del Owner ni reevalúes Q1–Q9 de infraestructura más allá de su consistencia documental.

**PROHIBIDO:** escrituras remotas, GitHub PR/forks/pushes, cambios de configuración, edición de registros congelados, publicación de política o aceptación de CORR-001, UNI, G2-B o G3/G4/G5.
