# PCM-GOV-AUTHREQ-001 — Separación explícita de recomendaciones, solicitudes y autorizaciones

**Proyecto:** Project Control Master
**Emisor/redactor:** PROJECT_CONTROL_MASTER / PCM-002 (provisional)
**Fecha:** 2026-11-22
**Estado del contenido:** PROPOSED / IMPROVEMENT PENDING / NOT ADOPTED / NO NORMATIVE EFFECT
**Publicación documental:** GRANTED únicamente por decisión Owner `PCM-002-AUTHREQ-001` de 2026-11-22; la autorización de archivo NO constituye aceptación normativa.
**Origen del problema:** Observación directa del Owner durante el relevo PCM-001 → PCM-002.
**Control de entrada:** `meta/project-control@1f0e2e2eda967bb90f7bb21c18446fa790b4fbad`
**Fuentes normativas y locales:** `GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0.md` blob `1ac3689c1e811d1594291afee6b2c1c6efd093d0` (FROZEN, no modificado); `records/provenance/PCM-GOV-PROV-DES-003_ATTRIBUTION_CONTRACT_R3_CORRECTIVE_DRAFT_2026-11-20.md` blob `9ed659715a47a199df4b21005382c68678958dc8`; constancia de aceptación local `records/provenance/PCM-GOV-PROV-R3-ACCEPTANCE-001_LOCAL_OWNER_DECISION_RECORD_2026-11-21.md` blob `107aab1f7332849385737655bb171da1b712980a`.

## 1. Hallazgo confirmado

Project Control dispone de separación conceptual entre recomendaciones, decisiones, autorizaciones y ejecución. Sin embargo, no se ha identificado un mecanismo normativo y verificable que obligue a presentar una solicitud de autorización **independiente y claramente comunicada** cuando una recomendación o un documento preparado requieran una acción reservada.

PCM-002 produjo documentación para su incorporación futura al repositorio, pero no presentó adecuadamente una solicitud formal de publicación. Una recomendación final sobre posible publicación fue erróneamente presentada después como si equivaliera a una solicitud de autorización. No la equivalía.

El resultado fue una entrega incompleta desde el punto de vista de trazabilidad y continuidad; la ausencia de escritura GitHub sin permiso fue correcta.

**Clasificación propuesta:** `WORKFLOW NONCONFORMITY / MISSING EXPLICIT AUTHORIZATION REQUEST`.

**Límite de evidencia:** observación en el diálogo de relevo PCM-002/Owner; no es dictamen de QA independiente. Los mensajes originales del Owner no se exportan con este archivo; su atribución es secundaria para lectores externos.

## 2. Requisito propuesto

Todo agente sujeto a Project Control deberá distinguir expresamente:

1. **RECOMMENDATION:** propuesta técnica o documental sin efecto autorizador y sin equivalencia automática con una solicitud.
2. **AUTHORIZATION_REQUEST:** petición expresa, identificable e independiente dirigida a la autoridad competente para una acción determinada.
3. **OWNER_DECISION:** resolución efectiva sobre el alcance solicitado.
4. **EXECUTION:** operación efectuada dentro de una autorización válida.
5. **VERIFICATION_RETURN:** evidencia posterior de ejecución y estado.

Una recomendación **nunca constituirá por sí misma** una solicitud de autorización. Una solicitud **nunca constituirá** una autorización. Una decisión de aceptar el diseño no implicará permiso de implementación o publicación salvo que su alcance lo establezca expresamente.

Una instrucción directa del Owner podrá ser autorización suficiente cuando defina inequívocamente acción y alcance. No será necesario exigir una solicitud artificial cuando ya exista autorización válida. Ante ambigüedad material, STOP y petición de precisión antes de escribir.

## 3. Gate propuesto: AUTHORIZATION REQUEST COMPLETENESS

Antes de concluir una entrega que requiera otra acción para completar su ciclo documental, el agente deberá:

- Identificar el artefacto preparado y su estado.
- Indicar su ubicación documental autoritativa prevista.
- Determinar si existe autorización efectiva para publicarlo.
- Si falta autorización, formular una solicitud explícita, inequívoca y separada de la recomendación.
- Identificar el actor decisor, la acción solicitada, los archivos/rutas, las restricciones y el resultado esperado.
- Registrar `PENDING_OWNER_DECISION` cuando corresponda.
- No presentar el resultado como completamente integrado hasta verificar su publicación autorizada.

**Verificación propuesta:** cualquier recomendación de acción reservada deberá finalizar con una disposición verificable: (a) una `AUTHORIZATION_REQUEST` explícitamente emitida; (b) autorización vigente y exacta; o (c) acción diferida/rechazada, con responsable y próxima ruta. Una mera sugerencia de “próxima operación” no satisface (a).

## 4. Aplicación a agentes, chats y modelos LLM

Se propone incorporar este control al procedimiento de bootstrap y recepción de nuevas instancias, con una comprobación inicial de:

- Protocolo y versión efectivamente adoptados.
- Revisión de control exacta y estado actual.
- Rol y permisos vigentes de la instancia.
- Requisitos documentales y rutas de publicación.
- Solicitudes y autorizaciones pendientes.
- Restricciones de ejecución y criterios STOP.

El agente deberá confirmar que ha interpretado esas obligaciones antes de realizar operaciones materiales.

La instrucción documental sola no garantiza el cumplimiento de otros LLM: se propone además evaluar un validador de transiciones y permisos en el adaptador, si es técnicamente integrable con el punto real de operación.

## 5. Validaciones propuestas

| Caso | Resultado exigido |
|---|---|
| LLM recomienda eliminar un archivo | No interpretar como solicitud ni permiso de borrado |
| LLM recomienda publicar documentación | Presentar solicitud independiente si carece de autorización |
| Owner acepta únicamente un diseño | No implementar ni publicar por inferencia |
| Owner autoriza expresamente una publicación delimitada | Ejecutar solo dentro de ese alcance y verificar |
| Chat sucesor recibe artefactos pendientes | Reconstruir estado y autoridad; no inventar GRANTED |
| Agente genera documento local sin autorización de publicación | Identificarlo como candidato pendiente y solicitar decisión |

## 6. Alcance y restricciones

Esta propuesta no modifica el protocolo v1.0 congelado, no concede permisos generales a PCM-002 y no constituye una norma efectiva.

La obligatoriedad para adoptantes futuros requiere diseño, evaluación de compatibilidad, QA, decisión del Owner y publicación de una versión sucesora.

Las herramientas de comprobación automática son una capacidad por diseñar. No se presume que un modelo externo pueda ser controlado sin integración y acceso efectivo al contrato.

**No autorizados por este expediente:** cambios en `main`, `dev/portable`, archivos congelados, rulesets, nuevos permisos, pruebas técnicas, QA, releases o implementación de validadores.

## 7. Disposición y ruta

**IMPROVEMENT REQUIRED — OPEN / PROPOSED.**

Siguiente acción: evaluar el diseño, definir condiciones de aceptación y preparar su posible incorporación futura al estándar portable. La autorización `PCM-002-AUTHREQ-001` cubre **solo esta publicación de propuesta y el registro en dos índices**. No cerrar hasta disponer de criterios de aceptación y evidencia de validación.

**Custodia histórica:** no reescribir ni recalificar las decisiones del Owner, el protocolo v1.0 o los contratos congelados. Preservar la separación entre propuesta, autorización documental, QA y adopción normativa.
