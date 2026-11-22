# PCM-P0-CUSTODY-001 — Catálogo residual del inventario local

**SOURCE:** PROJECT_CONTROL_MASTER / PCM-001 provisional. **TARGET:** Owner / sucesor PCM. **Corte:** 2026-11-22. **SOURCE HEAD:** `8426521ab0fa80c2f3eabc684fb3adec584aac21`.
**STATUS:** COMPLETE METADATA RECONCILIATION FOR LOCAL 107-FILE SET / RAW EVIDENCE CUSTODY OPEN.

## Cobertura y límites

- El censo local de **107 archivos** fue realizado sobre las rutas que podían observarse en este entorno; no significa que todos los expedientes de la historia total de PCM estén representados.
- **66 originales Markdown** ya publicados y verificados en `records/` de la rama `meta/project-control`. **41 fuentes residuales** identificadas por SHA-256 pero **NO incorporadas**.
- De esos 41: **18** requieren revisión sensible, **7** revisión administrativa, **12** son ZIP de transporte y **4** imágenes. La clasificación es un triaje técnico y **no** una decisión Owner de publicabilidad/confidencialidad.
- No se publica el contenido de ninguno de estos archivos con este catálogo. Los nombres/hashes son identificadores, NO prueba de autenticidad del emisor, aprobación o recuperación universal del material bruto.
- Los 12 ZIP se verificaron localmente con **CRC PASS** y sin rutas de extracción peligrosas observadas; pueden repetir archivos ya preservados, por lo que no se considera necesario almacenarlos duplicados en la rama pública. Esa decisión de economía de copias NO elimina la necesidad de custodia privada o reconstrucción comprobada de expedientes que contengan miembros únicos.
- Dos archivos `PCM-G2A-R3-IQA-FOCUSED-001_INFORME_REQA*.md` comparten exactamente el mismo SHA-256; se consideran dos nombres de una misma identidad de contenido, sin borrar ninguna ruta local.

## Inventario exacto de residuales

| Archivo | SHA-256 | Bytes | Tipo de revisión |
|---|---|---:|---|
| `PC-MASTER-DES-001_G2-A-R2_PUBLICATION_AND_PRIVACY_DECISION.md` | `59ad7db1b8275545eedede836265fea337c186835a615e57aa1c4e133ed3429b` | 33537 | CONF |
| `PCM-001_D-R3-APP_ADMIN_SNAPSHOT_RECONCILIATION_AND_OWNER_REQUEST_2026-11-16.md` | `a50836f161031d21926dce6f5fbdf0c4ba3c157e2b13451687f9aa5e8d997071` | 10206 | CONF |
| `PCM-001_D-R3-APP_OWNER_GRANT_AND_MANUAL_EXECUTION_CHECKLIST_2026-11-16.md` | `73610a0f2f3a11008fc8258bcf5bfecba7188724af07074bee1ad51ded967904` | 4398 | CONF |
| `PCM-001_D-R3-APP_POST_SAVE_READBACK_PASS_2026-11-16.md` | `4604228b41da94967e3bacdceaaaa789f612ebfda1739048e4bce275001e8b98` | 4823 | CONF |
| `PCM-001_D-R3-APP_READ_ONLY_ADMINISTRATIVE_INTAKE_2026-11-16.md` | `19e422114a1487fdd671e61f15581293c1dbbd7ecab9134140504d5cee2d394f` | 11816 | CONF |
| `PCM-001_G2-A-R3_CORRECTIVE_DESIGN_REVIEW_PACKET.zip` | `57f87ed69e1341fdf49430e9b4f8a91b1c3630c65412d68e67a755f052687e6d` | 27317 | ZIP |
| `PCM-001_G2-A-R3_FOCUSED_REQA_SHARED_PACKET_2026-11-15.zip` | `fb39e74c794ff0e9a2ea6c457569706dcf6d6d20be33ff139d1fed00984119c6` | 34745 | ZIP |
| `PCM-001_G2-A-R3_G2-B_CORRECTIVE_GENESIS_AND_ACCESS_CONTRACT_DRAFT.md` | `c8789106252618549052e25a4dc43eb0b36f3d8bc15ab7d8bdbda0e1fa7ffaeb` | 13124 | CONF |
| `PCM-001_G2-A-R3_INSTALLATION_162412374_ACCESS_MATRIX_READ_ONLY.md` | `e9f262bfc4103e87e7865ec3856b6d94b4b5897b60ad6dd999110b73e15748ac` | 6382 | CONF |
| `PCM-001_G2-A-R4_ADDITIVE_GENESIS_PROTECTION_AND_ACCESS_CORRECTION.md` | `bcacf7ed0d36454459c7a6f7846658f40b948b56149271a66dbe762ee3b12725` | 16435 | CONF |
| `PCM-001_G2-A-R4_FOCUSED_QA_MANIFEST.md` | `6f18759ae904b78671d4fb55fcdeee2792da9d1e5aec8c3b2a797c25bfb985f8` | 2568 | ADMIN |
| `PCM-001_G2-A-R4_FOCUSED_QA_SHARED_PACKET_2026-11-15.zip` | `0b4c08dc108783b3668c8cd9e0c09eae99b0b4f156803d6ea451dbd805520338` | 49515 | ZIP |
| `PCM-001_G2-A-R4_INDEPENDENT_FOCUSED_QA_ASSIGNMENT.md` | `e824733b27ed485be1b486f6f66797d543e3b115cb0dbb6072960b95c870b20a` | 3100 | ADMIN |
| `PCM-001_G2-A-R5_ADDITIVE_PHASE_AND_INTEGRATION_CORRECTION.md` | `9c329b3c4be0dca6cf60bc27e92bd586a931c9236bd786f402ce508f952562e8` | 14153 | CONF |
| `PCM-001_G2-A-R5_DUAL_QA_CONSOLIDATION_AND_D-R3-APP_INTAKE_2026-11-16.md` | `0c71c572e2189beabe1a05470edc2af78334be3d0fccf83d9411376c5b97049f` | 9704 | CONF |
| `PCM-001_G2-A-R5_FOCUSED_REQA_MANIFEST.md` | `516f69016333007364b68392492be0d60b883bdcb40e19a8e7dcf34b6fad1585` | 2240 | ADMIN |
| `PCM-001_G2-A-R5_FOCUSED_REQA_SHARED_PACKET_2026-11-15.zip` | `36f74d50563bcadbe3f37195d2531535dad9ff6b01eefdd58fdd2ee5ee3dc9e2` | 37304 | ZIP |
| `PCM-001_G2-A-R5_INDEPENDENT_FOCUSED_QA_ASSIGNMENT.md` | `e512496bc6fcd05821e987a45faa61101020c0048cc7a389354034c72609e8f6` | 1779 | ADMIN |
| `PCM-001_G2-A_D2-D4_CONTROL_PREPARATION.md` | `c946c518c081212564aaeb14dbe7295c6df66958881117b7ff5181988ad96e0b` | 10830 | CONF |
| `PCM-001_G2-A_INDEPENDENT_QA_SHARED_PACKET_2026-11-15.zip` | `d860ca78bc675eceac003ff1e7db5cf041483465960ccfe70f27ba7d52789033` | 40248 | ZIP |
| `PCM-001_G2-A_IQA_CONSOLIDATED_DISPOSITION_2026-11-15.md` | `27c229fcc93bf692ddf807d92f877f798bfa08b9394d739807fdde8e2318ff5a` | 6875 | CONF |
| `PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_PACKET_2026-11-16.zip` | `3cbcbc2825a2c644ba70c05b338b9714c967eae7f6fb52a554326ce03e7dd069` | 12175 | ZIP |
| `PCM-001_G2-B_P8_INDEPENDENT_INFRA_QA_SHARED_PACKET_2026-11-20.zip` | `2c4b4a0b7835386e7ec5e25cfd635bc0ae43a8ca3d49d511ba0e85af3496c499` | 43393 | ZIP |
| `PCM-001_G2-B_P8_UNIPERSONAL_FOCUSED_QA_SHARED_PACKET_2026-11-20.zip` | `373465c55c703bfda95f5985ba70b7059e87e31ae1ad90ecffced5a437bc4ab8` | 43260 | ZIP |
| `PCM-G2A-IQA-DES-001_GROK_INDEPENDENT_QA_REPORT.md` | `6208c452ae1e3a5644beae7be6949f1652bca2c5b9687e09ee062df7f486a407` | 10501 | CONF |
| `PCM-G2A-IQA-DES-001_INFORME_QA_INDEPENDIENTE.md` | `69704fefbe32beac533c0be41d8aec506190ab4c820968b983551b1c959a550e` | 26848 | ADMIN |
| `PCM-G2A-R3-IQA-FOCUSED-001_GROK_INDEPENDENT_REQA_REPORT.md` | `a013722d9c2fac9a9b65cf0690fedb5cee4ad18d8f81c2f72adce4c89d8b5a2e` | 8108 | CONF |
| `PCM-G2A-R3-IQA-FOCUSED-001_INFORME_REQA(1).md` | `42e12c2f9c7cf002a7a3cba18b71aabb7518c412de0d5f73bf8246b1368c53c4` | 18361 | ADMIN |
| `PCM-G2A-R3-IQA-FOCUSED-001_INFORME_REQA.md` | `42e12c2f9c7cf002a7a3cba18b71aabb7518c412de0d5f73bf8246b1368c53c4` | 18361 | ADMIN |
| `PCM-G2A-R4-IQA-FOCUSED-001_GROK_INDEPENDENT_REQA_REPORT.md` | `c6346c05ae9b81baa1e6a26dddd687fada19b0f0c7ef0932a72db32daf7f6111` | 6085 | CONF |
| `PCM-G2A-R5-IQA-FOCUSED-001_GROK_INDEPENDENT_REQA_REPORT.md` | `1b0e7fe769b385f6d9658bedda2a53c2a72ec993100a3b6b925bd4861300cccc` | 5464 | CONF |
| `PCM-GOV-PROV-CORR-001_R2_FOCUSED_QA_PACKET_2026-11-21.zip` | `0c255ae823e15a769994973e69dd02dcb0cd12f5e46b72bc05bb41da77bbcbf0` | 65420 | ZIP |
| `PCM-GOV-PROV-CORR-001_R3_FOCUSED_REQA_PROPOSED_PACKET_2026-11-21.zip` | `23461c4ed7db33897c517b0eaece3087f523e68ebbc45087008d97bd06335ab9` | 66537 | ZIP |
| `PCM-GOV-PROV-IQA-001_FOCUSED_QA_ASSIGNMENT_2026-11-20.md` | `4d07915b9cc1e0a2e24ac095aa2f0c151f8dc291df9afb2b693beb6f9053ebb6` | 2175 | CONF |
| `PCM-GOV-PROV-IQA-001_SHARED_REVIEW_PACKET_2026-11-20.zip` | `b7f98ed527b84cae73c8904c4348572709d914a3aedab32e2838fc91e60233fe` | 54498 | ZIP |
| `PCM-GOV-PROV-IQA-002_R3_FOCUSED_REQA_PROPOSED_PACKET_2026-11-20.zip` | `9d6d181b051f3e1d26944ce3ae2bf7138448df802f8509f76dd70d8feca79f11` | 41191 | ZIP |
| `PCM-GOV-PROV-IQA-002_R3_OWNER_GRANT_AND_DISPATCH_2026-11-21.md` | `5a65a0e71481256e905a07622076cbf078cdbbba6421acb380db0274df368b72` | 4126 | CONF |
| `image(1).png` | `3130e6284171d43e312935a40e4c1665a0700d716f1f6af216105c953442e7f3` | 44068 | MEDIA |
| `image(2).png` | `2d63b372ce36e44817d5c9a65782f245537678a0ded1695775ca0956c8b94491` | 35051 | MEDIA |
| `image(3).png` | `10166573fffedb1a260a5bc0e2e828e6f5da3b4cfdb0b19813e615d1d1abcf49` | 84498 | MEDIA |
| `image.png` | `03677ab2a8513979bf79c79bbd21d3a9567a39bb6e9a4626cd5843533711a0c3` | 60865 | MEDIA |

## Reglas de custodia propuestas, no ejecutadas

- `CONF`: SENSITIVE_REVIEW — no publicar original en GitHub público sin clasificación posterior.
- `ADMIN`: ADMIN_REVIEW — revisar inventarios/permisos y determinar publicación o custodia privada.
- `ZIP`: ZIP_PACKET — CRC verificado; paquete de transporte, posible duplicación de contenido; no importado.
- `MEDIA`: IMAGE_REVIEW — no inspeccionado para divulgación pública; no importado.

1. No subir automáticamente datos administrativos a la rama pública. Una clasificación de `CONF` o `ADMIN` es **pendiente** y no concede ni deniega permiso definitivo de publicación.
2. Para un reemplazo público sanitizado, producir **un objeto nuevo** con identidad y contenido distintos, enlazado al original, sin alterar el SHA original ni presentarlo como prueba primaria íntegra.
3. Confirmar después el destino autorizado de originales no publicables: repositorio privado u otro almacén versionado y recuperable, con responsables y acceso auditables. Hasta entonces, `EVIDENCE CUSTODY NOT COMPLETE`.
4. La colección de 107 archivos es una instantánea local, no prueba de que no existan otras fuentes en la Biblioteca, en chats o en repositorios previos. Documentar ampliaciones como censos sucesivos.
5. No reabrir G2-B, CORR-001, G3/G4/G5 ni nuevas QA por el solo hecho de catalogar. `main` permanece fuera de este gate.

**RETURN ROUTE:** PCM-001 → Owner con estado del inventario, custodia pendiente y propuesta de almacenamiento privado, para decisión posterior si resulta necesaria.
