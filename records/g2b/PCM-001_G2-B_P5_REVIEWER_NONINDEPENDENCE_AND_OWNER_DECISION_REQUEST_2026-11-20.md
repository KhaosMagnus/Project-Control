# PCM-001 — G2-B / P5 — Disposición sobre elegibilidad de revisor y solicitud de decisión

**Fecha:** 2026-11-20  
**Asignación:** `PCM-G2B-P5-REVIEWER-ELIGIBILITY-001`  
**Modo:** RECEPCIÓN DOCUMENTAL / SIN MODIFICACIONES GITHUB  
**Estado:** `P5 STOP — REVIEWER ELIGIBILITY NOT SATISFIED`  
**Autoridad:** Owner conserva decisiones sobre colaboradores, seguridad, cambios de diseño y cualquier continuidad de G2-B.

## 1. Evidencia y límites

1. **Owner, declaración directa:** no hay colaboradores agregados a `KhaosMagnus/Project-Control`; `JormungandrMagnus` es una cuenta bajo control del propio Owner, que controla igualmente `KhaosMagnus`.
2. **Segunda instancia:** identidad autenticada `JormungandrMagnus` (ID `354016236`), distinta técnicamente del Owner `KhaosMagnus` (ID `328893145`). La lectura de `get_repo` mostró `pull=true`, `push=false`; la consulta de permisos efectivos resultó `403 Resource not accessible by integration`.
3. **PCM-001 lectura GitHub:** `R-MAIN` ID `27709862` activo para `refs/heads/main`, exige PR y al menos una aprobación, historia lineal, sin bypass, con métodos permitidos squash y rebase. `PCM-GENESIS-SAFETY` ID `27708103` activo sobre `main` y `meta/project-control`, sin bypass, impide borrado y force-push. Única rama publicada `main`, commit raíz `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`. `meta/project-control` no publicada.
4. **GitHub documentación:** para satisfacer revisiones requeridas se necesita revisor con permiso de escritura; un autor de PR no puede aprobar su propio PR. En un repositorio personal, agregar un colaborador concede capacidades de escritura, no solo lectura.

**Determinación:** `JormungandrMagnus` no está acreditada como revisor elegible por permisos y, por declaración directa del Owner, **no constituye una segunda persona independiente**. El 403 de permisos no es evidencia de denegación ni de concesión, y no debe usarse para inferir más de lo observado. Aunque ambas cuentas fuesen técnicamente habilitadas, ello no resolvería la independencia humana exigida por el contrato aceptado.

## 2. Disposición de gate

- `P5 CONFIGURATION`: PASS (rulesets activos y adecuados).
- `P5 REVIEWER ELIGIBILITY / INDEPENDENCE`: NO SATISFECHO.
- `P5 OVERALL`: **STOP / NO CERRADO**.
- `P6`: NO AVANZAR ni publicar la segunda raíz.
- `P1–P4`: sus verificaciones no se invalidan por este hallazgo.
- Ningún cambio de permisos, invitaciones, rulesets, ramas, pushes ni aceptación de nuevas etapas está autorizado por esta disposición.

## 3. Alternativas y coste de oportunidad

### Ruta A — Conservar independencia humana [PREFERENTE SI ES UN CONTROL IRRENUNCIABLE]

El Owner identifica a **otra persona real, independiente del autor y del integrador cuando el contrato lo exija**, con cuenta GitHub propia, y decide si acepta el riesgo de otorgarle permisos de escritura al repositorio personal. Requiere autorización de alcance mínimo y específica para invitarla; verificar aceptación, acceso efectivo, separación de personas y que pueda aprobar un PR elegible. Mantener rulesets sin rebajar controles.

**Coste:** incorpora un colaborador con capacidades de escritura; no existe un rol puramente de aprobación en el repositorio personal bajo este flujo. No conceder el permiso sin evaluar confianza y responsabilidades.

### Ruta B — Gobernanza unipersonal con controles compensatorios [CAMBIO DE DISEÑO]

Si el Owner no quiere otra persona con escritura, preparar una **enmienda formal** al requisito de revisión GitHub y a la secuencia P5–P8, por ejemplo combinando PR obligatorio, historia lineal, seguridad común, QA documental externa de solo lectura y aceptación explícita del Owner, pero sin afirmar que eso sea una aprobación humana independiente en GitHub. La regla que requiere una aprobación no puede quedar intacta si se pretende integrar sin un segundo revisor válido. La modificación deberá pasar decisión del Owner y evaluación independiente del cambio documental antes de actualizar el ruleset.

**Coste:** reduce separación de funciones y hace la protección frente a autoaprobación menos robusta. No se considera equivalente al diseño aceptado ni está autorizada actualmente.

### Ruta C — Mantener STOP

No cambiar GitHub. Conservar `main` protegido y segunda raíz congelada hasta que exista una ruta que satisfaga los controles o un rediseño autorizado.

## 4. Decisión solicitada (NO otorgada)

**OWNER REQUEST — `PCM-G2B-P5-REVIEWER-PATH-001`**

Elegir exactamente una disposición:

- `A — GRANTED DESIGN PATH`: autorizo únicamente preparar una propuesta de incorporación de una persona independiente (sin invitar ni conceder permisos todavía). Identidad externa y criterios se fijarán antes de autorizar cualquier acción administrativa.
- `B — GRANTED DESIGN REVISION`: autorizo exclusivamente elaborar y someter a QA una enmienda de gobernanza unipersonal para P5–P8; no autorizo modificar `R-MAIN`, publicar ni cambiar permisos.
- `C — DEFERRED`: mantengo P5 detenido y G2-B en estado parcial, sin nuevas modificaciones.

No se presume la selección de ninguna opción. Ninguna equivale a autorización para invitar un colaborador o efectuar un push. La futura autorización operativa, si procede, debe ser expresamente acotada.

## 5. Referencias públicas

- GitHub, *About protected branches*: https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches
- GitHub, *Reviewing proposed changes in a pull request*: https://docs.github.com/en/pull-requests/how-tos/review-pull-requests/reviewing-proposed-changes-in-a-pull-request
- GitHub, *Permission levels for a personal account repository*: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/repository-access-and-collaboration/permission-levels-for-a-personal-account-repository

**Nota:** documento de coordinación basado en los resultados de lectura ya recibidos y en las declaraciones del Owner; no sustituye una aceptación operativa ni una inspección administrativa de permisos.
