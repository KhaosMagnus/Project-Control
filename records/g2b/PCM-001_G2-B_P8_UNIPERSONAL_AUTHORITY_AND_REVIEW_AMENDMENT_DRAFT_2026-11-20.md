# PROJECT CONTROL MASTER — Enmienda propuesta al contrato G2-B: autoridad del Owner y revisión unipersonal

**Documento:** `PCM-G2B-P8-UNI-DES-001`  
**Autor:** `PROJECT_CONTROL_MASTER / PCM-001` (PROVISIONAL)  
**Fecha:** 2026-11-20 (America/Mexico_City)  
**Estado:** `DRAFT / DESIGN ONLY / NO EXECUTABLE AUTHORITY / FOCUSED QA PENDING / OWNER ACCEPTANCE PENDING`  
**Fuente de autorización:** `OWNER DECISION — PCM-G2B-P8-P5-DISPOSITION-001 / GRANTED DESIGN ONLY — OPTION B`, expresada directamente por el Owner en la conversación el 20 de noviembre de 2026.  
**Prohibiciones vigentes:** ninguna modificación GitHub, invitación, permiso, ruleset, rama, PR, aprobación, escritura, experimento, aceptación G2-B, G3, G4 o G5.

## 0. Propósito, precedencia y reconocimiento de error

El Owner **siempre conserva la revisión humana decisoria y la aceptación final**. La transferencia inicial, los documentos de génesis y el contrato ejecutivo reservan la aceptación G2-B al Owner después del QA. La coordinación de PCM-001 añadió en el diseño de perfiles la exigencia de `1 eligible independent GitHub review`, que terminó interpretando como **una segunda persona humana**. Esa extrapolación no se deduce automáticamente de la exigencia técnica de GitHub de que el *usuario que aprueba* no sea el *autor del PR*, ni de la autoridad de aceptación que el Owner había reservado para sí. **El error de interpretación y de conducción es atribuible a PCM-001**, no al Owner.

El requisito de revisor GitHub independiente quedó, no obstante, **escrito en contratos aprobados**; por ello no se elimina retroactivamente mediante esta aclaración. El contrato congelado sigue siendo la referencia histórica hasta que exista QA focalizada, aceptación expresa del Owner y una enmienda de precedencia prospectiva. Se conserva la no conformidad de transición **P5→P6**: se ejecutó P6 sin acreditar una ruta de aprobación independiente como exigía literalmente el contrato entonces vigente. El Owner la ha reconocido como desviación histórica; **no hay convalidación retroactiva**.

Esta enmienda distingue cuatro controles que antes se confundieron:

| Control | Autoridad o sujeto | Lo que verifica y lo que NO significa |
|---|---|---|
| **Aceptación del Owner** | Persona física Owner | Decisión reservada de aceptar alcance, riesgos, integración, infraestructura o releases. Es indispensable y **no depende de que exista una segunda persona física**. No es automáticamente un `Approve` válido de GitHub. |
| **Revisión humana de contenido y riesgos** | El mismo Owner | Inspección real de diffs, árboles, linajes, QA y evidencia antes de autorizar; registrable y separada en el tiempo del acto de preparar el cambio. No equivale a *independencia entre personas*. |
| **Aprobación técnica de PR de GitHub** | Cuenta elegible distinta de la cuenta autora del PR | Satisface rulesets `R-MAIN`/`R-META` solo si GitHub computa la aprobación y el PR supera todas sus condiciones. La distinción de cuentas **no acredita dos personas**. |
| **QA documental independiente de artefactos** | Revisiones separadas, por ejemplo ChatGPT y Grok | Inspección autónoma del mismo paquete congelado; emitir `PASS/FAIL/INCONCLUSIVE` y pruebas observadas. **Los modelos no son una segunda persona humana ni reemplazan la aceptación del Owner.** |

## 1. Fuentes históricas congeladas y alcance exacto de la corrección

Se mantienen íntegras, sin sobrescritura:

| Fuente | SHA-256 |
|---|---|
| Contrato G2-B ejecutivo autorizado por Owner | `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349` |
| Runbook P0–P8 | `be382147d5ce5b9875625cd8436d4ed31c2bcc9ee93da79a068bad8b50c66b78` |
| Contrato de QA Q1–Q9 | `a1c10a91bc0947e3a84d4c8d48da404c7494f45154e8613c0a65bdd07b6633b3` |
| Corrección de diseño R5 | `9c329b3c4be0dca6cf60bc27e92bd586a931c9236bd786f402ce508f952562e8` |
| Conciliación P8 de doble QA | `90b9ed72050022bbc3e8307e80de75019bbf5d370b4d28039c947c9891d63d08` |
| QA1 ChatGPT P8 (Library) | `945acec3dd5fb5450aadbc30a3d3b06d0660af300f73d666e410d604e881c80f` |
| QA2 Grok P8 | `90a62af52e0c925818c98a617beb2710cc7f58da760ea538718a4d8de5f46349` |

**Precedencia propuesta, NO vigente:** en una futura aceptación expresa del Owner, las cláusulas de esta enmienda referentes a identidad humana, revisor de PR, elegibilidad Q6 y transición prospectiva prevalecerán **solo para ese alcance** sobre G2-B §3 P5, §4 y Q6. Las raíces, los SHA, la visibilidad pública, protección de borrados/force-push, separación `main`/`meta`, autoridad de decisión del Owner, QA y prohibición de merges cruzados no cambian. La enmienda no modifica el protocolo genérico congelado ni define automáticamente reglas para adoptantes.

## 2. Modelo propuesto: una persona Owner, identidades técnicas separadas

**Actores observados:** persona Owner controla `KhaosMagnus` y `JormungandrMagnus`. Ambas son cuentas GitHub distintas; **no hay independencia humana** entre ellas. No se propone disfrazar esta limitación.

| Función | Identidad propuesta | Restricción |
|---|---|---|
| Owner, revisor humano y aceptador final | Owner, desde `KhaosMagnus` | Lee y decide sobre evidencias; aprueba como usuario GitHub **solo cuando NO sea autor del PR** y GitHub confirme elegibilidad. |
| Autor técnico de futuras propuestas | `JormungandrMagnus` (segunda cuenta, bajo el mismo Owner) | En su momento, y solo bajo autorización por operación, podrá proponer un PR desde una rama/fork de su titularidad hacia la **misma familia de historia**; no se presupone escritura al maestro. |
| Coordinación, preparación de alcance y autorización | `PCM-001` provisional, sin credenciales heredadas | Prepara expedientes y comprueba evidencia en lectura. No se autoautoriza ni acepta por el Owner. |
| QA de contenido | ChatGPT y Grok en encargos separados | Evaluaciones independientes como procesos/documentos, sin equivalencia a independencia de personas; sin aprobaciones GitHub ni escrituras. |
| Integración | Función autorizada expresamente por Owner | Puede recaer operativamente en el Owner bajo separación **de actos y evidencia**, no separación de personas. Confirma reglas, método, refs y readback. |

**No se afirma segregación real de personas, de administración ni de credenciales.** La persona Owner controla las dos identidades y la administración del repositorio. La revisión de contenido por el Owner sigue siendo efectiva, pero **es autogobierno con doble comprobación**, no aprobación independiente de otro humano. El riesgo de sesgo y error correlacionado es residual y se reconoce expresamente.

## 3. Ruta propuesta para FUTURAS PR, no para la génesis ejecutada

La regla GitHub se mantiene: PR obligatorio, **una aprobación elegible** y linaje lineal (`squash` o `rebase`) en ambas refs. La documentación de GitHub indica que el autor de un PR no puede aprobar su propio PR y que las aprobaciones exigidas deben ser computables para la rama protegida. En principio es posible que la cuenta del Owner apruebe una PR abierta por otra cuenta; la viabilidad del circuito **no se ha probado en este repositorio**.

1. **Autorización de preparación por operación.** El Owner decide rama destino (`main` o `meta/project-control`), alcance, actor técnico, superficies visibles y límites; sin habilitación implícita por esta enmienda. Toda candidata parte del linaje de la misma rama. Prohibido PR que fusione `main` y `meta/project-control` entre sí.
2. **Propuesta de autor técnico.** Bajo GRANTED separado, la cuenta `JormungandrMagnus` puede preparar una rama de fuente propia, previsiblemente mediante fork de repositorio público. Debe comprobarse antes si GitHub permite esa ruta de PR hacia la ref correspondiente, sin añadir al autor al repositorio maestro. Ningún fork, PR o push está autorizado ahora.
3. **Congelación de aprobación previa.** Documentar PR/autor, destino, base `B`, cabeza `H`, delta `D`, árbol de salida `T_expected`, método (`squash` o `rebase`), rutas permitidas, permisos y evidencia de QA, como establece R5. Cambios materiales requieren nueva disposición previa.
4. **QA documental independiente.** Dos evaluaciones de un mismo candidato congelado cuando el contrato del cambio lo requiera; desacuerdos o insuficiencia se devuelven al Owner. QA no representa personas separadas ni es aprobación GitHub.
5. **Revisión y aceptación humanas.** El Owner inspecciona el diff/árbol/riesgos, registra `ACCEPT/REVISE/DEFER` y, **solo si** GitHub considera al Owner revisor elegible y no es autor del PR, emite `Approve` desde `KhaosMagnus`. La aceptación del Owner y el `Approve` son dos acciones distintas, aunque las ejecute la misma persona.
6. **Preflight de integración.** Confirmar que GitHub contabilizó las aprobaciones; `B/H/D/T_expected` vigentes; rutas, rulesets, ausencia de bypass, autoría y cuenta ejecutora correctos; método habilitado. `UNKNOWN` o cambios de alcance → STOP. No se presume CAS.
7. **Integración y readback.** Exclusivamente bajo GRANTED de integración: usar el método autorizado, comprobar `C`, árbol final, delta, continuidad de linaje y ausencia de contaminación cruzada. No inferir autorización de G3, G4, G5.
8. **Aceptación posterior del resultado.** Disposición distinta del Owner que registra el SHA final; no debe confundirse con autorización previa ni con el `Approve` de GitHub.

**Casos STOP obligatorios:** (a) PR abierto desde `KhaosMagnus` cuando el mismo usuario pretenda aprobarlo; (b) el `Approve` no cuenta para la protección; (c) método de integración global incompatible; (d) exige aprobaciones adicionales no disponibles; (e) base/candidata cambian materialmente; (f) cambios entre las historias; (g) cualquier ajuste de permisos/rulesets necesario y no autorizado. No se desactiva silenciosamente la revisión ni se añade un bypass para desbloquear.

**Caveat GitHub observable:** los dos rulesets actuales tienen `require_extra_approval_for_unattributed_changes=true`. GitHub documenta que esta opción puede exigir aprobación adicional cuando Copilot abre un PR sin colaborador humano atribuido. Por tanto, **no** se supone que un PR creado por Copilot sin atribución humana pueda aprobarse con una sola revisión del Owner. Esa ruta queda fuera del procedimiento unipersonal hasta una validación y decisión específica; el autor técnico nominal es la segunda **cuenta GitHub humana controlada por Owner**, no una PR emitida por Copilot.

## 4. Corrección propuesta de P5/Q6 y tratamiento de la desviación histórica

### 4.1 P5 prospectivo para génesis

El propósito de P5 es acreditar que `R-MAIN` esté `active` para `main`, con PR, una aprobación de GitHub, historial lineal, reglas de seguridad y sin bypass, y que exista un diseño verificable **propuesto** para la primera actualización. **En génesis no hay PR que aprobar.** La elegibilidad operativa y la contabilidad real de una aprobación se verifican en la autorización particular para la **primera PR**, no se simulan durante génesis. Que el Owner haya inspeccionado y aceptado la configuración de P5 es una **revisión humana**, no `Approve` de una PR.

Esta reformulación **modifica** el antiguo criterio `P5 STOP antes de P6 si el revisor independiente no es demostrablemente viable`; por ello exige aprobación formal prospectiva y QA focalizada. No debe reinterpretarse como si ya hubiera regido al publicar la segunda raíz.

### 4.2 Q6 prospectivo y resultados P8

Se propone dividir Q6 en:
- `Q6a — CONFIGURATION`: comprobar `R-MAIN/R-META`, selectores, seguridad, PR, approvals, métodos, historia lineal y bypass. Estado remoto actual: **VERIFIED** en ese alcance.
- `Q6b — GOVERNANCE MODEL`: confirmar que el Owner es la persona que revisa/acepta, que las cuentas técnicas no acreditan independencia humana, y que QA por modelos es diferente de aceptación. Estado documental: **propuesto para QA**.
- `Q6c — FIRST-PR ELIGIBILITY`: prueba de viabilidad concreta de autor/Owner reviewer de GitHub, fork/ruta de PR y regla de aprobaciones; **NOT TESTED/DEFERRED** hasta una autorización futura específica. No declarar `PASS` de operación por aprobación de diseño.

Los informes P8 ChatGPT y Grok **permanecen INCONCLUSIVE** contra el contrato de su fecha. Grok clasificó elegibilidad como `FAILED`; ese resultado histórico se conserva. No se reemplaza por `PASS` ni se afirma que la desviación P5→P6 estuviese autorizada.

### 4.3 No conformidad inmutable P5→P6

- **Hecho:** `main` y `meta/project-control` existen con SHA aprobados; ambos rulesets están activos.
- **Incumplimiento:** se permitió P6 sin acreditar el criterio literal de elegibilidad previsto por G2-B P5.
- **Responsabilidad de conducción:** PCM-001 facilitó instrucciones para avanzar tratando la revisión de configuración del Owner como suficiente, pese a la condición anterior.
- **Disposición propuesta:** `NONCONFORMITY ACCEPTED FOR HISTORICAL RECORD, NOT RETROACTIVELY CURED`; conservar evidencia original, commits y reglas; no borrar, recrear o reescribir.
- **Decisión posterior reservada:** el Owner deberá aceptar o rechazar expresamente el riesgo residual y el método prospectivo. Esto no es aún aceptación de la infraestructura G2-B.

## 5. Condiciones de aceptación de la enmienda y del G2-B pendiente

La presente decisión del Owner permite **solo diseño**. Para que esta enmienda tenga eficacia de contrato:

1. Dos revisiones focalizadas de QA documental reciben **el mismo paquete congelado**, examinan fidelidad a la autoridad del Owner, GitHub PR, separación de personas/cuentas/roles, caveats de Copilot, P5/Q6 y permanencia de no conformidad. `PASS/REVISE/FAIL/INCONCLUSIVE` por evaluador; PCM-001 concilia y propone.
2. El Owner examina el candidato exacto con SHA-256 y emite `ACCEPT/REVISE/DEFER` específico. Hasta ello el contrato ejecutivo original sigue vigente, incluida la descripción histórica P5 y la exigencia de aceptación G2-B tras QA.
3. Para el G2-B integral sigue faltando resolver Q7 (snapshot administrativo posterior a creación), Q5/Q8 (límites de cronología y evidencia original) y Q9 (declaración de incidentes/no observación). No sustituir ausencia de prueba histórica por ficción. Si se pretende modificar el criterio histórico de **dos QA `PASS` para aceptación G2-B**, debe proponerse y aceptarse explícitamente una decisión separada; esta enmienda **no lo cambia automáticamente**.
4. La validación de la primera PR de autor técnico/revisión Owner requiere un gate adicional de prueba controlada y un nuevo permiso específico. No está dentro de G2-B ni de esta enmienda de diseño.
5. Ninguna versión de este documento habilita importación G3, activación G4, adopción G5, release, modificación de permisos o rulesets, ni publicación en `main` o `meta/project-control`.

## 6. Estado actual verificable (snapshot de lectura)

- Repo público `KhaosMagnus/Project-Control`, ID `1465064417`.
- `main`: `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`, root sin padres, README blob `56fd6d6560434e067c126c152ab86298bd57d61f`.
- `meta/project-control`: `cac838940e0e824a1f828ff660e422a6441a1da7`, root sin padres, README blob `2b30688846710fe73b89a537bb5a8cfb21e738eb`.
- Rulesets activos: `PCM-GENESIS-SAFETY` ID `27708103`, `R-MAIN` ID `27709862`, `R-META` ID `27717600`; los perfiles exigen una aprobación, `squash`/`rebase`, historial lineal, lista de bypass vacía y el parámetro adicional antes descrito.
- Instalación `162412374`: conexión observada `repository_selection=selected`; evidencia administrativa posterior completa continúa pendiente.

Los objetos y reglas remotos se leen como evidencia de infraestructura existente. **No se han modificado** para preparar esta propuesta.

---

**Disposición de PCM-001:** `UNIPERSONAL DESIGN DRAFT COMPLETE / INDEPENDENT FOCUSED QA NEXT / NO EXECUTABLE AUTHORITY / G2-B NOT ACCEPTED / G3–G5 DEFERRED`.
