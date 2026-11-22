# PROJECT CONTROL MASTER — Propuesta de contrato de procedencia de recomendaciones, decisiones y responsabilidad

**ID propuesto:** `PCM-GOV-DES-PROVENANCE-001`  
**Autor del borrador:** `PROJECT_CONTROL_MASTER / PCM-001` (LLM, provisional)  
**Disparador:** Observación directa del Owner del 20 de noviembre de 2026 sobre la confusión entre propuesta de agente, aceptación de recomendación y orden originada por el Owner.  
**Estado:** `DRAFT / DESIGN ONLY / NOT APPROVED / NOT PUBLISHED`  
**Alcance:** Gobierno documental local de PCM-001. **No modifica automáticamente** el protocolo genérico, adopciones, ramas ni otros proyectos.  
**Autorización de trabajo en esta conversación:** el Owner solicitó analizar y avanzar con una propuesta de solución. **No equivale** a ratificación contractual de este borrador ni a autorización de escritura GitHub.  
**Sin acciones remotas:** No crear ni modificar repositorios, ramas, reglas, PR, permisos, credenciales, integraciones o releases.

## 1. Hallazgo y corrección conceptual

Un registro `OWNER GRANTED` **no demuestra** que el Owner haya originado el criterio técnico autorizado. Significa que emitió una decisión con autoridad. La génesis intelectual de la recomendación debe conservarse por separado.

Una recomendación de GPT/Grok aceptada por el Owner es **ambas cosas a la vez**: (a) una propuesta atribuible al agente que la formuló y (b) una decisión vinculante, dentro del alcance exacto autorizado, tomada por el Owner. No debe reclasificarse automáticamente como `OWNER-ORIGINATED DIRECTIVE`.

De forma equivalente, una frase del Owner que ratifica, adopta o reproduce un texto previamente redactado por el asistente conserva la autoridad de su emisión, **sin borrar la procedencia del texto ni la autoría de la recomendación**. Si el Owner introduce una regla nueva por iniciativa propia, registrar esa iniciativa de manera explícita. Si una misma intervención mezcla ambas cosas, **dividirla en unidades de decisión atómicas**.

### 1.1 Cinco ejes obligatorios (no sustituibles entre sí)

| Eje | Pregunta a contestar | Ejemplos de valor |
|---|---|---|
| `originated_by` | ¿Quién introdujo la idea, requisito o curso de acción? | `OWNER`, `PCM-001/GPT`, `GROK`, `EXTERNAL_SOURCE`, `UNKNOWN` |
| `proposed_by` / `drafted_by` | ¿Quién recomendó la alternativa y redactó su texto? | Modelo/rol/instancia concretos; pueden diferir entre sí |
| `authorized_by` / `decision_type` | ¿Quién otorgó autoridad, con qué tipo de acto y alcance? | `OWNER / ACCEPT_RECOMMENDATION`, `OWNER / DIRECT_ORDER`, `OWNER / GRANTED_EXECUTION`, `NONE` |
| `executed_by` / `verified_by` | ¿Quién actuó y quién observó o probó el resultado? | Owner operador, GitHub API, QA ChatGPT/Grok, etc. |
| `deviation_origin` / `remediation_owner` | ¿Quién introdujo el error de recomendación/conducción y quién debe disponerlo? | `PCM-001` para error de dirección; Owner conserva resolución formal, sin implicar autoría del defecto |

**Regla:** `authorized_by=OWNER` **no implica** `originated_by=OWNER` y `executed_by=OWNER` **no implica** `proposed_by=OWNER`. Los ejes pueden compartir actores sin colapsarse.

### 1.2 Tipos de actos

- `AGENT_PROPOSAL`: sugerencia del LLM, sin autoridad ejecutiva por sí misma.
- `OWNER_ADOPTION_OF_AGENT_PROPOSAL`: el Owner acepta total o parcialmente una propuesta previa, que se referencia por identidad/version/SHA.
- `OWNER_DIRECT_INITIATIVE`: instrucción iniciada por el Owner sin una propuesta identificada antecedente. **No inferir esta clase** solo porque el texto fue escrito o pegado por el Owner.
- `OWNER_DIRECT_DISPOSITION_OF_PRIOR_PROPOSAL`: el Owner usa un mandato expreso para disponer una materia planteada por un agente. La decisión expresa es suya, pero el antecedente y la propuesta no dejan de pertenecer al agente.
- `OWNER_AUTHORIZATION_TO_EXECUTE`: permiso separado, limitado a operación, actor y condiciones, que no equivale a recomendación autónoma del Owner.
- `LLM_OPERATIONAL_DIRECTION`: instrucción técnica operativa proporcionada por el asistente durante una ejecución ya autorizada, aun si reproduce la voz del Owner.
- `QA_FINDING`: diagnóstico de un evaluador; no es una autorización ni orden del Owner.

**Regla de ambigüedad:** `ADELANTE`, `ACEPTO`, `GRANTED` o un bloque de texto copiado pueden ser decisiones efectivas, pero su texto **no prueba por sí solo** la iniciativa intelectual. Cuando falte referencia a la propuesta, registrar `ORIGIN UNVERIFIED`; no inventar un origen. La autoridad del Owner sigue siendo efectiva en lo inequívocamente aceptado.

## 2. Registro de evidencia mínimo por decisión

Cada unidad `decision_id` o `recommendation_id` deberá conservar:

```yaml
record_id: PCM-PROV-<serial>
claim_or_control: <criterio específico; no paquete heterogéneo>
source_kind: AGENT_PROPOSAL | OWNER_MESSAGE | QA_REPORT | GITHUB_OBSERVATION
source_actor: <modelo, rol, cuenta o persona; no confundir cuenta/persona>
source_reference: <mensaje original con fecha/enlace o archivo con SHA-256>
verbatim_excerpt: <cita exacta breve o vacío si no disponible>
originated_by: OWNER | PCM-001/GPT | GROK | UNKNOWN
proposed_by: <actor | NONE | UNKNOWN>
drafted_by: <actor | UNKNOWN>
owner_decision: ACCEPT | REVISE | DEFER | GRANTED | DIRECT_ORDER | NONE
owner_decision_scope: <objeto, límites y condiciones>
owner_decision_source: <referencia literal del mensaje del Owner; no texto solo sugerido>
operator: <actor | NOT_APPLICABLE>
observed_effect: <resultado, evidencia, SHA o NOT_TESTED>
qa_disposition: <resultado + ref, cuando exista>
error_attribution: <diagnóstico y fuente; no inferir culpa del acto de aceptar>
status: PROPOSED | AUTHORIZED | EXECUTED | VERIFIED | DEVIATION | SUPERSEDED
confidence: OBSERVED_PRIMARY | DOCUMENTARY_ATTRIBUTED | UNVERIFIED
supersedes: <registro anterior solo si existe aceptación expresa, nunca sobrescritura>
```

**Prueba primaria:** mensajes originales con actor y fecha, documentos originales con hashes y respuestas GitHub verificables. **Prueba secundaria:** narrativa de handoff o resumen de otro agente. Si el texto original no está disponible, no se convierte un resumen en cita literal. Una propuesta de bloque de mensaje escrita por GPT **no es una decisión del Owner** hasta que este la emita o acepte explícitamente. Si un Owner la reproduce posteriormente, registrar la **doble procedencia**: redacción/propuesta GPT; decisión Owner.

## 3. Auditoría histórica P5→P6: clasificación CORRECTIVA PROPUESTA

Esta matriz es una **reconciliación documental propuesta**; no reescribe ni convalida los contratos o QA históricos. Las etiquetas `OBSERVADO` / `ATRIBUIDO` distinguen evidencia primaria de narrativa derivada.

| Hecho/acto | Origen de recomendación o texto | Autoridad/acción del Owner | Clasificación correcta |
|---|---|---|---|
| G2-B P5 exige `1 eligible independent GitHub review`; si no viable, STOP antes de P6 | Contrato `G2-B_EXECUTIVE_REQUEST.md`, `Prepared by PCM-001 PROVISIONAL` | G2-B posteriormente `GRANTED` por Owner, según mensaje de autorización en la conversación | **RECOMMENDATION PCM-001 → OWNER-AUTHORIZED CONTRACT**. La regla aprobada fue vinculante aunque no se originara en Owner |
| Comprobación P5 y preparación de push P6 | Handoff `P5_OWNER_REVIEW_AND_P6_HANDOFF.md` redactado por PCM-001 | Owner inspeccionó cinco controles, ejecutó manualmente el push, envió readback | **LLM OPERATIONAL DIRECTION → OWNER REVIEW / OWNER EXECUTION**; no `OWNER-ORIGINATED ORDER TO IGNORE STOP` |
| Desviación P5→P6 | Falta de satisfacción del STOP en la recomendación operativa de PCM-001; detectada después por QA P8 | El Owner operó bajo la ruta recomendada; no hay evidencia de una orden independiente del Owner para saltar explícitamente el STOP | **LLM COORDINATION ERROR / CONTRACT NONCONFORMITY**. Preservar aceptación y ejecución del Owner, sin atribuirle la formulación del error |
| Conservar P5→P6 como no conformidad histórica | Recomendación de PCM-001 en conciliación y solicitud de decisión | El Owner declaró expresamente `ordeno conservarla como no conformidad histórica, sin convalidación retroactiva` | **AGENT-PROPOSED DISPOSITION + OWNER DIRECT EXPRESS DISPOSITION**. La orden es real, pero la propuesta anterior es del agente |
| Exigir dos QA `PASS` para aceptación integral G2-B | Criterio escrito en el contrato ejecutivo preparado por `PCM-001 PROVISIONAL` | Integrado en el alcance G2-B que el Owner autorizó | **LLM-PROPOSED ACCEPTANCE GATE → OWNER-AUTHORIZED CONTRACT**; su modificación exige nueva decisión, no es una exigencia intelectualmente originada por el Owner solo por haberla aprobado |
| Adoptar `OPTION B` para diseño unipersonal | Alternativa recomendada por PCM-001 | `OWNER DECISION — PCM-G2B-P8-P5-DISPOSITION-001`: `GRANTED DESIGN ONLY — OPTION B` | **GPT-RECOMMENDED → OWNER-AUTHORIZED DESIGN**; no propuesta original inventada del Owner |
| Reserva de aceptación final, revisión humana y decisiones reservadas al Owner | Instrucción reiterada por el Owner | El Owner establece directamente el alcance de su autoridad | **OWNER-ORIGINATED DIRECTIVE / RESERVED AUTHORITY**. No es una decisión ideada por GPT |
| `PCM-G2B-P8-UNI-DES-001`, SHA-256 `410c12a8f2f46ac20322a6ec76d76e038c9b7979a565044d6db8ee5cec29ca76` | Redacción de PCM-001 derivada de `OPTION B` | Hasta el último intercambio revisado, el Owner **no ha emitido el ACCEPT documental propuesto**; ambos QA focalizados fueron `DESIGN PASS (CONDITIONAL)` | **AGENT DRAFT / QA PASS CONDITIONAL / OWNER ACCEPT PENDING**. No tratar una propuesta de mensaje como autorización consumada |

Fuentes concretas:
- Solicitud ejecutiva G2-B, SHA-256 `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349`, preparada por `PCM-001 PROVISIONAL`.
- Handoff P5→P6 (`04_CONTEXT/P5_OWNER_REVIEW_AND_P6_HANDOFF.md`), incluido en el paquete P8 SHA-256 `2c4b4a0b7835386e7ec5e25cfd635bc0ae43a8ca3d49d511ba0e85af3496c499`.
- QA de infraestructura P8: ChatGPT `INCONCLUSIVE`, Grok `INCONCLUSIVE` y elegibilidad Q6 `FAILED` en Grok.
- Doble QA documental unipersonal U1–U8: ChatGPT y Grok `DESIGN PASS (CONDITIONAL)`; no conceden aceptación del Owner.
- Mensajes del Owner sobre `OPTION B`, conservación de la desviación, revisión/aceptación humana y su observación actual sobre procedencia de propuestas, todos del 20 de noviembre de 2026.

**Límite de fuentes:** la matriz se apoya en los archivos inspeccionados y los mensajes visibles de esta conversación. La autoría intelectual anterior al primer documento (`PCM-001` frente a otras ideas previas) no debe suponerse exhaustiva sin contrastar la cadena fuente original. No atribuir a Grok recomendaciones que solo aparecen en una consolidación redactada por PCM-001, ni viceversa.

## 4. Reglas de integridad, reparación y precedencia

1. **No editar la historia**: mantener inalterados mensajes, contratos, registros congelados y los dos QA P8, aun cuando contengan atribuciones imprecisas.
2. **Corrección aditiva**: para cada atribución errónea crear `PROVENANCE_CORRECTION`, con `old_claim`, `source_ref`, `corrected_claim`, `evidence`, `confidence`, `owner_disposition` y `effective_date`.
3. **Dos hechos simultáneos**: que el Owner haya aceptado una mala recomendación no exime de registrar el acto de autorización, y no exonera al agente que la formuló del error de análisis o conducción.
4. **Las recomendaciones no autorizan**: GPT/Grok no pueden usar su propio dictamen para modificar normas, reglas o activar acciones; los límites de su autoridad permanecen intactos.
5. **La aceptación no reescribe procedencia**: un `ACCEPT` del Owner sobre el texto exacto convierte la propuesta en política aceptada desde el ámbito y fecha definidos, **no** cambia `originated_by` ni cura desviaciones previas.
6. **Correcciones significativas requieren QA**: someter este contrato y la matriz histórica a dos revisiones documentales focalizadas, especialmente a prueba de atribución errónea por redacción de bloques a nombre del Owner.
7. **No propagación automática**: esta política local es una propuesta para PCM; una eventual incorporación al estándar portátil y adopción por otros proyectos requieren decisiones y versiones separadas.

## 5. Controles de QA propuestos (A1–A8)

| Control | Validación documental esperada |
|---|---|
| A1 | La recomendación, la decisión y la ejecución se modelan con sujetos/cuentas y fuentes distintas |
| A2 | El texto preparado por GPT y posteriormente aceptado por Owner conserva doble procedencia |
| A3 | Las instrucciones originadas por el Owner no se degradan automáticamente a recomendaciones de LLM |
| A4 | P5→P6 identifica correctamente al autor del requisito, al autor del handoff y al operador, sin atribuir al Owner la propuesta de saltar STOP |
| A5 | La orden expresa del Owner de conservar la no conformidad permanece registrada, junto con el antecedente de propuesta LLM |
| A6 | La enmienda unipersonal `PCM-G2B-P8-UNI-DES-001` no se presenta falsamente como aceptada antes de su decisión efectiva |
| A7 | Registros congelados y QA históricos no se sobrescriben; solo enlaces aditivos / superseding expreso |
| A8 | No se habilitan escrituras ni se transfiere esta política automáticamente a G3/G4/G5 u otros adoptantes |

## 6. Siguiente secuencia recomendada — NO EJECUTABLE

**Paso D1:** Owner revisa esta propuesta e indica `REVISE / ACCEPT FOR QA / DEFER` solo para el diseño de procedencia. No se le solicita que ratifique retrospectivamente interpretaciones erróneas.

**Paso D2:** Si el Owner aprueba someterla a QA, congelar versión y SHA-256 del candidato y un paquete de fuentes, y enviar a GPT y Grok por separado para A1–A8. Los revisores deben citar evidencia primaria y distinguir expresamente decisión autoritativa de origen de recomendación.

**Paso D3:** Conciliar QA y solicitar aceptación documental **específica** del Owner con alcance, versión, precedencia y fecha.

**Paso D4:** Preparar anexo aditivo de corrección de procedencia de G2-B (sin publicar todavía) y aplicar esta norma de atribución a decisiones futuras solamente desde su entrada en vigor.

**Paso D5:** Retomar el cierre de Q5/Q7/Q8/Q9 y las condiciones de aceptación de G2-B **sin alterar por ello** los resultados históricos de QA P8 ni considerar automáticamente aceptada la enmienda unipersonal. Cualquier corrección de la política de dos QA PASS requiere decisión explícita y separada del Owner.

## 7. Decisiones y dudas pendientes

**No faltan datos para diseñar** esta política. Antes de hacerla vinculante, el Owner debe decidir específicamente su adopción. Queda una verificación documental focalizada: localizar el mensaje original exacto del primer `GRANTED` G2-B y, si existe, el texto anterior a la recomendación P5, para distinguir con máxima precisión el origen inicial de cada cláusula. Si el origen no puede acreditarse, anotar `UNKNOWN`, no inferir `OWNER`.

**Ninguna escritura GitHub ni aceptación G2-B o unipersonal se deduce de este borrador.**
