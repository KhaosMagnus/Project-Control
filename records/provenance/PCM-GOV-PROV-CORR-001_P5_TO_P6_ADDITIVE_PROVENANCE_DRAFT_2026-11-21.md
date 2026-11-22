# PCM-001 — Anexo aditivo propuesto de corrección de procedencia P5→P6

**Record:** `PCM-GOV-PROV-CORR-001`  
**Tipo:** `PROVENANCE_CORRECTION`  
**Autor del borrador:** `PCM-001/GPT`  
**Status:** `DRAFT / NOT OWNER-ACCEPTED / NO PUBLICATION AUTHORITY`  
**Base prospectiva:** aceptación local documental `PCM-GOV-PROV-R3-ACCEPTANCE-001` emitida por Owner el 2026-11-21.  
**Prohibición:** no sustituye el contrato G2-B congelado, el handoff P5, los SHAs/commits, las decisiones del Owner ni las dos QA de infraestructura `INCONCLUSIVE`.

## A. Objeto y corrección precisa

**Clasificación imprecisa a corregir:** cualquier resumen que transmita que el Owner **originó**, **recomendó** u **ordenó inicialmente** el criterio de revisión humana adicional o la continuación P5→P6 omitiendo que el procedimiento y el handoff de avance fueron redactados y recomendados por PCM-001/GPT.

**Clasificación corregida propuesta:** distinguir (1) redacción/recomendación de un procedimiento por PCM-001, (2) emisión de autorizaciones y revisión personal por el Owner, (3) instrucciones operativas dadas por PCM-001, (4) ejecución manual reportada por el Owner, (5) hallazgo de incumplimiento del STOP y (6) disposición posterior del Owner de conservar la no conformidad. Estos actos **no son intercambiables**.

## B. Tabla de afirmaciones atómicas y grado probatorio

| ID | Afirmación y actor documentado | Soporte accesible | Grado de esta instancia | Condición para uso portable |
|---|---|---|---|---|
| CORR-01 | El documento ejecutivo de PCM-001 incluyó P5: configurar `R-MAIN`, acreditar revisor GitHub elegible y **STOP antes de P6** si la ruta no es demostrablemente viable | `01_PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_REQUEST_2026-11-16.md` §3, P5; SHA-256 `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349` | **PRIMARY_OBSERVED** del texto; primera autoría intelectual de cada cláusula `UNKNOWN` | El documento acredita la recomendación escrita de PCM-001, no la primera idea absoluta |
| CORR-02 | El mismo contrato incluyó puerta de dos QA `PASS` y aceptación posterior del Owner | Documento ejecutivo §5, mismo hash | **PRIMARY_OBSERVED** del texto; autorización histórica G2-B documentada en otros handoffs `SECONDARY_ATTRIBUTED` donde falte original | No reclasificar la iniciativa como exclusiva del Owner por haber aceptado el contrato |
| CORR-03 | PCM-001 emitió un handoff que preparó y recomendó avanzar P5→P6 con elegibilidad futura aún pendiente | `PCM-001_G2-B_P5_OWNER_REVIEW_AND_P6_CONTROLLED_HANDOFF_2026-11-20.md` §§2–5; SHA-256 `c7bef232beed9e43b13dbb675dfb929ef9510e49047fa30798f2d6dd8cb6acdb` | **PRIMARY_OBSERVED** de la instrucción de PCM-001; incompatibilidad con CORR-01 **INFERRED_WITH_BASIS** | No convertir el handoff en enmienda del contrato o en una orden original del Owner |
| CORR-04 | El Owner comunicó su revisión personal P5 de cinco controles | Mensaje original `OWNER REVIEW — PCM-G2B-P5` visible en el hilo PCM-001 | **PRIMARY_OBSERVED LOCAL** del mensaje del Owner | QA externa sin export fiel: **SECONDARY_ATTRIBUTED** |
| CORR-05 | El Owner informó un push de la raíz `meta/project-control`, mostrando salida de creación de rama; PCM-001 realizó readback | Mensaje del Owner con salida `HEAD -> meta/project-control`; readbacks P6 y P8 del expediente; commit raíz `cac838940e0e824a1f828ff660e422a6441a1da7` | **PRIMARY_OBSERVED LOCAL** del reporte; readback histórico referido; número total de intentos `UNKNOWN` | No inferir «único intento» solo a partir del estado final |
| CORR-06 | PCM-001 reconoció que permitió avanzar pese al STOP; la desviación P5→P6 quedó documentada | Comparación CORR-01 contra CORR-03 y conciliación `PCM-001_G2-B_P8_DUAL_INDEPENDENT_QA_CONSOLIDATION_2026-11-20.md`, SHA-256 `90b9ed72050022bbc3e8307e80de75019bbf5d370b4d28039c947c9891d63d08` | Documentos **PRIMARY_OBSERVED** de sus propios textos; conclusión de incoherencia **INFERRED_WITH_BASIS** | No deducir intención, culpa exclusiva ni conocimiento no registrado de ninguno de los actores |
| CORR-07 | Tras propuesta de GPT, el Owner emitió una directiva expresa para conservar la desviación como no conformidad histórica, sin convalidarla | Mensaje original `OWNER DECISION — PCM-G2B-P8-P5-DISPOSITION-001` visible localmente: «ordeno conservarla como no conformidad histórica»; antecedente propuesto por GPT | **PRIMARY_OBSERVED LOCAL** del acto de Owner; redacción previa GPT observable localmente | QA externa sin export primario: **SECONDARY_ATTRIBUTED** del acto Owner |
| CORR-08 | La política de atribución R3 adquirió eficacia documental local por aceptación posterior del Owner, sin modificar historia de G2-B | `PCM-GOV-PROV-R3-ACCEPTANCE-001` original en conversación actual; SHA R3 `325bd44c8ab572cd7229219d7f08325e170c0e0797f9025c1abae4abb0a10cad` | **PRIMARY_OBSERVED LOCAL** del acto Owner para PCM-001 | El anexo no acredita publicación, eficacia general ni export original portable |

## C. Eventos y responsabilidades diferenciadas

- `AGENT_RECOMMENDATION` / `AGENT_DRAFT`: PCM-001 preparó el procedimiento ejecutivo y la guía operativa; sus textos congelados constituyen evidencia primaria de lo que escribió. Para la idea originaria anterior a cualquier fuente inspeccionada: `idea_originator=UNKNOWN` cuando corresponda.
- `OWNER_EXECUTION_GRANT`: la concesión G2-B reportada es un acto del Owner, con alcance del documento aceptado; si el mensaje original no está en el expediente externo, `SECONDARY_ATTRIBUTED` en ese entorno. La autorización no convierte al Owner en redactor ni recomendador de cada condición técnica.
- `OWNER_ISSUED_REVIEW`: el Owner hizo la revisión personal comunicada en el hilo; no constituye aprobación de un PR existente ni independencia de personas.
- `OPERATIONAL_DIRECTION_BY_AGENT`: PCM-001 recomendó el paso P6 a pesar de no tener acreditada la viabilidad requerida en P5. Este es el hallazgo de coordinación, basado en comparación contractual.
- `OWNER_OPERATOR_ACTION`: el Owner reportó el push P6; no hay en este borrador prueba exhaustiva del número de intentos y no se inventa.
- `HISTORICAL_NONCONFORMITY`: se conserva la desviación y la QA original; la aceptación de política R3 no la cura.
- `OWNER_DIRECT_DISPOSITION_OF_AGENT_TOPIC`: el Owner ordenó preservar la no conformidad tras recibir una propuesta de GPT; la decisión es suya, pero la propuesta antecedente sigue atribuida a GPT.

## D. Rectificación aditiva propuesta y disposición pendiente

- `old_claim`: resúmenes que fusionen «recomendación operativa de PCM-001» con «orden originaria del Owner».
- `corrected_claim`: PCM-001 redactó/recomendó la guía P5→P6; Owner conservó autoridad y realizó actos de revisión/operación reportados; el defecto del handoff se atribuye al análisis/conducción de PCM-001 y la disposición final de preservar la no conformidad al Owner.
- `reason`: corrección de procedencia y graduación por afirmación, conforme a R3 aceptado localmente.
- `evidence_refs`: CORR-01…08, archivos/SHAs y localizadores anteriores.
- `author_of_correction`: `PCM-001/GPT`.
- `owner_disposition`: `PENDING` — el anexo **no** está aceptado.
- `effective_from`: `NOT_EFFECTIVE_PENDING_OWNER_REVIEW`.
- `supersedes`: `NONE` — añade contexto a registros históricos sin sobrescribirlos.

## E. Decisión futura que sí se necesitaría

El Owner podrá **aceptar, pedir revisión o diferir** este anexo documental exacto una vez inspeccionado. La sola preparación no lo aplica ni publica. No es requisito repetir la génesis, crear PR o modificar GitHub para valorar la corrección de atribución.

**Estado:** `ADDITIVE PROVENANCE DRAFT / R3 LOCAL POLICY ACTIVE / OWNER REVIEW PENDING / G2-B NOT ACCEPTED / UNI AMENDMENT NOT ACCEPTED / NO GITHUB WRITES`.
