# PCM-P0 — Nueve contenidos auxiliares singulares de los ZIP
**SOURCE:** PCM-001, inspección de 12 ZIP y miembros SHA-256 en archivos de trabajo de 2026-11-22.
**STATUS:** MEMBER-LEVEL ANALYSIS COMPLETE / CONTAINER RETENTION SUBJECT TO HISTORICAL QA DEPENDENCIES.

Se observaron 127 entradas de ZIP, 76 identidades de contenido por SHA-256. De 12 miembros sin copia suelta en el censo local, dos son README de génesis ya existentes en GitHub, uno es una copia anidada de ZIP ejecutivo y los nueve restantes se documentan a continuación. Un miembro único no significa necesariamente que sea indispensable.

| Auxiliar único | SHA-256 exacto | Valor | Disposición recomendada |
|---|---|---|---|
| `G2-B executive MANIFEST.md` | `462b2fc18408225e3c2a14e7984d68b778600004c9cfd1a977cf5da8026f5557` | Conservación de nombres, bytes y digests de integrantes del contrato ejecutivo; fuente original dice CONTROLLED / NOT FOR PUBLIC GITHUB UPLOAD. | Resumen de integridad y SHA en catálogo; mantener el ZIP ejecutivo exacto mientras siga G2-B abierto. |
| `G2-B P8 MANIFEST.md` | `863f17a70582ae8247493f926bcd0530252f97da1ccd5828e7779cb8ac9d8fec` | Relación congelada de componentes proporcionados a auditores. | Manifest de verificación derivado; paquete P8 exacto RETAIN mientras dictámenes estén inconclusos. |
| `P7_OBSERVED_STATE_SUMMARY.json` | `84e911d346fb260e6d5029969c1eb962a878634c58c149dac4d156eebb600ef2` | Síntesis redactada por PCM-001, con ramas, reglas y estado administrativo históricos y limitaciones explícitas. | No publicar original por datos de instalación/identidad; conservar limitaciones y consultar respuestas GitHub independientes para nuevos hechos. |
| `CORR-001 R2 QA_MANIFEST.json` | `9e169d72c14f42211eb04316833d701928152130516afae133251ad906d93216` | Relación con hashes de miembros del paquete R2 de QA, cuya conciliación fue REVISE. | Retener paquete exacto temporalmente por gate abierto; manifest derivable. |
| `CORR-001 R3 REQA_MANIFEST.json` | `a45ff559ee1b910e19eeecbb6cf78a85b96b30cf1cf985163db0fd4bdbfc6c4b` | Composición del candidato de re-QA R3 PROPOSED, sin autorización emitida. | No confundir manifest/propuesta con QA ejecutada; preservar digest y lista de miembros mientras se prepara gate. |
| `PROV-IQA-001 MANIFEST.json` | `c3a68ee7a097c4fb133d7979c2b859a71f64eacea8ac1d1ae5ce06bb601bb750` | Integridad y alcance de propuesta de QA sobre R2. | Mantener referencia al contrato y dictámenes individuales; no conservar ZIP por defecto tras verificación. |
| `PROV-IQA-002 R3 REQA_MANIFEST.json` | `564425e9c43e5ca995d7f92578550c6751b29a384a4c3d389000ed2ec74e1e3a` | Composición de paquete de re-QA de procedencia R3 en el momento de propuesta. | No elevar una propuesta antigua al rango de autorización; preservar enlace a decisión posterior y QA realizada. |
| `CORR-001 R2_TO_R3.diff` | `e2defc9d8828fc2400ff5712661a40645bc6e10d4deba7ba1ce8287567d84026` | Diferencia exacta entre los dos originales R2 y R3 ya archivados. | Regeneración con Python difflib.unified_diff produce byte por byte el SHA original; almacenamiento redundante. |
| `PROV-DES-002_TO_003.diff` | `4c19625522935c1ea5fa670858f229e86e0e5b31252a8536a7314e72d7fc2383` | Diferencia exacta entre contrato de procedencia R2 y R3 ya archivados. | Regeneración difflib.unified_diff produce byte por byte el SHA original; almacenamiento redundante. |

**Reproducibilidad probada de los dos diffs:** `difflib.unified_diff(old.splitlines(keepends=True), new.splitlines(keepends=True), fromfile=old_filename, tofile=new_filename)`, unidos sin alterar terminadores, reproduce exactamente ambos SHA-256. Este resultado NO significa que sus documentos fueran aprobados, solo que el delta es reconstruible.

**ZIP exactos que conviene conservar temporalmente mientras haya gates abiertos:**
- `PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_PACKET_2026-11-16.zip` — SHA-256 `3cbcbc2825a2c644ba70c05b338b9714c967eae7f6fb52a554326ce03e7dd069`.
- `PCM-001_G2-B_P8_INDEPENDENT_INFRA_QA_SHARED_PACKET_2026-11-20.zip` — SHA-256 `2c4b4a0b7835386e7ec5e25cfd635bc0ae43a8ca3d49d511ba0e85af3496c499`.
- `PCM-001_G2-B_P8_UNIPERSONAL_FOCUSED_QA_SHARED_PACKET_2026-11-20.zip` — SHA-256 `373465c55c703bfda95f5985ba70b7059e87e31ae1ad90ecffced5a437bc4ab8`.
- `PCM-GOV-PROV-CORR-001_R2_FOCUSED_QA_PACKET_2026-11-21.zip` — SHA-256 `0c255ae823e15a769994973e69dd02dcb0cd12f5e46b72bc05bb41da77bbcbf0`.

**Ocho ZIP restantes:** candidatos a no retención permanente SOLO después de comprobación de dependencias y decisión de eliminación. Las cuatro imágenes no son objeto de migración permanente por defecto; tres son referencias temporales de configuración histórica y una es redundante frente a Git. No se han eliminado archivos, ni se dispone de custodia privada creada.

**RETURN:** PCM-001 → Owner con las dependencias; no reabrir CORR/G2-B QA solo por descubrir estos auxiliares.
