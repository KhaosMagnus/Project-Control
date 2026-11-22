# PCM-P1-PREP-001 — Preflight de extracción del bootstrap portable hacia main

**SOURCE:** PROJECT_CONTROL_MASTER / PCM-001 provisional. **TARGET:** Owner / futura autoridad de producto y QA. **MODE:** READ / DESIGN / RECORD ONLY.
**INPUT GOVERNANCE REVISION:** `dc4034b242faeb37cbd19f04a26a52cfa65e77e8` (resolver HEAD vigente en GitHub antes de nuevas acciones).
**SOURCE REPOSITORY:** `KhaosMagnus/YU3DOH-Carder`, commit congelado `056adb5097b7ce067082782e8d8c92b42db9082a`.
**DESTINATION:** `KhaosMagnus/Project-Control`, rama `main` — **NO EDITADA POR ESTE PREFLIGHT**.
**STATUS:** EXTRACTION PLAN PREPARED / SOURCE INTEGRITY REFERENCED / G3-G4-G5 DEFERRED / NO RELEASE AUTHORIZED.

## Propósito y división correcta

`main` debe alojar el producto reusable: protocolo congelado, bootstrap con sus seis plantillas, adaptador, guía, manifiesto, paquete reproducible, documentación, tests y futuras versiones. `meta/project-control` registra decisiones, QA, permisos, evidencias, cambios de alcance, autoría, solicitudes y transferencias. No fusionar ramas ni importar gobierno local a producto.

La importación histórica no adopta Project Control en YU3DOH ni otro proyecto. Cada adoptante fija su propia versión y su acto Owner. `PCM-VERSIONING-001` persigue una futura regla normativa de versionado; **todavía no aprobada ni efectiva**. No reinterpretar v1.0 como 1.0.0 ni cambiarlo silenciosamente.

## Inventario de fuente GitHub observado y pin exacto

| Elemento de origen | Git blob SHA-1 en commit 056adb5097b7ce067082782e8d8c92b42db9082a | Destino / clasificación propuestos |
|---|---|---|
| `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/START_HERE.md` | `96c3f6d5403ff7857f94c32b8fa4ceb5499edd31` | Guía portable, no autoriza adopción o ejecución |
| `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/PACKAGE_METADATA.md` | `95233ecfb1afd9004eabc07ecd8e7e9b84b05b4b` | Identidad, trazabilidad y reglas de reproducibilidad |
| `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/MANIFEST.sha256` | `0d84759f07155f17f60993ff9950655b4e54fec5` | Diez entradas, excluye el propio manifiesto |
| `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/protocol/GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0.md` | `1ac3689c1e811d1594291afee6b2c1c6efd093d0` | Protocolo FROZEN embebido |
| `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/adapters/GITHUB_DEFAULT.md` | `e2e563106a29ff3ae63a71009ad20035de906b09` | Adaptador GitHub portable; actualización condicional esperada |
| `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/templates/PROJECT_STATE.md` | `3ff9aba4a285e2d1a834db4d4fd3e874f032cd20` | Plantilla estado |
| `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/templates/REQUEST_LEDGER.md` | `9e3ee77a7b75f14e1d4b6ca431a427bb4f654ad6` | Plantilla solicitudes |
| `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/templates/ROLE_REGISTRY.md` | `81002c375212530db94be5eb4faf61f2da9c793b` | Plantilla roles |
| `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/templates/INSTANCE_REGISTRY.md` | `8a7a5d5231d9ac53aaeb2f40993e2f0040a18027` | Plantilla instancias |
| `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/templates/TRANSFER_ENVELOPE.md` | `b46aa8896d50db18d6c96177b8285fcf048f71a0` | Plantilla transferencia |
| `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/templates/BOOTSTRAP_RETURN.md` | `f1f5e136eff612e72915419058601d934e8abc69` | Plantilla retorno |
| `bootstrap/dist/PROJECT_CONTROL_BOOTSTRAP-v1.0.zip` | `13eae102d5aed553d4fb3a023ab77b71601306b2` | Paquete histórico reproducible de 62955 bytes, ZIP SHA-256 c3c5cb0c896d7e11696948e7677d74ea077a87d27350064b1ad6d521ceb74f6e |
| `bootstrap/dist/PROJECT_CONTROL_BOOTSTRAP-v1.0.zip.sha256` | `43d6943b5ac7a6df421f08e78bd993ce400164f1` | Sidecar con digest externo del ZIP |
| `bootstrap/build_package.py` | `83a580f9d2339e566ea2a2ceddfa98b39f9ef07f` | Builder histórico que hace git show a commit del repo YU3DOH; no funciona sin adaptar o incorporar ese objeto |
| `bootstrap/ZIP-001_PACKAGE_REPORT.md` | `11510212f6fa5f5441b9c94ad86ac41d19837cf1` | Reporte de empaquetado, no QA independiente; referencia de procedencia para meta, no necesariamente producto |

Protocolo canónico de fuente fuera del ZIP: `protocols/GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0.md`, mismo blob `1ac3689c1e811d1594291afee6b2c1c6efd093d0`, SHA-256 `586cb4d8740e33ac8a3a6db65a5ce1506fe855ca1968adacd3034352106c70e3`. Asegurar identidad de bytes con copia embebida si el maestro conserva ambas superficies. El historial del ZIP consta de **10 archivos de payload + MANIFEST**, 11 entradas en total. Los templates distribuidos no son los registros locales ya preenchidos en meta.

El `ZIP-001_PACKAGE_REPORT.md` (blob `11510212f6fa5f5441b9c94ad86ac41d19837cf1`) informa reproducibilidad, manifiestos, CRC y comparación de bytes, pero su texto reconoce expresamente **NO INDEPENDENT QA** y **NO ADOPTION**. La fuente metadata declara la revisión histórica de empaquetado `bd1840bf0b1dc8e294af1226ec6cfb0546f7bc89`; conservarla como procedencia, no tratarla como HEAD del nuevo proyecto.

## Bloqueo de portabilidad detectado

`bootstrap/build_package.py` histórico utiliza literalmente:
`PIN = 'bd1840bf0b1dc8e294af1226ec6cfb0546f7bc89'`
y ejecuta `git show PIN + ':protocols/GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0.md'` dentro del repositorio que contiene el builder. Copiado sin modificaciones al nuevo `Project-Control`, podría fallar porque ese objeto pertenece al historial de YU3DOH y **no está garantizado en el nuevo repo**. El ZIP histórico no necesita ese builder para ser consumido.

**Opciones propuestas para autorización posterior:**
- **A — Primera importación como snapshot inmutable:** publicar fuentes y distribución v1.0 sin alterar bytes; mantener el builder histórico como referencia no operativa y añadir una instrucción explícita sobre su dependencia anterior. QA verificaría manifiestos, integridad del ZIP, clasificación y reproducibilidad independiente antes de declarar aceptación/release.
- **B — Builder portable sucesor:** adaptar el builder para cotejar fuente canónica local + blob/digest histórico y pruebas de regresión, bajo nueva versión/control de compatibilidad aprobados. No reconstruir ZIP v1.0 con bytes distintos conservando su nombre/digest. No usar B como excusa para bloquear el archivo histórico.

**Recomendación PCM-001:** A como paso de preservación inicial tras un GRANT exacto; B como candidato posterior independiente. Esta es recomendación, no disposición Owner.

## Gates pendientes antes de cualquier escritura en main

1. **Owner:** decisión de importación/release con archivos exactos, rama, visibilidad, permisos, actor, estrategia de PR, expected-head y STOP. La autorización de clasificación en meta no abarca escrituras en main. G3/G4/G5 continúan diferidos.
2. **Licencia/publicabilidad:** comprobar procedencia, propiedad y licencias del material reutilizable. La portabilidad del código/producto no se demuestra por el solo hecho de que la fuente histórica sea accesible.
3. **Candidato congelado:** manifest exacto de las rutas a publicar; conservar bytes y digests históricos; distinguir reporte ZIP-001 (meta/procedencia) del estándar.
4. **QA proporcional e independiente de su autor cuando el contrato lo exija:** comprobar componentes, hash externo, ausencia de fuentes privadas, extracciones y conducta de bootstrap en un destino de prueba; packaging integrity no equivale a prueba de adopción real.
5. **Ruta Git:** `R-MAIN` exige PR aprobada. Verificar elegibilidad real del revisor y mecanismo de integración antes de declarar GO; no inferir que el permiso de escritura al repo demuestra capacidad de merge autorizada.
6. **Handoff:** `SOURCE=PCM-001`; `TARGET=Owner/autor/QA/integrador por asignación`; devolver commit exacto, árbol, blobs, QA, aceptación y próxima ruta; no reactivar PP-002 ni proyectos adoptantes.

**STOP:** ninguna escritura en `main`, ninguna QA activada, creación de ramas o release bajo este documento. La siguiente decisión puede ser `GRANTED / DEFERRED / REVISE` para un gate de importación exactamente delimitado.

## Dependencia documental local

P0 clasificó los 107 objetos de la instantánea local, archivó 76 originales Markdown en `meta` y conservó estados no aceptados; los paquetes exactos de algunos gates históricos no están respaldados independientemente fuera de la sesión/archivo local. Esa deuda es una cuestión de custodia histórica y **no debe mezclarse con el payload portable genérico**. No usar la ausencia de ZIP de QA privada como permiso para publicar información reservada.
