# PC-MASTER-DES-001 — Separación de Project Control Master y YU3DOH Carder

**Estado:** DESIGN PROPOSAL / OWNER REVIEW PENDING / NO EXECUTION  
**Fecha de corte:** 2026-11-11  
**Origen:** PROJECT_CONTROL / PC-004, proyecto ChatGPT YU3DOH Carder  
**Destino futuro:** proyecto ChatGPT `Project Control Master`  
**Repositorios:** `KhaosMagnus/YU3DOH-Carder` (existente); `KhaosMagnus/Project-Control` (nombre propuesto, no creado ni verificado como reservable)

## 1. Decisión arquitectónica propuesta

Separar simultáneamente **(a) la coordinación en ChatGPT** y **(b) los repositorios de GitHub**. El objetivo es que Project Control deje de desarrollarse dentro del control local de YU3DOH, manteniendo a YU3DOH como instancia autónoma y preservando toda su historia. El nuevo proyecto ChatGPT `Project Control Master` tendrá su propio coordinador `PROJECT_CONTROL_MASTER / PCM-001` (identidad **propuesta** hasta bootstrap y reconocimiento formal) y administrará el proyecto que construye la herramienta/estándar Project Control. No recibe automáticamente autorización para editar ningún proyecto adoptante.

**Distinción esencial:** un proyecto ChatGPT nuevo no hereda conversaciones, permisos, credenciales, archivos, identidad interna ni estado de GitHub por el mero nombre. La transferencia de «identidad» es un paquete documental explícito: misión, roles, fuente de verdad, límites, versiones, decisiones y recuperación. La independencia de gobierno no implica aislamiento técnico de cuentas o permisos; este se verifica por separado.

## 2. Dos autoridades y dos ciclos de vida

| Atributo | Instancia local de YU3DOH | Project Control Master |
| --- | --- | --- |
| ChatGPT Project | `YU3DOH Carder` | `Project Control Master` (por crear por el Owner) |
| Coordinador | `PROJECT_CONTROL / PC-004`, continuidad local | `PROJECT_CONTROL_MASTER / PCM-001`, **nueva instancia**, nunca sucesión automática de PC-004 |
| Repositorio | `KhaosMagnus/YU3DOH-Carder` | `KhaosMagnus/Project-Control` (por crear y autorizar) |
| Rama de gobierno | `meta/project-control` existente | `meta/project-control` nueva, gobierno local del maestro |
| Rama de producto | repositorio YU3DOH `main` y ramas de Workspace | futuro repositorio maestro `main` para protocolo, bootstrap, adaptadores, versiones, pruebas |
| Misión | cambios, QA, validaciones, decisiones y producto de YU3DOH | construcción, QA, releases, compatibilidad y adopción del estándar genérico |
| Historial | permanece inalterado | inicializado con procedencia explícita; **no** importa todos los registros operativos de YU3DOH |
| Derecho sobre el otro | ninguno implícito | ninguno implícito; las adopciones son actos separados del Owner de cada proyecto |

El maestro se autogobierna con una **versión fijada** del protocolo y una rama de control independiente. Modificar el estándar en su `main` no modifica automáticamente las reglas de su propio `meta/project-control` ni las de YU3DOH. El código/protocolo candidato, la release publicada y la política adoptada por cada instancia son identidades distintas.

## 3. Fuente verificable y corte documental

Verificado en GitHub al diseñar (volver a consultar antes de ejecutar):

- Control local YU3DOH: `meta/project-control @ 056adb5097b7ce067082782e8d8c92b42db9082a`.
- Producto YU3DOH: `main @ 54cc3aad246c89a29f2a18be63c539db68cae041`.
- Política Git local: `protocols/GIT_CONTROL_POLICY.md` blob `8e00dd5ae7a153a09ce88c2614fbea2ce3f2393d` (rama documental aislada; no merge al producto).
- Dirección federada estratégica: `control/PROJECT_CONTROL_FEDERATED_ARCHITECTURE_DIRECTION.md` blob `fb2ee2ffd44415a1a049de433b4e1fe005d89103`; objetivo alineado al Owner, **no autorización vigente de infraestructura**.
- Protocolo genérico congelado v1.0: `protocols/GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0.md` blob `1ac3689c1e811d1594291afee6b2c1c6efd093d0`.
- Bootstrap reutilizable: `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/`, metadatos blob `95233ecfb1afd9004eabc07ecd8e7e9b84b05b4b`; esta documentación declara **sin QA independiente ni adopción automática**.
- Recovery de soporte externo: `runs/PP-002_ONLINE-1C_SUPPORT_HUMAN_ESCALATION_RECOVERY_CHECKPOINT.md` blob `b2e64984be77e5884b25993a44ea937c93623e64`; ONLINE-1C-A1 `INCONCLUSIVE`, error P3 `UNKNOWN`, A2 `NO-GO`, soporte humano escalado, sin respuesta técnica aún documentada.
- En una consulta a GitHub, `KhaosMagnus/Project-Control` devolvió `404` desde la conexión disponible. Eso significa **no accesible/visible**, no una garantía de disponibilidad de nombre ni permiso de creación.

## 4. Matriz de extracción: no hacer copia masiva de la rama

**A. Portar como candidatos de origen inmutable:** protocolo genérico v1.0, bootstrap v1.0, plantillas, adaptador GitHub y evaluación de portabilidad v1.0. Cada entrada exige ruta, repositorio, SHA de origen, blob SHA, destino, categoría, hash del destino, transformación o «copia idéntica», y QA de integridad.

**B. Evaluar antes de generalizar:** reglas de concurrencia, políticas de publicación, recuperación, evidencias PP-002/Q01/Q02. Transferir patrones comprobados después de revisión técnica y aceptación independiente, no expedientes particulares como condiciones normativas genéricas.

**C. Mantener en YU3DOH:** estado y backlog local, RUN/CR particulares, decisiones de Owner y autorizaciones locales, código Carder/Workspace, roles/instancias históricas, reportes y evidencias completas de PP-002 y su checkpoint de soporte. El maestro puede mantener **índices y enlaces pinneados**, no sustituir la fuente original.

**D. Trabajo nuevo:** todo cambio genérico futuro nace en Project Control Master **después** del gate de activación. Durante la transición las solicitudes genéricas tienen un propietario designado, jamás dos coordinadores que publiquen simultáneamente como autoridad principal.

## 5. Estructura objetivo del repositorio maestro

Propuesta (sujeta a diseño final y comprobación real de permisos):

- `main`: `README.md`, `protocols/`, `bootstrap/`, `adapters/`, `tests/`, `docs/`, `releases/`, `provenance/` (estándar/proyecto de producto; no registro mutable de autoridad).
- `meta/project-control`: `PROJECT_STATE.md`, `control/`, `requests/`, `roles/`, `routing/`, `validations/`, `runs/`, registros de decisiones y QA del propio maestro. DOCUMENTACIÓN SOLAMENTE.
- `feature/*` / `experiment/*`: desarrollo, diseños, pruebas y candidatos autorizados; ninguna promoción implícita.

Preferencia: historias Git de `main` y `meta/project-control` separadas/orphan cuando sea factible; si la plataforma no lo soporta, parentage inicial explícito, árbol reemplazado y regla permanente de **NO MERGE** entre control/producto. No declarar que una rama por sí sola garantiza separación de permisos. `main` debe usarse para el estándar, no como sinónimo de la autoridad maestra sobre otros proyectos.

## 6. Plan con puertas de aceptación

### G0 — VALIDAR DISEÑO (ahora, sin implementación)

Owner acepta en una sola decisión: las **dos** separaciones, nombres, matriz de custodia, identificación nueva PCM-001, no herencia automática, nueva fuente de verdad y secuencia de bootstrap. Este documento sigue siendo propuesta hasta entonces.

### G1 — Inicializar ChatGPT Project `Project Control Master`

Owner crea el Project e instala manualmente `PC_MASTER_DES_001_PROJECT_INSTRUCTIONS.md` como instrucciones permanentes; inicia nueva conversación con `PC_MASTER_DES_001_INITIAL_TRANSFER.md`, más material de referencia. PCM-001 acusa recibo de SHA, procedencia y límites. **Modo inicial: preparación/read-only; no crea repo ni afirma ser autoridad efectiva todavía**. Nueva identidad por asignación funcional, no trasplante de memoria/credenciales.

### G2 — Autorizar y crear el repositorio GitHub

Tras propuesta de alcance exacto, Owner autoriza separadamente creación del repositorio, visibilidad (recomendación: privado inicialmente), ramas y permisos. Antes de escribir: verificar nombre, identidad, repositorio inexistente o reconciliar si ya existe, límites de credenciales, reglas de ramas, procedimiento de recuperación. No usar cuentas experimentales ni ampliar instalación del laboratorio sin autorización.

### G3 — Bootstrap maestro e importación reproducible

Inicializar `main` con fuentes genéricas pinneadas y manifiesto de procedencia. Inicializar `meta/project-control` con instancia propia, adopción explícita de una versión fija y cuatro registros mínimos: estado, rol, instancia y solicitudes. QA independiente sobre bytes, integridad, rutas, reglas, separación de referencias, recuperación y ausencia de cambios a YU3DOH. El bootstrap v1.0 original **no se declara QA PASS por estar copiado**.

### G4 — CUTOVER de investigación genérica

Solo tras `BOOTSTRAP COMPLETE`, QA independiente y aceptación específica del Owner: nueva investigación genérica se enruta a `Project Control Master`; YU3DOH conserva gobierno local. PP-002 histórico sigue en origen; su dependencia de soporte se referencia por SHA y un registro de transferencia de seguimiento, sin inventar una respuesta. Establecer un único responsable de la siguiente acción y una fecha/condición de seguimiento, no dos expedientes activos divergentes.

### G5 — Primera release/adopción de otro proyecto

Publicar release inmutable del estándar con compatibilidad y QA. Prueba en instancia sintética/segundo proyecto. Para que YU3DOH adopte una versión posterior se necesita decisión de adopción local, version pin, mapeo, dry-run, rollback y QA. No actualizarlo silenciosamente.

## 7. Riesgos, controles y supuestos

1. **Confusión de identidad (alto):** «PCM-001=PC-004» sería incorrecto. Son instancias distintas con contrato fuente/consumidor; no comparten autoridad ni memoria de manera garantizada.
2. **Doble fuente de verdad (alto):** el maestro gobierna la evolución del estándar, YU3DOH su gobierno local. El mismo documento congelado puede copiarse idéntico, pero cada adopción tiene revision/digest propios.
3. **Permisos (alto):** separación de ChatGPT Projects y ramas GitHub **no prueba** least privilege ni CAS atómico. S1/S2 y limitaciones ONLINE-1C siguen abiertas. Trabajo documental puede avanzar sin activar la vía bloqueada.
4. **Historial y procedencia (alto):** copiar cientos de expedientes pierde el significado de responsabilidades; hacer rebase/merge de ramas originales puede arrastrar producto al maestro. Preferir importación selectiva con hashes y enlaces originales.
5. **Bootstrap de sí mismo (medio):** fijar la versión de gobierno del maestro y separar releases en `main` de reglas efectivas en `meta/project-control` evita la autorreferencia circular.
6. **Proyecto ChatGPT (medio):** no asumir que sus archivos/conversaciones o permisos de conectores se sincronizan con este proyecto. Entregar paquete autocontenido; trasfondo de memoria de cuenta tampoco sustituye autoridad documental.
7. **Operación inicial (medio):** el conector actual quizá no permita crear repositorios/orphans de forma directamente autorizada. No prometer creación automatizada; Owner podrá hacerlo desde GitHub o Work tras alcance y preflight.

## 8. Entregables y criterios de validación de G0

- Este alcance congelado en propuesta; revisión del Owner y autorización expresa para G1/G2 cuando corresponda.
- Instrucciones de proyecto ChatGPT: `PC_MASTER_DES_001_PROJECT_INSTRUCTIONS.md`.
- Transferencia inicial autosuficiente: `PC_MASTER_DES_001_INITIAL_TRANSFER.md`.
- Registro de identidad y matriz de responsabilidades de dos instancias: sección 2.
- Manifest de extracciones que se preparará en G3, con hashes comprobados antes de escritura.
- Ruta de rollback: YU3DOH conserva autoridad local y todos los artefactos originales; si falla G1–G4, el maestro queda `PROVISIONAL/BLOCKED`, sin alterar el producto ni el control de YU3DOH.

## 9. Decisión solicitada

`ACCEPT DESIGN` para la doble separación y la nueva identidad PCM-001 en estado provisional; o `REVISE` especificando el punto a corregir.

**NO-GO hasta autorización específica de G2:** creación GitHub, nuevas ramas, permisos, copias de producto, publicación de releases, cambios de protocolo adoptado o migración de gobierno local. Se permite al Owner crear manualmente el ChatGPT Project G1 y realizar una recepción documental sin transferir autoridad efectiva.
