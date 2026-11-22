# PCM-001 — Preflight del anexo CORR-001 y corrección R2

**Autor:** PCM-001/GPT · **Fecha:** 2026-11-21 · **Modo:** PREPARACIÓN / REVISIÓN DOCUMENTAL DEL AUTOR / SIN QA INDEPENDIENTE / SIN ESCRITURAS GITHUB

## 1. Fuentes e integridad

- Política de atribución R3: `325bd44c8ab572cd7229219d7f08325e170c0e0797f9025c1abae4abb0a10cad`. Aceptación local original observada en esta conversación; constancia documental `ac4e43a0d123aaa8c32b35b38699132338e791970237c3194442b57b37b8ac81` (para un revisor externo es secundaria respecto de ese acto Owner).
- Anexo CORR-001 R1, sin modificaciones: `1a3f7d1cdb279637207f49d7205cc28158d729a25539029afaff3f39af958b3b`.
- Nuevo candidato CORR-001 R2: `d68d6563c94e2141a76e5126ca1d513974b82df9bee3fd3358afde8d21256572`.

## 2. Revisión del autor, NO dictamen independiente

El borrador R1 distingue correctamente recomendación de PCM-001, revisión/operación del Owner, readback y disposición posterior, pero aún presentaba las ocho afirmaciones como tabla resumen. R3 §2 exige registros **por evento y cláusula** con `claims[]`, `source`, `actor`, enlaces y estado de autorización. R2 presenta ocho registros YAML autónomos y explícitos.

La antigua fórmula «cualquier resumen» no identifica un fragmento histórico erróneo exacto. R2 la convierte en corrección **interpretativa y preventiva**, localizando la discrepancia comprobable: `EXEC §3 P5` frente a `P5 §2`. No se afirma como hecho probado que el Owner hubiera escrito una orden de saltar STOP.

La regla de evidencia también mejora: frases sobre mensajes originales visibles a PCM-001 se mantienen `SECONDARY_ATTRIBUTED` para revisores que solo reciben este ZIP; documentos congelados son primarios **de sus propios textos**, no de todos los actos narrados. Las clasificaciones internas `PRIMARY_OBSERVED LOCAL` nunca se transfieren automáticamente.

**Límite de este preflight:** PCM-001 es autor y coordinador, no revisor independiente. El resultado no es PASS de QA; el candidato queda pendiente de evaluaciones externas y posterior aceptación específica del Owner.

## 3. Diferencias intencionales frente a R1

| Punto | R1 | R2 propuesto |
|---|---|---|
| Datos de 8 afirmaciones | Tabla resumen | Ocho registros por evento/claim, esquema R3 |
| `old_claim` | Referencia genérica a resúmenes | Se admite ausencia de fragmento original preciso; rectificación interpretativa |
| Clasificación de mensajes Owner | Local/externa descrita en tabla | Calificación explícita por fuente y claim, `accessible_to_reviewer` y límites |
| Autorización de corrección | PENDING | `decision.value=NONE`, `execution_authorized=false`, `status=DRAFT` para el anexo |
| Trazabilidad | Citas por tabla | Fuentes fijadas, SHA documental y limitación por predicado |

## 4. Disposición recomendada

Someter **CORR-001 R2** a dos revisiones documentales focalizadas de QA bajo un alcance de solo lectura. Verificar schema, ocho hechos, graduación, tratamiento de STOP, no convalidación y ausencia de nuevas autorizaciones. Ni la preparación de este paquete ni un dictamen favorable sustituyen un `OWNER ACCEPT` del SHA exacto de CORR-001 R2.
