# PROJECT CONTROL MASTER — P8: conciliación de doble QA independiente de infraestructura

**Asignación:** `PCM-G2B-IQA-INFRA-001`  
**Disposición coordinadora:** `PCM-G2B-P8-DUAL-QA-CONSOLIDATION-001`  
**Responsable:** `PROJECT_CONTROL_MASTER / PCM-001`, **PROVISIONAL**  
**Fecha:** 2026-11-20 (America/Mexico_City)  
**Modo:** recepción, conciliación, lectura; **sin escrituras GitHub**  
**Estado:** `DOUBLE QA RECEIVED / BOTH INCONCLUSIVE / G2-B FULL ACCEPTANCE NOT SUPPORTED / P5 DEVIATION OPEN / G3–G5 DEFERRED`

## 1. Congelación de las fuentes y autoridad

| Objeto | SHA-256 verificado | Procedencia |
|---|---|---|
| QA1 — ChatGPT, `PCM-G2B-IQA-INFRA-001_INFORME_QA_INDEPENDIENTE.md` | `945acec3dd5fb5450aadbc30a3d3b06d0660af300f73d666e410d604e881c80f` | Biblioteca del Owner, `libfile_4dcb0ea639dc8191953f6b5034e2d32f`, copia íntegra en expediente local |
| QA2 — Grok, `PCM-G2B-IQA-INFRA-001_GROK_INDEPENDENT_INFRA_QA_REPORT.md` | `90a62af52e0c925818c98a617beb2710cc7f58da760ea538718a4d8de5f46349` | Adjuntado por Owner; lectura directa del archivo |
| Paquete P8 común examinado por ambos | `2c4b4a0b7835386e7ec5e25cfd635bc0ae43a8ca3d49d511ba0e85af3496c499` | `PCM-001_G2-B_P8_INDEPENDENT_INFRA_QA_SHARED_PACKET_2026-11-20.zip` |
| Solicitud ejecutiva G2-B (Owner `GRANTED`) | `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349` | `01_PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_REQUEST_2026-11-16.md` |
| Contrato Q1–Q9 y aceptación | `a1c10a91bc0947e3a84d4c8d48da404c7494f45154e8613c0a65bdd07b6633b3` | `03_PCM-001_G2-B_INFRASTRUCTURE_INDEPENDENT_QA_CONTRACT_2026-11-16.md` |

Los dos dictámenes son genuinamente distintos y mantienen sus propias reservas. Ambos dicen **`INCONCLUSIVE`**. Ninguna QA autorizó operaciones, ni la recepción constituye aceptación de infraestructura.

## 2. Matriz consolidada

| Control | QA1 ChatGPT | QA2 Grok | Disposición de PCM-001 |
|---|---|---|---|
| Q1 — Identidad y superficie pública | VERIFIED | VERIFIED | **VERIFIED** en las superficies inspeccionadas |
| Q2 — Raíz `main` y bytes exactos | VERIFIED | VERIFIED | **VERIFIED** |
| Q3 — Raíz `meta/project-control` y bytes exactos | VERIFIED | VERIFIED | **VERIFIED** |
| Q4 — Historias sin ancestro común | VERIFIED (ejecutó `git merge-base`, exit 1 y sin stdout) | PARTIAL (no ejecutó `merge-base`) | **VERIFIED** en alcance de QA1, con corroboración estructural independiente de QA2; la diferencia de clasificación deriva del método, no de un ancestro detectado |
| Q5 — Guardia anterior al primer push | PARTIAL | PARTIAL | **PARTIAL**: estado actual y `created_at` comprobados; continuidad/historia de aplicación no demostrada exhaustivamente |
| Q6 — Perfiles y elegibilidad del revisor | PARTIAL | Configuración VERIFIED; **FAILED** elegibilidad | **BLOCKED / MATERIAL NONCONFORMITY**: sin revisor humano distinto y elegible acreditado; avance P5→P6 pese al STOP documental |
| Q7 — Instalación y exclusión administrativa | PARTIAL | PARTIAL | **PARTIAL**: conector confirma `selected`, 11 IDs, maestro fuera; falta snapshot administrativo posterior a creación |
| Q8 — Secuencia y solo dos pushes autorizados | PARTIAL | PARTIAL | **PARTIAL**: mensajes originales de Owner, P3, P4 y P6 constan en conversación; no constituyen un log administrativo exhaustivo ni prueban inexistencia de intentos transitorios |
| Q9 — Incidentes ambiguos y recuperación | UNKNOWN / NOT OBSERVED | NOT OBSERVED | **NOT TRIGGERED / NOT TESTED** solo si Owner confirma no haber observado incidentes. No fabricar prueba negativa ni ensayo destructivo |

**Criterio de precedencia:** no rebajar `FAILED` de Q6 a PASS mediante mayoría o por correcto estado de las ramas. La aceptación original en §5 del contrato ejecutivo exige dos QA `PASS` y decisión posterior del Owner. Los resultados actuales no satisfacen esa puerta.

## 3. Objetos remotos congelados observados

Repositorio público: `KhaosMagnus/Project-Control`; ID `1465064417`; rama predeterminada `main`.

| Ref | Commit SHA | Tree SHA | Padres | Archivo único / blob |
|---|---|---|---|---|
| `main` | `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb` | `04bff84a661781fb8f3982235c6c93f668a658ed` | `[]` | `README.md` 100644 / `56fd6d6560434e067c126c152ab86298bd57d61f` |
| `meta/project-control` | `cac838940e0e824a1f828ff660e422a6441a1da7` | `3e39ae46b9e1690604387452ee7283062a79e182` | `[]` | `README.md` 100644 / `2b30688846710fe73b89a537bb5a8cfb21e738eb` |

README SHA-256: `main` `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340`; `meta` `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0`.

Rulesets: `PCM-GENESIS-SAFETY` ID `27708103`, `R-MAIN` ID `27709862`, `R-META` ID `27717600`, todos `active`, sin bypass; perfiles PR + 1 aprobación + historia lineal; métodos squash/rebase. La instalación `162412374` sigue `selected`; lectura de conector con 11 IDs aprobados y sin `1465064417`. Esta última es **evidencia del conector**, no prueba administrativa completa de Q7 ni de otras credenciales/OAuth.

## 4. Hallazgo rector: desviación P5→P6

La solicitud ejecutiva aprobada §3 P5 establece: **si la ruta de revisor GitHub elegible e independiente no es demostrablemente viable, STOP después de publicar/proteger `main` y no publicar `meta`**. El Owner revisó personalmente la configuración correcta de `R-MAIN`; PCM-001 indicó que la revisión del Owner permitía avanzar y se publicó `meta` bajo una ruta de revisión futura no acreditada. Posteriormente el Owner confirmó que `KhaosMagnus` y `JormungandrMagnus` son controladas por la misma persona y que no se habían incorporado colaboradores.

**Clasificación:** incumplimiento del criterio de transición del contrato; NO es prueba de adulteración de los commits, ni de bypass usado, ni de que exista un PR defectuoso. La dirección incorrecta fue facilitada por PCM-001. **No se retroautoriza** esa transición mediante una nueva nota. Se preservan commits y reglas; el Owner debe disponer expresamente de la desviación y de la política para futuras publicaciones.

Alternativas de diseño, sujetas a autorización separada:

- **A — Preservar el requisito actual:** conseguir y acreditar una persona revisora distinta con rol GitHub elegible; documentar invitación/permisos solo mediante autorización específica del Owner. Posteriormente ejecutar QA focalizada de elegibilidad y trazabilidad.
- **B — Operación unipersonal controlada:** preparar una **enmienda prospectiva** que reconozca al Owner como revisor humano cuando un autor técnico distinto abra un PR y añada QA documental independiente de contenido, `B/H/D/T_expected`, readback postintegración y límites de riesgo. Eliminaría o modificaría explícitamente la exigencia de **dos personas** en este caso, sin afirmar independencia humana inexistente. Comprobar viabilidad de acceso/fork/revisiones en gate posterior; no es autorización de permisos, pruebas de escritura ni cambio inmediato a rulesets. Requiere revisión focalizada y aceptación expresa del Owner.
- **C — Mantener diferido:** no modificar configuración ni política; conservar el estado técnico actual sin aceptación formal G2-B.

**Recomendación coordinadora:** presentar B como vía de diseño económica para un maestro mantenido por un solo Owner, con reserva explícita de que supone menos separación real de funciones; A sigue siendo la vía que cumple literalmente la política actual. **No ejecutar B por defecto.**

## 5. Evidencia adicional delimitada

- **Q5:** el readback P2 de la conversación mostró `PCM-GENESIS-SAFETY active`, sin ramas; el readback posterior a P4 mostró `main` publicado, `meta` ausente, guarda activa. Las fechas GitHub corroboran orden plausible, pero `commit.author.date` no equivale a hora del push. Registrar el intervalo observado, no declarar continuidad universal.
- **Q7:** solicitar **una sola** captura desde `Settings → Applications → Installed GitHub Apps → Configure` después de la creación, mostrando `Only select repositories`, lista completa o mecanismo verificable del conjunto de los 11 y ausencia de Project-Control. No pulsar Save.
- **Q8:** se conservaron en conversación el `GRANTED` del Owner, hashes de P3, salida exitosa del push de P4, aceptación personal de la configuración de P5, salida del push P6 y lecturas de P7. Incorporarlos en un anexo de procedencia, sin afirmar que una reconstrucción posterior sea un log nativo del servidor. Los revisores P8 no tuvieron esa conversación íntegra como fuente primaria.
- **Q9:** pedir al Owner atestación de si observó algún error/timeout/reintento. Si no hubo, `NOT TRIGGERED / UNTESTED` es una disposición honesta; no se precisa provocar fallos.

## 6. Disposición y siguiente control

**G2-B no se declara aceptado.** No existe autorización nueva para G3/G4/G5, adopción o release. Se propone exclusivamente un **gate documental focalizado de tratamiento de desviación P5 y diseño de revisión futura**, con la captura Q7 y testimonio Q8/Q9 como complementos. Tras disposición del Owner y eventual enmienda aprobada, solicitar re-QA únicamente de los puntos realmente cambiados; no repetir Q1–Q4 ni alterar historias congeladas.

No se ejecutó ninguna operación de escritura ni cambio de permisos en GitHub.
