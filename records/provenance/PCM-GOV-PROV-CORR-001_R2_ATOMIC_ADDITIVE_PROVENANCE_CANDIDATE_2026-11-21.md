# PCM-001 — CORR-001 R2: anexo aditivo de procedencia P5→P6

**Record ID:** `PCM-GOV-PROV-CORR-001` · **Revision:** `R2 / NEW CANDIDATE`  
**Autor / recomendador de esta revisión:** `PCM-001/GPT`  
**Origen del problema general:** observación directa del Owner, distinta de la propuesta de solución de PCM-001  
**Autoridad vigente para preparar este borrador:** política R3 aceptada localmente (`PCM-GOV-PROV-R3-ACCEPTANCE-001`) y encargo conversacional de continuar la revisión de CORR-001  
**Estado:** `DRAFT / NOT OWNER-ACCEPTED / NO HISTORICAL CORRECTION APPLIED / NO GITHUB WRITES`  
**Base normativa local:** `PCM-GOV-PROV-DES-003 / R3`, SHA-256 `325bd44c8ab572cd7229219d7f08325e170c0e0797f9025c1abae4abb0a10cad`.

## 0. Límite de la corrección

Este anexo **no reemplaza** el contrato congelado G2-B, el handoff P5, las decisiones Owner ni los informes de QA `INCONCLUSIVE`. Tampoco acredita por sí solo el cumplimiento histórico del STOP. La interpretación documentada debe reconocer que PCM-001 preparó el procedimiento y recomendó avanzar P5→P6, mientras que el Owner emitió decisiones propias y reportó operaciones, sin que aprobar una propuesta le atribuya su origen intelectual.

**Alcance negativo importante:** el borrador CORR-001 inicial aludía a «cualquier resumen» que confundiera ambos actores; no identificaba un fragmento original concreto que dijera literalmente «el Owner originó la instrucción de saltar STOP». Este R2 no inventa tal cita: opera como **rectificación interpretativa y preventiva** de la cadena histórica, con identificación positiva de las fuentes que sí existen. Para rectificar un texto histórico específico se necesitaría localizar el fragmento, fijar el SHA y emitir una anotación adicional específica. La contradicción comprobable es **EXEC §3 P5 frente a P5 §2**.

## 1. Decisión y efectos del presente candidato

- `event_type`: `PROVENANCE_CORRECTION` **propuesto**, no emitido.
- `classification.status`: `DRAFT`.
- `decision.value`: `NONE` (el Owner aún no decidió sobre este anexo).
- `decision.execution_authorized`: `false` (no existe permiso para alterar repositorios, fuentes congeladas o aplicar esta corrección como vigente).
- `links.adopts`: `NONE` hasta aceptación del Owner del **SHA exacto** de este R2.
- `effect.result`: `NOT_EXECUTED`; `supersedes=NONE`.
- `corrected_claim`: la dirección operativa P5→P6 fue redactada/recomendada por PCM-001; el Owner efectuó actos de revisión y reportó ejecución; la incompatibilidad con STOP es hallazgo documental. La posterior orden Owner de conservar la no conformidad se distingue de la propuesta GPT antecedente.
- `old_claim`: patrón de atribución imprecisa identificado por el Owner, **sin localizador primario de una frase histórica falsamente atribuida**. No se presupone que el Owner emitiera una orden de saltar STOP.

## 2. Registros de procedencia atómicos (ocho claims)

Cada registro se presenta con el esquema de R3. `claims[].evidence_grade` expresa **lo que puede acreditar el receptor del presente paquete**; una fuente textual congelada puede acreditar primariamente lo escrito y solo secundariamente un acto conversacional relatado. `local_observation` es una anotación contextual de PCM-001, **no evidencia primaria transferible** a QA externa. `source.portable_original_attached=false` se usa en mensajes conversacionales; en fuentes documentales significa que se adjunta el archivo, no el acto primario que pudiera relatar.

### CORR-01 — DOCUMENT_TEXT

```yaml
schema_version: PCM-PROVENANCE-R3-DRAFT
record_id: PCM-GOV-PROV-CORR-001-CORR-01
claim_id: CORR-01
event_type: AGENT_DRAFT
actor:
  human_actor: NONE
  account_or_agent: PCM-001/GPT
  role: drafter
provenance:
  idea_originator: UNKNOWN
  recommender: PCM-001/GPT
  drafter: PCM-001/GPT
  issuer: AGENT
source:
  kind: frozen_file
  locator: 01_PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_REQUEST_2026-11-16.md §3 P5
  sha256: 037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349
  timestamp: UNKNOWN
  exact_excerpt: STOP
  evidence_grade: PRIMARY_OBSERVED
  accessible_to_reviewer: true
  portable_original_attached: true
  local_observation: PRIMARY_OBSERVED
claims:
- predicate: DOCUMENT_TEXT
  asserted_value: En el contrato ejecutivo propuesto se incluyó exigir un revisor GitHub elegible y STOP antes de P6 si
    no se demostraba una ruta de revisión viable.
  evidence_grade: PRIMARY_OBSERVED
  evidence_locator: 01_PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_REQUEST_2026-11-16.md §3 P5
  limitation: Prueba los bytes del contrato y su redacción por PCM-001; no demuestra quién imaginó primero cada cláusula
    ni la emisión original del GRANTED.
links:
  recommends: PCM-G2B-EXEC-RECOMMENDATION
  adopts: NONE
  authorized_execution_of: NONE
  executed_under: NONE
  verified_by: []
decision:
  value: NONE
  execution_authorized: false
  scope: HISTORICAL_EVENT_DESCRIPTION_ONLY
  exclusions:
  - NOT AN AUTHORIZATION OF THIS ADDITIVE ANNOTATION
  modified_clause: NONE
  rejected_clause: NONE
effect:
  operator: NOT_APPLICABLE
  result: NOT_EXECUTED
  evidence_ref: NONE
classification:
  error_source: UNKNOWN
  status: DRAFT
  supersedes: NONE
  confidence_note: Prueba los bytes del contrato y su redacción por PCM-001; no demuestra quién imaginó primero cada cláusula
    ni la emisión original del GRANTED.
```

### CORR-02 — DOCUMENT_TEXT

```yaml
schema_version: PCM-PROVENANCE-R3-DRAFT
record_id: PCM-GOV-PROV-CORR-001-CORR-02
claim_id: CORR-02
event_type: AGENT_DRAFT
actor:
  human_actor: NONE
  account_or_agent: PCM-001/GPT
  role: drafter
provenance:
  idea_originator: UNKNOWN
  recommender: PCM-001/GPT
  drafter: PCM-001/GPT
  issuer: AGENT
source:
  kind: frozen_file
  locator: 01_PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_REQUEST_2026-11-16.md §5
  sha256: 037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349
  timestamp: UNKNOWN
  exact_excerpt: PASS
  evidence_grade: PRIMARY_OBSERVED
  accessible_to_reviewer: true
  portable_original_attached: true
  local_observation: PRIMARY_OBSERVED
claims:
- predicate: DOCUMENT_TEXT
  asserted_value: El texto ejecutivo preparado por PCM-001 establece dos QA PASS y aceptación posterior del Owner como
    puerta de G2-B.
  evidence_grade: PRIMARY_OBSERVED
  evidence_locator: 01_PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_REQUEST_2026-11-16.md §5
  limitation: Evidencia directa del requisito escrito. La concesión histórica del Owner se conoce en este paquete mediante
    documentos secundarios, no mediante el mensaje original; no atribuir autoría intelectual exclusiva al Owner.
links:
  recommends: PCM-G2B-EXEC-RECOMMENDATION
  adopts: NONE
  authorized_execution_of: NONE
  executed_under: NONE
  verified_by: []
decision:
  value: NONE
  execution_authorized: false
  scope: HISTORICAL_EVENT_DESCRIPTION_ONLY
  exclusions:
  - NOT AN AUTHORIZATION OF THIS ADDITIVE ANNOTATION
  modified_clause: NONE
  rejected_clause: NONE
effect:
  operator: NOT_APPLICABLE
  result: NOT_EXECUTED
  evidence_ref: NONE
classification:
  error_source: UNKNOWN
  status: DRAFT
  supersedes: NONE
  confidence_note: Evidencia directa del requisito escrito. La concesión histórica del Owner se conoce en este paquete
    mediante documentos secundarios, no mediante el mensaje original; no atribuir autoría intelectual exclusiva al Owner.
```

### CORR-03 — DOCUMENT_TEXT

```yaml
schema_version: PCM-PROVENANCE-R3-DRAFT
record_id: PCM-GOV-PROV-CORR-001-CORR-03
claim_id: CORR-03
event_type: OPERATIONAL_DIRECTION_BY_AGENT
actor:
  human_actor: NONE
  account_or_agent: PCM-001/GPT
  role: recommender
provenance:
  idea_originator: UNKNOWN
  recommender: PCM-001/GPT
  drafter: PCM-001/GPT
  issuer: AGENT
source:
  kind: frozen_file
  locator: PCM-001_G2-B_P5_OWNER_REVIEW_AND_P6_CONTROLLED_HANDOFF_2026-11-20.md §2 disposición operativa y §§3–5
  sha256: c7bef232beed9e43b13dbb675dfb929ef9510e49047fa30798f2d6dd8cb6acdb
  timestamp: UNKNOWN
  exact_excerpt: Se prepara un único push P6
  evidence_grade: PRIMARY_OBSERVED
  accessible_to_reviewer: true
  portable_original_attached: true
  local_observation: PRIMARY_OBSERVED
claims:
- predicate: DOCUMENT_TEXT
  asserted_value: PCM-001 publicó un procedimiento que recomendaba avanzar a P6 aun cuando la elegibilidad de un futuro
    revisor no se había acreditado.
  evidence_grade: PRIMARY_OBSERVED
  evidence_locator: PCM-001_G2-B_P5_OWNER_REVIEW_AND_P6_CONTROLLED_HANDOFF_2026-11-20.md §2 disposición operativa y §§3–5
  limitation: El texto es directo; la contradicción con el STOP de CORR-01 es INFERRED_WITH_BASIS por cotejo de dos textos.
    No se atribuye al Owner una orden de saltar STOP.
links:
  recommends: PCM-G2B-EXEC-RECOMMENDATION
  adopts: NONE
  authorized_execution_of: NONE
  executed_under: NONE
  verified_by: []
decision:
  value: NONE
  execution_authorized: false
  scope: HISTORICAL_EVENT_DESCRIPTION_ONLY
  exclusions:
  - NOT AN AUTHORIZATION OF THIS ADDITIVE ANNOTATION
  modified_clause: NONE
  rejected_clause: NONE
effect:
  operator: NOT_APPLICABLE
  result: NOT_EXECUTED
  evidence_ref: NONE
classification:
  error_source: UNKNOWN
  status: DRAFT
  supersedes: NONE
  confidence_note: El texto es directo; la contradicción con el STOP de CORR-01 es INFERRED_WITH_BASIS por cotejo de dos
    textos. No se atribuye al Owner una orden de saltar STOP.
```

### CORR-04 — OWNER_ISSUED_REVIEW

```yaml
schema_version: PCM-PROVENANCE-R3-DRAFT
record_id: PCM-GOV-PROV-CORR-001-CORR-04
claim_id: CORR-04
event_type: OWNER_DIRECT_DISPOSITION_OF_AGENT_TOPIC
actor:
  human_actor: OWNER
  account_or_agent: KhaosMagnus
  role: issuer
provenance:
  idea_originator: UNKNOWN
  recommender: PCM-001/GPT
  drafter: PCM-001/GPT
  issuer: OWNER
source:
  kind: original_chat_message
  locator: Mensaje Owner «OWNER REVIEW — PCM-G2B-P5» visible en conversación PCM; no incluido como export original en
    el paquete
  sha256: NOT_APPLICABLE
  timestamp: UNKNOWN
  exact_excerpt: Confirmo que he revisado personalmente los cinco controles de P5
  evidence_grade: SECONDARY_ATTRIBUTED
  accessible_to_reviewer: false
  portable_original_attached: false
  local_observation: PRIMARY_OBSERVED LOCAL
claims:
- predicate: OWNER_ISSUED_REVIEW
  asserted_value: El Owner comunicó haber revisado los cinco controles de P5 y solicitado cerrar su verificación.
  evidence_grade: SECONDARY_ATTRIBUTED
  evidence_locator: Mensaje Owner «OWNER REVIEW — PCM-G2B-P5» visible en conversación PCM; no incluido como export original
    en el paquete
  limitation: Grado de este paquete externo SECONDARY_ATTRIBUTED; para PCM-001 mensaje original visible localmente. No
    acredita aprobación de una PR ni elegibilidad para PR futuras.
links:
  recommends: NONE
  adopts: NONE
  authorized_execution_of: NONE
  executed_under: NONE
  verified_by: []
decision:
  value: ACCEPT
  execution_authorized: UNKNOWN
  scope: HISTORICAL_EVENT_DESCRIPTION_ONLY
  exclusions:
  - NOT AN AUTHORIZATION OF THIS ADDITIVE ANNOTATION
  modified_clause: NONE
  rejected_clause: NONE
effect:
  operator: NOT_APPLICABLE
  result: OBSERVED
  evidence_ref: NONE
classification:
  error_source: UNKNOWN
  status: DRAFT
  supersedes: NONE
  confidence_note: Grado de este paquete externo SECONDARY_ATTRIBUTED; para PCM-001 mensaje original visible localmente.
    No acredita aprobación de una PR ni elegibilidad para PR futuras.
```

### CORR-05 — GITHUB_READBACK

```yaml
schema_version: PCM-PROVENANCE-R3-DRAFT
record_id: PCM-GOV-PROV-CORR-001-CORR-05
claim_id: CORR-05
event_type: OWNER_OPERATOR_ACTION
actor:
  human_actor: OWNER
  account_or_agent: KhaosMagnus
  role: operator
provenance:
  idea_originator: UNKNOWN
  recommender: PCM-001/GPT
  drafter: UNKNOWN
  issuer: OWNER
source:
  kind: frozen_file
  locator: PCM-001_G2-B_P6_READBACK_PASS_AND_P7_OPERATOR_INSTRUCTIONS_2026-11-20.md §1 readback
  sha256: bc9e317409e0f54997ae046e454a7444396c9839d6f2b0e8afadfbd9fea06aa8
  timestamp: UNKNOWN
  exact_excerpt: P6 user-reported single push succeeded
  evidence_grade: PRIMARY_OBSERVED
  accessible_to_reviewer: true
  portable_original_attached: true
  local_observation: PRIMARY_OBSERVED
claims:
- predicate: GITHUB_READBACK
  asserted_value: El readback de PCM-001 informó que meta/project-control apuntaba al commit raíz cac838940e0e824a1f828ff660e422a6441a1da7;
    el Owner había reportado la salida del push.
  evidence_grade: PRIMARY_OBSERVED
  evidence_locator: PCM-001_G2-B_P6_READBACK_PASS_AND_P7_OPERATOR_INSTRUCTIONS_2026-11-20.md §1 readback
  limitation: El readback es observación primaria del estado remoto descrito; la acción humana y el número total de intentos
    son secundarios/UNKNOWN en este paquete. Para autoría del push, no inferir identidad humana solo por autor de commit.
links:
  recommends: NONE
  adopts: NONE
  authorized_execution_of: NONE
  executed_under: G2-B-GRANTED (SECONDARY_ATTRIBUTED)
  verified_by:
  - PCM-G2B-IQA-INFRA-001
decision:
  value: NONE
  execution_authorized: UNKNOWN
  scope: HISTORICAL_EVENT_DESCRIPTION_ONLY
  exclusions:
  - NOT AN AUTHORIZATION OF THIS ADDITIVE ANNOTATION
  modified_clause: NONE
  rejected_clause: NONE
effect:
  operator: OWNER (REPORTED)
  result: OBSERVED
  evidence_ref: cac838940e0e824a1f828ff660e422a6441a1da7
classification:
  error_source: UNKNOWN
  status: DRAFT
  supersedes: NONE
  confidence_note: El readback es observación primaria del estado remoto descrito; la acción humana y el número total
    de intentos son secundarios/UNKNOWN en este paquete. Para autoría del push, no inferir identidad humana solo por autor
    de commit.
```

### CORR-06 — CONTRACT_INCONSISTENCY

```yaml
schema_version: PCM-PROVENANCE-R3-DRAFT
record_id: PCM-GOV-PROV-CORR-001-CORR-06
claim_id: CORR-06
event_type: ERROR_FINDING
actor:
  human_actor: NONE
  account_or_agent: PCM-001/GPT
  role: verifier
provenance:
  idea_originator: UNKNOWN
  recommender: PCM-001/GPT
  drafter: PCM-001/GPT
  issuer: AGENT
source:
  kind: frozen_file
  locator: PCM-001_G2-B_P8_DUAL_INDEPENDENT_QA_CONSOLIDATION_2026-11-20.md §4 Hallazgo rector
  sha256: 90b9ed72050022bbc3e8307e80de75019bbf5d370b4d28039c947c9891d63d08
  timestamp: UNKNOWN
  exact_excerpt: desviación P5→P6
  evidence_grade: PRIMARY_OBSERVED
  accessible_to_reviewer: true
  portable_original_attached: true
  local_observation: INFERRED_WITH_BASIS
claims:
- predicate: CONTRACT_INCONSISTENCY
  asserted_value: La guía operativa de PCM-001 condujo a P6 con la condición documental STOP sin acreditar; es una no
    conformidad histórica de transición, no evidencia de corrupción de los commits.
  evidence_grade: INFERRED_WITH_BASIS
  evidence_locator: PCM-001_G2-B_P8_DUAL_INDEPENDENT_QA_CONSOLIDATION_2026-11-20.md §4 Hallazgo rector
  limitation: 'Fundamento: EXEC §3 P5 comparado con handoff P5 §2 y posterior P6 readback. No atribuir intenciones, conocimiento
    previo, culpabilidad exclusiva ni renuncia contractual del Owner.'
links:
  recommends: NONE
  adopts: NONE
  authorized_execution_of: NONE
  executed_under: NONE
  verified_by: []
decision:
  value: NONE
  execution_authorized: false
  scope: HISTORICAL_EVENT_DESCRIPTION_ONLY
  exclusions:
  - NOT AN AUTHORIZATION OF THIS ADDITIVE ANNOTATION
  modified_clause: NONE
  rejected_clause: NONE
effect:
  operator: NOT_APPLICABLE
  result: INCONCLUSIVE
  evidence_ref: NONE
classification:
  error_source: PCM-001/GPT (DOCUMENTARY COORDINATION)
  status: DRAFT
  supersedes: NONE
  confidence_note: 'Fundamento: EXEC §3 P5 comparado con handoff P5 §2 y posterior P6 readback. No atribuir intenciones,
    conocimiento previo, culpabilidad exclusiva ni renuncia contractual del Owner.'
```

### CORR-07 — OWNER_DIRECT_DISPOSITION

```yaml
schema_version: PCM-PROVENANCE-R3-DRAFT
record_id: PCM-GOV-PROV-CORR-001-CORR-07
claim_id: CORR-07
event_type: OWNER_DIRECT_DISPOSITION_OF_AGENT_TOPIC
actor:
  human_actor: OWNER
  account_or_agent: KhaosMagnus
  role: issuer
provenance:
  idea_originator: UNKNOWN
  recommender: PCM-001/GPT
  drafter: PCM-001/GPT
  issuer: OWNER
source:
  kind: original_chat_message
  locator: Mensaje Owner «OWNER DECISION — PCM-G2B-P8-P5-DISPOSITION-001», visible localmente; export original no incluido
  sha256: NOT_APPLICABLE
  timestamp: UNKNOWN
  exact_excerpt: ordeno conservarla como no conformidad histórica
  evidence_grade: SECONDARY_ATTRIBUTED
  accessible_to_reviewer: false
  portable_original_attached: false
  local_observation: PRIMARY_OBSERVED LOCAL
claims:
- predicate: OWNER_DIRECT_DISPOSITION
  asserted_value: Tras propuesta GPT, el Owner decidió conservar la desviación P5→P6 como no conformidad histórica y prohibió
    convalidación retroactiva.
  evidence_grade: SECONDARY_ATTRIBUTED
  evidence_locator: Mensaje Owner «OWNER DECISION — PCM-G2B-P8-P5-DISPOSITION-001», visible localmente; export original
    no incluido
  limitation: El paquete contiene solo transcripciones y relatos; no el original exportado. La directiva sí es del Owner,
    mientras que la propuesta de tratamiento fue de GPT.
links:
  recommends: NONE
  adopts: NONE
  authorized_execution_of: NONE
  executed_under: NONE
  verified_by: []
decision:
  value: GRANTED
  execution_authorized: UNKNOWN
  scope: HISTORICAL_EVENT_DESCRIPTION_ONLY
  exclusions:
  - NOT AN AUTHORIZATION OF THIS ADDITIVE ANNOTATION
  modified_clause: NONE
  rejected_clause: NONE
effect:
  operator: NOT_APPLICABLE
  result: OBSERVED
  evidence_ref: NONE
classification:
  error_source: UNKNOWN
  status: DRAFT
  supersedes: NONE
  confidence_note: El paquete contiene solo transcripciones y relatos; no el original exportado. La directiva sí es del
    Owner, mientras que la propuesta de tratamiento fue de GPT.
```

### CORR-08 — OWNER_R3_ACCEPTED

```yaml
schema_version: PCM-PROVENANCE-R3-DRAFT
record_id: PCM-GOV-PROV-CORR-001-CORR-08
claim_id: CORR-08
event_type: OWNER_ADOPTION_OF_RECOMMENDATION
actor:
  human_actor: OWNER
  account_or_agent: KhaosMagnus
  role: decision_maker
provenance:
  idea_originator: UNKNOWN
  recommender: PCM-001/GPT
  drafter: PCM-001/GPT
  issuer: OWNER
source:
  kind: frozen_file
  locator: PCM-GOV-PROV-R3-ACCEPTANCE-001_LOCAL_OWNER_DECISION_RECORD_2026-11-21.md §§1–2 constancia local
  sha256: ac4e43a0d123aaa8c32b35b38699132338e791970237c3194442b57b37b8ac81
  timestamp: UNKNOWN
  exact_excerpt: ACCEPT — LOCAL DOCUMENTARY POLICY ONLY
  evidence_grade: PRIMARY_OBSERVED
  accessible_to_reviewer: true
  portable_original_attached: true
  local_observation: PRIMARY_OBSERVED LOCAL
claims:
- predicate: OWNER_R3_ACCEPTED
  asserted_value: El Owner aceptó R3 para gobierno documental local y prospectivo; no aceptó la enmienda unipersonal ni
    G2-B.
  evidence_grade: SECONDARY_ATTRIBUTED
  evidence_locator: PCM-GOV-PROV-R3-ACCEPTANCE-001_LOCAL_OWNER_DECISION_RECORD_2026-11-21.md §§1–2 constancia local
  limitation: El archivo de constancia es evidencia primaria de su propio texto; secundaria del acto Owner para QA externa
    sin mensaje original. La aceptación R3 no aplica ni acepta este CORR-001.
links:
  recommends: NONE
  adopts: NONE
  authorized_execution_of: NONE
  executed_under: NONE
  verified_by: []
decision:
  value: ACCEPT
  execution_authorized: UNKNOWN
  scope: HISTORICAL_EVENT_DESCRIPTION_ONLY
  exclusions:
  - NOT AN AUTHORIZATION OF THIS ADDITIVE ANNOTATION
  modified_clause: NONE
  rejected_clause: NONE
effect:
  operator: NOT_APPLICABLE
  result: OBSERVED
  evidence_ref: NONE
classification:
  error_source: UNKNOWN
  status: DRAFT
  supersedes: NONE
  confidence_note: El archivo de constancia es evidencia primaria de su propio texto; secundaria del acto Owner para QA
    externa sin mensaje original. La aceptación R3 no aplica ni acepta este CORR-001.
```

## 3. Hallazgo y límites de certeza

**Hallazgo documental positivo:** `EXEC §3 P5` incluía STOP si la ruta de revisor elegible no era demostrablemente viable. El documento `P5 §2` recomendó el avance al push P6 aplazando la verificación del revisor. La diferencia es un **hallazgo basado en comparación**; no prueba intención ni exculpa o imputa culpabilidad exclusiva al Owner. El readback P6 confirma objeto remoto, pero no acredita todas las acciones transitorias ni el número total de intentos.

**Actos del Owner separados:** una instrucción de GPT no equivale a una orden originada por el Owner; su aceptación posterior tiene autoridad formal dentro del alcance emitido. En el paquete de QA externa no se exportan los mensajes originales del Owner: las afirmaciones correspondientes conservan `SECONDARY_ATTRIBUTED`, aunque PCM-001 observe esos mensajes directamente en su conversación.

**Permanencia:** el STOP original, los dos informes P8 `INCONCLUSIVE`, el hallazgo Q6 de elegibilidad de Grok, los SHAs y los commits de las dos raíces permanecen sin cambio. Tampoco cambia el requisito histórico de dos QA PASS ni se acepta la enmienda unipersonal mediante este anexo.

## 4. Integridad, decisión pendiente y aplicación

- El primer borrador `PCM-GOV-PROV-CORR-001` permanece como R1 sin sobrescritura; esta R2 añade una representación atómica verificable y precisión de fuentes.
- La revisión que haga PCM-001 sobre este R2 es **preflight del autor**, no QA independiente. Para contar QA separadas se necesitan evaluaciones sin dependencia de esta recomendación.
- `OWNER DISPOSITION: PENDING` hasta decisión `ACCEPT / REVISE / DEFER` que identifique el SHA exacto de R2, después de la revisión focalizada que el Owner estime pertinente.
- La aceptación documental futura no autoriza escribir en GitHub, actualizar el protocolo general, integrar, adoptar o ejecutar una prueba de primera PR.
- No atribuir al Owner el origen de una recomendación de PCM-001 por el simple hecho de haberla aceptado. No convertir tampoco esa separación en exoneración automática de todo acto decisorio posterior.

**Estado:** `R2 CANDIDATE / OWNER ACCEPTANCE PENDING / G2-B NOT ACCEPTED / UNI NOT ACCEPTED / NO GITHUB WRITES`.
