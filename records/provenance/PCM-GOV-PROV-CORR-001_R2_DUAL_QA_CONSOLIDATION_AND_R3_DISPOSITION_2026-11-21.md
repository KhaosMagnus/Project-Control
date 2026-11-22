# PCM-001 — Conciliación doble QA CORR-001 R2 y propuesta R3

**Estado:** COORDINATOR REVIEW / CORR-001 R2 NOT ACCEPTED / R3 CANDIDATE PREPARED / NO GITHUB WRITES.

## 1. Evidencia

- CORR-001 R2 (congelado): `d68d6563c94e2141a76e5126ca1d513974b82df9bee3fd3358afde8d21256572`.
- QA ChatGPT: `DOCUMENTARY REVISE`, SHA-256 `918859b5bfc6bf8601f61a48ea2708f9d8399f2d52467a594f0fd94474f25c6e`. C1/C3/C5/C7/C8 VERIFIED; C2/C4/C9 PARTIAL; C6 FAILED.
- QA Grok: `DOCUMENTARY PASS (CONDITIONAL)`, SHA-256 `073963740c2a6d1b0c27c4a5d4a640c39adcaf2859f6a07250d374ef2f2e3a38`. C1–C9 VERIFIED conforme a su criterio.
- R3 candidato exacto: `f4317eaae4047086d32e00247e5e6f36e01c7e2d6a5c0b87f086eab524291d09`; **no aceptado ni publicado**.

## 2. Conciliación

La coincidencia de integridad de paquete y conservación de STOP no resuelve los tres defectos detectados en la aplicación práctica del esquema R3. Se adopta `REVISE` como disposición de coordinación, sin convertir un dictamen de QA en otro.

| Hallazgo | Defecto R2 | Corrección de R3 | Estado |
|---|---|---|---|
| H1 / CORR-05 | Un claim PRIMARY incluía lectura textual y reporte del Owner | CORR-05 documental (primaria para texto) + CORR-05B reporte de push (secundario), sin inferir intentos completos | PREPARED / RE-QA NEEDED |
| H2 / CORR-08 y vínculos | Sin `adopts` y alcance genérico; ID EXEC sin destino | `links.adopts` ahora apunta al objeto R3 y su SHA, scopes específicos de CORR-04/07/08, recomendaciones enlazadas a archivo/sección/SHA | PREPARED / RE-QA NEEDED |
| H3 / CORR-04 | GPT indicado como redactor del mensaje Owner sin prueba portable | `provenance.drafter=UNKNOWN`; fuente secundaria y propuesta P5 diferenciadas | PREPARED / RE-QA NEEDED |

La rectificación sigue siendo interpretativa, sin cita histórica falsamente imputada al Owner. Se preservan los dictámenes de infraestructura P8 `INCONCLUSIVE`, la obligación STOP histórica y los límites del origen intelectual.

## 3. Evidencia y gobernanza

A la vista de esta conversación, PCM-001 puede identificar mensajes del Owner originales como observación **local**, pero un evaluador que solo recibe archivos debe conservar `SECONDARY_ATTRIBUTED` sobre esos actos. R3 distingue ambas situaciones. Una recomendación escrita por GPT y luego aceptada por el Owner no se clasifica `OWNER_ORIGINATED` por ello.

Esta conciliación es propuesta y preflight del autor, **no** QA independiente. La autorización previa cubría evaluaciones sobre R2; para R3 solo procede una nueva QA acotada de H1–H3 tras aprobación del Owner. No se modifica GitHub ni se acepta CORR-001, UNI o G2-B.
