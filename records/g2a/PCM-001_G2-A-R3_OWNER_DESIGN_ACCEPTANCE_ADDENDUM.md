# PCM-001 — Addendum de disposición del Owner y tratamiento de hallazgos R3

**Control:** `PCM-G2A-R3-DESIGN-OWNER-GRANT`  
**Fecha:** 2026-11-15  
**Estado:** `GRANTED DESIGN ONLY / NO GITHUB MUTATIONS`  
**Documento base inalterado:** `PCM-001_G2-A-R3_G2-B_CORRECTIVE_GENESIS_AND_ACCESS_CONTRACT_DRAFT.md`, SHA-256 `c8789106252618549052e25a4dc43eb0b36f3d8bc15ab7d8bdbda0e1fa7ffaeb`.  
**QA anterior:** GPT y Grok `DESIGN REVISE`. Los informes originales y su veredicto no se sobrescriben.

## Disposición efectiva recibida del Owner

> OWNER DISPOSITION — PCM-G2A-R3-DESIGN  
> DECISION: GRANTED  
> Acepto documentalmente GitHub Free público para main y meta/project-control, incluyendo su historial; topología T-A de raíces Git independientes y génesis mínima mediante operador humano autorizado, conforme al contrato R3. Autorizo preparar la re-QA focalizada y completar el inventario documental de permisos. No autorizo modificaciones GitHub, cambios de instalación ni ejecución G2-B/G3/G4/G5.

## Efecto normativo acotado

1. `D-R3-PUB`: **ACCEPTED DESIGN** para publicidad de `main`, `meta/project-control` e historial. El catálogo concreto de archivos de G2-B se limita a los dos README del diseño original; otras superficies o archivos futuros no quedan aprobados por implicación.
2. `D-R3-TOPO`: **ACCEPTED DESIGN** de dos commits raíz independientes (`T-A`), sin ancestro común y sin merge entre ramas. No autorizada una variante T-B ni ejecución CLI.
3. `D-R3-GENESIS`: **ACCEPTED DESIGN** de génesis mínima por operador humano futuro, con dos README neutrales. Sus hashes son `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340` (`main`) y `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0` (`meta/project-control`). No autorizados commit messages, identidad de autor, fechas o pushes por esta disposición.
4. `D-R3-APP`: **PLANNING ONLY** para matriz de instalación `162412374`. No autorizada transición `all -> selected`; el conjunto de once IDs es propuesta y requiere aceptación exacta independiente del Owner.
5. `D-R3-RE-QA`: **AUTHORIZED TO PREPARE** un encargo documental focalizado. No se ha delegado ni ejecutado automáticamente con los evaluadores.
6. `G2-B / G3 / G4 / G5`: **DEFERRED**. PCM-001 continúa **PROVISIONAL**.

## Reconciliación de la frase DRAFT / NOT APPROVED del contrato base

El contrato base se conserva byte a byte, por trazabilidad. Su leyenda `DRAFT / NOT APPROVED` describe el estado **al emitirlo**, antes de esta decisión. El presente addendum aprueba la orientación de diseño y deja claro el alcance exacto: **no** convierte el borrador en autorización de creación ni sustituye QA independiente R3. Las decisiones `D-R3-APP` ejecutiva y `D-R3-G2B` siguen ausentes.

## Dependencias y controles antes de permitir G2-B

- Validar integridad del contrato R3, las dos raíces propuestas y hashes del material de génesis.
- Resolver re-QA focalizada sobre topología, secuencia parcial, administración de reglas, publicación y control `all -> selected`.
- Obtener snapshot administrativo directo de instalación y aprobación de conjunto seleccionado exacto, con un plan de transición separado.
- Verificar si el gobierno G2-B exige anexos confidenciales: para génesis README, se propone `NONE`, sin prejuzgar etapas futuras.
- Congelar actor humano, identidad Git, mensajes de commit y procedimiento de protección/recovery. Corroborar control de acceso a GitHub antes de ejecución.
- Preparar después una solicitud G2-B ejecutiva delimitada, nunca autoactivada por PASS de QA.

**Disposición final:** `R3 DESIGN OWNER-ACCEPTED / DOCUMENTARY RE-QA PACKET PREPARED / INSTALLATION CHANGE NOT AUTHORIZED / G2-B DEFERRED`.
