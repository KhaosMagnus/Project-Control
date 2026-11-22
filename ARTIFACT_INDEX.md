# PCM-001 — Índice de artefactos (ubicaciones honestas)

**Principio:** este índice no crea una copia de los objetos. `EXTERNAL / NOT IN THIS REPOSITORY` significa que un nuevo coordinador debe recuperar el archivo por nombre y digest, y que **no** puede afirmar haberlo leído únicamente por ver el índice. No se vuelcan mensajes privados originales a un repo público sin clasificación.

| Objeto | Identidad exacta | Estado / disponibilidad |
|---|---|---|
| Protocolo genérico v1.0 FROZEN | Git blob `1ac3689c1e811d1594291afee6b2c1c6efd093d0` @ `KhaosMagnus/YU3DOH-Carder` commit `056adb5097b7ce067082782e8d8c92b42db9082a` | HISTÓRICO EN GITHUB FUENTE; no publicado en `main` maestro |
| Bootstrap v1.0 | `bootstrap/dist/PROJECT_CONTROL_BOOTSTRAP-v1.0.zip`, blob `13eae102d5aed553d4fb3a023ab77b71601306b2`, mismo commit origen | HISTÓRICO EN GITHUB FUENTE; no adoptado en maestro |
| Política de procedencia local R3 | `PCM-GOV-PROV-DES-003_ATTRIBUTION_CONTRACT_R3_CORRECTIVE_DRAFT_2026-11-20.md` SHA-256 `325bd44c8ab572cd7229219d7f08325e170c0e0797f9025c1abae4abb0a10cad` | OWNER ACCEPT LOCAL; TEXTO EXTERNO, no publicado aquí |
| Decisión Owner de aceptación R3, constancia GPT | `PCM-GOV-PROV-R3-ACCEPTANCE-001_LOCAL_OWNER_DECISION_RECORD_2026-11-21.md` SHA-256 `ac4e43a0d123aaa8c32b35b38699132338e791970237c3194442b57b37b8ac81` | EXTERNO, constancia documental; no reemplaza mensaje original |
| Re-QA R3 GPT | `PCM-GOV-PROV-IQA-002_INFORME_REQA_INDEPENDIENTE.md` SHA-256 `a24c116f02399946ccf7f7aaab11a460d0679af6d174e5d15fbe471434a2fb61` | EXTERNO, `DESIGN PASS (CONDITIONAL)` |
| Re-QA R3 Grok | `PCM-GOV-PROV-IQA-002_GROK_FOCUSED_R3_REQA_REPORT.md` SHA-256 `61b68c3ede0823d4286f73214e69b624c1b968709b09e14acc943942670bb7c9` | EXTERNO, `DESIGN PASS (CONDITIONAL)` |
| Corrección histórica CORR-001 R2 | `PCM-GOV-PROV-CORR-001_R2_ATOMIC_ADDITIVE_PROVENANCE_CANDIDATE_2026-11-21.md` SHA-256 `d68d6563c94e2141a76e5126ca1d513974b82df9bee3fd3358afde8d21256572` | EXTERNO, `DOCUMENTARY REVISE` tras QA discrepante |
| CORR-001 R2 QA GPT | `PCM-GOV-PROV-CORR-001-IQA-001_INFORME_QA_INDEPENDIENTE.md` SHA-256 `918859b5bfc6bf8601f61a48ea2708f9d8399f2d52467a594f0fd94474f25c6e` | EXTERNO, `DOCUMENTARY REVISE` |
| CORR-001 R2 QA Grok | `PCM-GOV-PROV-CORR-001-IQA-001_GROK_FOCUSED_PROVENANCE_QA_REPORT.md` SHA-256 `073963740c2a6d1b0c27c4a5d4a640c39adcaf2859f6a07250d374ef2f2e3a38` | EXTERNO, `DOCUMENTARY PASS (CONDITIONAL)` |
| CORR-001 R3 corrección preparada | `PCM-GOV-PROV-CORR-001_R3_ATOMIC_PROVENANCE_CORRECTIVE_CANDIDATE_2026-11-21.md` SHA-256 `f4317eaae4047086d32e00247e5e6f36e01c7e2d6a5c0b87f086eab524291d09` | EXTERNO; QA R3 NO AUTORIZADA, NO ACEPTADO |
| Enmienda unipersonal G2-B | `PCM-001_G2-B_P8_UNIPERSONAL_AUTHORITY_AND_REVIEW_AMENDMENT_DRAFT_2026-11-20.md` SHA-256 `410c12a8f2f46ac20322a6ec76d76e038c9b7979a565044d6db8ee5cec29ca76` | EXTERNO; OWNER ACCEPTANCE PENDING |

**Publicación siguiente:** no copiar indiscriminadamente el archivo local completo al repositorio público. Registrar allowlist de artefactos clasificados antes de importarlos. Un archivo con hash es evidencia de bytes, no autenticación del emisor ni aprobación de su contenido.

## Archivo nuevo verificado — PCM-P0-ARCHIVE-001 (2026-11-22)

| Ubicación de publicación | SHA-256 origen | Disposición |
|---|---|---|
| `records/provenance/PCM-GOV-PROV-DES-003_ATTRIBUTION_CONTRACT_R3_CORRECTIVE_DRAFT_2026-11-20.md` | `325bd44c8ab572cd7229219d7f08325e170c0e0797f9025c1abae4abb0a10cad` | Fuente original archivada sin cambios |
| `records/provenance/PCM-GOV-PROV-IQA-002_INFORME_REQA_INDEPENDIENTE.md` | `a24c116f02399946ccf7f7aaab11a460d0679af6d174e5d15fbe471434a2fb61` | Fuente original archivada sin cambios |
| `records/provenance/PCM-GOV-PROV-IQA-002_GROK_FOCUSED_R3_REQA_REPORT.md` | `61b68c3ede0823d4286f73214e69b624c1b968709b09e14acc943942670bb7c9` | Fuente original archivada sin cambios |
| `records/provenance/PCM-GOV-PROV-R3-ACCEPTANCE-001_LOCAL_OWNER_DECISION_RECORD_2026-11-21.md` | `ac4e43a0d123aaa8c32b35b38699132338e791970237c3194442b57b37b8ac81` | Fuente original archivada sin cambios |

**Inventario y restricciones:** `inventory/PCM-P0-DOCUMENTARY_RECONCILIATION_2026-11-22.md`. **Versionado:** `proposals/PCM-VERSIONING-001_SEMVER_POLICY_PROPOSAL_2026-11-22.md` (NO ADOPTED). Para estos cuatro documentos se debe usar la ubicación interna más reciente en vez de la marca anterior EXTERNAL; los registros históricos del índice se conservan como checkpoint previo.

## Archivos incorporados: PCM-P0-ARCHIVE-002 — 2026-11-22

| Archivo en `meta/project-control` | SHA-256 original | Estado |
|---|---|---|
| `records/provenance/PCM-GOV-PROV-CORR-001_R2_ATOMIC_ADDITIVE_PROVENANCE_CANDIDATE_2026-11-21.md` | `d68d6563c94e2141a76e5126ca1d513974b82df9bee3fd3358afde8d21256572` | R2 revisado y no aceptado |
| `records/provenance/PCM-GOV-PROV-CORR-001_R3_ATOMIC_PROVENANCE_CORRECTIVE_CANDIDATE_2026-11-21.md` | `f4317eaae4047086d32e00247e5e6f36e01c7e2d6a5c0b87f086eab524291d09` | R3 candidato pendiente |
| `records/provenance/PCM-GOV-PROV-CORR-001-IQA-001_INFORME_QA_INDEPENDIENTE.md` | `918859b5bfc6bf8601f61a48ea2708f9d8399f2d52467a594f0fd94474f25c6e` | GPT QA R2 REVISE |
| `records/provenance/PCM-GOV-PROV-CORR-001-IQA-001_GROK_FOCUSED_PROVENANCE_QA_REPORT.md` | `073963740c2a6d1b0c27c4a5d4a640c39adcaf2859f6a07250d374ef2f2e3a38` | Grok QA R2 PASS CONDITIONAL |
| `records/provenance/PCM-GOV-PROV-CORR-001_R2_DUAL_QA_CONSOLIDATION_AND_R3_DISPOSITION_2026-11-21.md` | `1e32610b82f4eab020fd0e6b9be5b4ba5221724efbc4dc57a13ef62ba655d644` | Conciliación / propuesta R3 |

Archivo de custodia: `inventory/PCM-P0-ARCHIVE-002_CORR_CUSTODY_AND_VERSIONING_2026-11-22.md`. Nota de decisión: `decisions/PCM-VERSIONING-001_OWNER_SCOPE_CLARIFICATION_2026-11-22.md`.

## PCM-P0-ARCHIVE-003 — 2026-11-22

Índice de once fuentes originales de recepción y G2-A: `inventory/PCM-P0-ARCHIVE-003_G2A_CHAIN_2026-11-22.md`. Los ficheros se localizaron en `records/initial/` y `records/g2a/`, con SHA-256 individuales y blobs verificables. Conservación aditiva; no aceptación implícita.

## PCM-P0-ARCHIVE-004 — 2026-11-22

El expediente G2-B contiene ahora 24 originales preservados en `records/g2b/`. Tabla completa de nombres y SHA-256: `inventory/PCM-P0-ARCHIVE-004_G2B_EVIDENCE_CHAIN_2026-11-22.md`. No asumir que un documento cuyo título dice Owner decision es una decisión primaria si su emisor real es GPT. Se mantienen el STOP P5→P6 y las reservas históricas.

## P0 archivo 005 — 2026-11-22

Otros 22 originales con identidad Git/SHA y estado histórico propio: `inventory/PCM-P0-ARCHIVE-005_PLANNING_AND_PROVENANCE_2026-11-22.md`; rutas enumeradas allí. Estos archivos complementan, no superseden, las fuentes G2-A/G2-B previamente archivadas.
