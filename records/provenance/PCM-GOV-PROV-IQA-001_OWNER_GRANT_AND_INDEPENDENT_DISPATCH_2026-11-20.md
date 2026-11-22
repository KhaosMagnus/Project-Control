# PROJECT CONTROL MASTER — Constancia de autorización y transferencia QA

**Registro:** `PCM-GOV-PROV-IQA-001 / OWNER-GRANT-AND-DISPATCH-001`  
**Fecha declarada por el entorno:** 2026-11-20 (America/Mexico_City)  
**Estado:** `OWNER GRANTED QA ONLY / DISPATCH PREPARED / REVIEWS NOT YET RECEIVED`  
**Modo:** Solo lectura y trabajo documental local; sin modificación o publicación GitHub.

## 1. Acto emitido por el Owner

El Owner emitió expresamente en la conversación actual la decisión `PCM-GOV-PROV-IQA-001`, `GRANTED QA ONLY`. Autoriza **exclusivamente** dos evaluaciones documentales separadas de A1–A12 sobre:

- Candidato `PCM-GOV-PROV-DES-002_ATTRIBUTION_CONTRACT_R2_2026-11-20.md`, SHA-256 `1391ca809bddaae1a2f6907ca1b9845dca616ee5a391bb7a1a8cef0a028b8375`.
- Paquete `PCM-GOV-PROV-IQA-001_SHARED_REVIEW_PACKET_2026-11-20.zip`, SHA-256 `b7f98ed527b84cae73c8904c4348572709d914a3aedab32e2838fc91e60233fe`.

La decisión no acepta la política R2 ni autoriza su aplicación normativa o publicación; tampoco acepta la enmienda unipersonal anterior ni G2-B. No permite escrituras GitHub, permisos, PR, integraciones, activación PCM-001 o G3/G4/G5.

## 2. Registro de procedencia de la decisión

- **Origen del problema de atribución:** observación original del Owner en la conversación (hecho comunicado directamente por el Owner).
- **Diseño técnico de la solución y documento R2:** elaborado/recomendado por PCM-001 (GPT).
- **Redacción inicial del bloque `GRANTED QA ONLY`:** sugerida por PCM-001 (GPT) en la respuesta precedente.
- **Emisión vinculante de `GRANTED QA ONLY`:** mensaje posterior del Owner reproduciendo/aceptando ese texto.
- **Alcance aprobado:** QA documental de diseño únicamente. Que el Owner adoptara el texto sugerido no le convierte en autor de sus recomendaciones técnicas originales.

Esta constancia es un **registro derivado de la conversación**, no una exportación certificada de la conversación. Los mensajes originales permanecen como fuentes primarias; cualquier divergencia requiere cotejo con ellos. No se incorpora esta constancia dentro del ZIP congelado.

## 3. Verificación local de integridad previa a distribución

El ZIP existente fue verificado en modo lectura: SHA-256 externo coincide con la decisión Owner; la prueba CRC del ZIP pasó; contiene **12 miembros**, de los que **11 constan en el manifiesto**; tamaños y SHA-256 coincidieron para los 11. El miembro 12 es el propio manifiesto. El candidato separado coincide con el SHA-256 aprobado.

## 4. Transferencia a dos evaluadores independientes

Entregar el **mismo ZIP** en dos chats/sesiones evaluadoras separadas, uno ChatGPT y otro Grok. No compartir los dictámenes entre ellos hasta que ambos se hayan emitido al Owner. Cada revisor deberá:

1. Verificar el ZIP, su manifiesto y el SHA-256 del candidato, y declarar el alcance real de la verificación.
2. Revisar A1–A12 conforme al `PCM-GOV-PROV-IQA-001_FOCUSED_QA_ASSIGNMENT_2026-11-20.md` incluido en el ZIP.
3. Distinguir siempre autor de propuesta, autor de redacción, emisor de decisión, autorizador, operador, observador y QA. Separar evidencias primarias de declaraciones atribuidas y marcar `UNKNOWN` donde falten.
4. Evaluar expresamente el caso P5→P6, la aceptación Owner y la no convalidación histórica.
5. Emitir por control `VERIFIED / PARTIAL / UNKNOWN / FAILED` y veredicto `DESIGN PASS (CONDITIONAL) / DESIGN REVISE / DESIGN FAIL / INCONCLUSIVE`, con citas de fuente y SHA cuando proceda.
6. Entregar solo al Owner un informe autocontenido. No modificar GitHub, permisos, repositorios, PR, ramas, reglas, aprobaciones ni registros congelados.

## 5. Próximo gate

Después de recibir ambos informes, PCM-001 podrá realizar una **conciliación documental**. La aceptación final de R2 corresponde exclusivamente al Owner mediante decisión nueva que identifique el candidato por su SHA exacto. Esta autorización de QA no contiene ni sustituye dicha decisión.

**Estado final de este registro:** `QA DISPATCH PREPARED / NO QA VERDICT CLAIMED / OWNER ACCEPTANCE PENDING / NO GITHUB WRITES`.
