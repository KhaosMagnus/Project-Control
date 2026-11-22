# PCM-GOV-PROV-IQA-001 — QA independiente de procedencia

| Campo | Registro |
|---|---|
| Proyecto | Project Control Master / PCM-001 |
| Revisor | ChatGPT, evaluación documental independiente del redactor del candidato |
| Destinatario | Exclusivamente el Owner, para transferencia a PCM-001 |
| Fecha | 20 de noviembre de 2026, Ciudad de México, UTC−06:00 |
| Mandato | GRANTED QA ONLY. STRICT READ-ONLY / FOCUSED DOCUMENTARY DESIGN QA |
| Candidato | `PCM-GOV-PROV-DES-002 / R2`, 18 627 bytes |
| SHA-256 del candidato | `1391ca809bddaae1a2f6907ca1b9845dca616ee5a391bb7a1a8cef0a028b8375` |
| Dictamen | **DESIGN REVISE** |
| Efecto | R2 pendiente de aceptación. Enmienda unipersonal y G2-B pendientes en las fuentes examinadas. Sin autorización de publicación ni ejecución |

R2 distingue correctamente origen de idea, recomendación, redacción, emisión, decisión y operación. Conserva la iniciativa de las recomendaciones de PCM-001 y la autoridad decisoria del Owner sin convertir una en la otra. El caso P5→P6 mantiene visibles el STOP contractual y la dirección operativa incompatible emitida por PCM-001.

El dictamen requiere dos correcciones documentales. El formato obligatorio carece de una representación explícita de rechazo para el caso mixto exigido por A4. La matriz histórica aplica etiquetas concluyentes a actos del Owner cuyos mensajes originales están ausentes, sin adjuntar a cada afirmación su grado de evidencia. La segunda brecha afecta A6, A7 y A9. Puede corregirse con las fuentes disponibles y etiquetas fieles a su alcance. La carencia del original, por sí sola, no obliga a detener la elaboración del diseño.

La integridad se verificó a las **18:54:44−06:00**. El ZIP `PCM-GOV-PROV-IQA-001_SHARED_REVIEW_PACKET_2026-11-20.zip` tiene **54 498 bytes** y SHA-256 `b7f98ed527b84cae73c8904c4348572709d914a3aedab32e2838fc91e60233fe`, idéntico al proporcionado por el Owner. CRC, unicidad de rutas y lectura UTF-8 válidos en **12/12 miembros**. Tamaños, pertenencia y SHA-256 válidos en **11/11 miembros declarados**. El manifiesto JSON es el miembro adicional y su digest observado es `c3a68ee7a097c4fb133d7979c2b859a71f64eacea8ac1d1ae5ce06bb601bb750`. El candidato coincide con su digest autorizado. Se cotejaron seis fuentes históricas byte por byte con las copias verificadas en encargos previos, incluido el informe P8 de este revisor.

Para las citas se usan los siguientes alias, todos resueltos a archivos íntegros del ZIP.

| Alias | Archivo y SHA-256 |
|---|---|
| R2 | `PCM-GOV-PROV-DES-002_ATTRIBUTION_CONTRACT_R2_2026-11-20.md`. `1391ca809bddaae1a2f6907ca1b9845dca616ee5a391bb7a1a8cef0a028b8375` |
| R1 | `PCM-001_ATTRIBUTION_OF_AGENT_RECOMMENDATIONS_AND_OWNER_DECISIONS_DRAFT_2026-11-20.md`. `77ad35f25c2be2dbb265f2a38ad6dac465e11960f8fb5f1f80cca18f02a6f8fd` |
| EXEC | `01_PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_REQUEST_2026-11-16.md`. `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349` |
| P5 | `PCM-001_G2-B_P5_OWNER_REVIEW_AND_P6_CONTROLLED_HANDOFF_2026-11-20.md`. `c7bef232beed9e43b13dbb675dfb929ef9510e49047fa30798f2d6dd8cb6acdb` |
| UNI | `PCM-001_G2-B_P8_UNIPERSONAL_AUTHORITY_AND_REVIEW_AMENDMENT_DRAFT_2026-11-20.md`. `410c12a8f2f46ac20322a6ec76d76e038c9b7979a565044d6db8ee5cec29ca76` |
| UNI-C | `PCM-001_G2-B_P8_UNI_DUAL_FOCUSED_QA_CONSOLIDATION_AND_OWNER_DECISION_2026-11-20.md`. `c97d1e9b6483eba84deef1a8ef0fb2881c3e1ea18d75838bce8a78b4275ca24b` |
| P8-C | `PCM-001_G2-B_P8_DUAL_INDEPENDENT_QA_CONSOLIDATION_2026-11-20.md`. `90b9ed72050022bbc3e8307e80de75019bbf5d370b4d28039c947c9891d63d08` |

La matriz siguiente evalúa el diseño y la aplicación piloto suministrada. VERIFIED acredita el criterio en ese alcance. PARTIAL identifica una corrección implementada de forma incompleta. La fuerza de cada afirmación histórica se precisa después de la matriz.

| Control | Clasificación | Evidencia y conclusión |
|---|---|---|
| **A1 — Dimensiones de atribución** | **VERIFIED** | R2 §1, líneas 23–41. Distingue `issuer`, `drafter`, `recommender`, `idea_originator` y `decision_maker`. El autor de una idea puede diferir del emisor de una decisión y del operador |
| **A2 — Texto LLM emitido por el Owner** | **VERIFIED** | R2, reglas R2 y R5, líneas 38 y 41; §4, línea 126. Exige doble procedencia y un acto efectivo del Owner antes de registrar adopción. UNI-C §5, líneas 65–69, ofrece un caso comprobable de texto propuesto que aún carece de eficacia |
| **A3 — Mandato propio del Owner** | **VERIFIED** como regla de diseño | R2 R0 y §1.1, líneas 17 y 47. Preserva el mandato propio y permite distinguirlo de una disposición directa sobre un tema sugerido por un agente. La prioridad de autoridad del Owner está reiterada directamente en el encargo actual. La primera emisión histórica exige su fuente específica según A9 |
| **A4 — Acepta A, modifica B, rechaza C** | **PARTIAL** | R2 R3 y §2, líneas 39, 57, 87–89 y 101, exigen unidades por cláusula. Sin embargo, los valores de decisión omiten rechazo y no definen cómo representarlo fielmente. Véase F1 |
| **A5 — Dirección incompatible P5→P6** | **VERIFIED** en atribución documental | EXEC §3 P5 impone STOP. P5 §2, línea 22, prepara P6 y difiere la viabilidad de revisión. R2 §3, líneas 109–112, atribuye esa dirección a PCM-001 y conserva separadamente la revisión/operación reportada del Owner. No hay fuente primaria aportada de una orden del Owner de ignorar el STOP |
| **A6 — Disposición de preservar la no conformidad** | **PARTIAL** | R2 §1.1 y §3, línea 112, modela correctamente una decisión Owner con antecedente GPT. La orden original no está adjunta y la fila piloto no rotula la decisión atribuida como secundaria ni enlaza la fuente de la propuesta y la de la emisión por separado. Véase F2 |
| **A7 — Gate de dos QA PASS** | **PARTIAL** | EXEC §5, línea 60, prueba que el texto propone ese criterio. R2 §3, línea 113, distingue redacción y posterior autoridad y preserva su vigencia histórica. La adopción por el Owner se conoce por relatos del expediente, sin el GRANTED original. Falta calificar esa parte de la cadena. Véase F2 |
| **A8 — Enmienda unipersonal pendiente** | **VERIFIED** | R2 §3, líneas 114 y 120, y §6.3; UNI-C §§5–6. La conciliación propone ACCEPT y declara expresamente que aún no es una decisión emitida. Los dos QA favorables reportados no se convierten en aceptación |
| **A9 — Graduación de evidencia y UNKNOWN** | **PARTIAL** | R2 §1.2 y §2, líneas 53 y 101, establecen una regla adecuada y §6.2 reconoce originales faltantes. La tabla piloto de §3 y la afirmación histórica de R0 no aplican esa graduación individualmente. Véase F2 |
| **A10 — Error, autorización, operación y disposición** | **VERIFIED** | R2 §2, línea 103; §4, líneas 128–132. Separa el defecto de recomendación del grant, operación, resultado y disposición. Prohíbe inferir culpabilidad exclusiva, exoneración e intenciones. La contradicción textual de la guía respalda un hallazgo de conducción, con causalidad histórica limitada a la evidencia |
| **A11 — Inmutabilidad y corrección aditiva** | **VERIFIED** | R2 §3, línea 120; §4, líneas 132–134; §6.4. Conserva STOP, hashes y ambos P8 INCONCLUSIVE. La corrección crea otro registro y la eficacia normativa es prospectiva |
| **A12 — Autoridades y etapas** | **VERIFIED** | R2 §1, líneas 29–32; §4 y §6; tabla de gates G1–G5 del plan de adopción. Distingue preparación, QA, aceptación local, autorización operativa, publicación y adopción. La petición actual solo concede QA |

**F1, severidad media.** El caso A4 contiene una decisión negativa real. La lista obligatoria de `decision.value` en R2 §2 admite GRANTED, ACCEPT, REVISE, DEFER y NONE. Registrar un rechazo como NONE perdería el hecho de que hubo una decisión. DEFER lo convertiría en aplazamiento y REVISE en petición de cambio. Una exclusión en el evento de aceptación de A puede limitar su alcance, pero el propio diseño exige una unidad autónoma para C.

La corrección necesaria es añadir una representación explícita de rechazo, por ejemplo REJECT, o documentar una codificación equivalente sin pérdida. Incluir el recorrido mínimo de A4 con tres unidades enlazadas al mismo mensaje. A conserva el origen de la propuesta y la aceptación Owner. B registra la cláusula modificada atribuible al Owner y la decisión sobre su versión exacta. C registra rechazo y ausencia de autorización para ese alcance. Este ejercicio documental no requiere implementación o prueba en GitHub.

**F2, severidad alta para la finalidad del contrato.** R2 reconoce que faltan mensajes originales y exige rótulos secundarios para transcripciones. Sin embargo, §3 usa expresiones como «Owner ordenó» o «Quedó incluido en el G2-B autorizado» sin grado de evidencia ni referencia propia de la decisión en esas filas. R0 también declara un origen histórico categórico. La instrucción actual del Owner sí es fuente primaria de su mandato actual. Los mensajes anteriores y su primera formulación se conocen aquí a través de documentos de PCM-001.

La corrección necesaria es aplicar el esquema a la propia auditoría piloto. Por cada afirmación, indicar cláusula, fuente concreta, autor de esa fuente, grado y límite. Un documento congelado puede ser evidencia primaria del texto que PCM-001 puso por escrito y simultáneamente evidencia secundaria de una decisión Owner que ese documento relata. Su hash preserva los bytes de ambas afirmaciones, con distinto valor probatorio.

Para las filas sobre GRANTED, revisión personal, ejecución reportada y orden de preservar la desviación, usar SECONDARY_ATTRIBUTED respecto del hecho conversacional mientras falte el original, con referencia al relato disponible. Para el origen intelectual anterior a la primera propuesta acreditada, mantener UNKNOWN. Conservar R0 como mandato de autoridad del Owner y vincular cada afirmación de su procedencia temporal a la fuente efectivamente disponible. El cierre documental puede lograrse así sin exigir recuperar todos los mensajes históricos como condición de diseño.

Este es el alcance de evidencia que aplico al caso P5→P6.

| Afirmación | Evidencia accesible | Calificación de esta QA |
|---|---|---|
| EXEC contiene el STOP P5 y la condición de dos QA PASS | Texto congelado EXEC §§3 y 5, preparado bajo el rótulo PCM-001 | **Primaria observada para el contenido contractual propuesto y su atribución documental**. La frase Prepared by no demuestra el origen intelectual anterior |
| PCM-001 proporcionó una guía que preparaba P6 con la viabilidad de revisión aún pendiente | P5 §2, especialmente línea 22, y §4 | **Primaria observada para esa dirección escrita**. Su contraste con EXEC respalda la inferencia de incompatibilidad procedimental |
| El Owner concedió G2-B, revisó los controles y ejecutó P6 | P5, P8-C y los informes P8 relatan esos actos | **Secundaria atribuida** para las intervenciones y actuaciones originales. No se aportan aquí su mensaje y salida de operación como fuentes primarias |
| El Owner ordenó conservar la no conformidad después de una propuesta GPT | R1 §3, R2 §3 y P8-C §4 recogen propuesta y disposición atribuida | Propuesta de PCM-001 **observable en el documento**. Emisión original de la disposición Owner **secundaria atribuida**. La redacción entre comillas de R1 sigue siendo una transcripción atribuida para este revisor |
| El Owner originó la idea de saltarse el STOP | Ningún mensaje original del Owner aportado sostiene esa iniciativa | **No acreditado**. No se imputa ese origen al Owner. La evidencia disponible sitúa la dirección operativa en el handoff de PCM-001 |
| Hubo una cadena intelectual anterior a la primera cláusula de revisión o al gate de dos QA PASS | El expediente carece de esa secuencia original completa | **UNKNOWN**. La presencia de ambos requisitos en la propuesta de PCM-001 no identifica por sí sola al primer originador absoluto |
| La enmienda unipersonal o R2 ya están aceptadas | Los textos ofrecen propuestas y conservan aceptación pendiente | No se acredita aceptación. **El GRANTED QA ONLY actual habilita esta revisión** y mantiene reservada la decisión final del Owner |

R2 permite registrar una recomendación aceptada y su autoridad sin transferir al Owner la iniciativa intelectual. Ese principio también impide desplazar de forma automática toda responsabilidad al agente. El acto de decidir y la actuación del operador deben conservarse con su evidencia y alcance. El hallazgo de esta QA se limita a una instrucción escrita incompatible con el contrato y a una clasificación de procedencia incompleta. No atribuye intenciones, culpa exclusiva o conocimiento previo a ningún actor.

La propuesta de decisión en el plan de adopción, líneas 39–43, es texto de PCM-001 hasta que el Owner lo emita o adopte. El encargo directo actual es una decisión efectiva de QA por su objeto y hashes. La ausencia del mensaje original histórico no se sustituye con esa autorización presente ni con la firma de un resumen. Tampoco la aceptación futura de una corrección de procedencia cambiaría el resultado histórico P8.

Los riesgos residuales principales son la propagación de una atribución repetida entre varios resúmenes sin fuente independiente, la pérdida del alcance negativo de una decisión y la lectura de un hash como prueba de iniciativa intelectual. Los campos y vínculos propuestos reducen esos riesgos si se aplican por afirmación y cláusula. La historia P5→P6 y los pendientes Q5/Q7/Q8/Q9 de G2-B siguen requiriendo su tratamiento propio. Este encargo no actualiza su clasificación.

La acción mejor sustentada es devolver **DESIGN REVISE** a PCM-001 para una versión aditiva que incorpore F1 y F2, mantenga R2 congelado y someta el delta al Owner. Después corresponde la conciliación de las QA y una decisión específica sobre la versión revisada. La publicación y cualquier adopción por el protocolo portable requieren sus actos separados.

Leí el ZIP autorizado y las fuentes documentales aportadas, recalculé hashes y cotejé copias históricas locales. No consulté GitHub, no alteré documentos congelados y no publiqué contenido. La única creación destinada al usuario es este informe exclusivo al Owner. Las comprobaciones locales fueron de integridad y consistencia documental. La atestación cubre las operaciones realizadas en esta revisión.

**Dictamen individual — DESIGN REVISE. A4, A6, A7 y A9 PARTIAL. Los otros ocho controles VERIFIED en el alcance documental definido.**
