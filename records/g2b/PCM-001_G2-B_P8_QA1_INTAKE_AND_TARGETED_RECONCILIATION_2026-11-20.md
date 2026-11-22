# PROJECT CONTROL MASTER — P8 / Recepción de QA1 y conciliación focalizada

**Identificador:** `PCM-G2B-P8-QA1-INTAKE-001`  
**Coordinador:** `PROJECT_CONTROL_MASTER / PCM-001 (PROVISIONAL)`  
**Fecha:** 2026-11-20 (America/Mexico_City)  
**Estado:** `QA1 RECEIVED / INCONCLUSIVE / G2-B OWNER ACCEPTANCE NOT YET SUPPORTED`  
**Modo:** Recepción, análisis documental y GET de GitHub únicamente. Ninguna escritura en GitHub.  
**Alcance:** Reconciliar evidencia de P8. No enmendar contratos congelados, no convalidar retrospectivamente P5 ni activar G3/G4/G5.

## 1. Objeto recibido e integridad

- Informe independiente de ChatGPT: `PCM-G2B-IQA-INFRA-001_INFORME_QA_INDEPENDIENTE.md`, 17,997 bytes, SHA-256 `945acec3dd5fb5450aadbc30a3d3b06d0660af300f73d666e410d604e881c80f`; procedencia: documento entregado por el Owner a través de la Biblioteca, `libfile_4dcb0ea639dc8191953f6b5034e2d32f`.
- Paquete congelado examinado: `PCM-001_G2-B_P8_INDEPENDENT_INFRA_QA_SHARED_PACKET_2026-11-20.zip`, 43,393 bytes, SHA-256 `2c4b4a0b7835386e7ec5e25cfd635bc0ae43a8ca3d49d511ba0e85af3496c499`.
- Veredicto individual: **INCONCLUSIVE**. Q1–Q4 VERIFIED, Q5–Q8 PARTIAL, Q9 UNKNOWN / NOT OBSERVED. El informe completo se conserva sin edición. **No existe aún aquí una segunda QA independiente P8 recibida**.
- Contrato de aceptación de QA incluido en el ZIP: `G2-B_INDEPENDENT_QA_CONTRACT.md`, SHA-256 `a1c10a91bc0947e3a84d4c8d48da404c7494f45154e8613c0a65bdd07b6633b3`. Exige dos dictámenes y aceptación explícita posterior del Owner.
- Solicitud ejecutiva G2-B original: SHA-256 `037b1c559c319fbca50b4aee3d86616f7c1c4c4399fe3a88426edd7350018349` (GRANTED del Owner constó directamente en la conversación).

## 2. Evidencia externa actual observada (solo lectura)

Repositorio: `KhaosMagnus/Project-Control`, ID `1465064417`, público. Refs observadas:

| Ref | Commit | Árbol | Padres | Evidencia |
|---|---|---|---|---|
| `main` | `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb` | `04bff84a661781fb8f3982235c6c93f668a658ed` | `[]` | QA1 verificó payload y raíz, repositorio vigente coincide |
| `meta/project-control` | `cac838940e0e824a1f828ff660e422a6441a1da7` | `3e39ae46b9e1690604387452ee7283062a79e182` | `[]` | QA1 verificó payload y raíz, repositorio vigente coincide |

Rulesets observados, todos `active`, sin bypass: `PCM-GENESIS-SAFETY` `27708103` (ambas refs, antieliminación/no fast-forward); `R-MAIN` `27709862` (main); `R-META` `27717600` (meta). Los dos perfiles tienen PR obligatorio, una aprobación, historial lineal y métodos squash/rebase.

Instalación `162412374`: `repository_selection=selected`, 11 IDs preservados, ID `1465064417` no figura en la enumeración. Esta es **evidencia del conector**, no sustituye la instantánea administrativa requerida por Q7.

## 3. Matriz de disposición

| Control | QA1 | Disposición coordinador | Evidencia o decisión restante |
|---|---|---|---|
| Q1–Q4 | VERIFIED | Conservar `VERIFIED` dentro del alcance de QA1. No reabrir por sistema. | Corroboración del segundo revisor, sin nuevas escrituras. |
| Q5 | PARTIAL | Ruleset y timestamps acreditados; continuidad *desde antes del primer push* no queda demostrada solo por estado actual. | Recuperar de la conversación la secuencia original P2→P3→P4, readbacks y salidas disponibles; señalar expresamente que hora de autoría del commit no es hora de recepción del push. No fabricar logs. |
| Q6 | PARTIAL | **Desviación material de procedimiento P5**: la solicitud ejecutiva exigía ruta de aprobación independiente y elegible demostrablemente viable y STOP antes de P6 si no se acreditaba. La revisión del Owner de la configuración P5 no sustituía ese requisito. P6 y P7 se realizaron. | Registrar no conformidad sin reescribir historial. Owner debe decidir disposición explícita de la desviación y cómo se resolverá la elegibilidad para futuras PR. Si exige dos personas físicas, actualmente no hay ruta demostrada. Conceder permisos o cambiar política requiere autorización propia. |
| Q7 | PARTIAL | `selected` + once IDs + maestro ausente acreditados a nivel de conector. | Captura actual de `Installed GitHub Apps → Configure → Only select repositories` desde administración, tomada **después** de la creación del maestro; conservar procedencia, fecha, lista de selección y correspondencia de ID. No tocar Save. Reconocer que el alcance de OAuth/tokens ajenos no está demostrado. |
| Q8 | PARTIAL | La conversación contiene el GRANTED original, hashes de P3, salidas de los dos pushes y verificaciones de P2–P7. Es evidencia adicional al ZIP Q8, pero no un log exhaustivo de todas las operaciones. | Compilar transcripción/autorización y salidas **originales** con fechas, señalando que su incorporación posterior no constituye un registro preexistente ni demuestra la ausencia universal de otros intentos. Que el Owner indique si reconoce otros intentos o fallos. |
| Q9 | UNKNOWN | No hay incidente documentado de timeout, fallo o recuperación. El contrato evalúa tales eventos **si existen**. | El Owner puede declarar si se presentaron; en ausencia de incidentes observados, registrar `NOT TRIGGERED / NO RECOVERY TEST` con reserva epistemológica, sin exigir ensayos destructivos ni atribuir PASS experimental. |

## 4. Desviación P5 — diagnóstico y límites

**Regla histórica vinculante, G2-B solicitud ejecutiva §3 P5:** `If not demonstrably viable -> STOP with protected main only; do not publish meta.` La comprobación previa de `JormungandrMagnus` concluyó `INCONCLUSIVE` y el Owner confirmó posteriormente que ambas cuentas pertenecen a una misma persona. El handoff coordinador de P5 dejó expresamente la elegibilidad para futuras PR sin acreditar y facilitó P6; dicha facilitación **no enmendó** la condición superior.

**Efecto:** no se acredita cumplimiento integral de la secuencia autorizada aunque los dos commits y protecciones actuales sean correctos. Esto es una no conformidad de proceso; el QA1 no informa que haya sido vulnerada una regla técnica de GitHub ni que haya commits espurios.

**Tratamiento permitido ahora:** congelar toda nueva escritura; preservar commits y rulesets; preparar `PCM-G2B-P5-DEVIATION-DISPOSITION` para decisión del Owner con impacto, opciones y límites. El Owner puede aceptar los efectos de un estado de infraestructura con reservas, exigir reparación prospectiva y QA adicional, o diferir G2-B. No se debe **declarar retroactivamente autorizado** el salto de P5 ni atribuir independencia humana a dos cuentas controladas por la misma persona. El contrato de aceptación G2-B exige dos QA PASS y aceptación posterior; no está satisfecho.

## 5. Acciones inmediatas, sin GitHub writes

1. Recibir el informe P8 del segundo revisor (Grok), usando el mismo ZIP congelado, y conciliar hallazgos en vez de copiar dictámenes.
2. Solicitar al Owner **únicamente** una captura administrativa posterior a creación que muestre `selected` y el conjunto, sin tocar controles, y una atestación breve de si hubo intentos fallidos/ambiguos y de si las salidas publicadas corresponden a los intentos realizados. La misma sesión del Owner ya aportó el GRANTED original, salida P3 y outputs de P4/P6.
3. Preparar el registro de desviación de P5 con dos decisiones distintas: (a) aceptación o no del estado infraestructural actual con desviación declarada; (b) política y permisos aplicables a revisiones futuras. No añadir colaborador ni cambiar `R-MAIN`/`R-META` de oficio.
4. Tras ambas QA y complementos, emitir dictamen consolidado y **solicitud de decisión del Owner**. Si se mantiene `INCONCLUSIVE`, no llamarlo PASS ni activar G3/G4/G5. Evitar nuevos ciclos de QA general cuando solo falten evidencias delimitadas.

## 6. Estado

`QA1 RECEIVED / VALID INCONCLUSIVE / Q1-Q4 VERIFIED / Q5-Q8 PARTIAL / Q9 UNKNOWN / P5 SEQUENCE DEVIATION OPEN / G2-B OWNER ACCEPTANCE PENDING / G3-G4-G5 DEFERRED / PCM-001 PROVISIONAL`

No se realizó ninguna modificación en GitHub, ni prueba de seguridad, ni operación de recuperación.
