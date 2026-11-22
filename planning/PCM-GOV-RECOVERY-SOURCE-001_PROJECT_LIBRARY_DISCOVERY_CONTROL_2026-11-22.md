# PCM-GOV-RECOVERY-SOURCE-001 — Control de descubrimiento de evidencia documental entre instancias

**Project:** Project Control Master
**Redactor:** PROJECT_CONTROL_MASTER / PCM-002 (provisional)
**Fecha:** 2026-11-22
**Estado:** `OWNER-AUTHORIZED LOCAL DOCUMENTARY GUIDANCE / PORTABLE STANDARD IMPROVEMENT PROPOSED / NOT NORMATIVE RELEASE`
**Autorización:** intervención directa del Owner en conversación PCM-002 del 2026-11-22, que autoriza integrar inmediatamente la recomendación previa de comprobar archivos del proyecto y Biblioteca antes de declarar indisponible un artefacto. **Alcance:** documentación local en `meta/project-control`. No es autorización de adoptar nuevas versiones normativas, publicar bytes confidenciales, extraer/transmitir archivos privados, QA, implementación o modificación de `main`/`dev/portable`.
**Control base:** `meta/project-control@6e4d67ec16a27ef40e9ba97e6241fd4e8cc10ada`
**Vínculos:** `PCM-GOV-AUTHREQ-001` (solicitud explícita y cierre de trabajo); `PCM-GOV-AUTHREQ-DES-001-IQA-001` (QA documental sobre otro candidato, no se modifica mediante este acto).

## 1. Incidente que origina el control

En el relevo PCM-002, el Owner indicó que el informe `PCM-GOV-AUTHREQ-DES-001_IQA-001_CHATGPT_REPORT.md` ya existía en los documentos del proyecto, generado por una instancia independiente de ChatGPT. Una búsqueda inicial restringida a adjuntos de la conversación no lo encontró; la búsqueda posterior en la **Biblioteca** sí recuperó el archivo original, sin necesitar una nueva carga por parte del Owner.

**Evidencia observada en esta instancia:** fuente Biblioteca identificada por el mismo nombre, tamaño **27,860 bytes** y SHA-256 recalculado `e5e8b04d89ce73fa48a5144fa1dde91d983036648d20ef8c4348c7e72979bed7`; informe QA2 Grok adjuntado, 6,459 bytes y SHA-256 observado `fbdc203ba5bd8ba8a37653fbab009d9bd6b63b2add2c8b05dd6eeeb45e0f8dbe`. La identidad del contenido no prueba por sí sola identidad externa del revisor ni autorización de publicación. El informe de QA1 es `DOCUMENTARY REVISE` y QA2 es `DESIGN PASS (CONDITIONAL)`; su conciliación y cualquier sucesor R2 se tramitan por separado.

**Clasificación de este incidente:** `DOCUMENT DISCOVERY FALSE NEGATIVE / UNNECESSARY REUPLOAD REQUEST`. No demuestra que todos los chats/Projects compartan almacenamiento o permisos: las superficies accesibles dependen de contexto y habilitación real.

## 2. Regla local de recuperación y búsqueda — aprobada para procedimiento documental PCM

Antes de solicitar al Owner que descargue y vuelva a subir un documento que indica que ya está disponible:

1. **Determinar identidad:** nombre literal, alias, fecha, fuente prevista, versión, posible hash y relación con el expediente. No ampliar a documentos personales ajenos al objetivo.
2. **Buscar en superficies realmente disponibles:** adjuntos/contexto de la conversación; archivos/documentos del Project; Biblioteca accesible y, si aplica, documentos vinculados a Pages/Spaces. Consultar con búsqueda por nombre literal y luego una variante de contenido si no aparece.
3. **Consultar el repositorio autoritativo:** si se trata de estado GitHub, buscar en repo/commit/ruta fijados; no usar una copia local para sustituir el estado actual ni asumir que HEAD y fuente congelada son iguales.
4. **Verificar acceso y contenido:** distinguir metadatos, fragmentos indexados y bytes originales; abrir el archivo suficiente para la tarea. Si se requiere integridad exacta, recuperar bytes originales por la vía permitida y comprobar hash/identidad. Si la copia solo permite índices, declarar límites.
5. **Evitar duplicación de custodia:** preferir referencias al archivo existente, con su ID/ruta/versión y hash comprobado, en vez de pedir reuploads o crear copias públicas. La materialización temporal para comparar o procesar bytes no equivale a subir otro archivo al proyecto.
6. **Ante ausencia real:** solo después de agotar las superficies pertinentes declarar `NOT LOCATED IN ACCESSIBLE SOURCES`, precisando qué lugares se consultaron. **No** afirmar `FILE DOES NOT EXIST` basándose en búsqueda limitada.
7. **Privacidad y autoridad:** encontrar un archivo no concede permiso para publicarlo en `meta/project-control` ni transferirlo a un tercero. Verificar su clasificación `PUBLICABLE / SANITIZABLE / CONFIDENTIAL` y solicitar autorización separada cuando corresponda.
8. **Relevo:** los nuevos chats/LLM reciben una matriz de localizadores recuperables, identidades y límites. No inventar accesibilidad compartida entre sesiones, proveedores o proyectos; si la superficie no existe, informar y conservar la dependencia explícita.

**Deber de cierre:** si un informe necesario ya está en el Project o la Biblioteca accesible, el estado correcto es `SOURCE LOCATED / VERIFIED AS APPLICABLE`, no `OWNER REUPLOAD REQUIRED`.

## 3. Contrato de evidencia mínima sugerido

```yaml
artifact_id: "stable record identifier"
literal_name: "exact filename"
primary_custody: "github | project_file | library | external_connector | other"
locator: "exact ref or path, if supported"
source_revision: "full immutable commit / file version / UNKNOWN"
size_bytes: "observed value or UNKNOWN"
sha256: "observed value or NOT_CALCULATED"
bytes_verified: "true | false"
source_access: "DIRECT_BYTES | INDEXED_TEXT | METADATA_ONLY | UNAVAILABLE"
publicability: "PUBLICABLE | SANITIZABLE | CONFIDENTIAL | UNCLASSIFIED"
authority_to_publish: "exact grant ID | NONE"
claim_grade: "PRIMARY_OBSERVED | SECONDARY_ATTRIBUTED | UNKNOWN"
duplication_action: "REFER_EXISTING | TEMPORARY_PROCESSING | OWNER_REQUESTED_REUPLOAD"
```

A SHA-256 digest proves **byte identity only** when calculated over actual bytes; it does not establish ownership, authorship, independence, legal consent, or publication authorization.

## 4. Minimal documentary validation cases (not executed tests)

| ID | Scenario | Expected decision |
|---|---|---|
| SR-T01 | Owner says a report was created in another chat within the project, but no current attachment exists | Search Project files and Library before asking reupload |
| SR-T02 | Conversation search returns no matches; Library search returns exact file | Read original, verify identity as needed, no duplicate reupload |
| SR-T03 | Library returns metadata but cannot yield exact bytes | Record `METADATA_ONLY`; no fabricated hash/content |
| SR-T04 | Same filename appears for two different versions | Disambiguate by version/content/hash; do not choose by name only |
| SR-T05 | GitHub has file at pinned SHA and a different HEAD | Keep both contexts distinct; cite exact commit/blob |
| SR-T06 | Private Library file found, repo is public | Do not publish original without classification and explicit grant |
| SR-T07 | Another Project or provider cannot access the current Library | Describe actual access limits; no claim of universal sharing |
| SR-T08 | Artifact already exists with verified identity | Reuse reference; do not create needless second copy |

## 5. Application and limitations

This is **effective local documentary guidance** for PCM-002's recovery and handoff procedure under the Owner's direct authorization; it is **not** a released portable standard. A future successor protocol would require separate design, compatibility review, QA and Owner acceptance. Current Projects/Library access cannot be guaranteed to every agent or external model; Tier 3 enforcement would require tool or gateway integration and explicit permission.

No frozen records altered; no reports replicated, archived or released by this guideline. The source report files remain in their existing custody until a separate publication decision.

**Status:** `DOCUMENTARY CONTROL RECORDED / FUTURE PORTABLE ADOPTION OPEN`.
