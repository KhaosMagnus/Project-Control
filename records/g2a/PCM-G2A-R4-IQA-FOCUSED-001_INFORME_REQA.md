# PCM-G2A-R4-IQA-FOCUSED-001 — Re-QA documental focalizada

| Campo | Registro |
|---|---|
| Proyecto | Project Control Master |
| Revisor | ChatGPT, revisor documental del candidato R4. Autor del candidato: PCM-001 |
| Destinatario | Owner, para transferencia a PCM-001 |
| Fecha | 15 de noviembre de 2026, Ciudad de México (UTC−06:00) |
| Mandato | Revisión independiente de F-R3-01, F-R3-02 y F-R3-03. Solo lectura |
| Veredicto | **DESIGN REVISE** |
| Efecto | **D-R3-APP / G2-B / G3 / G4 / G5 DEFERRED**. PCM-001 **PROVISIONAL** |
| Distribución | Revisión controlada para el Owner y PCM-001 |

## 1. Dictamen

R4 define una protección común antes del primer push, una protección adicional para `main` antes de intentar la segunda ref y perfiles de actualización separados. También corrige la aceptación de `all → selected` para que dependa del conjunto de IDs reconciliado y aprobado por el Owner. El cierre de esa corrección es **CLOSED DESIGN**.

Las dos correcciones Git quedan **PARTIAL** por defectos documentales. La tabla de recuperación ordena un STOP para el mismo estado que el paso P4 declara apto para avanzar a P5. En la actualización protegida, el texto combina la verificación previa con la identidad de un commit que el método `squash` o `rebase` puede generar al integrar. Ambos requisitos necesitan una secuencia inequívoca antes de convertir el diseño en un contrato ejecutable. La disponibilidad de reglas en un repositorio vacío y su aplicación efectiva están pendientes de verificación en el gate autorizado. Esas pruebas pendientes quedan fuera del fundamento del veredicto.

## 2. Integridad, cadena R3/R4 y autoridad

**Paquete recibido** — `PCM-001_G2-A-R4_FOCUSED_QA_SHARED_PACKET_2026-11-15.zip`, 49 515 bytes. SHA-256 calculado `0b4c08dc108783b3668c8cd9e0c09eae99b0b4f156803d6ea451dbd805520338`. El manifiesto indica que existe un digest exterior registrado por separado. El paquete y el encargo no aportan ese valor de referencia para cotejar. La comparación del digest exterior queda **NOT VERIFIED**.

| Evidencia | SHA-256 o resultado observado |
|---|---|
| Estructura y manifiesto R4 | A las 22:55:46, **12/12** miembros legibles por CRC, rutas y nombres únicos, pertenencia exacta, **11/11** tamaños y SHA-256 coincidentes. El propio manifiesto es el miembro adicional. Su SHA-256 es `6f18759ae904b78671d4fb55fcdeee2792da9d1e5aec8c3b2a797c25bfb985f8` |
| Candidato R4 `R4/PCM-001_G2-A-R4_ADDITIVE_GENESIS_PROTECTION_AND_ACCESS_CORRECTION.md` | `bcacf7ed0d36454459c7a6f7846658f40b948b56149271a66dbe762ee3b12725` |
| Contrato R3 | `c8789106252618549052e25a4dc43eb0b36f3d8bc15ab7d8bdbda0e1fa7ffaeb`, coincide con R4 línea 8 y el archivo del paquete R3 previo |
| Addendum del Owner R3 | `f23a9c66d1c5166c6645540d305afefa8a514a2eac75189a2355c59ab84eee40`, coincide con R4 línea 9 y el archivo del paquete R3 previo |
| Informe focalizado R3 (ChatGPT) | `42e12c2f9c7cf002a7a3cba18b71aabb7518c412de0d5f73bf8246b1368c53c4`, coincide con R4 línea 10 y con el archivo R3 adjunto separadamente, byte por byte |
| Comparación histórica | Siete miembros reutilizados de R3 coinciden byte por byte con el ZIP R3 previo, además del cotejo separado del informe focalizado. El informe Grok incluido pertenece a la QA inicial G2-A. El ZIP R4 contiene un solo informe focalizado R3. La comprobación se limita a este paquete |

| Ref de génesis | Bytes de README | SHA-256 de contenido | SHA-1 Git blob |
|---|---:|---|---|
| `refs/heads/main` | 414 | `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340` | `56fd6d6560434e067c126c152ab86298bd57d61f` |
| `refs/heads/meta/project-control` | 400 | `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0` | `2b30688846710fe73b89a537bb5a8cfb21e738eb` |

El recálculo de blobs con `git hash-object --no-filters` sin `-w` coincide con el cálculo independiente por encabezado Git y con R4 líneas 17–18. La evidencia corresponde a los bytes de los README. Los árboles, commits de cero padres y refs remotas se verificarán únicamente en el gate que autorice la génesis.

El addendum R3, líneas 9–26, conserva la aceptación documental del Owner de GitHub Free público, ambas ramas e historiales, T-A y los dos README de génesis. El encargo actual autoriza esta re-QA. R4 sigue como candidato documental. Para el futuro contrato ejecutivo, fijar expresamente que la secuencia corregida de génesis y el criterio reconciliado de instalación prevalecen, dentro de su alcance, sobre el procedimiento anterior, conservando los bytes y las decisiones históricas de R3. R3 §3 paso 6 protege ambas refs después de los dos pushes. R4 §§1.1–1.2 cambia ese orden de forma material.

## 3. Cierre de los tres hallazgos

| ID | Alcance | Evidencia R4 | Estado | Pendiente |
|---|---|---|---|---|
| F-R3-01 / H1 | Protección durante génesis, estados parciales y recuperación | §1.1 líneas 28–38 y §1.2 líneas 42–51. Guardia previa, protección adicional para `main` antes de la segunda ref y lectura posterior a respuestas ambiguas | **PARTIAL** | Corregir contradicción entre P4→P5 y la tabla sin fase. Incluir explícitamente las dos raíces correctas con `R-META` pendiente. Disponibilidad efectiva del ruleset temprano queda para G2-B autorizado |
| F-R3-02 / H2 y H6 de diseño | Perfiles efectivos propuestos para ambas refs, bypass y primera actualización | §2 líneas 55–73. Reglas separadas, PR del linaje correspondiente, revisión independiente, historia lineal, inspección de árbol y sin checks de arranque | **PARTIAL** | Separar objeto aprobado y resultado integrado, fijar el criterio para cambios de base/candidato y equivalencia postintegración. Configuración real en G2-B autorizado y primera escritura solo en su alcance autorizado |
| F-R3-03 / H4 | Inventario administrativo y aceptación de `all → selected` | §3 líneas 77–87. `S_admin`, `S_connector`, `S_approved`, comparación exacta, retención de `UNKNOWN`, recuperación por ID y exclusión posterior del maestro | **CLOSED DESIGN** | Captura administrativa, acuerdo por flujos prioritarios, aprobación independiente, operador y readback futuro. Toda dependencia o credencial sin acreditar conserva su límite |

### F-R3-01 — Hacer que la decisión dependa de la fase

P4 (línea 32) pide observar `main=expected` y `meta=absent` tras el primer push y pasar a P5. En ese instante `R-MAIN` está pendiente por diseño. La tabla general se anuncia «after any command or ambiguous response» (línea 42) y ordena `PARTIAL GUARD ONLY / STOP` para ese mismo estado (línea 46). La diferencia concreta es si P5 aún no se ha intentado o si ya se intentó activarlo y falló. Tras P6, la tabla también necesita decidir el caso de ambos SHAs correctos con `R-META` pendiente, en especial si la respuesta del segundo push fue ambigua. Una sola clasificación por refs y perfiles deja sin distinguir avance normal de recuperación.

| Fase y lectura confirmada | Decisión que debe fijar el contrato corregido |
|---|---|
| P4. `main` coincide, `meta` ausente, guarda común activa y `R-MAIN` aún sin intentar | Avanzar solo a P5, dentro de la autorización futura |
| P5 intentado. `R-MAIN` no puede acreditarse activo | STOP. Conservar la primera raíz. Registrar si la guarda común sigue acreditada y aplicar la ruta de recuperación aprobada. La segunda ref queda sin publicar |
| P6. Ambos SHAs y árboles coinciden, guarda y `R-MAIN` activos, `R-META` aún sin intentar | Registrar que los objetos remotos ya están presentes, incluso si el push devolvió timeout. Avanzar solo a P7 cuando el paso y el estado estén expresamente cubiertos |
| P6. Se confirma que falta `meta` tras intentar el segundo push | `PARTIAL PROTECTED / STOP`. Preservar `main` y escalar conforme a la recuperación aprobada. Una reanudación autorizada usa los mismos objetos congelados |
| P7 intentado. `R-META` no puede acreditarse activo | STOP por protección incompleta, con ambos objetos preservados. Remitir a P7 únicamente bajo el alcance de recuperación aplicable |
| SHA, árbol o controles exigidos para la fase difieren, o la lectura es inconclusa | STOP. Conservar evidencia. La clasificación y cualquier reanudación dependen de un readback concluyente y permiso vigente |

La guarda común separada y sin bypass es una respuesta válida de diseño para borrado y force-push si el canal administrativo del gate puede configurarla y acreditar las dos refs antes del primer push. R4 identifica la ventana residual en que esa guarda permite un fast-forward normal. El operador único previsto, el alcance sin la app y la protección adicional reducen la ventana, con riesgo residual hasta el readback. Si la guarda no puede acreditarse antes del primer push, se conserva el STOP de P2. [GitHub Docs — reglas de ramas y bypass](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets) · [GitHub Docs — selección de ramas y creación de rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository)

### F-R3-02 — Fijar la evidencia de aprobación y de integración

La separación entre el ruleset común de seguridad y `R-MAIN`/`R-META` permite limitar cualquier bypass de workflow a su propio ámbito. Es coherente introducir la ruta por PR después de existir cada raíz. La regla de aprobación humana requiere una identidad elegible distinta del autor del PR. La elegibilidad se comprueba en la configuración efectiva. El plan prevé STOP si esa identidad o el perfil no pueden acreditarse. [GitHub Docs — rulesets y requisitos de revisión](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets#require-a-pull-request-before-merging) · [GitHub Docs — revisión de cambios](https://docs.github.com/en/pull-requests/how-tos/review-pull-requests/reviewing-proposed-changes-in-a-pull-request)

La fila «Merge/integration» (línea 67) pide comprobar el commit resultante antes de la promoción final. La línea 71 prevé obtener el SHA que GitHub genere con `squash` o `rebase`. Si la promoción es la actualización de la ref protegida, hace falta un criterio previo basado en los objetos de entrada y el árbol esperado con el método elegido. El SHA final se obtiene después de la operación. «Determinar si hace falta una nueva aceptación» deja abierta la disposición precisamente si cambian los bytes o el alcance aprobado. [GitHub Docs — métodos de integración](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/about-merge-methods-on-github)

- **Antes de integrar:** vincular la aprobación al repositorio y ref destino, PR, SHAs de base y candidata, método permitido, alcance, delta y árbol esperado. Definir el criterio comprobable de linaje, incluida la ausencia de la raíz opuesta en la historia candidata. Verificar contenido mediante el delta y el árbol. Un cambio material de base, candidata, delta o árbol obliga a volver a evaluar la aprobación antes de promover.
- **Después de integrar:** leer la ref protegida y comprobar SHA nuevo, árbol, delta y continuidad del linaje frente al resultado autorizado. El contrato debe indicar cuándo la diferencia esperada de SHA queda cubierta por la aprobación del método y los bytes, y cuándo se exige STOP, preservación de evidencia y disposición del Owner. La aceptación posterior del resultado es un acto distinto del cambio de ref.
- Acreditar el método permitido y el revisor/integrador elegibles en el futuro perfil efectivo. La ruta humana y su readback dejan CAS autónomo `NOT VERIFIED`. Una prueba de escritura o de comparación atómica requiere su propia autorización.

### F-R3-03 — La selección ya se compara con el conjunto aprobado

El criterio R4 compara los IDs efectivos tras el cambio con `S_approved` y exige `repository_selection=selected` para la misma instalación. Once es el tamaño de la observación de alcance del conector. Una diferencia en el snapshot administrativo se reconcilia antes de aprobar `S_approved`. Un ID faltante, extra o de estado no verificable en el readback bloquea la aceptación de la transición y el avance a G2-B. Retener `UNKNOWN`, recuperar solo el ID afectado dentro del alcance aprobado y exigir autorización expresa para volver a `all` son condiciones documentadas. El diseño conserva el gate `D-R3-APP` separado y previo a G2-B, así como la comprobación del ID real del maestro tras su eventual creación fuera de la app y antes de publicar. [GitHub Docs — modificación de instalaciones](https://docs.github.com/en/apps/using-github-apps/reviewing-and-modifying-installed-github-apps) · [GitHub Docs — enumeración según credencial](https://docs.github.com/en/rest/apps/installations)

El snapshot administrativo actualizado, la decisión del Owner, las comprobaciones por flujo, la selección efectiva y la exclusión del nuevo ID quedan pendientes. El alcance de otras credenciales y el aislamiento entre repositorios retenidos siguen `NOT VERIFIED`.

## 4. Disposición para transferencia

1. PCM-001 corrige de forma aditiva la tabla de estados por fase y el contrato de aprobación e integración, documenta la precedencia de estos controles y devuelve únicamente esos cambios a re-QA. Mantener `S_approved` como criterio de diseño cerrado.
2. Antes de solicitar `D-R3-APP`, reconciliar y congelar inventario, conjunto, actores, ventana, readbacks y recuperación administrativa. Solo una autorización separada permite cambiar la instalación.
3. Antes de solicitar G2-B, obtener el readback autorizado de `selected` y congelar actor, metadatos, rutas, reglas y STOP. Solo G2-B autorizado habilita la creación, lectura efectiva de reglas, génesis y QA de infraestructura. G3 importa materiales en su propio gate. G4/G5 y cualquier prueba CAS quedan fuera de este encargo.

## 5. Atestación de solo lectura

Inspeccioné los ZIP y Markdown locales, cotejé miembros y hashes, y consulté documentación pública de GitHub. Git se usó únicamente para calcular hashes de blobs sin escribir objetos. No accedí al repositorio destino, al conector autenticado, a repositorios privados ni al plano administrativo de la instalación. No creé ni modifiqué repositorios, ramas, commits, PR, comentarios, reglas, permisos o instalaciones. No ejecuté pushes, pruebas de seguridad ni G2-B/G3/G4/G5. El único entregable nuevo es este informe al Owner. La atestación cubre las acciones de esta revisión.

**Disposición final — DESIGN REVISE. F-R3-01 PARTIAL. F-R3-02 PARTIAL. F-R3-03 CLOSED DESIGN. D-R3-APP / G2-B / G3 / G4 / G5 DEFERRED.**
