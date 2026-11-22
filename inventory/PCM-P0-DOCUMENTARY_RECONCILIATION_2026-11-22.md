# PCM-P0 — Recuperación e inventario documental (primer corte)
  
**Estado:** P0 IN_PROGRESS / FOCUSED ARCHIVE PASS / INVENTORY NOT EXHAUSTIVELY RECONCILED.
**Emisor:** PCM-001 (coordinador provisional). **Destino:** Owner / futuros coordinadores del maestro.
**Corte observado:** 2026-11-22. **Repositorio público:** KhaosMagnus/Project-Control, rama meta/project-control.
**Control de entrada:** 532d3e6186908654e212f9f40ee60d06612f7858. La revisión de publicación es el commit que contiene este archivo.

## Alcance del censo local

Inspección de los archivos de trabajo montados en esta sesión, no del universo completo de archivos de ChatGPT ni de todos los repositorios:

- 107 archivos locales: **91 .md / 12 .zip / 4 .png**; no afirmar que todos sean autoritativos.
- Al menos **8 Markdown con advertencias explícitas CONTROLLED / NO PUBLICAR** o indicaciones de contener inventarios privados. Se mantienen fuera del GitHub público.
- Hay duplicados por nombres de paquetes y versiones superseded en otros recursos de conversación/Biblioteca: no fusionar sin comparación SHA.
- Candidatos no aceptados, informes QA y decisiones Owner se clasifican por separado. Un paquete ZIP puede contener copias del mismo contrato; no contarlas como documentos distintos sin verificar bytes.
- Otros documentos, ZIP e imágenes permanecen **UNREVIEWED_FOR_PUBLICATION**; su sola presencia local no autoriza copiarlos públicamente.
- Este censo **no** prueba que las copias locales sean la fuente original de emisiones del Owner. Para auditores externos, decisiones no exportadas siguen SECONDARY_ATTRIBUTED.

## Primeras cuatro fuentes conservadas sin reescritura

| Documento fuente | SHA-256 de los bytes originales | Ubicación en meta/project-control | Tratamiento |
|---|---|---|---|
| PCM-GOV-PROV-DES-003 / R3 | `325bd44c8ab572cd7229219d7f08325e170c0e0797f9025c1abae4abb0a10cad` | `records/provenance/PCM-GOV-PROV-DES-003_ATTRIBUTION_CONTRACT_R3_CORRECTIVE_DRAFT_2026-11-20.md` | Archivo del candidato **aceptado localmente por decisión Owner posterior**; no modificar su viejo estado DRAFT |
| Re-QA R3 ChatGPT | `a24c116f02399946ccf7f7aaab11a460d0679af6d174e5d15fbe471434a2fb61` | `records/provenance/PCM-GOV-PROV-IQA-002_INFORME_REQA_INDEPENDIENTE.md` | DESIGN PASS (CONDITIONAL) |
| Re-QA R3 Grok | `61b68c3ede0823d4286f73214e69b624c1b968709b09e14acc943942670bb7c9` | `records/provenance/PCM-GOV-PROV-IQA-002_GROK_FOCUSED_R3_REQA_REPORT.md` | DESIGN PASS (CONDITIONAL) |
| Constancia de decisión R3 | `ac4e43a0d123aaa8c32b35b38699132338e791970237c3194442b57b37b8ac81` | `records/provenance/PCM-GOV-PROV-R3-ACCEPTANCE-001_LOCAL_OWNER_DECISION_RECORD_2026-11-21.md` | Constancia documental GPT; **no reemplaza mensaje Owner original** |

## Pendientes por expediente (no autoautorizados)

| Serie | Custodia actual | Gate |
|---|---|---|
| G2-A y D-R3-APP | Archivos locales/Biblioteca. Incluye documentos expresamente CONTROLLED con inventarios de repos privados | Separar versiones, clasificar, generar extractos sanitizados si procede; originales NO PUBLICAR |
| G2-B / P0–P8 | Expedientes en archivos/paquetes anteriores; contratos congelados preservados fuera de este primer archivo | G2-B NOT ACCEPTED; P8 QA INCONCLUSIVE, Q6 elegibilidad FAILED, P5→P6 STOP histórico intacto |
| Enmienda UNI | Fuentes locales, QA de diseño favorable, pendiente de decisión | OWNER ACCEPTANCE PENDING |
| CORR-001 R1/R2/R3 | Fuentes locales y paquetes. GPT REVISE sobre R2 y Grok PASS CONDITIONAL; R3 candidato | R3 re-QA NOT AUTHORIZED / NOT EXECUTED; no aceptar ni publicar como decisión histórica vigente |
| Producto portable `main` | Bootstrap 1.0 en fuente histórica YU3DOH, Git blob `13eae102d5aed553d4fb3a023ab77b71601306b2`; protocolo blob `1ac3689c1e811d1594291afee6b2c1c6efd093d0` | NO IMPORTADO / NO RELEASE / decisión posterior separada |

## Retorno y siguientes pasos

**SOURCE:** PCM-001; **TARGET:** Owner y próxima instancia de gobierno; **ACTION:** completar inventario por lotes, incorporando únicamente fuentes de publicación permitida con digest verificado y referencias de autoridad. **RETURN:** actualizar PROJECT_STATE, REQUEST_LEDGER y ARTIFACT_INDEX por commit aditivo tras cada lote.

La exportación literal de mensajes Owner a este repositorio público requiere tratamiento independiente. El índice es evidencia primaria de su propio inventario, no de autenticidad de las decisiones históricas relatadas.
