# PROJECT CONTROL MASTER — G2-A PREFLIGHT REPORT

**Expediente:** `PC-MASTER-DES-001 / G2-A`  
**Emisor:** `PROJECT_CONTROL_MASTER / PCM-001` (PROVISIONAL)  
**Autoridad de entrada:** Owner disposition `D1 GRANTED`, `D2 GRANTED / G2-A PREFLIGHT ONLY`, `G2-B DEFERRED`, `D3 DEFERRED`, `D4 DEFERRED`  
**Fecha:** 2026-11-11 (America/Mexico_City)  
**Modo:** Read-only observation and documentary design; NO GitHub writes; NO tests of mutation; NO inherited authority  
**Destino propuesto:** `KhaosMagnus/Project-Control`  
**Fuente histórica:** `KhaosMagnus/YU3DOH-Carder`, `meta/project-control @ 056adb5097b7ce067082782e8d8c92b42db9082a`.

## 0. Disposición ejecutiva

**Resultado:** `G2-A EVIDENCE COLLECTED / PREFLIGHT PARTIAL / G2-B NOT READY`.

La verificación de identidad de cuenta y el inventario accesible de instalación fueron satisfactorios. El repositorio propuesto devuelve `404 NOT_FOUND` a la conexión utilizada; la disponibilidad del nombre no está garantizada. Permanecen sin confirmar el plan GitHub, los permisos efectivos detallados de la aplicación y las dos piezas documentales expresamente exigidas. La instalación GitHub accesible declara `repository_selection=all`, riesgo material de exposición del futuro repositorio a dicha instalación. No es admisible declarar aislamiento ni G2-B READY hasta resolverlo.

**D1:** se recibe la excepción autorizada de secuencia: la infraestructura documental puede prepararse independientemente de Q02. **No modifica Q02**: A2 NO-GO, ONLINE-1C A1 INCONCLUSIVE/P3 UNKNOWN y garantías de CAS no probadas.

**Operaciones realizadas:** llamadas de solo lectura a GitHub para perfil, metadata de repositorio y lista de instalaciones; inspección documental de archivos adjuntos; consulta de documentación oficial pública de GitHub. **No se crearon o editaron repositorios, ramas, commits, tokens, instalaciones, settings, reglas, pruebas ni fuentes YU3DOH.**

## 1. Observaciones GitHub, separadas de inferencias

| ID | Pregunta | Evidencia observada | Estado / límite |
| --- | --- | --- | --- |
| GH-01 | Identidad autenticada | Perfil `nickname=KhaosMagnus`, user id `328893145` | **VERIFIED** para esta sesión; no identidad futura por inferencia |
| GH-02 | Tipo de cuenta propietario del origen | `KhaosMagnus/YU3DOH-Carder` owner type `User`, login `KhaosMagnus`, ID `328893145` | **VERIFIED**; propone mismo propietario para nuevo repo |
| GH-03 | Permisos observados en origen | `admin/maintain/pull/push/triage=true` en metadata del repositorio YU3DOH | **SOURCE-SCOPED**; NO extrapolar a destino ni token per-call |
| GH-04 | Existencia del destino | `get_repo(KhaosMagnus/Project-Control)` → HTTP 404 `NOT_FOUND` | **NOT ACCESSIBLE**; no prueba que el nombre esté libre ni no exista oculto |
| GH-05 | Instalación listada | ID `162412374`, account_login `KhaosMagnus`, `repository_selection=all` | **VERIFIED** para inventario expuesto; comprobar aplicación y permisos reales en GitHub UI |
| GH-06 | Identidad de App, matriz exacta de permisos | El endpoint de inventario accesible no expuso `permissions`, nombre/slug de aplicación, scopes per-call ni issuer | **NOT ESTABLISHED** |
| GH-07 | Plan GitHub de cuenta | El perfil y metadata de repositorio no exponen facturación/plan | **NOT ESTABLISHED**, requiere constatación Owner |
| GH-08 | Rama del origen | En el intake previo `main @ 54cc3aad246c89a29f2a18be63c539db68cae041`; `meta/project-control @ 056adb5097b7ce067082782e8d8c92b42db9082a` | **VERIFIED** al intake precedente; fuente inmutable |
| GH-09 | Existencia / reglas de destino | Destino no accesible, no hay configuración comprobable | **NOT CONFIGURED / NOT EVIDENCED**, no se declara seguridad |
| GH-10 | Capacidad de creación desde este conector | No aparece acción `create_repository` en la superficie de GitHub disponible; hay lecturas y otras mutaciones de recursos existentes | **NO CALLABLE CREATE REPOSITORY OBSERVED**; no se ejecutó ninguna acción |

**Riesgo R-01 (ALTO):** con `repository_selection=all`, no se puede asumir que crear el futuro repositorio bajo `KhaosMagnus` lo aísle de la instalación existente. Las instalaciones seleccionadas para «All repositories» abarcan los repositorios del ámbito correspondiente, incluidos futuros repositorios. Esto no prueba el alcance de escritura de cada acción. **Control propuesto:** antes de G2-B, Owner revisa la identidad de la GitHub App y sus repository permissions y decide explícitamente si restringir instalación a `Only select repositories` (requiere su propia autorización de modificación, sin afectar sin análisis el origen) o cambiar el diseño de propietario/identidades; no introducir una cuenta u organización alternativa sin decisión reservada.

## 2. Parámetros efectivos y recomendados

| Área | Propuesta de configuración | Naturaleza | Dependencia |
| --- | --- | --- | --- |
| Propietario | Cuenta personal `KhaosMagnus` | Propuesto, perfil verificado | Owner ratifica |
| Nombre | `Project-Control` | Propuesto, 404 a la conexión | Revalidar inmediatamente antes de G2-B |
| Visibilidad | **PRIVATE inicialmente**, sin datos operativos del adoptante | RECOMMENDED, no ejecutado | Plan y reglas privadas efectivamente disponibles |
| Plan | GitHub Pro o capacidad equivalente para protección de ramas en repo privado; **no afirmar actual plan** | CONDITIONAL | Owner verifica en `Settings → Billing & Licensing` y aporta evidencia no sensible |
| Rama producto | `main`: README/semilla inerte inicial; después protocolo, bootstrap, adapters, tests, docs, releases, provenance | RECOMMENDED | G2-B semilla; G3 importación por decisión posterior |
| Rama de gobierno maestro | `meta/project-control`: documento de génesis provisional; después estado, roles, solicitudes, decisiones, QA y rutas | RECOMMENDED | G2-B semilla; G3 bootstrap posterior |
| Relación Git entre ramas | Preferir raíces de historia independientes (`orphan`) y demostrar ausencia de merge-base; nunca fusionar gobierno con producto | RECOMMENDED | Ruta técnica aprobada y validador read-only |
| Feature branches | `feature/*` y `experiment/*` solo después de autorizaciones concretas | POLICY PROPOSED | No se crean en G2-B salvo alcance distinto explícito |
| Reglas | Dos protecciones explícitas para `main` y `meta/project-control`; evitar borrados, force pushes, bypass genérico, merges no aprobados | RECOMMENDED | Plan, capacidades de rulesets, actores concretos |
| Admin GitHub | Owner; facultad de configurar y rescatar repositorio | OWNER RESERVED | Sin herencia automática a PCM-001 |
| Coordinación PCM | Read-only hasta bootstrap+activación; luego edición documental únicamente bajo delegación verificada | PROVISIONAL | G3/G4 diferidos |
| QA | Función separada de autor y de integrador; lectura de candidatos exactos y reporte inmutable | RECOMMENDED | Nombramiento/criterios de independencia pendientes |
| Integrador | Escritor acotado a refs autorizadas tras Owner+QA; sin escritura automática por PCM | RECOMMENDED | Identidad/prueba de permisos pendientes |
| Conector GitHub | NO asumir aislamiento por proyecto ChatGPT; instalación actual `all` es exposición material | BLOCKER | Resolver R-01 antes de afirmar least privilege |

### 2.1 Restricción documentada del plan

La documentación oficial de GitHub indica que branch protections y branch/tag rulesets están disponibles para repositorios **públicos** con GitHub Free, y para **públicos y privados** con GitHub Pro/Team/Enterprise. Los **push rulesets** para repositorios privados tienen requisitos más exigentes (GitHub Team), por lo que no deben tratarse como control disponible con Pro sin verificar. La cuenta real es `NOT ESTABLISHED` hasta evidencia del Owner.

Fuentes: 
- https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches
- https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets

### 2.2 Matriz de permisos y fronteras propuestas

| Actor/rol | Leer control/producto | Publicar artefactos gobierno | Escribir `main`/release | Cambiar protecciones / instalaciones |
| --- | --- | --- | --- | --- |
| Owner | Sí | Decisiones reservadas y excepciones documentadas | Solo mediante integración explícita | Reservado, acto específico |
| PCM-001 (actual) | Sí en lo autorizado | **NO** | **NO** | **NO** |
| PCM-001 (futuro) | Según delegación | Índices/decisiones documentales delegados, no autoaprobación | **NO por defecto** | **NO** |
| Autor/Development | Lectura | Solo evidencias en rutas propias previa delegación | Candidatos en ramas autorizadas, nunca release directo | **NO** |
| QA independiente | Lectura | Informe aditivo de QA tras autorización | **NO** | **NO** |
| Integración | Lectura | Reporte de integración en ruta delegada | Únicamente fuente/objetivo y ventana autorizados | **NO** |
| App instalada `162412374` | Capacidad real por determinar | **UNKNOWN** | **UNKNOWN** | **UNKNOWN** |

Los roles conceptuales no son equivalentes a cuentas técnicas o token scopes. Las garantías de acceso deberán comprobarse en G2 posterior, sin realizar pruebas de mutación bajo G2-A.

## 3. Reglas de protección propuestas, no configuradas

**`main` (estándar):** bloquear delete/force push y exigir historia lineal, validación aplicable a cambios funcionales y revisión independiente cuando exista revisor habilitado; no integrar versiones ni releases solo por QA PASS. Fijar autenticidad de release (tag/digest/actor) en diseño posterior.

**`meta/project-control` (gobierno documental):** bloquear delete/force push, conservar historia aditiva, limitar quién mueve el ref, impedir sustitución silenciosa de contratos congelados y no recibir código/pruebas de producto. Para cambios de control, verificar Owner/competente autoridad, alcance, parent y nuevo SHA. Una simple regla de rama no garantiza restricción de contenido, independencia de identidades o ausencia de merges cruzados; inspección y QA documental siguen siendo necesarios.

**Bypass:** ninguno para actores no justificados. Las reglas en modo `evaluate/disabled` no equivalen a enforcement. Validar explícitamente status **Active**, rule-target patterns, bypass list y que la protección se aplica también al propietario/administradores según política elegida. La configuración de rulesets apila restricciones con branch protection: calcular el comportamiento efectivo, no contar pantallas aisladas.

**Advertencia:** reglas que exigen PR/revisión pueden bloquear el bootstrap si se activan antes de crear los commits semilla o si no existe revisor independiente disponible. Ordenar génesis → protecciones → inspección → G3; no activar suites de CI sin configuración/alcance autorizado.

Fuentes:
- https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository
- https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets

## 4. Procedimiento candidato G2-B, NO AUTORIZADO

**Prerequisitos STOP:** Owner aporta/coteja dos documentos pendientes; confirma plan/visibilidad; resuelve aplicación `repository_selection=all`; aprueba actor de creación, repo/ramas, archivos semilla exactos y mecanismo de control; define cuentas y pruebas permitidas; la operación tiene una autorización G2-B específica.

1. En GitHub, en sesión personal del Owner y sin reusar credenciales experimentales, verificar nuevamente si el nombre existe o está accesible, si la cuenta puede crear y si la visibilidad privada y reglas propuestas son realmente soportadas. Si existe algo con el nombre, STOP y conciliar; NO sobrescribir.
2. Crear **solo** el repositorio `KhaosMagnus/Project-Control` con visibilidad aprobada; no usar template YU3DOH, no transferir historial/archivos de YU3DOH y no habilitar automatizaciones no aprobadas.
3. Crear raíz mínima de `main` con una única semilla documental inerte marcada `NO GENERIC STANDARD ADOPTION / NO PRODUCT RELEASE`. La creación puede ser desde UI o un flujo git de Owner autorizado que pueda demostrar la identidad del primer commit. No copiar todavía protocolo/bootstraps.
4. Crear raíz **orphan** de `meta/project-control`, si el medio autorizado lo permite, sin ningún archivo de código/producto; añadir únicamente un `GENESIS_STATUS.md` provisional con las decisiones y límites exactos. Si se necesita un parent compartido por limitación técnica, STOP y someter una enmienda del diseño antes de escribir, no improvisar un merge.
5. Registrar SHA completo de ambos primeros commits, sus trees, padres, rutas y actor. Comprobar que `git merge-base main meta/project-control` no devuelve ancestro común cuando la modalidad aprobada sea orphan.
6. Activar las reglas de ambas ramas exclusivamente tras autorización y verificar su estado real, targets, bypass, protección de borrado/force push y semántica de actualizaciones. Evitar cualquier brecha innecesaria entre creación y protección; acotar la ventana de génesis a un actor y registrar las limitaciones de seguridad realmente observadas.
7. Entregar `G2-B_CREATION_RETURN`: repo id, owner, visibility, plan evidence, root commit SHAs, branch heads, enforcement proof, instalación/App scope observado, cambios realizados y cambios ausentes; adjudicar por Owner.
8. **STOP**. No ejecutar G3: ni importación, bootstrap, adopción del protocolo, activación, QA experimental, ni primer release.

El conector GitHub disponible en esta sesión **no expone un comando de creación de repositorio**; el método concreto de G2-B debe ser manual por Owner, GitHub CLI autorizado o otra ruta explícitamente inspeccionada/consentida. No se dispone de demostración de que el conector permita crear una rama orphan.

## 5. Recuperación y aceptación G2-B

**Recovery:** en caso de interrupción, recuperar con la identidad del repositorio y los SHAs exactos, leer ambos refs y trees por GitHub, comparar el ledger de acciones/Owner y los settings efectivos; no depender de chats. Si la creación queda parcial, marcar `G2-B PARTIAL / BLOCKED`, preservar evidencia e informar al Owner; **no borrar, resetear, forzar ni reparar automáticamente**. Un repositorio inicial sin protocolo/autoridad se mantiene INERTE; no es un bootstrap aceptado.

**Pruebas documentales posteriores permitidas únicamente bajo alcance específico:** verificaciones de existencia/ref/trees/history, distancia entre ramas, manifest SHA, lectura/reconstrucción por actor independiente, inspección de effective rules/installed apps. Pruebas negativas de escrituras, CAS, rechazo de force-push y controles de aislamiento de credenciales **requieren autorización posterior** (no están incluidas en G2-A), y sus resultados no rescatan las conclusiones históricas de Q02.

**Criterios de salida de G2-B:** fuente de verdad única y accesible; dos ramas exactas; separación de contenido y topología demostrada; protecciones activas y verificadas; Owner identificado; instalación/issuer y permisos reconciliados; no cambios a YU3DOH; ninguna importación/activación efectuada.

## 6. Brecha de los dos documentos de recepción

Archivos accesibles y hashes SHA-256 calculados sobre bytes adjuntos en esta conversación:

| Documento | SHA-256 local | Estado |
| --- | --- | --- |
| `PC_MASTER_DES_001_DUAL_PROJECT_SCOPE.md` | `820640547eb5c87185d871f2a359f69e033f1f5bf148914145fd93c4d70856ab` | Disponible y hash calculado; requiere cotejo con digest de emisor si se pretende certificación de identidad externa |
| `PC_MASTER_DES_001_INITIAL_TRANSFER.md` | `7067aa16e1145ba27b9a4b32c3efbb9b0d6e3bde8cd3cf14b3163f10b8e659e7` | Disponible y hash calculado; idem |
| `PC_MASTER_DES_001_PROJECT_INSTRUCTIONS.md` | `UNKNOWN` | **MISSING**, no hay copia de archivo para comprobar bytes |
| `PC_MASTER_DES_001_OWNER_ACCEPTANCE_ADDENDUM.md` | `UNKNOWN` | **MISSING**, no hay copia de archivo para comprobar bytes |

Las instrucciones de proyecto ya presentes en el entorno no sustituyen una copia verificable del documento original; el mensaje actual del Owner tampoco sustituye automáticamente el addendum documental formal. El cierre requiere **ambos archivos exactos** y **sus SHA-256 esperados de origen**; para mayor fuerza de procedencia, emisor/Owner, fecha y ubicación/commit o mecanismo de entrega. Una huella calculada sobre una copia recibida comprueba su integridad respecto de esa copia; compararla con un digest independiente de origen es lo que permite contrastar la transferencia. Si el documento fuente no está en GitHub, declararlo explícitamente en lugar de inventar un Git blob SHA.

## 7. Riesgos y prioridad

| Riesgo | Impacto | Evidencia / incertidumbre | Tratamiento |
| --- | --- | --- | --- |
| R-01 Instalación actual `all` incluye posible repo futuro | Alto | Selección `all` observada; permisos concretos no observados | STOP antes de afirmar aislamiento. Revisar identidad de app y seleccionar estrategia autorizada |
| R-02 GitHub Free con repositorio privado sin protección exigida | Alto | Plan NOT ESTABLISHED; GitHub documenta restricción | Verificar plan; Pro+ si protección privada es requisito, o Owner redefine arquitectura explícitamente |
| R-03 Creación insegura/genesis sin protección | Alto | Repo inexistente; pasos aún no autorizados | Publicación mínima, protección inmediata, validación y abortos definidos |
| R-04 Doble autoridad / admisión implícita | Alto | PCM provisional y G3/G4 DEFERRED | Bootstrap y cutover como decisiones independientes |
| R-05 Orphan no soportado en medio elegido | Medio | Herramientas no proporcionan garantía | Git CLI Owner autorizado o revisar diseño, STOP ante imposibilidad |
| R-06 Dos fuentes documentales ausentes | Medio/alto | Archivo y hash no disponibles | Solicitar copias y huellas, validar bytes/autoridad |
| R-07 CAS/issuer no demostrados | Alto para publishers futuros | Q02 y ONLINE-1C no han probado atomicidad y razón de fallo | Mantener NO-GO automatizado, pruebas separadamente autorizadas |

## 8. Solicitud de decisión y límites

**Recomendación actual:** `G2-A PARTIAL — REQUIRE EVIDENCE / G2-B DEFERRED`.

El Owner puede ordenar un complemento de G2-A con **evidencia solo de lectura** del plan GitHub y la instalación, sin abrir capacidad de escritura. Para la decisión G2-B hace falta adicionalmente:

1. Copia íntegra y SHA-256 de `PC_MASTER_DES_001_PROJECT_INSTRUCTIONS.md` y `PC_MASTER_DES_001_OWNER_ACCEPTANCE_ADDENDUM.md`.
2. Confirmación del plan de `KhaosMagnus` y soporte de protecciones sobre repos privados.
3. Identidad/nombre de la aplicación GitHub instalada ID `162412374`, permiso de repositorios (`Contents`, `Metadata`, `Administration`, `Workflows`, etc. según los que realmente aparezcan), elección explícita de su alcance `all` y efecto sobre `Project-Control`; NO cambiar todavía permisos.
4. Autorización posterior de G2-B con método, actor, archivos de génesis, ramas y política exacta de seguridad, sin incluir G3/G4.

No se invoca `GRANTED` por autodeclaración. Hasta entonces: `PCM-001 PROVISIONAL / NO GITHUB MUTATIONS / NO IMPORT / NO BOOTSTRAP / NO ACTIVATION / YU3DOH UNCHANGED`.

## 9. Enlaces normativos de consulta

- https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository
- https://docs.github.com/en/apps/using-github-apps/reviewing-and-modifying-installed-github-apps
- https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches
- https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets
- https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository
- https://docs.github.com/en/billing/how-tos/products/estimate-spending

**END — G2-A read-only report.**
