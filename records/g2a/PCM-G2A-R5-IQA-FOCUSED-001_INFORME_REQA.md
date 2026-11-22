# PCM-G2A-R5-IQA-FOCUSED-001 — Re-QA documental focalizada

| Campo | Registro |
|---|---|
| Proyecto | Project Control Master |
| Revisor | ChatGPT, QA documental independiente del candidato de PCM-001 |
| Destinatario | Owner, para transferencia a PCM-001 |
| Fecha | 16 de noviembre de 2026, Ciudad de México (UTC−06:00) |
| Mandato | Revisión de F-R3-01 y F-R3-02 en modo de solo lectura |
| Veredicto | **DESIGN PASS (CONDITIONAL)** |
| Disposición | **D-R3-APP / G2-B / G3 / G4 / G5 DEFERRED**. PCM-001 **PROVISIONAL** |

## 1. Dictamen

R5 cierra los dos defectos de especificación identificados en R4. La máquina de estados usa la fase, la acción ya intentada y el estado remoto acreditado para distinguir el avance normal de una recuperación. El contrato de integración aprueba las entradas y el resultado de contenido esperado, y verifica el SHA definitivo con el árbol y el delta después de la actualización. El PASS se limita al diseño. La factibilidad en GitHub, la ejecución y la aceptación de infraestructura quedan sujetas a las condiciones de §5.

| Hallazgo | Estado R5 | Fundamento |
|---|---|---|
| F-R3-01 — Protección durante génesis, estados parciales y recuperación | **CLOSED DESIGN** | R5 §§1.1–1.2 distingue P4 de una activación P5 fallida, y distingue P6 de una activación P7 fallida. Los avances con timeout exigen evidencia independiente y concluyente |
| F-R3-02 — Aprobación previa y verificación de la integración | **CLOSED DESIGN** | R5 §§2.1–2.2 congela `B/H/D/T_expected`, método y revisión. Después coteja `C`, árbol, delta y linaje. Fija STOP y nueva disposición ante diferencias materiales |
| F-R3-03 — `all → selected` | **CLOSED DESIGN**, heredado | R5 §3 conserva el criterio de R4. Fuera del alcance de esta re-QA |

## 2. Integridad y autoridad

**ZIP recibido** — `PCM-001_G2-A-R5_FOCUSED_REQA_SHARED_PACKET_2026-11-15.zip`, 37 304 bytes. SHA-256 calculado `36f74d50563bcadbe3f37195d2531535dad9ff6b01eefdd58fdd2ee5ee3dc9e2`. A las 00:18:53 se verificaron CRC, estructura, nombres únicos y lectura como UTF-8 en **11/11 miembros**, y pertenencia, tamaños y SHA-256 de **10/10 miembros declarados**. El miembro adicional es el propio manifiesto, SHA-256 `516f69016333007364b68392492be0d60b883bdcb40e19a8e7dcf34b6fad1585`. El digest externo anunciado en el manifiesto no se aportó con estos adjuntos. Su comparación queda `NOT VERIFIED`.

| Objeto cotejado | SHA-256 calculado |
|---|---|
| Candidato `05_CANDIDATE/R5_PHASE_AND_INTEGRATION_CORRECTION.md` | `9c329b3c4be0dca6cf60bc27e92bd586a931c9236bd786f402ce508f952562e8` |
| Fuente R4 `02_BASE/R4_ADDITIVE_CORRECTION.md` | `bcacf7ed0d36454459c7a6f7846658f40b948b56149271a66dbe762ee3b12725` |
| Informe R4 ChatGPT | `1bcb91d5397b05d502ddc03b58d6bf1a995bb48c7394184a75a9dc6ff9ba4c56` |
| Informe R4 Grok | `c6346c05ae9b81baa1e6a26dddd687fada19b0f0c7ef0932a72db32daf7f6111` |
| Conciliación R4 de PCM-001 | `bf38f7291cb847e5bc7a6c4c16b0e43d6d1764c4d62d4be17a197f39ac734a56` |
| Contrato base R3 | `c8789106252618549052e25a4dc43eb0b36f3d8bc15ab7d8bdbda0e1fa7ffaeb` |
| Addendum de aceptación documental R3 | `f23a9c66d1c5166c6645540d305afefa8a514a2eac75189a2355c59ab84eee40` |

Los hashes de R4, los dos informes y el addendum coinciden con las referencias del candidato y de la conciliación. El informe ChatGPT en el ZIP es idéntico al adjunto separado. Los dictámenes R4 son documentos distintos y conservan su divergencia histórica. La fuente R4, el contrato R3 y el addendum corresponden byte por byte a sus copias en el expediente R4 anterior.

| Ref prevista | README | SHA-256 de contenido | SHA-1 Git blob |
|---|---:|---|---|
| `refs/heads/main` | 414 bytes | `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340` | `56fd6d6560434e067c126c152ab86298bd57d61f` |
| `refs/heads/meta/project-control` | 400 bytes | `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0` | `2b30688846710fe73b89a537bb5a8cfb21e738eb` |

Los dos README coinciden con los del ZIP R4 y con los digests fijados en R5. El addendum R3 conserva la aceptación del Owner de la arquitectura pública, T-A y esos bytes como **decisiones de diseño**. R5 §0 fija una precedencia prospectiva y acotada, sujeta a aceptación expresa del Owner. §1 gobierna las transiciones P4–P7 frente a la anterior tabla general y §2 aclara el flujo de integración. Los documentos históricos quedan congelados. La revisión se realizó sobre ese delta documental.

## 3. F-R3-01 — Verificación documental de las transiciones

R5 §1.1, líneas 31–44, da al operador una decisión según fase y acción intentada. Contrasté estos casos directamente con las cláusulas del candidato.

| Caso documental | Resultado exigido por R5 |
|---|---|
| P4 intentado. Primer SHA y árbol exactos, segunda ref ausente, guarda y exclusión acreditadas, P5 aún sin intentar | `EXPECTED POST-P4`. Pasar solo a P5. La ausencia de `R-MAIN` corresponde a esta fase y ya no dispara el STOP de la tabla R4 |
| P4 intentado, primera ref confirmada ausente | `PUSH NOT APPLIED / STOP`. Cualquier reentrada exige que el GRANTED cubra el caso |
| P5 intentado. `R-MAIN` acreditado sobre la primera raíz esperada, incluso si hubo timeout | `MAIN PROTECTED`. Pasar solo a P6. Si el perfil queda inactivo o sin acreditar, STOP con la primera raíz preservada; segunda ref sin publicar |
| P6 intentado. Ambos SHAs y árboles exactos, guarda y `R-MAIN` acreditados, P7 aún sin intentar | `EXPECTED POST-P6`. Pasar solo a P7. El mismo resultado aplica tras una respuesta ambigua reconciliada. Si solo consta la primera raíz tras un segundo push intentado, `PARTIAL PROTECTED / STOP` |
| P7 intentado con las dos raíces exactas | `GENESIS PROTECTED` y paso solo a P8 cuando ambos perfiles se acreditan. Si `R-META` queda sin acreditar, `PROTECTION INCOMPLETE / STOP` con ambos objetos preservados |
| En cualquier fase, ref o árbol ajenos a lo esperado, guarda exigida discrepante o lectura insuficiente | `UNEXPECTED OR UNKNOWN / STOP`. La respuesta del comando por sí sola aporta evidencia insuficiente para reintentar |

La cláusula de repositorio vacío se aplica a su creación y a la entrada a P4. Para P6 rige el estado específico de P5 ya verificado, con `main` publicado y protegido. Consignar esa distinción al congelar el procedimiento ejecutivo. Cuando hay STOP, §1.2 exige preservar fase, reglas, SHAs y logs. La reanudación requiere alcance expreso del Owner, mismos objetos congelados y lectura nueva del estado previo. Esto cierra la contradicción de R4 sin depender de una prueba remota.

La guarda común debe estar activa, cubrir ambas refs y carecer de bypass antes del primer push. La capacidad del plan, la cobertura efectiva y la lectura administrativa en un repositorio vacío permanecen `NOT VERIFIED`. Aunque la guarda sea viable, el avance normal por fast-forward en la ventana anterior al perfil individual y la capacidad administrativa de modificar reglas son riesgos residuales expresos del candidato. [GitHub Docs — reglas disponibles y aplicación](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets)

## 4. F-R3-02 — Objeto aprobado y resultado verificado

| Momento | Evidencia y decisión |
|---|---|
| Aprobación previa, R5 §2.1 líneas 57–66 | Fijar repositorio y ref, PR y autor, linaje, base `B`, cabeza `H`, árbol candidato, método exacto, delta `D` con rutas/modos/eliminaciones, árbol de salida `T_expected`, evidencia y revisión elegible. Separar al autor del revisor GitHub y registrar quién integra y bajo qué autorización |
| Comprobación inmediatamente anterior, línea 68 | Confirmar que base y candidata siguen en sus SHAs congelados, que el delta y árbol siguen correspondiendo a la aprobación, que el método y las reglas aplican y que la revisión sigue vigente. Una diferencia material obliga a STOP y nueva revisión/aprobación antes del merge |
| Lectura posterior, líneas 72–76 | Identificar el SHA `C` publicado, verificar que la ref apunta a ese resultado y cotejar continuidad del linaje desde `B`, árbol completo y delta efectivo. Para `squash`, comprobar un commit nuevo con padre `B`. Para `rebase`, comprobar la cadena lineal aplicada sobre `B` y las diferencias intermedias |
| SHA distinto con resultado conforme, línea 77 | La diferencia prevista por el método aprobado está cubierta si se acreditan la base, la candidata, el árbol, el delta, el linaje y la vigencia de la revisión. Registrar la verificación de `C` y la aceptación posterior del resultado |
| Resultado materialmente distinto o indeterminado, líneas 77–78 | STOP, preservar evidencia y remitir al Owner. Cualquier corrección requiere la autorización correspondiente. Un timeout con lectura insuficiente queda `UNKNOWN / STOP`; no habilita un segundo merge |

La aprobación queda vinculada a contenido y entradas verificables aunque GitHub genere commits con identidades nuevas al hacer `squash` o `rebase`. El readback es posterior a la actualización de la ref. Si el estado cambia entre la comprobación previa y el merge, la ruta manual conserva ese riesgo residual y no acredita CAS. Si un gate futuro exige CAS para integrar, R5 lo clasifica `NOT READY` para esa ruta. [GitHub Docs — métodos de integración de PR](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/about-merge-methods-on-github)

## 5. Condiciones del PASS y atestación

| Fase posterior | Evidencia o decisión exigida |
|---|---|
| Aceptación documental R5 | PCM-001 recibe este dictamen individual, completa la conciliación que corresponda y somete la versión exacta de R5 al Owner. La aceptación documental es una decisión distinta de una autorización de escritura |
| `D-R3-APP` | Tratarlo como gate separado conforme a F-R3-03. Obtener la autorización exacta antes de modificar la instalación y acreditar `selected` con el conjunto aprobado antes de solicitar G2-B |
| G2-B autorizado | Congelar operador, identidades, refs, bytes, modo y metadatos. Verificar exclusión real de la app y guarda efectiva antes del primer push. Si P2 no se acredita, STOP. Comprobar los perfiles precisos en P5/P7, leer ambas raíces y reglas, y obtener QA de infraestructura antes de la aceptación del Owner |
| Escritura posterior bajo reglas | Comprobar actores y método efectivos, y reunir evidencia de `B/H/D/T_expected` y de `C` bajo el alcance que autorice esa operación. CAS autónomo sigue `NOT VERIFIED` y requiere decisión propia |

Inspeccioné los adjuntos y copias históricas locales. Calculé CRC, tamaños, SHA-256 y SHA-1 de blobs en solo lectura y consulté documentación pública de producto. No accedí al destino, al plano administrativo de la instalación ni a repositorios privados. No utilicé credenciales o herramientas de escritura de GitHub. No creé ni modifiqué repositorios, refs, commits, PR, comentarios, permisos o reglas. No hubo push, pruebas de seguridad ni ejecución de G2-B/G3/G4/G5. La única entrega nueva es este informe al Owner para transferencia a PCM-001.

**Disposición final — DESIGN PASS (CONDITIONAL). F-R3-01 y F-R3-02 CLOSED DESIGN. D-R3-APP / G2-B / G3 / G4 / G5 DEFERRED.**
