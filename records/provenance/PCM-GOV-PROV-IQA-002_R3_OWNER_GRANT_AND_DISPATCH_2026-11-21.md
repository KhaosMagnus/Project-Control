# PROJECT CONTROL MASTER — CONSTANCIA DE AUTORIZACIÓN Y TRANSFERENCIA R3

**Assignment:** `PCM-GOV-PROV-IQA-002`  
**Source:** Owner, mensaje original de esta conversación, 2026-11-21 (America/Mexico_City).  
**Mode:** `GRANTED QA ONLY — R3 FOCUSED RE-QA / STRICT READ-ONLY`  
**Coordinator:** `PCM-001` (provisional; sin autoridad ejecutiva).  
**Destination:** dos evaluadores documentales separados, ChatGPT y Grok.  

## 1. Objeto exacto autorizado

- Candidato `PCM-GOV-PROV-DES-003 / R3`, archivo `PCM-GOV-PROV-DES-003_ATTRIBUTION_CONTRACT_R3_CORRECTIVE_DRAFT_2026-11-20.md`, SHA-256 `325bd44c8ab572cd7229219d7f08325e170c0e0797f9025c1abae4abb0a10cad`.
- Paquete compartido `PCM-GOV-PROV-IQA-002_R3_FOCUSED_REQA_PROPOSED_PACKET_2026-11-20.zip`, SHA-256 `9d6d181b051f3e1d26944ce3ae2bf7138448df802f8509f76dd70d8feca79f11`.
- Alcance: F1 (rechazo explícito `REJECT`, `ACCEPT_MODIFIED`, escenario A/B′/C); F2 (fuentes primarias, secundarias y `UNKNOWN` por afirmación). Regresión A1–A12, comparación R2→R3 y preservación de los registros originales.

## 2. Comprobación local de integridad

Comprobación de este coordinador: SHA-256 del candidato y del ZIP coinciden con el texto emitido por el Owner. `zipfile.testzip()` devolvió `None` (sin CRC fallidos), 8/8 entradas únicas. Manifiesto JSON: 7/7 miembros declarados coinciden exactamente en nombre, tamaño y SHA-256. Ningún miembro fue alterado.

El ZIP contiene el assignment histórico con `NOT AUTHORIZED` porque fue preparado antes del GRANTED. Ese texto original permanece intacto: la **decisión posterior y separada del Owner** es la que habilita hoy esta QA, sin reescribir el manifiesto ni el paquete congelado.

## 3. Instrucción homogénea a ambos evaluadores

Cada evaluador recibe **el mismo ZIP y el mismo encargo** en un contexto de revisión separado. No se entregan las conclusiones del otro hasta finalizar ambos informes.

- Verificar primero la integridad del ZIP, el manifiesto y SHA-256 del candidato.
- Contrastar R2, R3 y su diff; comprobar F1 y F2 en el esquema **y en la matriz piloto histórica**, no solo en las declaraciones de principios.
- Evaluar regresión A1–A12 como `VERIFIED`, `PARTIAL`, `UNKNOWN` o `FAILED`, con fuente y límite por control.
- Distinguir `idea_originator`, `recommender`, `drafter`, `issuer`, `decision_maker`, `execution_authorizer`, `operator`, `verifier` y `qa_author`.
- Tratar los mensajes originales del Owner no incluidos en el paquete como `SECONDARY_ATTRIBUTED` respecto de esos actos en esta QA, aunque sean accesibles como evidencia primaria local en la conversación de PCM-001. `UNKNOWN` para origen intelectual no probado. Un SHA prueba bytes y no procedencia intelectual.
- Registrar prueba atómica A / B′ / C: aceptación, aceptación modificada y rechazo inequívoco, sin autorización de ejecución para C.
- Preservar R2, los informes de QA previos y la no conformidad histórica P5→P6. No confundir aceptación de recomendaciones con autoría del Owner.
- Emitir dictamen independiente `DESIGN PASS (CONDITIONAL)`, `DESIGN REVISE`, `DESIGN FAIL` o `INCONCLUSIVE`, con hallazgos y correcciones precisas.

## 4. Prohibiciones y estado

**No** modificar GitHub, no crear ramas, PR ni revisiones, no cambiar permisos, no publicar archivos, no aplicar normativamente R3, no aceptar G2-B ni activar PCM-001, ni continuar G3/G4/G5. Esta transferencia no concede permisos nuevos a los evaluadores.

**Estado:** `R3 QA GRANTED / DISPATCH READY / TWO INDEPENDENT REPORTS PENDING / R3 NOT ACCEPTED / G2-B NOT ACCEPTED`.

## 5. Trazabilidad de la autorización

- **Necesidad inicial de mejorar la atribución:** planteada directamente por el Owner.
- **Propuesta y redacción técnica R3:** PCM-001/GPT.
- **Autorización de QA vigente:** mensaje efectivamente emitido por el Owner en esta conversación; la posible redacción previa propuesta por GPT no transfiere al Owner el origen de la propuesta.
- **Aceptación de R3:** no emitida.

Esta constancia es una copia documental aditiva de coordinación, no un acta normativa ni un reemplazo del mensaje primario del Owner.
