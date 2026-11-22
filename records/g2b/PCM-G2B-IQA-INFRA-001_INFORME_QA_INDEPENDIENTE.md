# PCM-G2B-IQA-INFRA-001 — Informe independiente de infraestructura P8

| Campo | Registro |
|---|---|
| Proyecto y candidato | Project Control Master, G2-B / P8, repositorio `KhaosMagnus/Project-Control` |
| Revisor | ChatGPT, QA independiente de los operadores y del autor PCM-001 para este encargo |
| Destinatario | Owner, para transferencia a PCM-001 |
| Fecha | 20 de noviembre de 2026, Ciudad de México, UTC−06:00 |
| Modo | STRICT READ-ONLY / INDEPENDENT INFRASTRUCTURE QA |
| Veredicto global | **INCONCLUSIVE** |
| Alcance del resultado | Objetos de génesis y separación de historias verificados. La aceptación integral Q1–Q9 queda pendiente de evidencia material |
| Autoridad | Aceptación del Owner pendiente. G3/G4/G5 continúan diferidos |

La infraestructura observable conserva las dos raíces y los bytes aprobados. Los tres rulesets están activos y las reglas aplicables a cada rama coinciden con el expediente. La QA completa queda **INCONCLUSIVE** porque Q6 carece de prueba de una ruta de revisión humana independiente y elegible, Q7 carece de la selección administrativa posterior a la creación y Q5/Q8/Q9 tienen límites históricos que el estado actual no resuelve. No se observó un SHA, árbol o regla de seguridad que contradiga el candidato congelado.

La clasificación **VERIFIED** acredita el control dentro de la cobertura indicada. **PARTIAL** identifica una parte corroborada con requisitos todavía sin acreditar. **UNKNOWN** indica evidencia insuficiente para decidir. **FAILED** se reserva para una condición exigida contradicha por evidencia suficiente. Ninguna calificación parcial se convierte en PASS global por acumular controles correctos.

La integridad del expediente quedó verificada antes de usar sus afirmaciones. El ZIP `PCM-001_G2-B_P8_INDEPENDENT_INFRA_QA_SHARED_PACKET_2026-11-20.zip` mide **43 393 bytes** y su SHA-256 es **`2c4b4a0b7835386e7ec5e25cfd635bc0ae43a8ca3d49d511ba0e85af3496c499`**, idéntico al aportado directamente por el Owner. CRC y nombres únicos válidos en **13/13 miembros**. El manifiesto coteja tamaños y SHA-256 de **12/12 miembros**, además del propio manifiesto, cuyo SHA-256 observado es `863f17a70582ae8247493f926bcd0530252f97da1ccd5828e7779cb8ac9d8fec`. El ZIP ejecutivo anidado pasó CRC, tamaños y hashes **5/5**, con coincidencia byte por byte de sus cinco documentos/payloads frente a las copias exteriores.

| Contrato o fuente congelada | SHA-256 |
|---|---|
| Solicitud ejecutiva G2-B | `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349` |
| Contrato de QA Q1–Q9 | `a1c10a91bc0947e3a84d4c8d48da404c7494f45154e8613c0a65bdd07b6633b3` |
| Runbook del operador | `be382147d5ce5b9875625cd8436d4ed31c2bcc9ee93da79a068bad8b50c66b78` |
| Corrección de diseño R5 | `9c329b3c4be0dca6cf60bc27e92bd586a931c9236bd786f402ce508f952562e8` |
| ZIP ejecutivo original incluido | `3cbcbc2825a2c644ba70c05b338b9714c967eae7f6fb52a554326ce03e7dd069` |

La solicitud ejecutiva incluida conserva su estado histórico de propuesta. La asignación y los informes P5–P7 reportan que el Owner concedió `PCM-G2B-INFRA-GENESIS-001` para P0–P8. El expediente no contiene el mensaje original de concesión como registro separado ni transcripción completa de ejecución. Esas afirmaciones se tratan como procedencia documental atribuida a PCM-001. El mensaje directo del Owner en esta conversación autoriza esta QA de solo lectura.

| Control | Clasificación | Evidencia independiente y límite |
|---|---|---|
| **Q1 — Identidad y superficies públicas** | **VERIFIED** para el estado observable examinado | ID `1465064417`, Owner `KhaosMagnus`, público, rama predeterminada `main`. Dos refs de ramas, sin tags, releases, PR, issues, comentarios de commit, workflows o ejecuciones Actions en las colecciones consultadas. Cada árbol tiene un README. La comprobación cubre las superficies enumeradas y el contenido alcanzable, con límites históricos en Q8 |
| **Q2 — Raíz y payload de main** | **VERIFIED** | Commit `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`, `parents=[]`, árbol y blob exactos, único `README.md` `100644`, 414 bytes y SHA-256 aprobado. Mensaje exacto conforme a la solicitud |
| **Q3 — Raíz y payload de meta** | **VERIFIED** | Commit `cac838940e0e824a1f828ff660e422a6441a1da7`, `parents=[]`, árbol y blob exactos, único `README.md` `100644`, 400 bytes y SHA-256 aprobado. Mensaje exacto conforme a la solicitud |
| **Q4 — Ausencia de ancestro común** | **VERIFIED** | Recuperación Git completa, sin shallow ni replace refs, dos commits en el grafo. `git merge-base` sobre ambos SHAs devolvió **1**, sin stdout ni stderr. `git fsck --full --strict` pasó |
| **Q5 — Guarda previa al primer push** | **PARTIAL** | Ruleset `27708103` activo, cobertura exacta de ambas refs, `deletion` + `non_fast_forward`, bypass vacío y aplicación efectiva actual verificados. Su creación precede a las fechas declaradas de los commits. La continuidad activa desde antes del primer push depende de los relatos P2/P4, sin registro original de recepción ni historial completo de reglas |
| **Q6 — Perfiles, métodos y revisor elegible** | **PARTIAL** | `R-MAIN` y `R-META` activos, PR, una aprobación, historial lineal, squash/rebase, sin checks requeridos ni bypass, aplicados a sus respectivas refs. La ruta humana independiente y elegible sigue **UNKNOWN**. Los GET de roles devolvieron 403. La habilitación global de los métodos del repositorio tampoco se expuso en las respuestas disponibles |
| **Q7 — Instalación selected y exclusión** | **PARTIAL** | `162412374` informa `selected`. Listado por instalación devuelve los once IDs previstos, sin extras ni faltantes; segunda página vacía; ID del maestro ausente. Falta el snapshot administrativo después de su creación, requerido por Q7. Exclusión administrativa y alcance de otras credenciales quedan **UNKNOWN** |
| **Q8 — Operaciones autorizadas y un push por raíz** | **PARTIAL** | Estado actual y mensajes corresponden a génesis mínima, sin importación ni release observables. P5/P6/P7 atribuyen los cambios al Owner. Faltan transcripciones originales completas y registros suficientes para acreditar un solo intento por rama, freeze P3 y toda la secuencia de decisiones. No se acredita ausencia universal de otras mutaciones |
| **Q9 — Eventos parciales o ambiguos y recuperación** | **UNKNOWN** | **NOT OBSERVED** en el expediente como incidente de ejecución documentado. No hay un registro original completo para excluir esos eventos o evaluar una recuperación real. Se revisó la regla documental, sin ejecutarla ni simularla |

Los objetos de Q2–Q4 se verificaron con lecturas GitHub y con una copia bare recuperada por transporte público de Git. Se recalcularon los SHAs de commit a partir de sus bytes y se inspeccionaron `cat-file`, `ls-tree` y el grafo completo. Los README descargados desde Git coinciden byte por byte con el payload del ZIP.

| Ref | Commit y árbol |
|---|---|
| `refs/heads/main` | Commit `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`. Árbol `04bff84a661781fb8f3982235c6c93f668a658ed` |
| `refs/heads/meta/project-control` | Commit `cac838940e0e824a1f828ff660e422a6441a1da7`. Árbol `3e39ae46b9e1690604387452ee7283062a79e182` |

| Rama | Única entrada ls-tree | SHA-256 de bytes |
|---|---|---|
| main | `100644 blob 56fd6d6560434e067c126c152ab86298bd57d61f README.md` | `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340` |
| meta/project-control | `100644 blob 2b30688846710fe73b89a537bb5a8cfb21e738eb README.md` | `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0` |

Los mensajes son `chore(genesis): reserve portable standard branch` y `chore(genesis): reserve local governance branch`. Ambos commits declaran autor y committer `KhaosMagnus`, con fecha **01:26:52−06:00** del 20 de noviembre. GitHub informa `unsigned`. Se inspeccionaron los metadatos públicos y se omitieron los correos en este informe. La conformidad de los bytes de atribución está observada. Su aprobación local por el Owner antes de publicar sigue atribuida al relato operativo, con el límite Q8.

Fuentes de los objetos y refs. [Repositorio](https://github.com/KhaosMagnus/Project-Control) · [Refs Git](https://api.github.com/repos/KhaosMagnus/Project-Control/git/refs) · [Commit main](https://api.github.com/repos/KhaosMagnus/Project-Control/git/commits/6d6f3639bc0cb84bc76845ad66f859e3fa1117bb) · [Commit meta](https://api.github.com/repos/KhaosMagnus/Project-Control/git/commits/cac838940e0e824a1f828ff660e422a6441a1da7) · [Árbol main](https://api.github.com/repos/KhaosMagnus/Project-Control/git/trees/04bff84a661781fb8f3982235c6c93f668a658ed) · [Árbol meta](https://api.github.com/repos/KhaosMagnus/Project-Control/git/trees/3e39ae46b9e1690604387452ee7283062a79e182)

La lectura pública efectiva de reglas terminó **04:24:50−06:00**. Se cotejaron tanto la configuración de rulesets como los resultados `rules/branches` aplicados a cada rama.

| Ruleset | Selector exacto | Estado, reglas y bypass | Tiempos declarados por GitHub, UTC−06:00 |
|---|---|---|---|
| `PCM-GENESIS-SAFETY`, `27708103` | Ambas refs | ACTIVE. `deletion`, `non_fast_forward`. `bypass_actors=[]` | Creado 01:09:59.320. Actualizado 01:09:59.354 |
| `R-MAIN`, `27709862` | Solo `refs/heads/main` | ACTIVE. Las dos reglas de seguridad, `pull_request` con 1 aprobación y métodos squash/rebase, `required_linear_history`. `bypass_actors=[]` | Creado 01:50:53.429. Actualizado 02:47:19.937 |
| `R-META`, `27717600` | Solo `refs/heads/meta/project-control` | ACTIVE. Misma configuración normativa de `R-MAIN` para meta. `bypass_actors=[]` | Creado 04:15:23.475. Actualizado 04:15:23.510 |

Los rulesets y refs se releyeron y permanecieron idénticos en la segunda observación, registrada **04:25:42−06:00**. La coincidencia de esas dos observaciones acredita estabilidad durante las lecturas. La cobertura temporal de Q5 exige además evidencia histórica. La fecha de autoría de un commit es metadato local y no identifica su recepción por el servidor. El endpoint público de eventos devolvió una lista vacía. No se realizaron pruebas de rechazo mediante escrituras.

Fuentes de configuración y aplicación. [Guarda común](https://api.github.com/repos/KhaosMagnus/Project-Control/rulesets/27708103) · [R-MAIN](https://api.github.com/repos/KhaosMagnus/Project-Control/rulesets/27709862) · [R-META](https://api.github.com/repos/KhaosMagnus/Project-Control/rulesets/27717600) · [Reglas aplicadas a main](https://api.github.com/repos/KhaosMagnus/Project-Control/rules/branches/main) · [Reglas aplicadas a meta](https://api.github.com/repos/KhaosMagnus/Project-Control/rules/branches/meta%2Fproject-control)

Q6 contiene una distinción material de autoridad humana. La asignación P8 y el registro P5 informan que **KhaosMagnus y JormungandrMagnus pertenecen al mismo Owner humano**. Esa pareja no satisface una exigencia de personas independientes. El acceso público de la segunda cuenta tampoco acredita que sus aprobaciones cuenten. Las consultas específicas de permiso para ambos usuarios devolvieron **403 Resource not accessible by integration**, lo que limita esta credencial de lectura y deja los roles sin verificar por ese endpoint. La documentación de GitHub exige un revisor elegible para las aprobaciones requeridas y prohíbe que el autor apruebe su propio PR. Una cuenta diferente permite distinguir usuarios en GitHub, mientras que la independencia de personas exigida por el contrato requiere evidencia propia. [GitHub Docs — revisiones y elegibilidad](https://docs.github.com/en/pull-requests/how-tos/review-pull-requests/reviewing-proposed-changes-in-a-pull-request) · [GitHub Docs — reglas de PR](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets)

La solicitud ejecutiva §3 P5 exige que la ruta de revisión sea demostrablemente viable y prevé STOP antes de P6 si no puede acreditarse. El handoff P5 §§2 y 5 conserva esa primacía contractual, pero difiere la revisión de elegibilidad para PR futuros y prepara P6. El expediente muestra después P6 realizado. Falta una disposición explícita que concilie esa condición pendiente con el avance o una prueba previa de la ruta elegible. La aceptación del Owner de la configuración de P5 y la QA documental de modelos aportan clases distintas de evidencia. PCM-001 debe resolver esta discrepancia de cumplimiento antes de proponer aceptación completa. No se crea un PR ni se modifican colaboradores para obtener esa evidencia dentro de esta QA.

Ambos perfiles tienen `dismiss_stale_reviews_on_push=false` y `require_last_push_approval=false`. R5 conserva como control de operación la comprobación de B/H/D/árbol y la revalidación ante cambios materiales. Se registra la configuración observada y la dependencia del procedimiento humano. No se impone una nueva política de revisión en este informe. La viabilidad completa de squash/rebase sigue limitada porque las respuestas de repositorio disponibles no exponen sus flags globales de habilitación, aunque sí aparecen como métodos permitidos en ambas reglas.

Para Q7 se consultó la instalación autenticada en modo lectura y se enumeraron las páginas con offset 0 y 100. El conjunto observado coincide con los once IDs del snapshot del expediente y excluye `1465064417`. El recálculo del conjunto y las respuestas se registraron **04:25:11−06:00**. No se reproducen nombres ni IDs de repositorios privados en esta entrega. La propia capacidad consultada enumera repositorios accesibles a la identidad autenticada dentro de una instalación. Esa evidencia respalda la observación del conector. Q7 exige además la selección administrativa antes/después, y el expediente reconoce que falta su captura posterior a la creación. Los campos `permissions.admin/push/pull` del usuario y el GET público exitoso del maestro dejan sin probar los scopes efectivos de un token de instalación concreto. El alcance de otros tokens, OAuth y otras autorizaciones sigue UNKNOWN. [GitHub Docs — enumeración de instalaciones y accesos](https://docs.github.com/en/rest/apps/installations) · [GitHub Docs — configuración de la selección](https://docs.github.com/en/apps/using-github-apps/reviewing-and-modifying-installed-github-apps)

Q8 y Q9 tienen una cobertura distinta del estado final. Los relatos P5–P7 registran pasos nominales y éxitos, pero el paquete no incluye el registro original íntegro de P0–P7, las salidas crudas de cada push ni un freeze P3 fechado previo a la publicación. Se desconoce el número completo de intentos y la existencia de cualquier cambio transitorio fuera del grafo actual. Tampoco existe en lo recibido un incidente con timeout o recuperación real que pueda evaluarse. El estado intermedio nominal con solo main, documentado en P5, se distingue de un fallo de ejecución o una recuperación. Q9 queda NOT OBSERVED / UNKNOWN en su componente operativo. No se inventan ensayos de recuperación para rellenar el contrato.

La acción mejor sustentada es **devolver INCONCLUSIVE a PCM-001 para completar la evidencia material antes de proponer al Owner la aceptación integral G2-B**.

| Pendiente para PCM-001 y el Owner | Evidencia concreta que permitiría reevaluar |
|---|---|
| Q6, independencia y elegibilidad | Identificar una ruta humana conforme al contrato, quién sería autor/revisor/integrador y qué permisos efectivos respaldan al revisor. Aportar evidencia administrativa de lectura o la decisión expresa que corresponda sobre el requisito de P5 y el avance P6. Cualquier cambio de permisos o contrato requiere su autorización propia |
| Q7, exclusión administrativa | Snapshot posterior a creación, fechado, de instalación `162412374`, `selected`, conjunto aprobado y maestro excluido por ID, con procedencia administrativa. Mantener separados el alcance de esa instalación y las restantes credenciales |
| Q5/Q8, cronología y autorización | Mensaje original del GRANTED, freeze P3, evidencia P2/P4/P5/P6/P7 y salidas originales disponibles de los dos intentos de push. Si alguna no existe, conservar UNKNOWN y elevar esa limitación al Owner, sin fabricar reconstrucciones |
| Q9, historia de eventos | Declaración y registro original de incidentes o de ausencia de incidentes observados. Si no se ensayó recuperación, mantenerla como no probada. Cualquier ensayo necesitaría un encargo separado |

Este informe se entrega como resultado individual. PCM-001 debe conciliar los informes independientes sobre la misma evidencia, conservando los límites y cualquier discrepancia. El Owner conserva la aceptación de G2-B. Esta QA no activa PCM-001 ni habilita G3/G4/G5, adopción, release o publicación autónoma.

Las acciones del revisor se limitaron a lectura del ZIP, cálculos locales, GET de GitHub mediante capacidades existentes, enumeración de instalación, consultas de permisos, lectura pública anónima y recuperación Git del repositorio público hacia una copia bare local. Cuando la capacidad pública rechazó algunas rutas por su allowlist, se consultaron endpoints públicos con GET anónimo mediante curl, sin encabezado de autorización. Las rutas clásicas de protección y permisos que devolvieron 403 se registraron como límites. Los objetos descargados se verificaron localmente sin crear commits ni mover refs remotas. Las herramientas disponibles no constituían un aislamiento técnico universal de escritura, por lo que la atestación se basa en los métodos y operaciones efectivamente invocados y registrados. No hubo push, PR, review, comentario, invitación, modificación de instalación, permisos, reglas o integración. Las únicas escrituras fueron de trabajo local y del informe al Owner.

**Resultado final — INCONCLUSIVE. Q1–Q4 VERIFIED. Q5–Q8 PARTIAL. Q9 UNKNOWN / NOT OBSERVED.**
