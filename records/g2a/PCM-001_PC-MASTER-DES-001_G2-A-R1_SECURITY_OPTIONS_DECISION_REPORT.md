# PCM-001 — PC-MASTER-DES-001 / G2-A-R1
## Informe complementario de arquitectura, privacidad, permisos y decisión

**Fecha de análisis:** 2026-11-11 (America/Mexico_City)
**SOURCE:** PROJECT_CONTROL / PC-004 — YU3DOH Carder
**TARGET:** PROJECT_CONTROL_MASTER / PCM-001 (PROVISIONAL)
**MODE:** EVIDENCE INTAKE / ARCHITECTURE DECISION PREPARATION / READ-ONLY
**OWNER AUTHORITY:** D1 GRANTED; D2 G2-A PREFLIGHT ONLY GRANTED; G2-B, D3 y D4 DEFERRED
**EJECUCIÓN:** NONE. No se modificaron repositorios, ramas, reglas, instalaciones, permisos ni credenciales.

## 1. Dictamen

**RECOMMENDATION: B — GitHub Pro + repositorio privado + acceso seleccionado**, sujeto a verificar la contratación efectiva, reconstruir las dependencias de la instalación actual, reducir su alcance mediante autorización separada y probar reglas/recuperación antes de ejecutar bootstrap. Es la alternativa que mejor preserva la confidencialidad de `meta/project-control` y permite las protecciones de ramas requeridas en el mismo repositorio. No basta por sí sola para acreditar identidades distintas, CAS atómico, segregación por rol o aislamiento técnico completo.

**A — GitHub Free + público + seleccionado** es técnicamente elegible para protecciones de ramas y no requiere suscripción, pero **solo aceptable** si el Owner aprueba la publicidad irreversible de toda la historia de **ambas** ramas y confirma por revisión que los registros de gobierno y seguridad serán públicos/sanitizados. Puede ser preferible a B para un estándar intencionalmente abierto con gobierno totalmente publicable, pero ese requisito no está acreditado.

**C — GitHub Free + privado** es **NO-GO para el contrato vigente**: carece de branch protection/rulesets en repositorios privados según GitHub Docs, aunque sí permite crear repositorios privados. Ser privado no protege refs contra escrituras privilegiadas ni equivale a control de concurrencia.

## 2. Integridad documental

Se dispuso de los cuatro originales y se calcularon SHA-256 sobre los archivos locales. Los tres hashes declarados en el addendum coinciden byte a byte:

| Archivo | SHA-256 calculado | Contraste |
|---|---|---|
| `PC_MASTER_DES_001_DUAL_PROJECT_SCOPE.md` | `820640547eb5c87185d871f2a359f69e033f1f5bf148914145fd93c4d70856ab` | MATCH, declarado por addendum |
| `PC_MASTER_DES_001_PROJECT_INSTRUCTIONS.md` | `58540642f1fe566e78d6507355cc7b2f49534b8e33361c5aaaf0404f2637cf62` | MATCH, declarado por addendum |
| `PC_MASTER_DES_001_INITIAL_TRANSFER.md` | `7067aa16e1145ba27b9a4b32c3ef14b3163f10b8e659e7` | MATCH, declarado por addendum |
| `PC_MASTER_DES_001_OWNER_ACCEPTANCE_ADDENDUM.md` | `06c0f6052ccb663b464847a9f4578beddf5424115ec42a180f73dc612ebf3cb4` | Hash calculado ahora; sin hash de tercero previo contra el cual comparar |

**DISPOSITION:** DOCUMENT_INTAKE COMPLETE / 3 DECLARED DIGESTS MATCH / ADDENDUM LOCAL DIGEST ESTABLISHED. Se cierra la brecha de archivos ausentes. El hash del addendum es una identidad de bytes; su autenticidad independiente no puede inferirse de un valor autorreferido o derivado después de la recepción. El Owner ha comunicado directamente la aceptación y las disposiciones G2 en la conversación actual.

Las instrucciones originales mantienen provisional `PCM-001` y autorizaciones de escritura nulas. El addendum tiene precedencia temporal sobre las notas anteriores de “Owner Review Pending” y “ChatGPT Project not yet created” sin alterar los documentos originales.

## 3. Evidencia de GitHub y sus límites

### 3.1 Observado independientemente por conector GitHub, lectura solamente

- Cuenta autenticada: `KhaosMagnus`, GitHub User ID `328893145`.
- Instalación listada: ID `162412374`, `account_login=KhaosMagnus`, `account_type=User`, `repository_selection=all`, sin testing override.
- `KhaosMagnus/Project-Control`: `404 NOT_FOUND` en consulta de repositorio; **no prueba disponibilidad de nombre** ni permite demostrar configuración inexistente.
- El origen `KhaosMagnus/YU3DOH-Carder` sigue visible, público, con permisos admin/push en la credencial conectada (no son prueba de scopes efectivos por operación).
- Búsqueda de repositorios instalados con consulta vacía: 11 repositorios visibles, sin más elementos en la siguiente página. Es **inventario candidato**, no prueba de que cada repositorio dependa de acciones de la instalación ni prueba de que no existan otras rutas de autorización. Repositorios visibles: `PLXMonitor`, `YU3DOH-Model-Showcase`, `YU3DOH-LoRA-Profiler`, `NazarickBot`, `YU3DOH-Carder`, `Orgizador-Biblioteca`, `YU3DOH-PromptKit`, `certificador-aoi`, `YU3DOH-Aspect-Ratio-Visualizer`, `Bot-MO-SHI`, `Respaldo` (todos bajo `KhaosMagnus`). No portar este inventario a un repositorio público sin revisión de privacidad.

### 3.2 Owner-reported / transferencia PC-004 (no capturas reexaminadas por esta instancia)

- Plan actual: **GitHub Free**.
- Nombre de app: **ChatGPT Codex Connector**.
- Permisos observados: lectura de checks/status/metadata, lectura/escritura de actions/code/issues/PR/workflows; autorización de usuario para identidad, acceso a recursos y correo.
- No se reportan cambios a instalación.

La identidad y selección `all` quedaron también corroboradas mediante conector. El plan y la presentación visual exacta de permisos provienen de la evidencia facilitada por el Owner y transmitida por PC-004, no de un endpoint de facturación accesible aquí. El conector no ofrece prueba de token por operación ni capacidades del mecanismo CAS.

### 3.3 Normativa GitHub verificada, 2026-11-11

- Branch protection: GitHub Free en repositorios **públicos**, GitHub Pro en repositorios públicos y **privados**.
  https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches
- Repository rulesets: GitHub Free público y GitHub Pro privado/público; **push rulesets** en repositorios privados tienen restricciones de plan más fuertes y no deben confundirse con branch rulesets.
  https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets
- GitHub Pro incluye protected branches y revisores requeridos en repositorios privados de cuentas personales.
  https://docs.github.com/en/get-started/learning-about-github/githubs-plans
- La instalación GitHub App puede seleccionarse para `all` o `only select repositories`; en `all`, los repos futuros caen en su alcance. Incluso con `selected`, los repositorios públicos mantienen exposición de lectura pública; la selección es una frontera de capacidades de la app, no de visibilidad pública ni una garantía de identidad de ejecutor.
  https://docs.github.com/en/apps/using-github-apps/reviewing-and-modifying-installed-github-apps
  https://docs.github.com/en/apps/using-github-apps/installing-a-github-app-from-a-third-party
- Tokens GitHub App de usuario solo pueden acceder a la intersección de accesos del usuario y la app; tokens de instalación tienen alcance de los repositorios autorizados a la instalación. Esta propiedad documental no demuestra cuál token usa cada operación en ChatGPT Work.
  https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/generating-a-user-access-token-for-a-github-app
  https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/authenticating-as-a-github-app-installation
- Para cuentas personales, la documentación histórica de GitHub indica GitHub Pro ~USD 4/mes. Confirmar monto actual, periodicidad, impuestos y divisa **en la pantalla de contratación** antes de decisión de compra; no se ha verificado precio contractual para esta cuenta.
  https://docs.github.com/en/get-started/learning-about-github/faq-about-changes-to-githubs-plans
  https://docs.github.com/en/billing/how-tos/manage-plan-and-licenses/upgrade-plan

## 4. Comparativa de opciones

| Criterio | A. Free / Público / Selected | B. Pro / Privado / Selected | C. Free / Privado |
|---|---|---|---|
| Cuota base | USD 0 | Históricamente ~USD 4/mes; confirmar checkout | USD 0 |
| Control de visibilidad de `main` y `meta/*` | Ninguno: ambos públicos en un mismo repo | Sí, ambos privados para público general | Sí, ambos privados para público general |
| Branch protection | Disponible | Disponible | **No disponible** |
| Branch rulesets | Disponibles (funciones según tipo) | Disponibles (funciones según tipo) | **No disponibles** |
| Control de escrituras de la app por repo | Potencial tras pasar de `all` a selección efectiva; requiere prueba | Igual; Pro no modifica scopes de app | Igual, pero sin controles necesarios sobre refs |
| QA independiente, identidades y CAS | No probado | No probado | No probado |
| Compatibilidad con estándares congelados | Condicional a reglas e importación/QA | Condicional a reglas e importación/QA | Insuficiente para política de protección requerida |
| Principal riesgo | Divulgación e historia pública irreversible | Coste y falsa sensación de aislamiento si app sigue en `all` | Ref no protegido pese a privacidad |
| Disposición | `CONDITIONAL` | **`PREFERRED — CONDITIONAL`** | `NO-GO` |

**No confundir rama con ACL:** separar `main` de `meta/project-control` permite historias y normas diferentes, **no** restringe lectura de una sola rama en un repositorio público ni da permisos por rama automáticamente. En un repositorio privado, ambos quedan privados respecto al público, pero los usuarios con acceso al repositorio normalmente ven ambas ramas.

**No confundir protección con infalsificabilidad:** en un repositorio personal, quien puede administrar las reglas puede modificarlas. Las protecciones reducen mutaciones accidentales o no autorizadas por los flujos ordinarios, pero no sustituyen custodia de evidencia, verificaciones externas ni control sobre el Owner administrador.

## 5. Matriz de riesgos (impacto × probabilidad cualitativos)

| Riesgo | Impacto | Probabilidad condicionada | Tratamiento |
|---|---|---|---|
| App `all` incluye repositorio nuevo | Alto | Alta si se crea sin cambiar instalación | No declarar aislamiento; autorización separada para restricción antes de creación o STOP |
| A: exposición de gobierno, rutas de recuperación o evidencia | Alto | Alta si tales datos se publican | Puerta de clasificación y sanitización **antes del primer commit público** |
| C: control refs privado sin protección efectiva | Alto | Alta bajo Free actual | Rechazar C para este contrato |
| Cambiar instalación rompe flujos GitHub existentes | Alto | Indeterminada hasta inventario | Mapear dependencias y rollbacks antes de cambio |
| Requerir PR/revisor/checks sin ejecutores habilitados | Medio/alto | Condicional | Probar política, asignar revisor externo, configurar etapa inicial sin lockout |
| CAS/issuer no verificados | Alto | Sin evidencia para concluir | Bloquear publicador autónomo y escrituras multiwriter hasta prueba específica, sin reactivar PP-002 |
| Brecha inicial de repositorio antes de aplicar reglas | Medio/alto | Inherente a secuencia si no se prepara | Inicialización mínima de Owner, aplicar reglas lo antes posible, verificar refs y auditoría; no reclamar protección retroactiva |

## 6. Arquitectura propuesta y procedimiento condicionado de G2-B (NO AUTORIZADO)

**Precondiciones no ejecutadas:** Owner selecciona A o B; verifica facturación si B; completa clasificación del contenido publicable si A; delimita install scope actual y dependencias; aprueba esquema de protección; fija actor e instrucciones de recuperación; autoriza exactamente los cambios que ejecutará él o el agente designado.

### Repositorio

- Identidad: `KhaosMagnus/Project-Control`; visibilidad elegida **al crear**, no por corrección posterior de exposición.
- Rama `main`: producto estándar. En G2-B solo la génesis mínima, sin importar todavía protocolo/bootstrap/adaptadores ni emitir release.
- Rama `meta/project-control`: gobierno documental del **maestro**, nunca del adoptante. Preferencia: historia inicial orphan, si herramienta disponible y segura; de lo contrario árbol documental inicial y parentage explícitos con regla de **NO MERGE** permanente.
- Identidades y políticas locales no heredan historia o permisos de YU3DOH. Protecciones de ambas ramas: negar borrado y force-push, aplicar a admins cuando la opción exista, historial lineal si compatible, revisiones y checks solo cuando hay revisor/ruta realmente disponible y roles definidos. Documentar límites y bypasses efectivos.

### Secuencia segura propuesta

0. **Antes de cambios:** Owner autoriza expresamente plan de visibilidad, coste, lista de repositorios admitidos, efecto de alcance sobre flujos existentes y quien puede modificar instalación. Congelar mapa de dependencias y procedimiento de rollback.
1. **Acceso:** una autorización distinta de G2-A debe permitir cambiar `162412374` de `all` a `selected` (incluyendo los repositorios que efectivamente necesiten la app), preferentemente **antes de crear el repositorio maestro**. No retirar repos existentes sin diagnóstico. Comprobar post-cambio la selección y funcionamiento de rutas críticas; detenerse si aparece regresión. Si no es posible reducir el alcance sin riesgo, revisar arquitectura/identidad propietaria; no aceptar `all` como aislado.
2. **Crear infraestructura:** únicamente con G2-B explícito, Owner o actor autorizado crea repositorio vacío con visibilidad preaprobada. No inicializar simultáneamente protocolo, runners, workflows, claves o tokens. Comprobar inmediatamente ID, URL y visibilidad exactos.
3. **Génesis controlada:** establecer ramas con registros mínimos si G2-B lo permite, capturar commits/trees/ref parentage. Configurar branch rulesets/protection según capacidad real, inspeccionar cumplimiento y ausencia de bypasses imprevistos; el administrador conserva capacidad de cambiar reglas, por lo que hay riesgo residual.
4. **Postflight:** releer refs, SHA exactos, políticas de protección, instalación y repos fuente. Guardar reporte sin modificar material congelado. Si los requisitos de seguridad fallan, clasificar `G2-B BLOCKED`; no pasar a importación.
5. **G3 separado:** importación selectiva y reproducible, manifest y SHA-256, QA independiente y bootstrap requieren nuevas autorizaciones. **G4 separado:** activación PCM-001 y cutover requieren decisión posterior.

**Condición de creación inicial:** no se requiere que el repositorio ya exista para autorizar un preflight; sí se requiere que el Owner acepte las limitaciones de la ventana entre creación y aplicación efectiva de reglas y establezca un método de ejecución verificable. No prometer protección retroactiva.

### Recuperación

Ante fallo, STOP sin force/reset y sin seguir con G3; preservar repositorio y refs observados; documentar estado de instalación antes/después, allowed set y funcionamiento de proyectos afectados; aplicar rollback de instalación solo si estaba específicamente autorizado y si puede restaurar la selección previa sin interrumpir otros sistemas; reconsultar todas las identidades; permitir al Owner decidir si conservar/quarantinar un repo vacío o corregir configuración. No reescribir la historia de YU3DOH ni recuperar con privilegios ampliados por defecto.

## 7. Solicitud de decisión al Owner

**PCM-001 / G2-A-R1 — REQUEST FOR OWNER DISPOSITION**

1. **Selección de arquitectura:** `B — GitHub Pro, repositorio privado, acceso selected` (recomendación); o `A — GitHub Free, público, selected` con aceptación expresa de publicación integral de ambas ramas. `C — Free, privado` se recomienda rechazar para el contrato actual. Solicito `GRANTED / REVISE / DEFERRED` para la **elección de diseño**, **NO para compra, creación ni cambios de acceso**.
2. **Inventario de dependencias:** autorizar por decisión posterior el alcance concreto y el responsable de cambio de instalación, con lista permitida de repos, rollback y QA de rutas críticas. Hasta entonces `162412374=all` permanece sin cambios.
3. **G2-B:** mantener `DEFERRED` hasta formalizar la opción, verificar restricciones reales, resolver la exposición por instalación y aprobar una acción de escritura exacta, separada y auditable.
4. **G3 y G4:** mantener `DEFERRED`; PCM-001 `PROVISIONAL`; Q02/ONLINE-1C sin alteración.

**STOP STATE:** `G2-A-R1 DOC COMPLETE / OPTIONS ASSESSED / SELECTED ACCESS NOT ESTABLISHED / G2-B DEFERRED / D3 DEFERRED / D4 DEFERRED / NO GITHUB MUTATIONS`.
