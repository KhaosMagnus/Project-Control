# PCM-VERSIONING-001 — Propuesta de versionado del producto portable

**SOURCE IDEA / POLICY DIRECTION:** Owner, mensaje del 2026-11-22. **DRAFTER:** PCM-001/GPT. **TARGET / DECISION AUTHORITY:** Owner / Project Control Master.
**STATUS:** PROPOSED / NOT ADOPTED / NO VERSION BUMP AUTHORIZED.
**SCOPE:** semántica de versiones para el producto genérico en `main`, NO para los commits de gobierno `meta/project-control`.

## Criterio propuesto: MAJOR.MINOR.PATCH

- **MAJOR** (`X.0.0`): ruptura de compatibilidad de contratos, formato de estado o invariantes de gobierno, o migración obligatoria para adoptantes.
- **MINOR** (`X.Y.0`): nuevo componente, herramienta o capacidad compatible con las versiones actuales; nuevas opciones documentales no obligatorias.
- **PATCH** (`X.Y.Z`): corrección compatible de defecto de especificación, herramienta o documentación; no altera contratos de adopción de modo incompatible.
- Una mejora llamada “protocolo de documentación” puede ser MINOR si es añadida sin romper contratos anteriores, **o MAJOR** si impone nuevas obligaciones incompatibles. El nombre o tamaño del cambio no determinan la versión por sí solos.
- Un cambio solo administrativo en `meta/project-control` incrementa el **commit de control**, no obliga a publicar otra versión del estándar.
- Cada release necesita diff, decisión de compatibilidad, version pin, integridad SHA, QA proporcional a sus criterios y autorización de publicación. Los adoptantes NO se actualizan automáticamente.
- **Precedencia:** el protocolo histórico `GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0.md` es FROZEN, su nombre v1.0 no se renombra de forma silenciosa a v1.0.0 ni se reetiquetan sus bytes. Esta propuesta añade semántica para sucesores **si el Owner la acepta explícitamente**.
- Un cambio de política de versionado necesita su propia decisión Owner; ningún ejemplo aquí emite una release.

**Criterio del fuente original:** §17 de v1.0 obliga a sucesores versionados y preservación de congelados, pero NO establece formalmente esta asignación MAJOR/MINOR/PATCH. Esta tabla es una propuesta inspirada por la directiva actual del Owner, no una cita del contrato original.
