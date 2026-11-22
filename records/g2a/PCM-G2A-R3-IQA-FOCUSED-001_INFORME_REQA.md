# PCM-G2A-R3-IQA-FOCUSED-001 — Re-QA documental focalizada

| Campo | Registro |
|---|---|
| Proyecto | Project Control Master |
| Revisor y destinatario | ChatGPT, QA documental independiente de R3. Entrega al Owner para transferencia a PCM-001 |
| Fecha de revisión | 15 de noviembre de 2026, Ciudad de México (UTC−06:00) |
| Mandato | Encargo directo del Owner. Inspección documental de solo lectura del diseño G2-A-R3 |
| Veredicto | **DESIGN REVISE** |
| Efecto | Cambio de instalación sin autorización. **G2-B / G3 / G4 / G5 DEFERRED**. PCM-001 **PROVISIONAL** |
| Distribución | Revisión controlada para el Owner y PCM-001 |

## 1. Disposición

R3 resuelve la elección de visibilidad y topología, reduce la génesis a dos archivos comprobados y define un camino Git plausible con dos raíces sin padre. El addendum registra la aceptación documental del Owner para GitHub Free público, ambos historiales, T-A y esos dos README. La transición conservadora también mejora el diseño, pues conserva repositorios cuya dependencia todavía se desconoce.

El veredicto **DESIGN REVISE** se debe a tres brechas del contrato, observables antes de cualquier operación. El procedimiento puede dejar `main` sin protección cuando falla el segundo push. La política de ambas ramas carece de una configuración por ref y de una ruta de actualización revisada que preserve linaje y contenido bajo las reglas activas. El criterio de éxito de instalación utiliza «once IDs exactos» aunque el inventario administrativo que se apruebe podría ser distinto. Las pruebas en vivo seguirán pendientes una vez corregido el documento. Su ausencia, por sí sola, no determina el veredicto.

## 2. Integridad y autoridad del expediente

**ZIP recibido** — `PCM-001_G2-A-R3_FOCUSED_REQA_SHARED_PACKET_2026-11-15.zip`, 34 745 bytes. SHA-256 observado `fb39e74c794ff0e9a2ea6c457569706dcf6d6d20be33ff139d1fed00984119c6`. Manifiesto SHA-256 `5aee9056c29a80a4b559332238a437a223c2f3548b416a71ff4cf91ec7405edc`. El manifiesto anuncia un digest exterior publicado por separado. Ese valor de referencia no se adjuntó a este encargo, por lo que el cotejo del digest exterior queda `NOT VERIFIED`. La integridad interna pudo comprobarse.

| Evidencia | Método y resultado |
|---|---|
| Manifiesto R3, líneas 8–22 | A las 21:14:01, CRC, nombres únicos, rutas y miembros exactos. **10/10** miembros legibles, **9/9** tamaños y SHA-256 coinciden. El décimo miembro es el propio manifiesto |
| Contrato R3 y addendum | Contrato SHA-256 `c8789106252618549052e25a4dc43eb0b36f3d8bc15ab7d8bdbda0e1fa7ffaeb`, idéntico al fijado por el addendum. Addendum SHA-256 `f23a9c66d1c5166c6645540d305afefa8a514a2eac75189a2355c59ab84eee40` |
| QA histórica y consolidación | Los SHA-256 de ambos informes coinciden con el manifiesto y la consolidación. El informe ChatGPT es idéntico byte por byte al ya emitido. El dictamen Grok se cotejó contra los registros del expediente. La copia disponible del ZIP original conserva SHA-256 `d860ca78bc675eceac003ff1e7db5cf041483465960ccfe70f27ba7d52789033` y pasó de nuevo **8/8** cotejos de manifiesto |
| Fuente histórica | `KhaosMagnus/YU3DOH-Carder`, corte `056adb5097b7ce067082782e8d8c92b42db9082a`, árbol `65b5dca91a94459533fcda506f657e42f6bae5d4`. Se cotejó el pin con la evidencia pública de la primera QA y se recalculó a partir de sus copias el blob del protocolo `1ac3689c1e811d1594291afee6b2c1c6efd093d0` y **10/10** entradas del manifiesto bootstrap. Se reutilizó la procedencia del primer encargo, sin repetir la consulta remota al repositorio |
| Matriz de instalación | SHA-256 `e9f262bfc4103e87e7865ec3856b6d94b4b5897b60ad6dd999110b73e15748ac`. **11 IDs únicos**, el mismo conjunto citado en R2, diez privados y uno público. Todos constan como `UNKNOWN` / `KEEP-PROVISIONAL`. La página 2 vacía y el modo `all` constan como observaciones del autor bajo el alcance de su credencial |

| Ref prevista | Único archivo | Tamaño | SHA-256 recalculado | SHA-1 Git blob recalculado |
|---|---|---:|---|---|
| `refs/heads/main` | `README.md` | 414 bytes | `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340` | `56fd6d6560434e067c126c152ab86298bd57d61f` |
| `refs/heads/meta/project-control` | `README.md` | 400 bytes | `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0` | `2b30688846710fe73b89a537bb5a8cfb21e738eb` |

Los dos README son UTF-8, LF y con salto final. Sus bytes coinciden con los bloques del contrato y los SHA-256 citados en el addendum. Comprobé los blobs con `git hash-object --no-filters`, sin `-w`, y recalculé el hash Git sobre el encabezado y contenido. La revisión de texto confirma que los dos archivos declaran estado provisional y carecen de importaciones, datos reservados y autoridad operativa. La génesis futura deberá acreditar el modo Git aprobado, el árbol exacto y los metadatos de commit, que son objetos distintos del blob.

**Precedencia del Owner.** El estado `DRAFT / NOT APPROVED` del contrato describe su emisión. El addendum `PCM-G2A-R3-DESIGN-OWNER-GRANT`, líneas 9–26, es posterior y cita su digest. Registra el `GRANTED DESIGN ONLY` para plan, visibilidad de ambas ramas e historial, T-A y la génesis de los dos README por operador humano futuro. Los mensajes, identidades Git, fechas y pushes requieren su decisión en el alcance ejecutivo. La aceptación tampoco autoriza publicar el expediente o añadir contenido a otras superficies públicas. La declaración previa se verificó como registro documental incluido y ligado al contrato. Firma u original firmado independiente `NOT VERIFIED`. El encargo directo del Owner autoriza esta re-QA.

## 3. Cierre de hallazgos originales

`CLOSED DESIGN` indica que la decisión y el control exigidos para el alcance indicado están documentados. `PARTIAL` indica que existe una corrección material con un requisito pendiente. `OPEN` identifica una brecha que sigue activa en la fase indicada. Los informes GPT y Grok originales conservan sus dictámenes y no se reemplazan con este informe.

| ID | Hallazgo original | Evidencia R3 | Severidad | Estado | Fase afectada |
|---|---|---|---|---|---|
| H1 | Método de génesis y protección inicial sin criterio exacto | Contrato §§2–3, addendum líneas 17–19. Dos `git init` limpios, ramas y bytes fijos, orden de push y STOP si falla el segundo | Alta | **PARTIAL**. T-A y la génesis mínima quedan cerradas documentalmente. Falta decidir cómo queda protegida la primera ref y cómo se reconcilia un resultado parcial o ambiguo | Diseño previo a G2-B |
| H2 | Separación de linaje y contenido, protección efectiva de ambas refs | Contrato §3 pasos 6–7 y §5. QA de las raíces, bloqueo de borrado y force-push, bypass inventariado, reconocimiento de la copia entre ramas | Alta | **PARTIAL**. Faltan el perfil exacto por ref, la política de bypass y un criterio de revisión de rama candidata, árbol y actualización final | Diseño previo a G2-B. Lectura efectiva durante G2-B autorizado |
| H3 | Aceptación de divulgación, catálogo de bytes y custodia | Addendum líneas 13–19 y 28–34, contrato §§1–3. Ambas ramas e historial aceptados en diseño. Un README por ref, con hashes y preflight de metadatos | Alta | **CLOSED DESIGN** para la divulgación de la génesis mínima. Resta congelar para aprobación ejecutiva modo y metadatos, confirmar documentalmente `NONE` para anexos, y revisar los objetos exactos antes del envío | Preparación de G2-B. Custodia de registros posteriores se evalúa antes de publicarlos |
| H4 | Integridad del inventario y transición reproducible | Contrato §4, matriz líneas 25–52. Evidencia más específica de la credencial conectada, retención del conjunto reconciliado, precondición `selected`, exclusión futura del maestro, recuperación por ID | Alta | **PARTIAL**. La aceptación posterior de la matriz está fijada a once IDs y falta el snapshot administrativo. Los flujos prioritarios carecen de criterio y evidencia acordados | Gate independiente `D-R3-APP`, previo a G2-B |
| H5 | Clasificación de importaciones y derechos de distribución | Contrato §§1–2 y §6. Portability Review como `REFERENCE`, adaptador congelado separado de su sucesor y builder como posible `TRANSFORM` | Media | **PARTIAL** en el hallazgo original. **CLOSED DESIGN** para la exclusión de imports en G2-B. Derechos, procedencia de salida y manifiesto final siguen **OPEN** para G3 | G3 para los pendientes |
| H6 | Ruta de actualización protegida y capacidad CAS | Contrato §3 pasos 6 y 8 y §5. Diferencia génesis humana, PR, integración y autonomía. CAS queda `NOT VERIFIED` | Alta para publicación autónoma | **PARTIAL**. La ruta humana de génesis está especificada a nivel de diseño. Falta una ruta de actualización viable por ref y sigue **OPEN** cualquier prueba de CAS autónomo | Diseño de protecciones G2-B. Escrituras efectivas y CAS solo bajo autorización posterior específica |

## 4. Correcciones focalizadas

### 4.1 T-A, estados parciales y protección inicial

Dos inicializaciones limpias con un commit de cero padres en cada una producen el grafo esperado. Los dos pushes secuenciales son una elección razonable para una génesis mínima y se pueden mantener si el contrato gobierna el estado intermedio. El paso 5 detiene el proceso si falla el segundo push. El paso 6 aplica protecciones después de ambos. Por tanto, el procedimiento publicado puede detenerse con `main` alcanzable y sin el control previsto. Un timeout también deja indeterminado si la ref cambió. [Git — git-commit-tree](https://git-scm.com/docs/git-commit-tree) · [Git — git-push](https://git-scm.com/docs/git-push)

- Fijar qué protección de `main` existirá antes de intentar la segunda ref. El contrato debe elegir reglas preconfiguradas compatibles con la creación o una protección inmediata tras verificar `main`, antes del segundo push. Si se requiere una ventana inicial, fijar límites, operador, estado permitido, evidencia y una medida de contención expresamente cubierta por el futuro GRANTED. Un STOP genérico deja sin resolver esa contención.
- Para cada paso, fijar repositorio/ID, ref, objetos previstos, rama por defecto `main` y criterios. Obtener los SHAs de los dos commits locales y congelar su identidad antes de cada envío. Después de cada operación o respuesta ambigua, cotejar desde una ruta autorizada ambos heads y controles con los valores congelados. Un SHA esperado ya presente se registra y verifica. El contrato debe especificar quién puede reanudar con los mismos objetos y qué cambios exigen al Owner una autorización específica de recuperación. La siguiente matriz fija las situaciones que el procedimiento corregido debe resolver.
- Mantener la evidencia esperada de T-A para el futuro gate. Cada tip inicial coincide con su commit raíz sin padres, cada árbol contiene un único README aprobado, y el grafo completo disponible carece de ancestro común. El resultado de `merge-base` se interpreta con sus dos entradas accesibles y su código de salida, junto con el inventario de refs y contenido. El futuro readback comprobará esa propiedad. [Git — git-merge-base](https://git-scm.com/docs/git-merge-base)

| Lectura posterior a un fallo o respuesta incierta | Disposición que debe especificar el contrato |
|---|---|
| Ambas refs ausentes, confirmadas | Génesis sin aplicar. Repetir el preflight y reanudar solo dentro de una ruta ya autorizada |
| Solo `main` con su SHA esperado, segunda ref ausente | `PARTIAL GENESIS / STOP`. Conservar evidencias, verificar contención de `main` y aplicar la decisión de recuperación prevista |
| Ambas refs en sus SHAs esperados | El envío ya está aplicado. Verificar ramas, protecciones y resto de controles antes de pasar a QA |
| Refs remotas sin lectura concluyente, SHA distinto, solo la segunda ref, refs adicionales o protección exigida para ese punto sin comprobar | `STOP` por estado indeterminado, inesperado o incompleto. Reconciliar y escalar según autoridad vigente |

### 4.2 Operación bajo reglas en ambas ramas

Cerrar un perfil para `refs/heads/main` y otro para `refs/heads/meta/project-control` que defina reglas activas, actores, tratamiento separado de creación/actualización y de borrado/force-push, alcance y duración de excepciones, revisión requerida y fuente de readback administrativo. Si un bypass se necesita para crear o actualizar, el contrato debe explicar cómo preserva las prohibiciones de borrado y force-push. Dar al gate un criterio viable para el primer cambio autorizado en cada rama, con destino y linaje de la candidata, revisión del delta y del árbol, aprobación del operador y revisión del SHA resultante si el método reescribe el candidato. Basta especificar esa ruta como diseño antes de G2-B. G2-B verifica la configuración, y una escritura de prueba requiere su alcance propio. El requerimiento de historia lineal permite flujos de integración que generan commits nuevos. Por sí solo no controla los archivos copiados entre linajes. [GitHub Docs — reglas disponibles y bypass](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets) · [GitHub Docs — estado y acumulación de reglas](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets)

### 4.3 Instalación `all → selected`

La matriz informa una enumeración acotada y una segunda página vacía para esa credencial. Ambas son compatibles con que la UI administrativa muestre otro conjunto. El contrato §4 define correctamente la población a preservar como el conjunto existente completo y reconciliado. La aceptación de la matriz, línea 48, debe usar **exactamente el conjunto de IDs reconciliado, congelado y aprobado por el Owner**, con once como conteo de la observación actual. Si el snapshot difiere, reconciliar altas, bajas o diferencias de alcance antes de autorizar el cambio. Conservar los `UNKNOWN` reduce el riesgo de interrupción sin exigir demostrar todas las dependencias antes de esa primera transición. Tampoco prueba aislamiento entre los repos retenidos. [GitHub Docs — repositorios accesibles según la credencial](https://docs.github.com/en/rest/apps/installations) · [GitHub Docs — selección de repositorios de una app](https://docs.github.com/en/apps/using-github-apps/reviewing-and-modifying-installed-github-apps)

Para `D-R3-APP` preparar un snapshot administrativo fechado con ID de instalación, modo, permisos y conjunto completo, la lista exacta a conservar, el operador, la ventana, verificaciones por flujo prioritario y los criterios de STOP y recuperación. Mantener explícita la recuperación individual por ID bajo autorización. Después de un cambio autorizado, cotejar instalación, modo `selected`, IDs y lecturas acordadas del flujo. La creación manual fuera de la app es posterior a ese readback. Cuando exista un ID real del maestro, comprobar su exclusión antes del primer push. La lectura anónima del maestro confirma visibilidad. La exclusión debe acreditarse en la configuración autorizada de la instalación. La cobertura de otras credenciales y el emisor por operación quedan `NOT VERIFIED`. [GitHub Docs — selección e inclusión de repos creados por la app](https://docs.github.com/en/apps/using-github-apps/reviewing-and-modifying-installed-github-apps)

## 5. Evidencia por fase y siguiente transferencia

| Cuándo | Evidencia o decisión exigible |
|---|---|
| Revisión documental, antes de pedir autorizaciones ejecutivas | PCM-001 emite una corrección aditiva del procedimiento de estados parciales, la matriz de protecciones/rutas por ref y la comparación del conjunto de IDs conciliado. Incluir actor futuro, preflight de metadatos, archivo/modo y disposición `NONE` para anexos de génesis, o la decisión de custodia si aparece un anexo indispensable |
| Gate `D-R3-APP`, previo a G2-B | Snapshot administrativo, conjunto exacto, responsables, validación y recuperación. Autorización independiente y luego readback tras la transición |
| Solo con G2-B autorizado | Identidad real del destino y exclusión de la app, preflight de objetos, estado intermedio, SHAs de refs y árbol remoto, parentage, reglas activas y bypass, comparación de configuración y QA independiente. Una comprobación de configuración por lectura documenta el estado observado |
| Autorizaciones futuras independientes | Evidencia de escritura efectiva bajo reglas si se exige, CAS para publicación autónoma, permisos efectivos por identidad, licencia/manifiesto y adopción G3. Derechos y custodia posteriores se resuelven antes de sus publicaciones |

**Siguiente acción del Owner.** Transferir este dictamen a PCM-001 y pedir la corrección aditiva de los tres puntos materiales de §4. Resolver los tres como parte de la re-QA focalizada antes de someter `D-R3-APP` o `D-R3-G2B`. Conservar este dictamen separado de la segunda re-QA hasta que se emita, según la independencia prevista.

## 6. Atestación y límites

Leí el ZIP aportado y las fuentes históricas locales del encargo anterior. Inspeccioné CRC, tamaños, estructura, hashes, bytes y contenido. Consulté documentación pública de producto. Git se usó para calcular hashes sin escribir objetos. No usé el conector GitHub, credenciales de GitHub, lectura de repositorios privados ni acceso administrativo. No realicé operaciones sobre repositorios, ramas, commits, pull requests, comentarios, instalaciones o permisos. No ejecuté los pasos del contrato, una prueba de seguridad ni G2-B/G3/G4/G5. Las únicas escrituras fueron de trabajo local y de entrega del informe al Owner. La atestación se limita a las acciones de esta revisión.

El estado actual de la instalación, el inventario administrativo, las dependencias operativas, la disponibilidad del nombre, los commits de génesis, las reglas efectivas, la recuperación en vivo y la actualización condicional en refs protegidas quedan `UNKNOWN` o `NOT VERIFIED`. La matriz de revisión distingue qué parte se sostiene por integridad de bytes, observación histórica o aceptación documental.

**Disposición final — DESIGN REVISE. G2-B / G3 / G4 / G5 DEFERRED.**
