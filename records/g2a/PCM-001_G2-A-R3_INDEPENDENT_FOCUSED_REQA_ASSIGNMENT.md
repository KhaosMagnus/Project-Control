# PCM-001 — Encargo focalizado R3 para dos evaluadores independientes

**Assignment:** `PCM-G2A-R3-IQA-FOCUSED-001`  
**Modo:** `INDEPENDENT DOCUMENTARY QA / STRICT READ-ONLY`  
**Estado inicial:** `R3 DESIGN OWNER-ACCEPTED / G2-B,G3,G4,G5 DEFERRED`.

Adjunto un ZIP controlado con los dos dictámenes independientes originales, el contrato correctivo R3 **sin alterar**, los dos archivos README exactos, el addendum de aceptación documental del Owner, una matriz de instalación con 11 IDs observados y un manifiesto de integridad.

### Alcance verificable

1. Comprobar SHA-256 del ZIP y de cada miembro contra el manifiesto; verificar los dos README y sus SHA de blob Git si es posible, sin publicarlos.
2. Cotejar los hallazgos bloqueantes del primer QA (`H1-H4`; `H5-H6` según fase) con correcciones R3. Registrar `CLOSED DESIGN / PARTIAL / OPEN`, justificando por evidencia, sin reclamar pruebas de ejecución inexistentes.
3. Verificar la coherencia técnica de dos raíces Git (`T-A`), procedimiento manual propuesto, orden de publicación, protección, manejo de génesis parcial, condición STOP y ausencia de importación en G2-B.
4. Revisar que el addendum documenta **aceptación de diseño únicamente**. Comprobar exposición pública de ambas ramas y que la selección `all -> selected` continúa sin autorizar.
5. Examinar el inventario por instalación (11 IDs, página 2 vacía) y la propuesta conservadora de conservar todos inicialmente, sin equiparar acceso con dependencia ni permisos del usuario con scopes de la instalación. Evaluar validación administrativa y recuperación.
6. Determinar si la corrección está lista como **diseño de G2-B condicionado**, o si requiere otra revisión antes de pedir las autorizaciones de permisos y ejecución.
7. Atestar acciones utilizadas: lecturas de documentos y, si se decide, consultas GET públicas exclusivamente. No usar escrituras ni acceder a repositorios privados por el mero hecho de estar listados.

### Salida requerida

- Informe individual autónomo con tabla `ID / hallazgo / evidencia / severidad / estado / fase afectada`.
- Separar faltas del diseño de pruebas que solo pueden obtenerse **después de autorización** y no convertir automáticamente esa ausencia en defecto insalvable.
- Veredicto `DESIGN PASS (CONDITIONAL) / DESIGN REVISE / DESIGN FAIL / INCONCLUSIVE`, con condiciones exactas.
- Distinguir integridad del paquete, integridad de fuentes históricas, acceso a instalaciones y autoridad para ejecutar.
- El resultado de un QA no constituye GRANTED para G2-B ni G3/G4/G5.

### Prohibiciones

NO: modificar GitHub, crear commits/ramas/repositorios/PR/issues/comentarios, alterar permisos, ejecutar security tests, usar tokens de escritura, extraer credenciales o publicar anexos en repositorios. NO iniciar G2-B/G3/G4/G5.

Entregar al Owner, fuera de GitHub. Este expediente contiene nombres e IDs de repositorios privados y **no es apto para publicación pública como está**. No asumir acceso cruzado entre chats.
