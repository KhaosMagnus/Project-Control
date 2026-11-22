# PCM-BRANCH-STRATEGY-001 — Recepción de aprobación del Owner y activación local limitada
**PROVENANCE:** Owner expresó aprobación plena y orden de aplicar el modelo tras el análisis de PCM-001 en la conversación del 2026-11-22. **DRAFTER:** PCM-001/GPT; esta constancia es secundaria para lectores sin mensaje Owner original.  
**DECISION:** GRANTED — **estrategia local de ramas y arranque de desarrollo fuera de main**. No se adopta automáticamente como norma del protocolo portable ni sustituye contratos frozen de otros proyectos.
**BASE DE INSPECCIÓN:** `KhaosMagnus/Project-Control` `main@6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`, `meta/project-control@4604dd834ca619566ce23218e935d9569220c632` (verificar antes de escribir).
**SCOPE / ALLOWED WRITES:** crear `dev/portable` desde ese exacto main; importar como snapshot de referencia los archivos históricos congelados `PROJECT_CONTROL_BOOTSTRAP-v1.0` y su digest, con hash byte a byte; mantener segregado cualquier constructor históricamente dependiente de YU3DOH y documentar su limitación. Documentar continuación en `meta/project-control`.
**BASIS FOR CONTINUATION:** el Owner pidió expresamente aplicar el esquema y seguir avanzando; esta autorización cubre la puesta en marcha de la rama de trabajo y la preservación inicial, **NO** implica permiso permanente de integración a main, release, adopción global, creación de otras ramas sin necesidad justificada ni modificar protecciones.
**BRANCH LIFECYCLE (LOCAL DESIGN ACCEPTED):**
- `main` producto estable; **mantener R-MAIN y PCM-GENESIS-SAFETY activos** en todo momento.
- `dev/portable` rama de producto estable de ciclo para staging/desarrollo; se crea una vez y conserva historial del snapshot.
- `feat/*` y `fix/*` solo si una tarea precisa aislamiento; una vez integradas y verificada la conservación por SHA, evaluar eliminación de ramas temporales con alcance Owner/política local. No borrar ramas protegidas.
- `release/*` opcional si QA o candidate freeze lo necesita, no obligatoria por interacción.
- `meta/project-control` sigue aislada y no se fusiona con producto.
**INTEGRATION POLICY:** QA del candidato exacto, autorización Owner/delegado separada nombrando before/head/target/mecánica, y verificación posterior. `R-MAIN` hoy exige PR con aprobación y permite squash/rebase, que pueden cambiar el SHA; resolver elegibilidad/revalidación con política antes de integrar. No aflojar ruleset para evitar la revisión.
**PRESERVATION:** `PROJECT_CONTROL_BOOTSTRAP-v1.0` y `GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0` frozen; los sucesores se versionarán solo bajo decisión futura. `PCM-VERSIONING-001` sigue propuesta normativa no adoptada.
**STATUS:** OWNER APPROVED LIMITED EXECUTION / DEV BRANCH INITIALIZATION GRANTED / MAIN LOCKED / QA & RELEASE NOT AUTHORIZED.
**RETURN:** PCM-001 debe registrar commit/refs y blobs reales posteriores a la ejecución; hasta entonces el resultado de creación es NOT YET OBSERVED.
