# PROJECT CONTROL MASTER — Solicitud de decisión focalizada tras doble QA P8

**ID:** `PCM-G2B-P8-P5-DISPOSITION-001`  
**Proponente:** `PCM-001 PROVISIONAL`  
**Fecha:** 2026-11-20  
**Efecto actual:** `G2-B NOT ACCEPTED / QA1+QA2 INCONCLUSIVE / NO GITHUB WRITES`

## Fundamento

Dos revisores P8 independientes devolvieron **INCONCLUSIVE**. Q1–Q4 son aceptables en su alcance; reglas y commits actuales coinciden con la génesis, pero Q6 no acredita una persona revisora distinta y elegible. Se documentó un avance P5→P6 que contravino el STOP del contrato ejecutivo aprobado (SHA-256 `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349`). Q7 carece de captura administrativa posterior a la creación. Q5/Q8/Q9 contienen límites probatorios históricos. No existe base para declarar que las dos QA son PASS.

## Decisión reservada al Owner

**Primera cuestión: tratamiento histórico de la desviación P5**

Propuesta `ACKNOWLEDGE / PRESERVE / REMEDIATE PROSPECTIVELY`: reconocer el incumplimiento del STOP original, conservar objetos y reglas, no reescribir históricos, prohibir cambios de refs hasta regularizar los controles. **No es una convalidación retroactiva**.

**Segunda cuestión: ruta de revisión para futuras PR (elegir una)**

- `A — STRICT INDEPENDENCE`: conservar la exigencia actual de una persona distinta del Owner; preparar la autorización específica para un colaborador independiente elegible. No invitar ni conceder permisos todavía.
- `B — SOLO OWNER MODEL (DESIGN ONLY)`: autorizar **exclusivamente el diseño** de una enmienda explícita: autor técnico y Owner como revisor humano; QA documental independiente externa a la escritura; revisión de objetos `B/H/D/T_expected` y readback de `C`; límites de fork, permisos y ausencia de independencia humana declarados. Ninguna escritura, invitación, PR, cambio de rulesets o adopción queda autorizada por esta elección. Se exige QA focalizada del cambio de contrato antes de ejecutarlo.
- `C — DEFER`: mantener G2-B sin aceptación y sin cambios, a la espera de nueva propuesta.

**Tercera cuestión: declaraciones operativas del Owner (sin efecto de retroprueba)**

- Indicar si hubo o no timeouts, reintentos, pushes fallidos o recuperaciones durante P1–P7 que no se hayan incluido en esta conversación.
- Proporcionar captura administrativa POST-creación de la instalación `162412374` en `selected`, confirmando la exclusión del repositorio ID `1465064417`. No cambiar ninguna opción.

## Texto propuesto de respuesta del Owner (Opción B)

> **OWNER DECISION — PCM-G2B-P8-P5-DISPOSITION-001**  
> **DECISION: GRANTED DESIGN ONLY — OPTION B**  
> Reconozco la desviación de transición P5→P6 y ordeno preservarla como no conformidad histórica sin convalidación retroactiva. Autorizo únicamente a PCM-001 a preparar una enmienda documental limitada para operación unipersonal con separación de identidades técnicas, revisión humana por el Owner, QA documental independiente y controles verificables de PR. El nuevo modelo no se considerará equivalente a independencia entre personas. Antes de aplicarse exigirá QA focalizada y una aceptación específica. No autorizo cambios GitHub, permisos, colaboradores, PR, pruebas de escritura, G3/G4/G5 ni aceptación G2-B.

**Alternativa recomendada:** B es compatible con operación unipersonal, pero debilita el control de separación humana. A cumple el estándar aprobado sin modificarlo. La elección es del Owner.

**Advertencia:** Esta solicitud no tiene valor ejecutivo hasta que el Owner emita una disposición explícita. Incluso con `GRANTED DESIGN ONLY`, G2-B sigue `NOT ACCEPTED` y su contrato de éxito con dos PASS no se satisface.
