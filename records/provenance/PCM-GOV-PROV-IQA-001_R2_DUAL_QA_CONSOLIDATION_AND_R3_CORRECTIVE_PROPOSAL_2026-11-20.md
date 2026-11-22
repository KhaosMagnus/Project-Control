# PCM-001 — Conciliación de QA R2 y propuesta correctiva R3

**Assignment:** `PCM-GOV-PROV-IQA-001` / conciliación de diseño, 2026-11-20.  
**Authority:** Owner `GRANTED QA ONLY` sobre R2; no aceptación, publicación, adopción ni GitHub writes.  
**R2 frozen:** `PCM-GOV-PROV-DES-002_ATTRIBUTION_CONTRACT_R2_2026-11-20.md` SHA-256 `1391ca809bddaae1a2f6907ca1b9845dca616ee5a391bb7a1a8cef0a028b8375`.  
**R3 proposed draft:** `PCM-GOV-PROV-DES-003_ATTRIBUTION_CONTRACT_R3_CORRECTIVE_DRAFT_2026-11-20.md` SHA-256 `325bd44c8ab572cd7229219d7f08325e170c0e0797f9025c1abae4abb0a10cad`.

## 1. Recepción y diferencias

- **GPT QA:** `DESIGN REVISE`. Controles A4, A6, A7 y A9 PARTIAL. Dos defectos F1/F2. Fuente: `PCM-GOV-PROV-IQA-001_INFORME_QA_INDEPENDIENTE.md` SHA-256 `53df292462247b0f0f8e5fd986cea2f923ed9f6d04f1ffd384778a36616492df`.
- **Grok QA:** `DESIGN PASS (CONDITIONAL)`, A1–A12 VERIFIED. Fuente: `PCM-GOV-PROV-IQA-001_GROK_FOCUSED_PROVENANCE_QA_REPORT.md` SHA-256 `f2cb0cf1340b865002ace49e2c5c8ca7c6f488db62f2bc23b3350d40269c2042`.
- Coinciden en integridad de paquete y objetivo de separar recomendación, emisión, autorización y ejecución. Discrepan sobre completitud del esquema negativo y **aplicación** de las etiquetas probatorias al piloto.
- **Disposición PCM-001: `REVISE R2`**. La existencia de un `PASS (CONDITIONAL)` no anula defectos replicables de R2. R2 y sus QA quedan congelados; R3 es nuevo candidato aditivo.

## 2. Matriz de hallazgos

| Hallazgo | Evidencia primaria documental | Corrección propuesta R3 | Cierre esperado |
|---|---|---|---|
| F1 / A4 | R2 campo `decision.value` omitía rechazo; A4 exige aceptar, modificar y rechazar | Añade `REJECT` y `ACCEPT_MODIFIED`, efecto negativo explícito y ejemplo A/B′/C enlazado al mismo mensaje | Registrar rechazo sin transformarlo en ausencia de decisión, demora o revisión |
| F2 / A6, A7, A9 | R2 §3 usaba afirmaciones categóricas de actos Owner sin grado específico en cada fila, pese a regla R2 §1.2 | Introduce `claims[]` con evidencia individual y tabla histórica con grados por predicado y disponibilidad local/portátil | No convertir resúmenes en fuentes primarias; no degradar originales efectivamente visibles en el chat local |
| R0 | Redacción R2 daba por acreditado origen histórico absoluto | Separar mandato actual directamente emitido de primera formulación histórica `UNKNOWN` | Mantener autoridad Owner sin inventar origen temprano |

## 3. Lo que no cambia

- Que el **Owner** conserva decisiones reservadas, revisión humana y aceptación final.
- Que una recomendación GPT/Grok adoptada no se reclasifica como idea originada por Owner.
- Que P5→P6 conserva su no conformidad histórica; la dirección operativa incompatibile estuvo en el handoff PCM-001, sin imputar al Owner su formulación.
- Que R2 no fue aprobado ni se corrige retrospectivamente; R3 no altera G2-B, rulesets, SHAs, ramas, QA P8 `INCONCLUSIVE` ni UNI pendiente.
- Que G3/G4/G5, publicación y toda modificación en GitHub siguen prohibidas.

## 4. Fuente primaria local frente a portabilidad

Durante esta conversación PCM-001 ve mensajes originales del Owner (p. ej. su revisión P5, su orden directa de preservar la no conformidad, su concesión de QA R2). Los evaluadores de R2 **no recibieron necesariamente los originales**. Un reclamo puede ser `PRIMARY_OBSERVED` en esta conversación y `SECONDARY_ATTRIBUTED` dentro de otro paquete. La tabla de R3 señala esta diferencia; no presenta un resumen como si fuera un export original.

## 5. Gate recomendado

**No aceptar R2 ni aplicar R3**. Solicitar Owner `GRANTED QA ONLY` para un examen focalizado del **nuevo SHA R3**: F1/F2 y regresión A1–A12, con el mismo delta para dos evaluadores separados. Ninguna QA de R2 se convierte en QA de R3. Después conciliar y presentar al Owner `ACCEPT / REVISE / DEFER` del R3 exacto.

## 6. Atribución de esta corrección

Los hallazgos F1/F2 fueron emitidos por el revisor GPT independiente; Grok emitió otro juicio independiente. La conciliación y las propuestas correctivas de R3 proceden de **PCM-001/GPT**, NO son órdenes originadas ni aceptación emitida por el Owner. El Owner autorizó la revisión de R2; la eventual QA o aceptación de R3 requiere acto nuevo.
