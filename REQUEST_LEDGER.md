# PCM-001 — Registro inicial de solicitudes y disposiciones

**Tipo:** índice evolutivo de trabajo; no sustituye contratos congelados ni autorizaciones originales. **Emisor:** PCM-001. **Corte:** 2026-11-22. Los mensajes Owner no exportados son `SECONDARY_ATTRIBUTED` para auditores externos.

| ID | Origen / solicitud | Estado documentado | Responsable / siguiente ruta |
|---|---|---|---|
| PCM-BOOTSTRAP-RECOVERY-001 | Owner solicita documentar y operar desde el repositorio maestro; autoriza avanzar en esta conversación | IN_SCOPE: checkpoint documental aditivo; **bootstrap completo no demostrado** | PCM-001 prepara registros; Owner revisa cualquier ampliación de autoridad/publicación |
| PCM-G2-B | Infraestructura y protección inicial del maestro | NOT ACCEPTED; defectos y evidencias pendientes, P8 INCONCLUSIVE | Owner decide sobre G2-B; no reinterpretar este checkpoint como cierre |
| PCM-P5-P6-NC | Desviación histórica del STOP contractual P5→P6 | PRESERVED / NO RETROACTIVE CURE | PCM-001 conserva fuentes y propuesta de rectificación; Owner dispone actos reservados |
| PCM-GOV-PROV-R3-ACCEPTANCE-001 | Política local de atribución y procedencia | ACCEPTED — LOCAL DOCUMENTARY POLICY ONLY (decisión Owner en conversación, sin export primario para terceros) | PCM-001 aplica prospectivamente a sus registros locales |
| PCM-GOV-PROV-CORR-001 | Corrección aditiva histórica; R2 recibió QA discrepante y R3 correctivo preparado | R3 CANDIDATE / QA NOT AUTHORIZED / OWNER ACCEPTANCE PENDING | Owner decide re-QA del candidato R3 si procede; no publicación del candidato |
| PCM-G2B-P8-UNI | Propuesta de enmienda unipersonal | OWNER ACCEPTANCE PENDING | Owner decide de modo independiente; no cambio implícito al gate anterior |
| PCM-G3-G4-G5 | Extracción/adopción/etapas posteriores | DEFERRED | Owner decide por etapa y alcance nuevos |
| PCM-RELEASE-PATH | Publicación del estándar y releases en `main` | NOT AUTHORIZED | Owner define diseño, QA y release; ninguna adopción automática |

**Provenance:** Owner originó la necesidad de centralizar y simplificar el trabajo operativo actual; PCM-001 propuso soluciones y elaboró la documentación. La aceptación posterior de propuestas no convierte al Owner en autor de ideas del agente. La falta de mensajes originales transportables se rotula y no se sustituye por resúmenes.

**Bloqueo principal de cierre:** adopción formal de política/bootstrap maestro y control de archivo público/privado. Evitar repetir QA documentales sin registrar primero sus objetos y estado aquí.

## Actualización P0 — 2026-11-22

**PCM-P0-ARCHIVE-001** — Owner autorizó continuar centralizando documentación en el repositorio de gobierno. PCM-001 ejecutó una **primera incorporación acotada** de cuatro fuentes R3 y una matriz de custodia. Estado `IN_PROGRESS`. El volumen remanente necesita clasificación por archivo para evitar publicar fuentes CONTROLLED. **Próximo destinatario:** PCM-001 para continuar inventario documentado; Owner decide cambios normativos, de seguridad y futuras importaciones a main.

**PCM-VERSIONING-001** — Owner propuso semántica mayor / herramientas compatibles / correcciones. Borrador detallado en `proposals/`, estado `PROPOSED; NOT ADOPTED`. No implica publicar v1.0.1/v1.1.0/v2.0.0 ni alterar protocolo FROZEN.

## Actualización P0 archivo 002 — 2026-11-22

**PCM-P0-ARCHIVE-002:** IN_PROGRESS; cinco originales CORR-001 archivados, con estados de QA R2 preservados. `CORR-001 R3` todavía candidato, re-QA NO AUTORIZADA. Próxima ruta: clasificar G2-B sin publicar evidencia controlada.

**PCM-VERSIONING-001 — aclaración vinculante del alcance de la propuesta, no adopción de su contenido:** Owner especifica que se persigue una **regla futura del protocolo**, no una pauta opcional. Estado de la política `PROPOSED FOR FUTURE NORMATIVE EVALUATION / NOT EFFECTIVE`. Documento `decisions/PCM-VERSIONING-001_OWNER_SCOPE_CLARIFICATION_2026-11-22.md`. Destinatario futuro: Owner mediante diseño/QA/release separadas; no hay autorización para cambiar `main`.

## PCM-P0-ARCHIVE-003 — 2026-11-22

Estado: `IN_PROGRESS`; once documentos históricos iniciales/G2-A incorporados como fuentes originales y ubicados por SHA-256, sin cambiar decisiones congeladas. Fuente y retorno: `inventory/PCM-P0-ARCHIVE-003_G2A_CHAIN_2026-11-22.md`. Siguiente ruta: PCM-001 revisa G2-B, Owner decide solamente gates reservados; no nuevas QA en este archivo.

## PCM-P0-ARCHIVE-004 / 2026-11-22

**G2-B historical evidence:** 24 fuentes archivadas. Estado: **DOCUMENTATION ARCHIVED; NOT ACCEPTED**; no QA adicional realizada ni Owner acceptance inferida. Fuente exacta y SHA en `inventory/PCM-P0-ARCHIVE-004_G2B_EVIDENCE_CHAIN_2026-11-22.md`. Siguiente ruta: PCM-001 para clasificación de G2-A/R3-R5 y D-R3-APP no publicados; Owner decide cualquier nuevo gate. 

## P0 archivo 005 — 2026-11-22

Recuperados 22 originales complementarios en `records/initial`, `records/g2a`, `records/planning` y `records/provenance`; fuente de custodia `inventory/PCM-P0-ARCHIVE-005_PLANNING_AND_PROVENANCE_2026-11-22.md`. Estado: ARCHIVED (histórico) sin aceptar ninguna propuesta nueva. Próximo control: clasificación de fuentes administrativas/privadas remanentes.

## PCM-P0-CUSTODY-001 — 2026-11-22

**STATUS:** CATALOG COMPLETE FOR OBSERVED LOCAL SET / PRIVATE RAW EVIDENCE CUSTODY OPEN. 66 originales publicados; 41 restantes catalogados por SHA-256: 18 SENSITIVE_REVIEW, 7 ADMIN_REVIEW, 12 ZIP_PACKET, 4 IMAGE_REVIEW. Documento `inventory/PCM-P0-CUSTODY-001_REMAINING_LOCAL_SOURCES_2026-11-22.md`. **NEXT OWNER:** PCM-001 continúa clasificación de evidencia; Owner decide depósito autorizado de fuentes no publicables y cualquier nueva infraestructura. No avanzar gates técnicos por inferencia.

## PCM-P0-CUSTODY-002 — 2026-11-22

Estado: `DOCUMENTARY LOCAL CENSUS RECONCILED / RAW PRIVATE CUSTODY OPEN`. Cuatro documentos QA G2-A archivados, 70 originales en GitHub; 37 objetos restantes registrados en `inventory/PCM-P0-CUSTODY-002_RECONCILED_RESIDUAL_CATALOG_2026-11-22.md`. Owner decide custodia no pública antes de afirmar recuperación documental integral. No autorización adicional de QA ni de `main`.

## PCM-P0-RETENTION-001 — 2026-11-22

Owner ordenó evaluar el valor documental de capturas, ZIP y archivos administrativos antes de definir almacenamiento privado. PCM-001 completó clasificación individual de 37 entradas; **resultado: RECOMMENDATION / NO OWNER RETENTION POLICY ACCEPTANCE**, `inventory/PCM-P0-RETENTION-001_EVIDENCE_VALUE_AND_PRIVACY_ASSESSMENT_2026-11-22.md`. Cuatro paquetes en `RETAIN_EXACT_PENDING_GATE`, nueve auxiliares singulares por clasificar y 20 Markdown de publicación pendiente (6 candidatos a original público y 14 candidatos a síntesis sanitizada). **RETURN:** PCM-001 → Owner cuando haya matriz de dependencias y propuesta definitiva de retención; no solicitar repo privado todavía.

## PCM-P0-CUSTODY-003 — 2026-11-22

Owner autorizó finalizar clasificación y recuperación documental sin añadir infraestructura ni eliminar originales. Se incorporan 6 originales públicos, 14 fichas resumidas sanitizadas y un análisis de nueve auxiliares singulares. **P0 CLASSIFICATION/ARCHIVE WORK COMPLETE FOR OBSERVED LOCAL SET**, mientras `EXACT BYTE PRIVATE EVIDENCE RECOVERY OPEN` para gates históricos. Siguiente fase propuesta: preparación documental de extracción del estándar en main (read/design only). Decisión Owner reservada para nuevas releases, integración y custodia privada.

## PCM-P1-PREP-001 — 2026-11-22

PREPARED DOCUMENTARY ONLY: extracción propuesta desde `KhaosMagnus/YU3DOH-Carder` @ `056adb5097b7ce067082782e8d8c92b42db9082a`; fuentes y blobs exactos en `planning/PCM-P1-PREP-001_PORTABLE_BOOTSTRAP_EXTRACTION_READINESS_2026-11-22.md`. **OWNER IMPORT AUTHORIZATION NOT GRANTED**, QA/release/deployment not started. Se encontró dependencia del builder histórico a SHA de otro repositorio. Próxima ruta: Owner decide `GRANTED / DEFERRED / REVISE` para importación exacta a `main` cuando proceda; no hay ejecución por este registro.

## PCM-BRANCH-STRATEGY-001 — 2026-11-22

OWNER GRANTED (local): activar desarrollo del estándar en `dev/portable`, nacida desde main `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`; preservar primero bootstrap histórico v1.0 como snapshot original. Sin autorización para fusionar en main, publicar release ni cambiar rulesets. Rutas de autoridad `decisions/PCM-BRANCH-STRATEGY-001_OWNER_APPROVAL_2026-11-22.md`. Estado de ejecución por verificar después de la creación de rama/importación.
