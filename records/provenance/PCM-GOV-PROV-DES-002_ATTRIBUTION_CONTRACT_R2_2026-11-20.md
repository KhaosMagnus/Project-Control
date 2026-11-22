# PROJECT CONTROL MASTER — Contrato de atribución y procedencia de recomendaciones, decisiones y ejecución

**Candidate:** `PCM-GOV-PROV-DES-002 / R2`  
**Authored by:** `PCM-001` (assistant LLM; provisional coordinator)  
**Trigger:** Observación directa del Owner, 2026-11-20, sobre procedencia de recomendaciones frente a actos de autorización.  
**Source:** `PCM-GOV-DES-PROVENANCE-001` primer borrador, SHA-256 `77ad35f25c2be2dbb265f2a38ad6dac465e11960f8fb5f1f80cca18f02a6f8fd`.  
**Authorization for this work:** mensaje del Owner «prepares la mejora, el cambio, el ajuste y me des más o menos el plan … adelante», 2026-11-20, interpretado **exclusivamente como encargo de preparación documental**.  
**Status:** `FROZEN CANDIDATE FOR FOCUSED DOCUMENTARY QA / NOT APPROVED / NOT EFFECTIVE / NO EXECUTABLE AUTHORITY`.  
**Scope:** gobernanza documental **local y prospectiva** de PCM-001; sin aplicación al protocolo genérico `main`, a proyectos adoptantes ni a la infraestructura G2-B sin actos posteriores expresos.

## 0. Problema que se corrige y criterio de éxito

**Defecto:** los registros pueden indicar correctamente `Owner GRANTED` y, a la vez, atribuir **incorrectamente al Owner la iniciativa intelectual** de una política formulada por GPT, Grok u otro actor. También pueden ocultar quién recomendó la ruta técnica que produjo una desviación. La autoridad del Owner es real y vinculante en su alcance, pero **aceptar una recomendación no implica haberla originado**.

**Éxito documental:** para toda decisión material, un auditor puede seguir `fuente primaria → idea/recomendación → texto propuesto → mensaje de decisión → autorización de ejecución → actuación → readback/QA → disposición`, separando actores, credenciales, fechas y niveles de evidencia. Las lagunas quedan explícitas como `UNKNOWN`, nunca se llenan por inferencia disfrazada de hecho.

**Regla R0 (de prioridad máxima):** el Owner **originó y reiteró directamente** la regla de autoridad: él realiza la revisión humana y conserva exclusivamente la aceptación final y decisiones reservadas. Ese mandato NO será reclasificado como una recomendación de GPT. Es distinta la procedencia de la propuesta técnica unipersonal, que sí fue preparada por PCM-001 y autorizada para diseño por el Owner.

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
- **R3:** La adopción parcial se descompone en cláusulas; exclusiones, condiciones o modificaciones introducidas por el Owner se atribuyen a él **en esas cláusulas**, no en toda la propuesta.
- **R4:** Expresiones como «adelante», «sí», «acepto» y «GRANTED» se interpretan por contexto y objeto inequívoco; cuando el alcance material sea ambiguo, solo se registra la decisión comprobable y se solicita precisión antes de una ejecución nueva.
- **R5:** Los textos ofrecidos por GPT bajo el rótulo `OWNER DECISION` son **propuestas no emitidas** hasta que el Owner las adopte explícitamente. Mostrar un WritingBlock no genera autorización.

### 1.1 Tipos de eventos válidos

`OWNER_ORIGINATED_DIRECTIVE`, `AGENT_RECOMMENDATION`, `AGENT_DRAFT`, `OWNER_ADOPTION_OF_RECOMMENDATION`, `OWNER_DIRECT_DISPOSITION_OF_AGENT_TOPIC`, `OWNER_EXECUTION_GRANT`, `OPERATIONAL_DIRECTION_BY_AGENT`, `OWNER_OPERATOR_ACTION`, `READBACK_OBSERVATION`, `INDEPENDENT_DOCUMENTARY_QA`, `ERROR_FINDING`, `HISTORICAL_NONCONFORMITY`, `OWNER_FINAL_ACCEPTANCE`, `PROVENANCE_CORRECTION`.

`OWNER_ORIGINATED_DIRECTIVE` exige una intervención iniciada por el Owner y evidencia de que el criterio no es simplemente la adopción de una propuesta identificada; si esta última existe, usar ambos registros ligados. Una disposición del Owner **puede ser directa y vinculante** aunque trate una idea sugerida previamente por GPT: `OWNER_DIRECT_DISPOSITION_OF_AGENT_TOPIC` conserva ambos hechos.

### 1.2 Identidades y fiabilidad

Para personas y cuentas se almacenan claves distintas: `human_actor`, `service_account`/`github_login`, `agent_instance`, `model_family_if_known`, `role_in_event`. Dos cuentas GitHub controladas por la misma persona no acreditan independencia humana; dos evaluaciones GPT/Grok separadas no equivalen a dos humanos independientes.

Niveles: `PRIMARY_OBSERVED` (mensaje original, artefacto con hash, resultado de GitHub), `SECONDARY_ATTRIBUTED` (resumen de coordinador/handoff), `INFERRED_WITH_BASIS`, `UNKNOWN`. El código de una decisión, una firma o un SHA identifica el documento y sus bytes, **no** acredita por sí solo quién originó intelectualmente el requisito.

## 2. Formato portable de registro atómico (propuesta local; aún no norma general)

Un registro por **evento y cláusula**; la cadena se reconstruye por relaciones, no se sobreescribe. Campos obligatorios:

```yaml
schema_version: "PCM-PROVENANCE-R2-DRAFT"
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
  evidence_grade: "PRIMARY_OBSERVED | SECONDARY_ATTRIBUTED | INFERRED_WITH_BASIS | UNKNOWN"
links:
  recommends: "<proposal-record-id | NONE>"
  adopts: "<proposal/clause-id | NONE>"
  authorized_execution_of: "<scope-id | NONE>"
  executed_under: "<grant-id | NONE>"
  verified_by: ["<readback/QA-id>"]
decision:
  value: "GRANTED | ACCEPT | REVISE | DEFER | NONE"
  scope: "<exact approved scope or NONE>"
  exclusions: ["<unauthorized acts>"]
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

**Integridad:** para cambios de estado crear **un evento adicional**, no actualizar silenciosamente registros anteriores. Fuentes textuales deben quedar congeladas por hash; si el mensaje no ofrece referencia estable, conservar transcripción fiel **rotulada secundaria** y señalar la ausencia de locator primario. No transcribir como comillas literales contenido que no se ha recuperado. Para una decisión mixta, incluir tantas unidades atómicas como cláusulas autónomas.

**Controles de origen erróneo:** requiere `actor` y `source` específicos para toda afirmación `Owner ordered/initiated`. Un Owner que **aprueba una mala recomendación** sigue siendo quien decidió y autorizó según la evidencia; la responsabilidad técnica del análisis equivocado se documenta por separado. No se infiere exoneración, culpa exclusiva, intenciones o causalidad sin prueba.

## 3. Auditoría piloto de procedencia: P5→P6 (propuesta, NO corrección vigente)

| Unidad | Recomendó/redactó | Decisión o acto del Owner | Conclusión de procedencia (calificación) |
|---|---|---|---|
| Exigir revisor GitHub independiente elegible y STOP previo a P6 | Contrato ejecutivo redactado por `PCM-001 PROVISIONAL`; fuente congelada SHA-256 `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349` | `GRANTED` G2-B emitido por Owner en conversación; texto exacto no incorporado al primer paquete P8 | **GPT-DRAFTED CONTRACT → OWNER-APPROVED EXECUTION SCOPE**. `idea_originator` anterior al contrato: `UNKNOWN` salvo fuente primaria adicional |
| Revisión de los cinco controles R-MAIN | Handoff PCM-001, instrucciones de configuración | El Owner realizó revisión personal y lo confirmó por mensaje | **AGENT-INSTRUCTED CHECK → OWNER-EXECUTED HUMAN REVIEW**, no orden originada por Owner de saltar STOP |
| Instrucción posterior de pasar a P6 | Handoff PCM-001 preparado por GPT después de constatar la elegibilidad aún pendiente | Owner reportó y aportó salida de un push P6 conforme a la guía entregada; el número total de intentos no está acreditado; salida incluida en conversación | **AGENT OPERATIONAL DIRECTION + OWNER ACTION**; no se atribuye al Owner la idea de ignorar el requisito |
| Desviación histórica P5→P6 | Incompatibilidad de la recomendación operativa PCM-001 con STOP G2-B vigente | Owner ordenó conservar la no conformidad, tras recibir propuesta PCM-001 | **COORDINATION DEFECT PCM-001** en la instrucción; **OWNER DISPOSITION** vinculante para mantener el historial. No convalidación retroactiva |
| Gate dos QA `PASS` para aceptación integral G2-B | Contrato ejecutivo redactado por PCM-001 | Quedó incluido en el G2-B autorizado por el Owner | **GPT-DRAFTED GATE → OWNER-GRANTED RULE**; sigue vigente hasta decisión explícita modificatoria |
| Alternativa B y enmienda unipersonal | Recomendación GPT, documento `PCM-G2B-P8-UNI-DES-001` redactado por PCM-001 SHA-256 `410c12a8f2f46ac20322a6ec76d76e038c9b7979a565044d6db8ee5cec29ca76` | Owner autorizó `GRANTED DESIGN ONLY — OPTION B`; la aceptación posterior de la enmienda sigue **pendiente** | **GPT RECOMMENDATION → OWNER DESIGN GRANT**, no aceptación final de la enmienda |
| Mandato: revisión humana y aceptación final corresponden al Owner | Mensajes directos reiterados del Owner, incluidos los del 20/11/2026 | Originó/reafirmó su autoridad y exigió no requerir un segundo humano por inferencia | **OWNER-ORIGINATED DIRECTIVE**; no degradar a «GPT-proposed» |
| Política nueva de procedencia (presente documento) | Propuesta redactada por PCM-001 en respuesta a observación originada por Owner | Owner pidió preparar el ajuste y el plan, **no lo ha aceptado** | **OWNER-ORIGINATED PROBLEM STATEMENT → GPT-DRAFTED SOLUTION → OWNER AUTHORIZED DESIGN ONLY** |

**No inferir origen intelectual completo** del requisito de PR por la sola línea `Prepared by PCM-001`. Se acredita que PCM-001 lo **redactó** y lo recomendó en el contrato; un eventual antecedente anterior podría cambiar `idea_originator` sin cambiar la responsabilidad de la recomendación operativa P5→P6.

**Prohibición retroactiva:** conservar completos G2-B histórico, readbacks, commits, notas P5/P6 y los dos informes P8 `INCONCLUSIVE` (Grok `FAILED` para elegibilidad Q6). Un anexo `PROVENANCE_CORRECTION` aditivo explicará clasificaciones imprecisas si se aprueba, **sin convertir** INCONCLUSIVE en PASS, sin eliminar STOP histórico, sin cambiar SHAs ni afirmar nueva autorización. La enmienda unipersonal tampoco queda aceptada por este contrato.

## 4. Workflow de control de procedencia propuesto

**Entrada:** al generar una recomendación con efecto contractual, de seguridad, permisos, QA, integración, costo o dependencias, PCM-001 debe iniciar un registro `AGENT_RECOMMENDATION` con texto y SHA de versión. Para asesoría incidental sin decisión de impacto, el registro es opcional; evitar burocracia no material.

**Decisión:** solo la respuesta efectiva del Owner crea `OWNER_ADOPTION_OF_RECOMMENDATION`, `OWNER_ORIGINATED_DIRECTIVE`, `OWNER_DIRECT_DISPOSITION_OF_AGENT_TOPIC` o `OWNER_EXECUTION_GRANT`, según corresponda. Cuando combine cláusulas, separarlas. No convertir preguntas, comentarios o «adelante» de alcance limitado en aceptación global.

**Antes de ejecutar:** comprobar `decision → specific scope → actor → preconditions → STOP`; diferenciar aprobación de diseño y permiso de ejecución. Si el asistente sugiere saltar una condición contractual, debe elevar una solicitud de revisión antes, no dar instrucciones de avance.

**Después de ejecutar:** registrar resultado/errores/readback/QA por fuentes originales. Un dictamen QA no equivale a aceptación del Owner. En fallos, separar `defective_recommendation`, `owner_grant`, `operator_action`, `observable_result` y `owner_remediation_decision` sin borrar ninguno.

**Corrección posterior:** producir `PROVENANCE_CORRECTION` con `old_claim`, `corrected_claim`, `evidence_refs`, `reason`, `confidence`, `author_of_correction`, `owner_disposition`, `effective_from`. Preservar documento y resultado históricos; no reemplazar el primer registro ni cambiar QA retroactivamente.

**Precedencia:** este contrato solo sería vigente para gobierno documental local **tras dos QA documentales focalizadas y `OWNER ACCEPT` del SHA exacto**. Antes de ello es candidato. Aun aceptado, no crea permiso de publicación en `meta/project-control`, no activa PCM-001 ni regula proyectos adoptantes automáticamente; no modifica la política histórica de G2-B por sola implicación.

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
2. El mensaje original del GRANTED G2-B y la historia antecedente que dio origen a algunas frases del contrato pueden no estar disponibles en el paquete. Es una **limitación explícita**, no autorización para inventar atribución. Quien tenga acceso al mensaje original debe cotejarlo antes de afirmar que una cláusula vino originalmente del Owner.
3. La adopción de esta política es **distinta** de la aceptación pendiente de `PCM-G2B-P8-UNI-DES-001` y de la aceptación integral G2-B, que aún depende de evidencias Q5/Q7/Q8/Q9 y del gate histórico de dos QA PASS.
4. La política local, si aceptada, se aplicará desde la fecha de aceptación a decisiones materiales nuevas y a **anexos correctivos aditivos** del historial; no se reescribe la historia.
5. No habilita crear repositorios, ramas, PR, cambios de permisos, rulesets, fusiones, releases, G3, G4, G5, ni adopción externa.
6. Incorporar esta característica al protocolo portable requiere especificación, versión, QA y decisión de release separadas.

**Disposition:** `DESIGN READY FOR INDEPENDENT FOCUSED QA / NOT ACCEPTED / NO EXECUTION`. 
