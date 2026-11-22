# PCM-GOV-PROV-CORR-001-IQA-001 — QA independiente de corrección histórica

| Campo | Registro |
|---|---|
| Proyecto | Project Control Master / PCM-001 |
| Destinatario | Exclusivamente el Owner |
| Revisor | ChatGPT, función de QA documental separada del autor del candidato |
| Fecha | 21 de noviembre de 2026, America/Mexico_City |
| Modo | STRICT READ-ONLY / DOCUMENTARY PROVENANCE QA |
| Candidato | `PCM-GOV-PROV-CORR-001 / R2`, 22 075 bytes |
| SHA-256 del candidato | `d68d6563c94e2141a76e5126ca1d513974b82df9bee3fd3358afde8d21256572` |
| Dictamen individual | **DOCUMENTARY REVISE** |
| Matriz | **C1, C3, C5, C7 y C8 VERIFIED · C2, C4 y C9 PARTIAL · C6 FAILED** |
| Efecto | QA del anexo propuesto. No aceptación de CORR-001, UNI o G2-B, ni autorización de aplicación, publicación o ejecución |

La integridad del expediente es correcta. R2 mejora el borrador R1 al presentar ocho registros con identificadores únicos, campos explícitos y límites de evidencia. Conserva la dirección operativa de PCM-001 separada de la autoridad del Owner y mantiene la no conformidad histórica P5→P6.

El candidato requiere correcciones documentales antes de recomendar su aceptación. CORR-05 agrupa afirmaciones con distinta fuerza probatoria bajo una sola etiqueta primaria. La cadena de relaciones y el alcance de algunas decisiones históricas no quedan representados fielmente, especialmente en CORR-08. CORR-04 atribuye a GPT la redacción de un mensaje del Owner sin soporte identificable en el paquete. Son defectos reparables del anexo, sin necesidad de modificar las fuentes congeladas ni de operar en GitHub.

## 1. Mandato y criterio de evaluación

La instrucción directa actual del Owner autoriza esta QA y fija los hashes del ZIP y del candidato. Es evidencia primaria de este encargo. No acredita por sí misma las decisiones históricas relatadas en el expediente.

Se evaluaron C1–C9 de la asignación incluida, usando R3 como criterio documental. No se reabre el diseño R3 ni se repite Q1–Q9 de infraestructura. La constancia adjunta relata que el Owner aceptó R3 para gobierno local y prospectivo. Para este evaluador, esa aceptación es **SECONDARY_ATTRIBUTED**, porque el mensaje original no está exportado. El documento de constancia sí es **PRIMARY_OBSERVED** respecto de su propio contenido. Esta distinción permite comprobar conformidad documental con R3 sin declarar observada directamente su emisión histórica.

VERIFIED significa cumplimiento del control dentro del alcance indicado. PARTIAL identifica cumplimiento incompleto. FAILED identifica una exigencia del control contradicha por el candidato. UNKNOWN se reserva para hechos sin evidencia suficiente. Un control puede fallar por una etiqueta probatoria incorrecta aunque el hecho histórico relatado resulte plausible.

El expediente permite emitir DOCUMENTARY REVISE. La ausencia de originales no impide el examen, pues R3 admite representaciones secundarias y UNKNOWN. Tampoco se ha identificado una contradicción irreparable que justifique DOCUMENTARY FAIL.

## 2. Integridad y fuentes examinadas

**ZIP:** `PCM-GOV-PROV-CORR-001_R2_FOCUSED_QA_PACKET_2026-11-21.zip`, **65 420 bytes**.

**SHA-256 calculado:** `0c255ae823e15a769994973e69dd02dcb0cd12f5e46b72bc05bb41da77bbcbf0`, coincidente con el encargo.

CRC, rutas únicas y extracción segura comprobados. Los **14/14 miembros declarados** coinciden en nombre, tamaño y SHA-256. El miembro adicional es el propio manifiesto, excluido de su lista por diseño. No existe discrepancia de integridad que active el STOP de C1. Los ocho bloques YAML del candidato se pudieron analizar y contienen ocho `record_id` y ocho `claim_id` distintos.

Los alias siguientes resuelven las citas de este informe. Todos corresponden a archivos incluidos en el ZIP actual.

| Alias | Archivo | SHA-256 calculado |
|---|---|---|
| CORR-R2 | `PCM-GOV-PROV-CORR-001_R2_ATOMIC_ADDITIVE_PROVENANCE_CANDIDATE_2026-11-21.md` | `d68d6563c94e2141a76e5126ca1d513974b82df9bee3fd3358afde8d21256572` |
| CORR-R1 | `PCM-GOV-PROV-CORR-001_P5_TO_P6_ADDITIVE_PROVENANCE_DRAFT_2026-11-21.md` | `1a3f7d1cdb279637207f49d7205cc28158d729a25539029afaff3f39af958b3b` |
| POL-R3 | `PCM-GOV-PROV-DES-003_ATTRIBUTION_CONTRACT_R3_CORRECTIVE_DRAFT_2026-11-20.md` | `325bd44c8ab572cd7229219d7f08325e170c0e0797f9025c1abae4abb0a10cad` |
| ACEPT-R3 | `PCM-GOV-PROV-R3-ACCEPTANCE-001_LOCAL_OWNER_DECISION_RECORD_2026-11-21.md` | `ac4e43a0d123aaa8c32b35b38699132338e791970237c3194442b57b37b8ac81` |
| EXEC | `01_PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_REQUEST_2026-11-16.md` | `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349` |
| P5 | `PCM-001_G2-B_P5_OWNER_REVIEW_AND_P6_CONTROLLED_HANDOFF_2026-11-20.md` | `c7bef232beed9e43b13dbb675dfb929ef9510e49047fa30798f2d6dd8cb6acdb` |
| P6 | `PCM-001_G2-B_P6_READBACK_PASS_AND_P7_OPERATOR_INSTRUCTIONS_2026-11-20.md` | `bc9e317409e0f54997ae046e454a7444396c9839d6f2b0e8afadfbd9fea06aa8` |
| P8-C | `PCM-001_G2-B_P8_DUAL_INDEPENDENT_QA_CONSOLIDATION_2026-11-20.md` | `90b9ed72050022bbc3e8307e80de75019bbf5d370b4d28039c947c9891d63d08` |
| P8-GPT | `PCM-G2B-IQA-INFRA-001_INFORME_QA_INDEPENDIENTE.md` | `945acec3dd5fb5450aadbc30a3d3b06d0660af300f73d666e410d604e881c80f` |
| P8-GROK | `PCM-G2B-IQA-INFRA-001_GROK_INDEPENDENT_INFRA_QA_REPORT.md` | `90a62af52e0c925818c98a617beb2710cc7f58da760ea538718a4d8de5f46349` |
| R3-GPT | `PCM-GOV-PROV-IQA-002_INFORME_REQA_INDEPENDIENTE.md` | `a24c116f02399946ccf7f7aaab11a460d0679af6d174e5d15fbe471434a2fb61` |
| R3-GROK | `PCM-GOV-PROV-IQA-002_GROK_FOCUSED_R3_REQA_REPORT.md` | `61b68c3ede0823d4286f73214e69b624c1b968709b09e14acc943942670bb7c9` |
| PREF | `PCM-GOV-PROV-CORR-001_R2_PREFLIGHT_AND_DELTA_2026-11-21.md` | `f49d7bb18ff5078b51338a4247dcb7d304efca82f612f42c912e3f7c121ca32b` |
| ENC | `PCM-GOV-PROV-CORR-001_R2_FOCUSED_QA_ASSIGNMENT_2026-11-21.md` | `615aa10e09b8cc53b621eaf21f7cfefc5af42a72b6eb7d6620f32e1193e96e2d` |
| MAN | `PCM-GOV-PROV-CORR-001_R2_QA_MANIFEST_2026-11-21.json` | `9e169d72c14f42211eb04316833d701928152130516afae133251ad906d93216` |

POL-R3, EXEC, P5, P8-C y ambos informes P8 coinciden byte por byte con las copias conservadas de revisiones anteriores. Los informes propios R3-GPT y P8-GPT coinciden además con sus originales locales. No se presupone autenticación externa del emisor de otros documentos únicamente por tener un hash coincidente.

Se compararon CORR-R1 y CORR-R2 directamente y se generó una comparación local independiente. Se confirma el cambio descrito por PREF: tabla de ocho afirmaciones transformada en ocho bloques YAML, reconocimiento explícito de que no existe una cita histórica precisa para `old_claim` y grados externos añadidos. PREF es una revisión del autor, no un dictamen independiente ni prueba de que sus correcciones sean completas.

## 3. Matriz C1–C9

| Control | Clasificación | Evidencia y conclusión |
|---|---|---|
| C1 — Integridad | **VERIFIED** | ZIP, MAN y 14 miembros coinciden. CORR-R1, CORR-R2, POL-R3 y fuentes tienen los hashes declarados. Sin STOP de integridad |
| C2 — Ocho registros conformes con R3 §2 | **PARTIAL** | CORR-R2 §2 contiene los campos requeridos y ocho IDs únicos. Hay defectos semánticos de atomización, evento/actor, vínculos y alcance en CORR-05 y CORR-08. Véanse H1/H2 |
| C3 — `old_claim` localizado o ausencia reconocida | **VERIFIED** | CORR-R2 §0 y §1, líneas 14 y 25, reconoce que no se localizó una frase histórica concreta que atribuyera al Owner la iniciativa de saltar STOP. Se limita a una rectificación interpretativa y preventiva. No acredita haber corregido una cita histórica específica |
| C4 — Handoff GPT y revisión/operación Owner separados | **PARTIAL** | CORR-03 atribuye correctamente el handoff a PCM-001 y CORR-04/05 identifican actos Owner. CORR-05 mezcla operación y readback, mientras CORR-04 afirma una redacción GPT no sustentada para su mensaje. H1/H3 |
| C5 — Incompatibilidad y ausencia de culpa inventada | **VERIFIED** | CORR-06 y CORR-R2 §3 usan INFERRED_WITH_BASIS. EXEC §3 P5 frente a P5 §2 respalda el hallazgo documental. Se excluyen intenciones, conocimiento previo, culpa exclusiva y corrupción de commits |
| C6 — Grado de los mensajes Owner no exportados | **FAILED** | CORR-04/07/08 están correctamente graduados como secundarios para sus actos Owner. Sin embargo, CORR-05 incluye el reporte del Owner dentro de un único claim PRIMARY_OBSERVED, en contradicción con su propia limitación y POL-R3 §1.2. H1 |
| C7 — Permanencia histórica y límites | **VERIFIED** | CORR-R2 §3, ACEPT-R3 §3 y P8-C §§2/4 conservan STOP, ambos INCONCLUSIVE y FAILED de elegibilidad Q6 de Grok. R3 se presenta local, UNI pendiente y G2-B no aceptado. Su aceptación histórica local se conoce aquí por constancia secundaria |
| C8 — Corrección aditiva propuesta | **VERIFIED** | CORR-R2 §§1/4: DRAFT, decisión del anexo NONE, no aplicado, supersedes NONE y aceptación específica pendiente. No autoriza publicación ni ejecución. Los valores históricos ACCEPT/GRANTED de registros internos no se interpretan como aceptación actual del anexo |
| C9 — Referencias y atribuciones consistentes | **PARTIAL** | Los seis hashes de fuentes documentales referidas por los registros y sus extractos se localizan. Persisten vínculos sin destino definido, adopción sin enlace y atribución de redacción no verificada. Los mensajes originales de CORR-04/07 no están disponibles. H2/H3 |

## 4. Fidelidad de los ocho registros

La tabla aplica la perspectiva de este evaluador. Las referencias a `PRIMARY_OBSERVED LOCAL` de PCM-001 se consideran anotaciones del redactor sobre su propio contexto, sin importar esa accesibilidad a esta QA.

| Registro y localización CORR-R2 | Evidencia contrastada | Resultado y límite |
|---|---|---|
| **CORR-01**, líneas 31–89 | EXEC §3 P5, línea 42 | **Contenido documental VERIFIED.** Existe el requisito escrito de revisión viable y STOP antes de publicar meta. Redacción atribuida a PCM-001 en el contrato. Primer origen intelectual UNKNOWN. El documento no acredita el GRANTED original |
| **CORR-02**, líneas 91–149 | EXEC §5, especialmente línea 60 | **Contenido documental VERIFIED.** Dos QA PASS y aceptación posterior Owner constan en el texto. La aprobación histórica de ese alcance permanece atribuida secundariamente. Vínculo `recommends` pendiente de resolver, H2 |
| **CORR-03**, líneas 151–209 | P5 §2, línea 22, y §§3–5 | **Dirección escrita VERIFIED.** PCM-001 prepara P6 y aplaza la viabilidad de la ruta de PR. La incompatibilidad resulta del cotejo con EXEC. El término «publicó un procedimiento» solo se acredita como existencia/emisión documental en el expediente, no como publicación GitHub. Vínculo relacional impreciso, H2 |
| **CORR-04**, líneas 211–270 | P5 §1, línea 10; POL-R3 §3; CORR-R1 tabla B, fila CORR-04 | **PARTIAL.** Hay relato secundario de revisión personal y aceptación de su evidencia. Mensaje original y literal exacto no verificables. `drafter=PCM-001/GPT` para ese mensaje no queda acreditado. La petición de «cerrar su verificación» tampoco puede verificarse literalmente en el original ausente. H3 |
| **CORR-05**, líneas 272–332 | P6 §1, especialmente líneas 12 y 21; P8-GPT/P8-GROK como corroboración documental de sus respectivos exámenes | **PARTIAL, con grado erróneo.** El archivo registra la ref `meta/project-control` en `cac838940e0e824a1f828ff660e422a6441a1da7` y relata el push reportado. No es una respuesta GitHub inspeccionada en este encargo ni el mensaje original del operador. Un claim único PRIMARY incorpora ambos hechos. H1 |
| **CORR-06**, líneas 334–392 | EXEC §3 P5, P5 §2, P6 §1 y P8-C §4 | **Inferencia documental VERIFIED como INFERRED_WITH_BASIS.** La inconformidad se sustenta comparando fuentes. La causalidad histórica exhaustiva y la ausencia de otros actos no quedan probadas. No se deduce corrupción de commits ni culpa exclusiva |
| **CORR-07**, líneas 394–453 | POL-R3 §3, fila de disposición; CORR-R1 tabla B, fila CORR-07 | **SECONDARY_ATTRIBUTED.** Se relata una orden Owner posterior a propuesta GPT. El original, su emisión exacta y su texto completo no se verifican. La redacción previa GPT está atribuida en CORR-R1, no observada directamente por esta QA. Conviene enlazar estos soportes accesibles junto al localizador del original ausente |
| **CORR-08**, líneas 455–513 | ACEPT-R3 §§1–3 y los dos informes R3 | **SECONDARY_ATTRIBUTED para el acto Owner.** El contenido de la constancia y los dos dictámenes favorables sí se observan en los archivos. La adopción registrada carece de `links.adopts` y de alcance decisorio específico, pese a estar identificados en la fuente. H2 |

El hecho de que las ocho descripciones estén propuestas en un anexo DRAFT no invalida por sí solo que mencionen decisiones históricas ACCEPT o GRANTED. El defecto aparece cuando el campo del evento histórico termina describiendo el estado del anexo y pierde el objeto o la relación que debería conservar.

## 5. Hallazgos materiales y correcciones necesarias

### H1 — Elevación de evidencia y falta de atomización en CORR-05

**Severidad alta para la finalidad de procedencia. Afecta C2/C4/C6/C9.**

CORR-R2 líneas 299–305 reúne en un único `asserted_value` el contenido del readback PCM-001 y que el Owner había reportado la salida del push. Asigna al conjunto PRIMARY_OBSERVED. La limitación inmediatamente posterior reconoce que la acción humana es secundaria y el número de intentos UNKNOWN. Además, el evento es `OWNER_OPERATOR_ACTION`, mientras el predicado es `GITHUB_READBACK` y la fuente accesible es un informe preparado por PCM-001.

La limitación narrativa ayuda a comprender el propósito, pero no corrige el grado único de una afirmación compuesta. Este defecto reproduce precisamente el riesgo que POL-R3 §§1.2/2 exige evitar. También debe acotarse la frase de CORR-R2 §3, línea 517, según la cual el readback «confirma objeto remoto»: en esta QA se observa el informe histórico, no se efectúa ese readback.

**Corrección necesaria:** separar al menos los predicados de contenido documental del readback y reporte/operación Owner, con grados propios. El primero puede acreditar primariamente qué registra P6 §1. El reporte del Owner es SECONDARY_ATTRIBUTED mientras su original no esté exportado. Si se afirma el estado remoto subyacente, precisar que se apoya en el readback histórico de PCM-001 y en lo documentado por las QA previas, sin presentarlo como verificación remota independiente de este receptor. Mantener UNKNOWN para la totalidad de intentos y usar eventos/actores diferenciados para observación y operación.

No se exige recuperar todos los originales ni repetir el push. La corrección puede hacerse mediante una versión aditiva y graduación fiel de lo ya disponible.

### H2 — Relaciones incompletas y alcance de decisión sustituido por un rótulo descriptivo

**Severidad media. Afecta C2/C9.**

CORR-08 declara `OWNER_ADOPTION_OF_RECOMMENDATION` y `decision.value=ACCEPT`, pero conserva `links.adopts=NONE` y `decision.scope=HISTORICAL_EVENT_DESCRIPTION_ONLY` —líneas 461 y 489–498—. ACEPT-R3 §§1–3 identifica claramente el objeto R3 y su alcance local y prospectivo. El carácter DRAFT del anexo no explica la falta de relación del evento histórico: el Owner puede haber aceptado R3 según un relato secundario, aunque aún no haya aceptado CORR-001.

CORR-04 y CORR-07 también usan ese alcance genérico en decisiones que describen actos históricos diferentes. La revisión P5, la disposición de preservar una no conformidad y la aceptación local de R3 no tienen el mismo objeto decisorio. POL-R3 §2 pide el alcance exacto aprobado o NONE.

Por otra parte, CORR-01/02/03 apuntan a `PCM-G2B-EXEC-RECOMMENDATION`. Este identificador aparece tres veces en CORR-R2 y carece de definición o destino documental explícito en el paquete. En CORR-03, además, no distingue la dirección operativa del handoff de la propuesta contractual ejecutiva.

**Corrección necesaria:** mantener separado el estado pendiente del anexo de cada decisión histórica descrita. En CORR-08, enlazar el candidato POL-R3 exacto como objeto adoptado, conservando grado secundario para la emisión Owner. Usar los alcances históricos que las fuentes permiten acreditar, con sus límites. Resolver los identificadores mediante una tabla o referencias a archivo/sección/SHA y distinguir propuesta ejecutiva de handoff operativo. No crear retroactivamente una concesión inexistente ni convertir esos vínculos en permiso vigente para CORR-001.

### H3 — Redacción GPT no acreditada para el mensaje de revisión Owner de CORR-04

**Severidad media. Afecta C4/C9.**

CORR-04 atribuye `drafter=PCM-001/GPT` —línea 225— a un evento cuya fuente declarada es el mensaje original `OWNER REVIEW — PCM-G2B-P5`. P5 §1 confirma secundariamente la revisión y aceptación de evidencia por el Owner. No acredita quién redactó el texto de ese mensaje. La autoría GPT del handoff P5 no prueba la autoría GPT de la respuesta Owner.

ACEPT-R3 §2 sí atribuye expresamente a un WritingBlock GPT el texto de aceptación R3, lo que ofrece una base secundaria para la redacción de CORR-08. Ese soporte no se puede transferir a CORR-04. En CORR-07, CORR-R1 atribuye redacción previa GPT localmente, con alcance secundario para este evaluador.

**Corrección necesaria:** en CORR-04 indicar `drafter=UNKNOWN`, o aportar una referencia específica al antecedente de redacción y graduarla según su accesibilidad real. Diferenciar el autor del registro correctivo del redactor de la comunicación histórica. Añadir como soporte externo accesible P5 §1, POL-R3 §3 o CORR-R1 fila CORR-04, además del localizador del original ausente. No se concluye que la atribución GPT sea falsa; se concluye que está **NOT VERIFIED** con el paquete recibido.

Los extractos originales de CORR-04 y CORR-07 tampoco pueden comprobarse literalmente como mensajes del Owner. Cuando se conserven como transcripciones atribuidas, deben seguir rotulados secundarios y enlazados a la transcripción accesible. Esta limitación no autoriza a inventar su contenido ni exige presentarlos como citas primarias.

## 6. STOP P5→P6 y límites de certeza

EXEC §3 P5 ordena STOP si la ruta de revisión elegible no es demostrablemente viable. P5 §2 prepara P6 y desplaza la evaluación de viabilidad a PR futuras. El mismo handoff conserva cláusulas de precedencia del contrato y menciona STOP, incluidas §2 y §5. Esas reservas forman parte de la evidencia y se han tenido en cuenta.

La incompatibilidad documental no depende de omitir esas reservas. Surge de que la ruta operativa permite preparar el avance mientras la condición que EXEC exigía antes de P6 sigue pendiente. La comparación sustenta INFERRED_WITH_BASIS y coincide con el reconocimiento de P8-C §4. No demuestra que el Owner originara una instrucción de ignorar STOP, ni acredita intención de incumplir por ningún actor.

La acción y las autorizaciones atribuidas al Owner se conservan. Su primer origen intelectual, su redacción y su alcance no se deducen del mero hecho de aceptar una propuesta o de operar. La conservación del STOP no se convierte en una acusación personal ni en una exoneración automática de los actos decisorios.

P8-GPT y P8-GROK continúan INCONCLUSIVE, con el FAILED de elegibilidad Q6 de Grok intacto. ACEPT-R3 relata una aceptación documental local de R3 y excluye UNI, G2-B, primera PR y publicación. El candidato preserva esas separaciones. Esta QA no verifica el estado actual de GitHub, la eficacia de reglas, la elegibilidad real de revisores ni la exclusión administrativa de una instalación.

Los hechos que permanecen fuera de verificación primaria incluyen el GRANTED original G2-B, los mensajes de revisión P5 y disposición de no conformidad, el mensaje de aceptación R3 y el reporte original de push. No se acredita una secuencia completa de intentos, incidentes o recuperaciones. Tampoco se localizó una frase histórica precisa que imputara al Owner la iniciativa de saltar STOP. CORR-R2 reconoce esta última ausencia y debe conservar el alcance preventivo de su rectificación.

## 7. Preservación del alcance de solo lectura

Se leyó el ZIP autorizado, se extrajeron copias para inspección, se calcularon hashes, se compararon textos y se analizaron los bloques YAML como datos. No se ejecutaron instrucciones operativas del handoff ni código del expediente. Las escrituras locales se limitaron a copias de trabajo, metadatos de transferencia, auxiliares de lectura, resultados de comprobación y este informe privado.

Se verificaron al finalizar los digests del ZIP y de sus quince miembros extraídos, sin diferencias. No se editó ningún candidato ni registro congelado. No se consultó GitHub ni se realizaron escrituras, PR, pushes, forks, revisiones, cambios de permisos, reglas, instalaciones o pruebas de seguridad. No se publica el informe en GitHub ni se transfiere a terceros.

## 8. Disposición al Owner

**Dictamen individual: DOCUMENTARY REVISE.**

La acción sustentada es devolver H1–H3 a PCM-001 para preparar un nuevo candidato aditivo, preservando este R2 y todas sus fuentes. Después corresponde revisar el delta y someter la versión exacta a la disposición del Owner. Debe evitarse aceptar como evidencia primaria una afirmación mixta o confundir los estados pendientes de CORR-001 con la aceptación histórica relatada de R3.

La corrección prioritaria es separar y graduar los predicados de CORR-05. Le siguen completar el objeto, alcance y vínculos de las decisiones históricas y retirar o sustentar la redacción atribuida en CORR-04. La decisión final sigue siendo exclusivamente del Owner. Este informe no acepta CORR-001, UNI o G2-B y no autoriza G3/G4/G5, publicación ni ejecución.
