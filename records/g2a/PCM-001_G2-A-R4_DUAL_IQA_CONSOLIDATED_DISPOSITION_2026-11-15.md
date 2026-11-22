# PCM-001 — Consolidación de doble QA documental R4

**Control:** `PCM-G2A-R4-DUAL-IQA-CONSOLIDATED-001`  
**Fecha:** 2026-11-15  
**Rol:** `PROJECT_CONTROL_MASTER / PCM-001 PROVISIONAL`  
**Modo:** RECEPCIÓN Y DISPOSICIÓN DOCUMENTAL / SIN EJECUCIÓN  
**Estado:** `DESIGN REVISE` / CORRECCIÓN R5 REQUERIDA / `D-R3-APP,G2-B,G3,G4,G5 DEFERRED`.

## 1. Insumos y hashes constatados

| Insumo | SHA-256 de bytes recibidos |
|---|---|
| R4 candidato documental | `bcacf7ed0d36454459c7a6f7846658f40b948b56149271a66dbe762ee3b12725` |
| Informe R4 ChatGPT | `1bcb91d5397b05d502ddc03b58d6bf1a995bb48c7394184a75a9dc6ff9ba4c56` |
| Informe R4 Grok | `c6346c05ae9b81baa1e6a26dddd687fada19b0f0c7ef0932a72db32daf7f6111` |
| R3 contrato fuente | `c8789106252618549052e25a4dc43eb0b36f3d8bc15ab7d8bdbda0e1fa7ffaeb` |
| R3 addendum de aceptación documental Owner | `f23a9c66d1c5166c6645540d305afefa8a514a2eac75189a2355c59ab84eee40` |

Los informes son dos documentos **distintos** y se identifican con dos revisores distintos. Son independientes según las declaraciones de sus autores; aquí no se afirma un análisis forense de sus sesiones. Ambos reportan el mismo SHA del candidato R4 y la misma decisión Owner R3. La diferencia de veredicto se conserva sin sobrescribir ninguno.

## 2. Conciliación por hallazgo

| Hallazgo | ChatGPT | Grok | Disposición PCM-001 |
|---|---|---|---|
| `F-R3-01` — protección previa a la génesis y estados parciales | `PARTIAL`: la tabla genérica ordena STOP en un estado que P4 autoriza antes de P5 y falta tratar P6→P7 | `CLOSED DESIGN`: guarda previa y STOP suficientemente previstos | **Corrección documental requerida**: tabla por fase/acción intentada/guardas exigibles. Conservar la guarda común, el STOP si no es verificable y la prohibición de recuperación implícita. |
| `F-R3-02` — publicación bajo reglas, aprobación y SHA final | `PARTIAL`: confunde una identidad de commit que no existe antes de integrar con el objeto que puede aprobarse antes | `CLOSED DESIGN`: método PR/revisión y readback posterior suficientemente previstos | **Corrección documental requerida**: aprobación preintegración sobre entradas y árbol esperado; verificación postintegración del commit generado y su árbol; criterio material de nueva aprobación. |
| `F-R3-03` — instalación `all → selected` | `CLOSED DESIGN` | `CLOSED DESIGN` | **CLOSED DESIGN**: R4 §3 permanece, con `S_admin / S_connector / S_approved` y readback futuro; no reabrir. |

**Regla de conciliación:** la aceptación condicional de Grok es evidencia válida, pero no cancela dos contradicciones expresas encontradas por ChatGPT. Estas son defectos de especificación, no ausencia de pruebas que correspondan únicamente a G2-B. Por eso se conserva `DESIGN REVISE` hasta que el delta R5 reciba revisión.

## 3. Alcance de la corrección R5

1. Una tabla normativa por fase para `P4→P5→P6→P7`, estados esperados, lecturas ambiguas y reanudación.
2. Un contrato de aprobación **antes** de integración y validación **después**, con política exacta para resultados distintos.
3. Precedencia aditiva explícita sobre los segmentos ambiguos de R4, sin alterar R3, R4, dictámenes ni README congelados.

Fuera de alcance: reeditar `F-R3-03`, investigar otra plataforma, publicar, crear el repositorio, cambiar la instalación, ejecutar pruebas de seguridad, probar CAS o activar `PCM-001`.

## 4. Evidencia pendiente por fase

- **Antes de `D-R3-APP` (solicitud ejecutiva):** snapshot administrativo acreditado, listado exacto `S_approved` reconciliado, operador autorizado, comprobaciones de continuidad y recuperación por ID, `GRANTED` separado.
- **Antes de `G2-B` (solicitud ejecutiva):** `D-R3-APP` aplicado y verificado; identidad y metadatos de la génesis, operator/credential, mensajes, refs, guardas y condiciones de STOP congelados. No se presupone que GitHub Free permita aplicar/verificar reglas sobre un repositorio vacío.
- **Durante `G2-B` autorizado:** comprobar disponibilidad de guardas, materializar dos raíces y validar rulesets con readback independiente. Sin una capacidad exigida, STOP y volver al Owner.
- **G3/G4/G5/CAS:** fuera de la autoridad de esta revisión.

## 5. Próxima transferencia

Entregar a dos evaluadores independientes **el mismo R5 delta**, R4 fuente, ambos informes R4, la aceptación Owner y un manifiesto SHA. Revisar únicamente el cierre documental de `F-R3-01` y `F-R3-02`. Un PASS condicionado no ejecuta cambios. Una nueva divergencia exige identificar una discrepancia material y no reiniciar auditorías generales por defecto.

**DISPOSICIÓN:** `R4 DUAL QA RECEIVED / DESIGN REVISE / F-R3-03 CLOSED DESIGN / R5 DRAFT / NO GITHUB MUTATIONS`.
