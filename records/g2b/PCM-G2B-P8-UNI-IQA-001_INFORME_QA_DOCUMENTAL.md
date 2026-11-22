# PCM-G2B-P8-UNI-IQA-001 — QA documental del modelo unipersonal

| Campo | Registro |
|---|---|
| Proyecto | Project Control Master / PCM-001 |
| Revisor | ChatGPT, evaluación documental independiente del redactor de la enmienda |
| Destinatario | Owner, para transferencia a PCM-001 |
| Fecha | 20 de noviembre de 2026, Ciudad de México (UTC−06:00) |
| Mandato | STRICT READ-ONLY / DOCUMENTARY DESIGN QA, controles U1–U8 |
| Candidato | `PCM-G2B-P8-UNI-DES-001`, 16 020 bytes |
| SHA-256 del candidato | `410c12a8f2f46ac20322a6ec76d76e038c9b7979a565044d6db8ee5cec29ca76` |
| Veredicto | **DESIGN PASS (CONDITIONAL)** |
| Efecto actual | Enmienda pendiente de aceptación del Owner. G2-B sigue sin aceptación integral. G3/G4/G5 diferidos |

La enmienda satisface U1–U8 como diseño documental. Reserva al Owner la revisión humana y la aceptación final, reconoce que sus dos cuentas representan una sola persona y conserva la aprobación técnica de PR como un control separado, sujeto a elegibilidad efectiva. Mantiene expresamente la desviación histórica P5→P6 y los dos resultados P8 INCONCLUSIVE. No identifico un defecto documental material que requiera otra versión antes de la decisión del Owner.

El PASS está condicionado a la aceptación expresa de esta versión por el Owner y a los gates de evidencia y operación que el propio candidato conserva. **La viabilidad de autoría, fork, revisión y contabilización de aprobaciones permanece NOT TESTED.** El resultado tampoco resuelve por sí mismo la aceptación integral de G2-B bajo su contrato histórico.

| Evidencia | Clase | Método, fecha y resultado |
|---|---|---|
| Paquete recibido `PCM-001_G2-B_P8_UNIPERSONAL_FOCUSED_QA_SHARED_PACKET_2026-11-20.zip` | **OBSERVED** | SHA-256 `373465c55c703bfda95f5985ba70b7059e87e31ae1ad90ecffced5a437bc4ab8`, idéntico al aportado por el Owner. Tamaño 43 260 bytes. A las **13:08:57−06:00**, CRC y lectura UTF-8 en 10/10 miembros, nombres únicos, conjunto exacto y tamaños/SHA-256 de 9/9 miembros declarados |
| Manifiesto | **OBSERVED** | SHA-256 del miembro adicional `e0ad951700338fae834f4afc91c0b6c170ea7dc536079612a1d2e906e18e269f` |
| Fuentes originales del expediente | **OBSERVED / SOURCE CONTRACT** | Siete hashes citados en la enmienda coinciden con los documentos incluidos. Solicitud ejecutiva, runbook, contrato Q1–Q9 y R5 coinciden byte por byte con el expediente P8 previo. El informe P8 ChatGPT coincide con el ya emitido y conservado |
| Habilitación de diseño | **SOURCE CONTRACT** | Candidato líneas 7–8 y manifiesto líneas 5 y 23 atribuyen al Owner `PCM-G2B-P8-P5-DISPOSITION-001 — GRANTED DESIGN ONLY — OPTION B`. El mensaje directo del Owner en este encargo confirma ese alcance y autoriza esta QA. El texto original completo de esa disposición no está incluido como miembro separado |
| Rulesets `R-MAIN` y `R-META` | **OBSERVED** | GET durante esta revisión. IDs `27709862` y `27717600`, selectores exactos por rama, ACTIVE, PR con una aprobación, squash/rebase, historial lineal, borrado y non-fast-forward restringidos, bypass vacío. En ambos, `require_extra_approval_for_unattributed_changes=true` |
| Circuito de primera PR | **PROPOSED** | La enmienda §3 fija una ruta que requiere autorización y prueba posteriores. No se creó fork, rama, PR o revisión |
| Plausibilidad del circuito | **INFERENCE** | La documentación oficial contempla PR desde forks y revisores distintos de la cuenta autora. Su combinación es compatible con la propuesta en términos generales. La contabilización y elegibilidad concretas del maestro siguen pendientes |

La integridad preserva estas identidades de origen.

| Fuente | SHA-256 |
|---|---|
| Contrato ejecutivo G2-B | `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349` |
| Runbook P0–P8 | `be382147d5ce5b9875625cd8436d4ed31c2bcc9ee93da79a068bad8b50c66b78` |
| Contrato de QA Q1–Q9 | `a1c10a91bc0947e3a84d4c8d48da404c7494f45154e8613c0a65bdd07b6633b3` |
| Corrección R5 | `9c329b3c4be0dca6cf60bc27e92bd586a931c9236bd786f402ce508f952562e8` |
| Conciliación P8 | `90b9ed72050022bbc3e8307e80de75019bbf5d370b4d28039c947c9891d63d08` |
| QA1 P8 ChatGPT | `945acec3dd5fb5450aadbc30a3d3b06d0660af300f73d666e410d604e881c80f` |
| QA2 P8 Grok | `90a62af52e0c925818c98a617beb2710cc7f58da760ea538718a4d8de5f46349` |

En la matriz siguiente, **VERIFIED** acredita que el requisito está especificado y es coherente en el diseño revisado. Las pruebas operativas conservan sus estados pendientes.

| Control | Clasificación | Evidencia puntual y conclusión |
|---|---|---|
| **U1 — Autoridad del Owner** | **VERIFIED** | Enmienda §0, líneas 12 y 20–23; §2, líneas 47 y 51; §3, pasos 5 y 8. El Owner conserva revisión humana, autorización y aceptación. `Approve` GitHub depende de su cuenta elegible y del PR concreto. El modelo permite que una persona desempeñe las funciones con actos y evidencia diferenciados |
| **U2 — Cuentas y personas** | **VERIFIED** | §2, líneas 43–53; §3, líneas 57–60 y 68. Declara que KhaosMagnus y JormungandrMagnus pertenecen al mismo Owner. Se propone autoría de PR con la segunda cuenta y aprobación con la primera, sujeta a validación de GitHub. La propuesta no acredita independencia humana ni elegibilidad en vivo |
| **U3 — QA documental** | **VERIFIED** | §0, línea 23; §2, línea 50; §3, paso 4; §5, paso 1. Revisores separados reciben el mismo candidato congelado y devuelven dictámenes propios. La QA de modelos conserva su función de inspección de artefactos y el Owner su decisión humana |
| **U4 — Procedimiento de PR e integración** | **VERIFIED** | §3, pasos 1–8 y STOP; R5 §§2.1–2.2 como fuente conservada. Mantiene linaje de destino, `B/H/D/T_expected`, método, revisión, revalidación por cambio material, autorización de integración y lectura posterior de `C`, árbol y delta. La aceptación del resultado es posterior y separada |
| **U5 — Reglas, Copilot y pruebas pendientes** | **VERIFIED** | §3, líneas 57, 60, 64, 68 y 70; §4.2, línea 85. La configuración actual de una aprobación y el parámetro adicional se corroboraron por GET. Copilot sin atribución humana queda fuera de esta ruta. Fork, elegibilidad y contabilización quedan NOT TESTED/DEFERRED |
| **U6 — Desviación histórica P5→P6** | **VERIFIED** | §0, línea 14; §4.1, línea 78; §4.2, línea 87; §4.3, líneas 89–95. Reconoce que P6 avanzó sin acreditar la condición literal entonces vigente. Conserva la no conformidad y atribuye la conducción a PCM-001. Los informes P8 y el FAILED de elegibilidad de Grok se preservan. Aceptar un método prospectivo no cura ese hecho histórico |
| **U7 — Precedencia y límites** | **VERIFIED** | §1, líneas 27–39; §5, líneas 99–105. Propone eficacia solo tras aceptación expresa, limitada a identidad humana, revisión, P5 y Q6 prospectivos. Preserva fuentes, raíces, bytes y SHAs, protección, separación de ramas y autoridad de adopción. El protocolo genérico queda fuera del cambio |
| **U8 — Nuevas decisiones y G2-B pendiente** | **VERIFIED** | §5, pasos 1–5. Separa QA, aceptación de la enmienda y prueba autorizada de primera PR. Conserva Q5/Q7/Q8/Q9 pendientes y la puerta histórica de dos QA PASS más aceptación del Owner. Cualquier cambio a esa puerta requiere una decisión explícita adicional |

La propuesta modifica de forma expresa el criterio escrito de P5. El contrato ejecutivo original, §3 P5 y §4, condicionó avanzar a P6 a una ruta de revisión independiente demostrablemente viable. La enmienda §4.1 permite, prospectivamente, cerrar la configuración de génesis con un diseño propuesto y comprobar el circuito real en el gate de primera PR. Este desplazamiento de la prueba exige la aceptación contractual que el candidato reserva al Owner. Los dos dictámenes P8 previos siguen INCONCLUSIVE frente al contrato de su fecha, aun si se acepta esta nueva regla.

La declaración de error de interpretación de PCM-001 es una atribución documental del candidato, respaldada por su conciliación. La exigencia escrita en el contrato histórico tenía eficacia para la transición ejecutada. Su modificación hacia un esquema de autogobierno con revisión del mismo Owner es una decisión legítimamente reservada al Owner y con menor separación humana de funciones. El diseño hace visible ese coste y conserva el registro de la desviación.

La regla técnica de GitHub exige distinguir al autor del PR de quien aprueba, y la aprobación debe ser elegible para contar hacia la protección. El circuito propuesto puede evaluarse posteriormente con autoría de JormungandrMagnus, rama fuente propia del mismo linaje y revisión desde KhaosMagnus. El mero acceso público de una cuenta o un error 403 en una consulta de permisos sigue siendo insuficiente para certificar esa ruta. La revisión actual verifica el contrato de comprobación y sus STOP. [GitHub Docs — revisión y aprobación de PR](https://docs.github.com/en/pull-requests/how-tos/review-pull-requests/reviewing-proposed-changes-in-a-pull-request) · [GitHub Docs — PR desde fork](https://docs.github.com/en/pull-requests/how-tos/create-pull-requests/creating-a-pull-request-from-a-fork)

El parámetro `require_extra_approval_for_unattributed_changes` exige una aprobación adicional cuando Copilot abre un PR sin colaborador humano y ya se requiere un número de aprobaciones distinto de cero. En los perfiles observados ese valor es true y el mínimo es uno. La exclusión de esa ruta en el candidato evita prometer que la única revisión del Owner bastará para ese caso. GitHub también restringe la aprobación por la persona que encargó a Copilot el PR. El gate futuro deberá identificar la autoría y todas las condiciones que efectivamente apliquen. [GitHub Docs — parámetros de rulesets](https://docs.github.com/en/rest/repos/rules) · [GitHub Docs — controles del agente Copilot](https://docs.github.com/en/copilot/concepts/security-governance-and-network-settings/risks-and-mitigations)

Fuentes de configuración leídas en esta QA. [R-MAIN](https://api.github.com/repos/KhaosMagnus/Project-Control/rulesets/27709862) · [R-META](https://api.github.com/repos/KhaosMagnus/Project-Control/rulesets/27717600)

El modelo conserva riesgos residuales concretos. La misma persona controla preparación, revisión, aceptación y administración, con posibilidad de errores correlacionados. Cambiar de cuenta no aísla credenciales ni reduce por sí mismo esa concentración. Los dictámenes documentales separados pueden detectar errores del artefacto, con límites propios. La viabilidad del circuito de primera PR, los permisos de ambas identidades, la ruta desde fork y los métodos habilitados globalmente siguen sin prueba específica. R5 y la enmienda mantienen el límite de CAS y el STOP ante discrepancias.

| Decisión posterior | Alcance y condición |
|---|---|
| Aceptar la enmienda | El Owner examina este candidato por su SHA-256, la otra QA y la conciliación que corresponda, y decide ACCEPT/REVISE/DEFER. La decisión debe dar eficacia prospectiva al cambio P5/Q6 y registrar su riesgo residual |
| Preparar o probar la primera PR | Gate separado con alcance, identidades, rama/fork, evidencia esperada y recuperación. Solo su GRANTED habilitaría los actos técnicos allí definidos. El permiso de diseño actual no cubre esa prueba |
| Autorizar una integración concreta | Congelar entradas y método, verificar elegibilidad efectiva y revisiones, obtener la disposición de integración y comprobar el resultado final conforme a R5 |
| Proponer aceptación integral G2-B | Resolver Q5/Q7/Q8/Q9 con evidencia o disposición explícita de límites. La enmienda no transforma los INCONCLUSIVE existentes en los dos PASS exigidos. Si se pretende cambiar esa regla de aceptación, proponer y aceptar expresamente esa modificación por separado |

La acción mejor sustentada es transferir este **DESIGN PASS (CONDITIONAL)** a PCM-001 para la conciliación focalizada y la decisión del Owner sobre la versión exacta. La aceptación integral G2-B seguirá necesitando su propio expediente y decisión. El ensayo del circuito PR permanece pendiente de autorización específica.

Las operaciones del revisor fueron lectura del ZIP y documentos, cálculo de tamaños y SHA-256, cotejo de copias históricas locales, consulta de documentación oficial y dos GET de rulesets. La comprobación de integridad mantuvo todas las fuentes sin editar. No repetí la QA de las raíces ni realicé una prueba del circuito de PR. No se crearon PR, forks, ramas, commits, reviews o invitaciones. No se modificaron permisos, instalación, reglas o refs. Las únicas escrituras fueron de trabajo local y de este informe al Owner. La atestación cubre las acciones efectivamente realizadas.

**Resultado individual — DESIGN PASS (CONDITIONAL). U1–U8 VERIFIED en alcance documental. Enmienda y G2-B pendientes de aceptación del Owner.**
