# Project Control Master — G2-A-R5 Corrección aditiva focalizada de fases y publicación

**Control:** `PCM-G2A-R5-PHASE-GUARD-AND-INTEGRATION-DES-001`  
**Autor:** `PROJECT_CONTROL_MASTER / PCM-001 PROVISIONAL`  
**Fecha:** 2026-11-15  
**Estado:** `DRAFT FOR FOCUSED DOCUMENTARY QA / NO EXECUTABLE AUTHORITY`  
**Motivo:** cierre de `F-R3-01` y `F-R3-02` tras doble QA R4. `F-R3-03` = `CLOSED DESIGN`; su tratamiento original no cambia.  
**Fuente R4 SHA-256:** `bcacf7ed0d36454459c7a6f7846658f40b948b56149271a66dbe762ee3b12725`  
**Informes R4, SHA-256:** GPT `1bcb91d5397b05d502ddc03b58d6bf1a995bb48c7394184a75a9dc6ff9ba4c56` / Grok `c6346c05ae9b81baa1e6a26dddd687fada19b0f0c7ef0932a72db32daf7f6111`.  
**Fuente de autoridad documental:** addendum del Owner R3, SHA-256 `f23a9c66d1c5166c6645540d305afefa8a514a2eac75189a2355c59ab84eee40`.

## 0. Precedencia y límites

Este archivo es una **propuesta aditiva**, no una sustitución de bytes congelados ni una autorización de repositorio. Una vez aceptada específicamente por el Owner, **§1 sustituiría a efectos del procedimiento la tabla general de R4 §1.2 y aclararía P4–P7**, y **§2 aclararía la fila «Merge/integration» y el párrafo «First subsequent change» de R4 §2**. En lo demás rige R4 dentro de la disposición R3 aceptada. Si existen diferencias entre R3 y R4/R5 sobre el orden de protección, solo la secuencia corregida y posteriormente aceptada tendría precedencia prospectiva; el origen histórico no se sobrescribe.

Se conservan: GitHub Free **público**, `KhaosMagnus/Project-Control` **propuesto**, dos raíces independientes `T-A`, un único README neutral en cada raíz, prohibición de importar material de YU3DOH en G2-B, instalación `162412374` separada y sin incluir al nuevo maestro, guardia previa `PCM-GENESIS-SAFETY`, protección por rama `R-MAIN` y `R-META`, ausencia de bypass de seguridad, QA independiente y `D-R3-APP / G2-B / G3 / G4 / G5` **DEFERRED**.

Los hashes SHA-256 de los README aprobados como diseño permanecen:

- `main/README.md`: `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340` (414 bytes; blob Git `56fd6d6560434e067c126c152ab86298bd57d61f`).
- `meta/project-control/README.md`: `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0` (400 bytes; blob Git `2b30688846710fe73b89a537bb5a8cfb21e738eb`).

## 1. F-R3-01 — Máquina de estados de génesis dependiente de la fase

### 1.1 Estados y comprobaciones vinculantes

**Variables de lectura:** `H_main`, `H_meta` (SHA remoto o ausencia confirmada); `C_main`, `C_meta` (SHA de raíz local congelado, cada uno sin padres); `G` = ruleset común activo y acreditado sobre ambas refs; `M` = perfil `R-MAIN` activo; `T` = perfil `R-META` activo; `A` = destino excluido de la instalación compartida. Verificar también los árboles, los modos, el repositorio/ID, visibilidad y ausencia de refs extra. Toda lectura se efectúa por un canal autorizado e independiente del resultado de push. **La respuesta de un comando no sustituye readback.**

**Invariantes antes de cualquier push:** el Owner habrá autorizado separadamente `D-R3-APP` y `G2-B`; el readback `selected` será válido; repositorio vacío creado fuera de la app; `A=true`; `G=true`, sin bypass a la guarda de borrado/force-push; ambos `C_main`/`C_meta` y sus metadatos previamente congelados. Si no puede verificarse la guardia previa en GitHub Free con repositorio vacío, **STOP ANTES DEL PRIMER PUSH**. No existe ruta alternativa automática desprotegida.

El estado del mismo par de refs **no basta** para decidir: son necesarias la fase, la acción intentada, su respuesta y las protecciones exigibles en ese punto. El único avance nominal es `P4 → P5 → P6 → P7 → P8`; un timeout solo permite avanzar si un readback concluyente acredita el resultado exacto de la acción y el perfil requerido por la fase.

| Fase / acción anterior | Readback suficiente y protección exigible | Clasificación y siguiente acción permitida |
|---|---|---|
| `P0–P3` preflight; no pushes autorizados aún | Destino creado y vacío, `G=true`, `A=true`, dos raíces locales exactas congeladas | `READY FOR P4`; si no, `STOP`. Ninguna ref remota debe existir antes de P4 |
| `P4`, primer push ejecutado (aunque haya timeout) | `H_main=C_main`, `H_meta=absent`, árbol y metadatos exactos, `G=true`, `A=true`; `M` **todavía no intentado** | `EXPECTED POST-P4`; **AVANZAR SOLO A P5**. La ausencia de `M` aquí es normal, no `PARTIAL GUARD ONLY / STOP` |
| `P4` intentado; `H_main=absent` confirmado | No hay primera raíz remota; `G=true` y `A=true` | `PUSH NOT APPLIED / STOP`; registrar evidencia y reentrada solo si el GRANTED ejecutivo la contempla expresamente; nunca reintento ciego |
| `P5`, configuración/activación de `R-MAIN` intentada | `H_main=C_main`, `H_meta=absent`, `G=true`, `M=true`, `A=true`; árboles correctos | `MAIN PROTECTED`; **AVANZAR SOLO A P6**. Si la API respondió ambiguamente pero la configuración coincide, no repetir la activación |
| `P5` intentado; `M` no confirmado activo | `H_main=C_main`, `H_meta=absent`, `G=true`, `A=true`, `M=false/UNKNOWN` | `PARTIAL GUARD ONLY / STOP`; preservar `main`, no publicar `meta`. La recuperación de P5 requiere alcance ejecutivo vigente o decisión específica |
| `P6`, segundo push intentado (también con timeout) | `H_main=C_main`, `H_meta=C_meta`, `G=true`, `M=true`, `A=true`; ambos árboles/commit IDs exactos; `T` **aún no intentado** | `EXPECTED POST-P6`; **AVANZAR SOLO A P7**. La ausencia de `T` aquí es normal; no repetir push si el SHA esperado ya está presente |
| `P6` intentado; segunda raíz no apareció | `H_main=C_main`, `H_meta=absent`, `G=true`, `M=true`, `A=true` | `PARTIAL PROTECTED / STOP`. Conservar `main`; reanudación con `C_meta` idéntico solo tras recuperación autorizada y nueva inspección |
| `P7`, activación `R-META` intentada | `H_main=C_main`, `H_meta=C_meta`, `G=true`, `M=true`, `T=true`, `A=true`; árboles/ref IDs exactos | `GENESIS PROTECTED / AVANZAR SOLO A P8` (QA de infraestructura). Un timeout con readback conforme no justifica repetir operación |
| `P7` intentado; `T` no acreditado | Ambas raíces exactas presentes, `G=true`, `M=true`, `T=false/UNKNOWN`, `A=true` | `BOTH ROOTS PRESENT / PROTECTION INCOMPLETE / STOP`; conservar objetos; no pasar a QA de aceptación ni G3; recuperación sujeta a permiso |
| **Cualquier fase** con SHA, árbol, ref, visibilidad, guarda requerida o inclusión de app distintos; readback denegado/ambiguo | Discordancia o ausencia de prueba suficiente | `UNEXPECTED OR UNKNOWN / STOP`. No borrar, resetear, force-push, modificar autorización ni inferir fallo de un timeout |

### 1.2 Recuperación, contención y límites de prueba

- **STOP es una suspensión de escrituras**, no una orden de eliminar el repositorio o devolver protecciones. Preservar SHAs locales/remotos, estado de reglas, logs de operación y la fase exacta. Un estado parcial puede contener `main` accesible públicamente; el carácter público de los bytes aprobados no autoriza operaciones nuevas.
- La recuperación puede permitir completar **la misma acción y los mismos objetos** si el Owner lo autoriza expresamente y un readback nuevo acredita que el estado previo sigue siendo el esperado. Autorizar recuperación no implica force-push, borrar refs, relajar guardas o volver la instalación a `all`.
- La guarda `G` se mantiene desde antes de P4; `M` protege `main` antes de P6; `T` protege `meta` tras P6. El riesgo de *fast-forward* ordinario durante la breve ventana pre-perfil sigue existiendo y es **riesgo residual**, no «aislamiento perfecto». El administrador conserva poder de editar rulesets.
- La factibilidad real de un ruleset sobre un repo vacío, su cobertura y readback, el acceso de identidades y el comportamiento del servidor siguen `NOT VERIFIED`. Estas pruebas no se inventan ni se ejecutan sin GRANTED específico.

## 2. F-R3-02 — Aprobación previa e integración posterior con SHAs no conocidos anticipadamente

### 2.1 Paquete de aprobación **antes de integrar**

La autorización de integración se refiere a **entradas verificables y resultado de contenido esperado**, no al SHA futuro que GitHub asignará al commit de squash/rebase.

| Campo vinculante | Qué debe congelarse antes de promover |
|---|---|
| Destino/linaje | Repositorio/ID, `refs/heads/main` **o** `refs/heads/meta/project-control`, raíz esperada del linaje, ausencias de ancestros de la raíz opuesta y revisión de rutas permitidas |
| PR | Identificador/URL, autor, candidata originada desde la propia rama de destino, ref origen, SHA de base `B`, SHA de cabeza `H`, SHA del árbol candidato y alcance aprobado |
| Método | Elegir **exactamente uno**: `squash` o `rebase` si está habilitado y es compatible con reglas. `merge-commit` no autorizado por la topología/historial lineal. Cambiar método exige nueva aprobación |
| Contenido aprobado | Delta congelado `D` (incluidas eliminaciones/renombres/modos), conjunto de rutas permitidas, árbol completo de salida esperado `T_expected` derivado de `B` más el delta aprobado y hash SHA del expediente de QA |
| Personas/autoridades | Revisor humano elegible **distinto del autor** con aprobación GitHub vigente; integrador separado y autorizado; disposición Owner sobre ese cambio si procede; identidad/token de ejecución y perfiles activos verificados |
| Estado de protección | Rulesets comunes y particulares activos en la ref; aprobación GitHub no sustituye el QA independiente del artefacto ni la autorización del Owner |

**Preflight inmediatamente anterior al merge:** comprobar que la ref protegida sigue en `B`, candidata sigue en `H`, PR conserva método y delta, aprobación no ha caducado y `T_expected` continúa siendo el árbol calculado desde el estado actual. Verificar que la candidata no trae la raíz opuesta ni una historia ajena. Un cambio material de `B`, `H`, `D`, rutas, modo, `T_expected`, estado de aprobación o conjunto de reglas produce **STOP y nueva revisión/aprobación**; no confiar en que la interfaz impida automáticamente todas las carreras. Nunca emitir un merge con un PR cuyo resultado de contenido está `UNKNOWN`.

### 2.2 Verificación **después** de que GitHub genere el commit

El integrador debe inspeccionar el SHA remoto nuevo `C` y su cadena, aunque el comando devolviera timeout o el servidor confirmara éxito. Nunca inferir que `C=H` para `squash/rebase`.

1. Confirmar que `HEAD_target=C`, que `C` es avance permitido del linaje desde `B`, y que no incorpora la raíz opuesta. Verificar `tree(C) == T_expected` y que el delta efectivo `B..C` coincide con `D` en contenido, rutas y modos; inspeccionar también refs ajenas para descartar alteraciones no autorizadas.
2. Para **squash**, esperar un **nuevo commit** en la ref destino cuyo padre es `B`, con árbol `T_expected` y un delta permitido. El SHA de ese commit no se conoce antes: debe identificarse y verificarse después.
3. Para **rebase**, esperar una cadena lineal de commits nuevos aplicada sobre `B`, con tip `C`, árbol final `T_expected` y sin ancestros externos; auditar el número y las diferencias intermedias frente a la candidata aprobada. Si no puede verificarse, `STOP` y reconciliar, sin reintentar la operación.
4. Diferencia **solo de SHA por los metadatos/reescritura propios del método aprobado**, con `B`, `H`, `D`, `T_expected`, linaje y revisiones invariables, **no requiere nueva aprobación preventiva**: estaba expresamente cubierta por aprobar el método. Sí exige readback postintegración y registro/aceptación del resultado. Diferencia de árbol, delta, linaje, ref, método, aprobaciones, base o alcance **no está aprobada**, implica `STOP`, conservar evidencia y consultar al Owner antes de cualquier corrección.
5. Si no se puede demostrar qué commit quedó publicado (respuesta ambigua y readback insuficiente), clasificar `UNKNOWN / STOP`; nunca ejecutar nuevamente el merge sin reconciliación. La aceptación del resultado por QA/Owner es posterior e independiente de la operación.

**Riesgo residual:** Entre el último preflight y el merge puede existir una carrera. Esta ruta es **manual, supervisada y sujeta a readback**; no declara atomicidad *compare-and-swap* ni autoriza publicación autónoma. Si una política exige CAS demostrable antes de cualquier integración, entonces la ruta propuesta es `NOT READY` y deberá rediseñarse mediante otra autorización.

## 3. F-R3-03 — Decisión conservada, no reabierta

R4 §3 sigue siendo la norma propuesta para `S_admin(t)`, `S_connector(t')` y `S_approved`: **el criterio de aceptación es igualdad del conjunto administrativo efectivo con el conjunto exacto reconciliado y aprobado**, no «exactamente 11 repositorios». Los once IDs existentes son observación histórica, no una invariante. `D-R3-APP` necesita autorización separada, ventana, operador, lectura administrativa y recuperación por ID. No se realizó cambio alguno a la instalación.

## 4. Solicitud de revisión focalizada y siguiente puerta de decisión

**QA de R5, exclusivamente documental**: verificar que el estado nominal P4/P6 deja de confundirse con un STOP, que el tratamiento de fallos/timeout y R-MAIN/R-META depende de fase, y que la autorización de merge se ancla a `B/H/D/T_expected` antes de conocer el SHA resultante `C`. Confirmar que R4 §3 y las decisiones Owner R3 se conservan. Clasificar `F-R3-01` y `F-R3-02` como `CLOSED DESIGN / PARTIAL / OPEN`, sin tratar comprobaciones en vivo como defectos documentales automáticos.

**Después, no antes de QA/aceptación documental:** preparar la autorización del gate `D-R3-APP` como decisión **independiente**. Precisa snapshot administrativo, `S_approved`, operador, pruebas de continuidad de lectura de proyectos y recuperación, y `GRANTED` expreso del Owner. Solo cuando `selected` esté aplicado/verificado podrá solicitarse G2-B. Ningún PASS documental habilita modificar GitHub.

**FIN:** `R5 DRAFT / F-R3-01+02 FOCUSED QA PENDING / F-R3-03 CLOSED DESIGN / NO GITHUB MUTATIONS / PCM-001 PROVISIONAL`.
