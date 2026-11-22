# PROJECT CONTROL MASTER — RE-QA FOCALIZADA R5

**ASSIGNMENT:** `PCM-G2A-R5-IQA-FOCUSED-001`  
**SOURCE:** Owner / Project Control Master  
**MODE:** INDEPENDENT DOCUMENTARY QA / STRICT READ-ONLY

El expediente contiene el contrato R3, su aceptación documental Owner, la corrección R4, los **dos informes distintos de QA R4**, la conciliación PCM-001 y el nuevo delta **R5**.

## Único objeto de revisión

1. `F-R3-01`: comprobar que las transiciones P4/P5/P6/P7 dependen de la fase, de la acción intentada y de protecciones verificadas; que un estado esperado no produce STOP contradictorio; y que la reconciliación de timeout, estado parcial y recuperación no autoriza acciones ciegas.
2. `F-R3-02`: comprobar que la aprobación previa se vincula a base `B`, candidata `H`, método, delta/árbol esperado y revisiones; que el SHA `C` generado se verifica **después** y que las diferencias materiales fuerzan STOP y nueva autorización.
3. Confirmar **sin reabrir** que `F-R3-03` sigue `CLOSED DESIGN`, que R3 Owner GRANTED era solo diseño, y que R5 no cambia los dos README históricos, la topología T-A ni las reglas de autoridad.

Entregar informe autónomo: integridad del paquete, atestación de alcance, estado `CLOSED DESIGN / PARTIAL / OPEN` para los dos hallazgos y veredicto `DESIGN PASS (CONDITIONAL) / DESIGN REVISE / DESIGN FAIL / INCONCLUSIVE`. Diferenciar siempre defectos del diseño de pruebas que solo se autorizan en D-R3-APP/G2-B.

**Prohibido:** modificar repositorios o configuraciones GitHub, crear refs, commits, PR, comentarios, cambiar instalación/permisos, ejecutar Git push, probar seguridad, ejecutar G2-B/G3/G4/G5 o publicar el reporte en GitHub. Esta transferencia no concede ejecución. Entregar el reporte exclusivamente al Owner.
