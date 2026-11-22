# PCM-001 — Plan de control y aprobación de atribución de decisiones

**Propuesta de PCM-001 — No es una orden emitida por el Owner.**  
**Estado:** `DESIGN PREPARED / QA NOT YET REQUESTED / OWNER ACCEPTANCE PENDING`.

## Qué cambia exactamente

- No cambia el poder de decisión del Owner; hace auditable **quién originó/recomendó/redactó una cláusula**, quién la emitió, quién la aceptó y quién operó.
- Corrige el defecto de etiquetar `Owner GRANTED` como si el Owner hubiera inventado el requisito técnico.
- Para P5→P6 conserva **dos verdades simultáneas**: el Owner autorizó/ejecutó conforme a propuestas recibidas; PCM-001 redactó la instrucción operativa que omitió respetar el STOP histórico. No reescribe P5, P6 ni P8.
- Cambia el **formato de registros futuros** y permite anexos correctivos aditivos, no cambios a contratos congelados.

## Gates de aprobación (ninguno ocurre automáticamente)

| Gate | Responsable | Entradas | Resultado y STOP |
|---|---|---|---|
| G0 — preparar | PCM-001 | Solicitud actual del Owner; borrador previo | **Cumplido**: R2 + paquete con hash + plan; sin publicación |
| G1 — autorizar QA | Owner | Revisión superficial de objetivo, límites y fuentes; hash exacto de R2 y paquete | `GRANTED QA ONLY / REVISE / DEFER`; si no se concede, no presentar QA como encargada |
| G2 — dos QA | ChatGPT y Grok, separadas | Mismo ZIP y contrato A1–A12 | Dos informes independientes; diferencias materiales → `REVISE` y nuevo candidato, no aceptación implícita |
| G3 — aceptar política local | Owner | R2 exacto + informes + conciliación de PCM-001 | `ACCEPT / REVISE / DEFER`. **Solo aquí** podría cobrar vigencia prospectiva local |
| G4 — corregir historial | PCM-001 redacta, Owner dispone | Fuentes primarias disponibles y registros originales | Anexos `PROVENANCE_CORRECTION` aditivos; no reabrir ni modificar congelados; publicación GitHub requiere autorización aparte |
| G5 — retomar G2-B | Owner / PCM-001 | Evidencia Q5/Q7/Q8/Q9, gate histórico QA P8, enmienda unipersonal separada | Solicitud específica de aceptación G2-B; no se autoriza por esta política |

**No se requiere** probar GitHub ni modificar rulesets para evaluar esta política documental.

## Cómo se usaría en una decisión futura

1. GPT recomienda una medida: `AGENT_RECOMMENDATION`, expediente y versión exactos.
2. Tú respondes «acepto la recomendación, solo como diseño»: `OWNER_ADOPTION_OF_RECOMMENDATION`, `scope=DESIGN_ONLY` ligado a la propuesta.
3. Una segunda respuesta autoriza una acción concreta: `OWNER_EXECUTION_GRANT` con operador, condiciones, STOP.
4. Se ejecuta y se relee: `OWNER_OPERATOR_ACTION` y `READBACK_OBSERVATION` separados.
5. QA evalúa y tú aceptas o rechazas: `INDEPENDENT_DOCUMENTARY_QA` y `OWNER_FINAL_ACCEPTANCE` separados.
6. Si GPT se equivocó en un paso, registrar el defecto de recomendación/conducción y tu autorización **sin convertir** el error de GPT en una idea originada por ti.

## Qué puede autorizarse ahora

**Opción recomendada — `GRANTED QA ONLY`**: autorizar exclusivamente la remisión del ZIP para QA focalizada, sin dar vigencia aún al contrato. La política solo debería aceptarse tras dos dictámenes favorables y tu aceptación específica.

**Decisión propuesta (NO emitida):**

> OWNER DECISION — `PCM-GOV-PROV-IQA-001` — `GRANTED QA ONLY`. Autorizo únicamente el envío del paquete congelado `PCM-GOV-PROV-IQA-001_SHARED_REVIEW_PACKET_2026-11-20.zip` (SHA-256 informado por PCM-001) a dos evaluadores documentales separados para los controles A1–A12. La propuesta fue redactada por PCM-001 a partir de una observación iniciada por mí. No acepto todavía `PCM-GOV-PROV-DES-002`, no doy permiso de publicación o escrituras GitHub, no acepto la enmienda unipersonal ni G2-B, y mantengo G3/G4/G5 diferidos.

La decisión anterior es **un texto recomendado por GPT** hasta que el Owner lo emita o adopte; su posterior adopción deberá registrar `drafter=PCM-001`, `issuer/decision_maker=OWNER`.

## Acción de mayor impacto

Revisar R2 y, si coincide con tu intención, **autorizar solo su QA**. Evitar aceptar la política y la infraestructura al mismo tiempo. Cuando regresen las dos QA, prepararé una conciliación y el acto exacto de aceptación documental por separado.
