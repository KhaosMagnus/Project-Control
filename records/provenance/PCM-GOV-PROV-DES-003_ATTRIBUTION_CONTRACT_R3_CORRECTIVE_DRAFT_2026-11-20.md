# PROJECT CONTROL MASTER — Contrato de atribución y procedencia de recomendaciones, decisiones y ejecución

**Candidate:** `PCM-GOV-PROV-DES-003 / R3`  
**Authored by:** `PCM-001` (assistant LLM; provisional coordinator)  
**Trigger:** Observación directa del Owner, 2026-11-20, sobre procedencia de recomendaciones frente a actos de autorización.  
**Sources:** `PCM-GOV-DES-PROVENANCE-001` primer borrador, SHA-256 `77ad35f25c2be2dbb265f2a38ad6dac465e11960f8fb5f1f80cca18f02a6f8fd`; candidato R2 congelado, SHA-256 `1391ca809bddaae1a2f6907ca1b9845dca616ee5a391bb7a1a8cef0a028b8375`; QA R2 GPT `DESIGN REVISE` y QA R2 Grok `DESIGN PASS (CONDITIONAL)`.  
**Authorization for this work:** mensaje del Owner «prepares la mejora, el cambio, el ajuste y me des más o menos el plan … adelante», 2026-11-20, interpretado **exclusivamente como encargo de preparación documental**.  
**Status:** `CORRECTIVE DESIGN DRAFT / NOT AUTHORIZED FOR R3 QA / NOT APPROVED / NOT EFFECTIVE / NO EXECUTABLE AUTHORITY`.
**Disposition of R2:** preserved as frozen historic candidate; neither its QA results nor its original bytes are changed.  
**Scope:** gobernanza documental **local y prospectiva** de PCM-001; sin aplicación al protocolo genérico `main`, a proyectos adoptantes ni a la infraestructura G2-B sin actos posteriores expresos.

## 0. Problema que se corrige y criterio de éxito

**Defecto:** los registros pueden indicar correctamente `Owner GRANTED` y, a la vez, atribuir **incorrectamente al Owner la iniciativa intelectual** de una política formulada por GPT, Grok u otro actor. También pueden ocultar quién recomendó la ruta técnica que produjo una desviación. La autoridad del Owner es real y vinculante en su alcance, pero **aceptar una recomendación no implica haberla originado**.

**Éxito documental:** para toda decisión material, un auditor puede seguir `fuente primaria → idea/recomendación → texto propuesto → mensaje de decisión → autorización de ejecución → actuación → readback/QA → disposición`, separando actores, credenciales, fechas y niveles de evidencia. Las lagunas quedan explícitas como `UNKNOWN`, nunca se llenan por inferencia disfrazada de hecho.

**Regla R0 (de prioridad máxima):** el Owner realiza la revisión humana y conserva exclusivamente la aceptación final y decisiones reservadas. Existen intervenciones **directas** del Owner visibles en la conversación de PCM-001 que reiteran ese mandato. **La autoría de su primera formulación histórica** debe calificarse con la fuente específica: `PRIMARY_OBSERVED` para una intervención original efectivamente accesible al revisor, `SECONDARY_ATTRIBUTED` si solo se dispone del relato de PCM-001, o `UNKNOWN` cuando ninguna evidencia sostiene quién lo originó por primera vez. No transferir a GPT la autoría de los mandatos emitidos efectivamente por el Owner; tampoco confundir una directiva de autoridad con una propuesta técnica de PCM-001.

## 1. Modelo de hechos separados, no de una sola etiqueta

Una intervención puede generar varios registros atómicos. Son dimensiones distintas:

| Campo | Pregunta / qué prueba | Estado ante ausencia de evidencia |
|---|---|---|
| `idea_originator` | Quién introdujo primero la idea **dentro de las fuentes acreditadas**; no se confunde con quien luego la repitió | `UNKNOWN`, nunca inferir por el actor que autoriza |
| `recommender` | Quién recomendó la medida concreta | `UNKNOWN` si no hay propuesta identificada |
| `drafter` | Quién redactó el texto utilizado (p. ej. un WritingBlock GPT) | `UNKNOWN`, incluso si luego se copia como mensaje del Owner |
| `issuer` | Quién **emitió** un mensaje de decisión o instrucción | `OWNER` cuando el mensaje procede del Owner; no prueba la autoría intelectual |
| `decision_maker` | Quién seleccionó o aceptó una opción, qué alcance y condiciones | `NONE` hasta una decisión real; siempre Owner para las materias reservadas |
| `execution_authorizer` | Quién autorizó la operación específica y bajo qué límites | No inferir de un `ACCEPT` de diseño |
| `operator` | Quién ejecutó actos técnicos o manuales | `NOT_APPLICABLE` / `UNKNOWN` según corresponda |
| `verifier` / `qa_author` | Quién observó y quién evaluó | No equiparar a quien aceptó, ni QA LLM con segunda persona física |
| `error_source` / `disposition_authority` | Procedencia acreditada de fallo de análisis/conducción y quién lo dispone | No sustituir causalidad por culpa; autoridad de corrección reservada al Owner |

**Reglas R1–R5:**

- **R1:** `decision_maker=OWNER` no implica `idea_originator=OWNER`. `operator=OWNER` no implica `recommender=OWNER`.
- **R2:** Un bloque escrito por GPT, después pegado o aceptado por el Owner, se registra como `drafter=GPT`; `issuer=OWNER` en la decisión efectiva, con `decision_link` al texto exacto. Si no se demuestra quién formuló originalmente una cláusula previa, su origen intelectual es `UNKNOWN` aunque el documento tenga firma de coordinación.
- **R3:** La adopción parcial se descompone en cláusulas; aceptación, modificación y rechazo son resultados autónomos. Exclusiones, condiciones o modificaciones introducidas por el Owner se atribuyen a él **en esas cláusulas**, no en toda la propuesta. Un rechazo explícito nunca se codifica como `NONE`, `DEFER` o `REVISE`.
- **R4:** Expresiones como «adelante», «sí», «acepto» y «GRANTED» se interpretan por contexto y objeto inequívoco; cuando el alcance material sea ambiguo, solo se registra la decisión comprobable y se solicita precisión antes de una ejecución nueva.
- **R5:** Los textos ofrecidos por GPT bajo el rótulo `OWNER DECISION` son **propuestas no emitidas** hasta que el Owner las adopte explícitamente. Mostrar un WritingBlock no genera autorización.

### 1.1 Tipos de eventos válidos

`OWNER_ORIGINATED_DIRECTIVE`, `AGENT_RECOMMENDATION`, `AGENT_DRAFT`, `OWNER_ADOPTION_OF_RECOMMENDATION`, `OWNER_REJECTION_OF_RECOMMENDATION`, `OWNER_DIRECT_DISPOSITION_OF_AGENT_TOPIC`, `OWNER_EXECUTION_GRANT`, `OPERATIONAL_DIRECTION_BY_AGENT`, `OWNER_OPERATOR_ACTION`, `READBACK_OBSERVATION`, `INDEPENDENT_DOCUMENTARY_QA`, `ERROR_FINDING`, `HISTORICAL_NONCONFORMITY`, `OWNER_FINAL_ACCEPTANCE`, `PROVENANCE_CORRECTION`.

`OWNER_ORIGINATED_DIRECTIVE` exige una intervención iniciada por el Owner y evidencia de que el criterio no es simplemente la adopción de una propuesta identificada; si esta última existe, usar ambos registros ligados. Una disposición del Owner **puede ser directa y vinculante** aunque trate una idea sugerida previamente por GPT: `OWNER_DIRECT_DISPOSITION_OF_AGENT_TOPIC` conserva ambos hechos.

### 1.2 Identidades y fiabilidad

Para personas y cuentas se almacenan claves distintas: `human_actor`, `service_account`/`github_login`, `agent_instance`, `model_family_if_known`, `role_in_event`. Dos cuentas GitHub controladas por la misma persona no acreditan independencia humana; dos evaluaciones GPT/Grok separadas no equivalen a dos humanos independientes.

Niveles: `PRIMARY_OBSERVED` (mensaje original efectivamente accesible, bytes de artefacto, respuesta GitHub), `SECONDARY_ATTRIBUTED` (resumen de coordinador/handoff), `INFERRED_WITH_BASIS`, `UNKNOWN`. **Calificar cada afirmación, no cada archivo en bloque.** Un contrato es `PRIMARY_OBSERVED` respecto de lo que está escrito en él, y puede ser solo `SECONDARY_ATTRIBUTED` respecto de una decisión del Owner que relata. La calificación es relativa a las fuentes accesibles al evaluador y debe indicar si el original está disponible en el paquete portable. Una lectura directa en la conversación actual sin un export estable puede ser primaria para PCM-001 y solo secundaria para una QA externa que recibe una transcripción. El código de decisión, firma o SHA identifica bytes, **no** acredita por sí solo el origen intelectual del requisito.

## 2. Formato portable de registro atómico (propuesta local; aún no norma general)

Un registro por **evento y cláusula**; la cadena se reconstruye por relaciones, no se sobreescribe. Campos obligatorios:

```yaml
schema_version: "PCM-PROVENANCE-R3-DRAFT"
record_id: "PCM-PROV-<unique-id>"
claim_id: "<clause-or-control-id>"
event_type: "AGENT_RECOMMENDATION | OWNER_ADOPTION_OF_RECOMMENDATION | ..."
actor:
  human_actor: "OWNER | OTHER_HUMAN | NONE | UNKNOWN"
  account_or_agent: "KhaosMagnus | JormungandrMagnus | PCM-001/GPT | Grok | UNKNOWN"
  role: "recommender | drafter | issuer | decision_maker | operator | verifier"
provenance:
  idea_originator: "OWNER | PCM-001/GPT | Grok | OTHER | UNKNOWN"
  recommender: "PCM-001/GPT | Grok | OTHER | NONE | UNKNOWN"
  drafter: "PCM-001/GPT | Grok | OWNER | OTHER | UNKNOWN"
  issuer: "OWNER | AGENT | SYSTEM | UNKNOWN"
source:
  kind: "original_chat_message | frozen_file | github_readback | third_party_report"
  locator: "<stable reference if available>"
  sha256: "<file hash if applicable; otherwise NOT_APPLICABLE>"
  timestamp: "<observed timestamp, or UNKNOWN>"
  exact_excerpt: "<short verbatim quote, or NOT_AVAILABLE>"
  evidence_grade: "PRIMARY_OBSERVED | SECONDARY_ATTRIBUTED | INFERRED_WITH_BASIS | UNKNOWN" # valoración del objeto fuente, NO de todas las afirmaciones citadas
  accessible_to_reviewer: true # false si solo existe una transcripción o resumen
  portable_original_attached: false # true SOLO con original exportado/incorporado
claims: # obligatorio: una entrada por afirmación material
  - predicate: "DOCUMENT_TEXT | OWNER_GRANTED | OWNER_EXECUTED | IDEA_ORIGIN | ..."
    asserted_value: "<literal or structured fact>"
    evidence_grade: "PRIMARY_OBSERVED | SECONDARY_ATTRIBUTED | INFERRED_WITH_BASIS | UNKNOWN"
    evidence_locator: "<original message, exact file/section, or NONE>"
    limitation: "<scope and inference restriction>"
links:
  recommends: "<proposal-record-id | NONE>"
  adopts: "<proposal/clause-id | NONE>"
  authorized_execution_of: "<scope-id | NONE>"
  executed_under: "<grant-id | NONE>"
  verified_by: ["<readback/QA-id>"]
decision:
  value: "GRANTED | ACCEPT | ACCEPT_MODIFIED | REJECT | REVISE | DEFER | NONE"
  execution_authorized: "true | false | UNKNOWN"
  scope: "<exact approved scope or NONE>"
  exclusions: ["<unauthorized acts>"]
  modified_clause: "<exact replacement if ACCEPT_MODIFIED, otherwise NONE>"
  rejected_clause: "<exact rejected content if REJECT, otherwise NONE>"
effect:
  operator: "<actor | NOT_APPLICABLE | UNKNOWN>"
  result: "NOT_EXECUTED | OBSERVED | INCONCLUSIVE | FAILED"
  evidence_ref: "<commit, blob, QA ID, log or NONE>"
classification:
  error_source: "<actor or UNKNOWN>"
  status: "DRAFT | PROPOSED | AUTHORIZED | EXECUTED | VERIFIED | NONCONFORMITY | SUPERSEDED"
  supersedes: "<prior record ID | NONE>"
  confidence_note: "<limitations>"
```

**Integridad:** para cambios de estado crear **un evento adicional**, no actualizar silenciosamente registros anteriores. Fuentes textuales deben quedar congeladas por hash; si el mensaje no ofrece referencia estable, conservar transcripción fiel **rotulada secundaria** y señalar la ausencia de locator primario. No transcribir como comillas literales contenido que no se ha recuperado. Para una decisión mixta, incluir tantas unidades atómicas como cláusulas autónomas. `REJECT` es decisión expresa negativa y fija `execution_authorized=false` en ese alcance; no significa `NONE` (sin decisión), `DEFER` (aplazamiento) ni `REVISE` (solicitud de cambio). `ACCEPT_MODIFIED` exige nueva versión exacta y conserva la propuesta anterior como no aceptada en su forma original.

**Controles de origen erróneo:** requiere `actor` y `source` específicos para toda afirmación `Owner ordered/initiated`. Un Owner que **aprueba una mala recomendación** sigue siendo quien decidió y autorizó según la evidencia; la responsabilidad técnica del análisis equivocado se documenta por separado. No se infiere exoneración, culpa exclusiva, intenciones o causalidad sin prueba.

### 2.1 Caso de prueba obligatorio A4: decisión mixta sobre un único mensaje del Owner

**Ejemplo didáctico, NO decisión real:** un LLM propone A, B y C. El Owner responde: «Acepto A; acepto B solo con la modificación B′; rechazo C». Propuesta y respuesta deben enlazarse al mismo `decision_source_id`, sin convertir al Owner en autor de A, B o C.

| Unidad | Fuente de la propuesta | Decisión emitida | Registro exacto | Efecto |
|---|---|---|---|---|
| A | `AGENT_RECOMMENDATION/A`, actor LLM | Owner acepta A | `decision.value=ACCEPT`; `adopts=A`; `issuer=OWNER` | A queda aceptada **solo** en el alcance expreso; no es autorización de ejecución por defecto |
| B | `AGENT_RECOMMENDATION/B`, actor LLM | Owner sustituye B por B′ | `decision.value=ACCEPT_MODIFIED`; `adopts=B`; `modified_clause=B′`; fuente Owner para el **delta**, no para toda B | B original no aceptada tal cual; B′ aceptada y trazada a la intervención Owner |
| C | `AGENT_RECOMMENDATION/C`, actor LLM | Owner rechaza C | `decision.value=REJECT`; `rejected_clause=C`; `execution_authorized=false` | No se ejecuta C; el rechazo permanece verificable |

Cada unidad exige su propio `claim_id`, enlace al mensaje original y grado probatorio. Un ejemplo pedagógico no debe registrarse como decisión efectiva del proyecto.

## 3. Auditoría piloto de procedencia: P5→P6 (propuesta, NO corrección vigente)

| Unidad | Fuentes observables y grado sobre lo que efectivamente contienen | Acto del Owner: evidencia disponible y límite | Atribución conservadora |
|---|---|---|---|
| Contrato que exige revisor elegible, STOP P5 y dos QA PASS | `EXEC` §§3/5; **PRIMARY_OBSERVED** para la redacción contractual de PCM-001 | La aprobación G2-B se **relata** en handoffs: **SECONDARY_ATTRIBUTED** dentro del paquete R2 sin mensaje original de GRANTED. Origen intelectual previo de cláusulas: **UNKNOWN** | `PCM-001 DOCUMENTED/PROPOSED THE CLAUSES`; `OWNER GRANTED` solo conforme a la fuente efectiva de cada revisión; sigue sin demostrar quién tuvo primero cada idea |
| Revisión personal de cinco controles | Handoff P5 y conversación de PCM-001: **PRIMARY_OBSERVED** para la instrucción escrita por GPT | Mensaje original del Owner es visible **en esta conversación de PCM-001**, pero no fue incluido como original en el paquete R2: **PRIMARY_OBSERVED LOCAL / SECONDARY_ATTRIBUTED FOR EXTERNAL QA** | `AGENT-INSTRUCTED CHECK → OWNER-ISSUED REVIEW`; no prueba que el Owner originó la idea de saltar STOP |
| Instrucción de avanzar P5→P6 | Handoff P5 del agente: **PRIMARY_OBSERVED** para la dirección operativa que permitió seguir pese al requisito pendiente | La salida del push P6 fue aportada por el Owner **en esta conversación**, pero no como registro primario portable a la QA R2: **PRIMARY_OBSERVED LOCAL / SECONDARY_ATTRIBUTED FOR EXTERNAL QA** | Defecto documentable de coordinación de PCM-001. No inferir número total de intentos ni ordenar retroactivamente otras operaciones |
| Disposición de preservar la no conformidad | Propuesta de PCM-001 y handoffs: **PRIMARY_OBSERVED** para esos textos | El mensaje original del Owner **sí está visible en esta conversación**: «ordeno conservarla como no conformidad histórica»; no está incluido como export original en el paquete R2. **PRIMARY_OBSERVED LOCAL / SECONDARY_ATTRIBUTED FOR EXTERNAL QA** | Decisión vinculante emitida por Owner sobre una cuestión previamente propuesta por GPT; **no** autoría Owner de la propuesta antecedente |
| Gate de dos QA PASS | `EXEC` §5: **PRIMARY_OBSERVED** de su inclusión en un texto de PCM-001 | Su adopción como parte de G2-B **SECONDARY_ATTRIBUTED** en el paquete R2 sin el mensaje original; no elevar a primaria por el SHA del contrato | Puerta histórica conservada como regla del diseño autorizado según el expediente, sin atribuir al Owner su origen intelectual |
| Opción B y enmienda unipersonal | Candidato UNI: **PRIMARY_OBSERVED** para su texto de PCM-001 | `OWNER DECISION — PCM-G2B-P8-P5-DISPOSITION-001` aparece originalmente en esta conversación, pero solo relatado en paquete R2: **PRIMARY_OBSERVED LOCAL / SECONDARY_ATTRIBUTED FOR EXTERNAL QA** | `GPT-PROPOSED → OWNER-GRANTED DESIGN ONLY`; no equivale a aceptación de UNI |
| Mandato de revisión humana y aceptación final por el Owner | Mensajes directos de Owner visibles en esta conversación **PRIMARY_OBSERVED LOCAL**, con origen previo no plenamente documentado **UNKNOWN** | Frente a QA externa sin el original: **SECONDARY_ATTRIBUTED**. La identidad del emisor actual es Owner | `OWNER-ISSUED DIRECTIVE`; no adjudicar primera autoría absoluta de todo antecedente sin su prueba |
| Política de procedencia y diseño R2/R3 | Propuesta del agente: **PRIMARY_OBSERVED** como texto propio. Problema señalado por Owner en mensaje original visible aquí: **PRIMARY_OBSERVED LOCAL** | Owner concedió `GRANTED QA ONLY` para R2 en esta conversación: **PRIMARY_OBSERVED LOCAL**, sin aceptación normativa. QA externa dispone solo de lo recibido | `OWNER-ORIGINATED PROBLEM STATEMENT → PCM-001-DRAFTED SOLUTION → OWNER AUTHORIZED QA ONLY` |

**Regla de portabilidad:** las calificaciones `PRIMARY_OBSERVED LOCAL` de la tabla no se transfieren automáticamente como primarias. Si el original no se adjunta mediante un export fiel, fechado y verificable, cualquier QA que solo vea este documento debe usar `SECONDARY_ATTRIBUTED` para el acto conversacional. No se inventan URLs a mensajes individuales ni evidencias de primera emisión histórica. Cada afirmación tiene grado propio, aun cuando comparta archivo con otras de mayor fuerza probatoria.

**No inferir origen intelectual completo** del requisito de PR por la sola línea `Prepared by PCM-001`. Se acredita que PCM-001 lo **redactó** y lo recomendó en el contrato; un eventual antecedente anterior podría cambiar `idea_originator` sin cambiar la responsabilidad de la recomendación operativa P5→P6.

**Prohibición retroactiva:** conservar completos G2-B histórico, readbacks, commits, notas P5/P6 y los dos informes P8 `INCONCLUSIVE` (Grok `FAILED` para elegibilidad Q6). Un anexo `PROVENANCE_CORRECTION` aditivo explicará clasificaciones imprecisas si se aprueba, **sin convertir** INCONCLUSIVE en PASS, sin eliminar STOP histórico, sin cambiar SHAs ni afirmar nueva autorización. La enmienda unipersonal tampoco queda aceptada por este contrato.

## 4. Workflow de control de procedencia propuesto

**Entrada:** al generar una recomendación con efecto contractual, de seguridad, permisos, QA, integración, costo o dependencias, PCM-001 debe iniciar un registro `AGENT_RECOMMENDATION` con texto y SHA de versión. Para asesoría incidental sin decisión de impacto, el registro es opcional; evitar burocracia no material.

**Decisión:** solo la respuesta efectiva del Owner crea `OWNER_ADOPTION_OF_RECOMMENDATION`, `OWNER_ORIGINATED_DIRECTIVE`, `OWNER_DIRECT_DISPOSITION_OF_AGENT_TOPIC` o `OWNER_EXECUTION_GRANT`, según corresponda. Cuando combine cláusulas, separarlas. No convertir preguntas, comentarios o «adelante» de alcance limitado en aceptación global.

**Antes de ejecutar:** comprobar `decision → specific scope → actor → preconditions → STOP`; diferenciar aprobación de diseño y permiso de ejecución. Si el asistente sugiere saltar una condición contractual, debe elevar una solicitud de revisión antes, no dar instrucciones de avance.

**Después de ejecutar:** registrar resultado/errores/readback/QA por fuentes originales. Un dictamen QA no equivale a aceptación del Owner. En fallos, separar `defective_recommendation`, `owner_grant`, `operator_action`, `observable_result` y `owner_remediation_decision` sin borrar ninguno.

**Corrección posterior:** producir `PROVENANCE_CORRECTION` con `old_claim`, `corrected_claim`, `evidence_refs`, `reason`, `confidence`, `author_of_correction`, `owner_disposition`, `effective_from`. Preservar documento y resultado históricos; no reemplazar el primer registro ni cambiar QA retroactivamente.

**Precedencia:** este contrato R3 solo sería vigente para gobierno documental local **tras nueva autorización de QA sobre R3, dos QA documentales focalizadas favorables y `OWNER ACCEPT` del SHA exacto**. La QA previa de R2 no se convierte en QA de R3. Antes de ello es candidato. Aun aceptado, no crea permiso de publicación en `meta/project-control`, no activa PCM-001 ni regula proyectos adoptantes automáticamente; no modifica la política histórica de G2-B por sola implicación.

## 5. QA focalizada: criterios A1–A12

| ID | Prueba documental que debe realizar cada revisor |
|---|---|
| A1 | `issuer`, `drafter`, `recommender`, `idea_originator` y `decision_maker` se distinguen inequívocamente |
| A2 | GPT redacta un bloque y Owner lo pega: doble procedencia + autoridad correcta + no adopción antes del acto Owner |
| A3 | Owner emite un mandato propio: se registra `OWNER_ORIGINATED_DIRECTIVE`, no atribución automática al LLM |
| A4 | Una respuesta mixta Owner (acepta A, cambia B, rechaza C) se descompone en unidades con diferente origen y alcance |
| A5 | P5→P6: la instrucción operativa incompatible se atribuye a PCM-001 y queda visible la autorización/operación Owner, sin imputar orden de saltar STOP |
| A6 | La orden Owner de preservar la no conformidad se registra como decisión suya con antecedente GPT |
| A7 | El requisito de dos QA PASS se registra como redactado/recomendado por GPT y luego adoptado en contrato Owner; permanece vigente |
| A8 | La enmienda unipersonal R1 permanece pendiente de aceptación, pese a doble QA documental favorable |
| A9 | Fuentes sin mensaje original ni antecedente completo muestran `UNKNOWN`/`SECONDARY_ATTRIBUTED`; el SHA documental no se usa para probar autoría intelectual |
| A10 | Registro de error distingue recomendador, autorizador, operador, QA y disposición; no inventa culpabilidad o exoneración |
| A11 | Los registros congelados permanecen intactos; corrección aditiva, precedencia solo prospectiva, sin cambiar QA históricos |
| A12 | Distingue diseño, QA, aceptación Owner, publicación y adopción; ninguna acción GitHub queda implícita |

**Verdictos:** `DESIGN PASS (CONDITIONAL)` si A1–A12 cumplen y las pruebas operativas y de procedencia original no disponibles se reconocen; `DESIGN REVISE` si existen defectos documentales corregibles; `DESIGN FAIL` por contradicción material; `INCONCLUSIVE` ante imposibilidad de verificar las fuentes contractuales relevantes. Cada revisor incluye citas por archivo, cláusula y SHA; debe separar su análisis autónomo de la narrativa de PCM-001.

## 6. Límites, pendientes y alcance de aceptación futura

1. **QA de este diseño** no modifica GitHub ni suple revisión humana. Se propone GPT y Grok, mismo paquete congelado, informes separados al Owner.
2. El mensaje original del GRANTED G2-B y la historia antecedente que dio origen a algunas frases del contrato no están incluidos como originales en el paquete R2; otros mensajes originales del Owner son visibles localmente en la conversación actual, pero no portables por ello. Es una **limitación explícita**, no autorización para inventar atribución. Quien tenga acceso al mensaje original debe cotejarlo antes de afirmar que una cláusula vino originalmente del Owner.
3. La adopción de esta política es **distinta** de la aceptación pendiente de `PCM-G2B-P8-UNI-DES-001` y de la aceptación integral G2-B, que aún depende de evidencias Q5/Q7/Q8/Q9 y del gate histórico de dos QA PASS.
4. La política local, si aceptada, se aplicará desde la fecha de aceptación a decisiones materiales nuevas y a **anexos correctivos aditivos** del historial; no se reescribe la historia.
5. No habilita crear repositorios, ramas, PR, cambios de permisos, rulesets, fusiones, releases, G3, G4, G5, ni adopción externa.
6. Incorporar esta característica al protocolo portable requiere especificación, versión, QA y decisión de release separadas.

**Disposition:** `R3 CORRECTIVE DESIGN DRAFT / R2 DOUBLE QA RECONCILED AS REVISE / R3 QA REQUIRES SEPARATE OWNER GRANT / NOT ACCEPTED / NO EXECUTION`. 
