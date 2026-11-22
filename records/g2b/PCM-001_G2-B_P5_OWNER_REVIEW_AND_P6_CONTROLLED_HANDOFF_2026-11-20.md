# PCM-001 — G2-B / P5 Owner Review & P6 Controlled Handoff

**Gate**: `PCM-G2B-INFRA-GENESIS-001` — Owner `GRANTED`, alcance de infraestructura de génesis únicamente.
**Estado**: `P5 RULESET CONFIGURATION PASS / OWNER REVIEW RECEIVED / P6 SINGLE PUSH STAGED`.
**Fecha de consulta**: 2026-11-20 (Ciudad de México).
**Modo del coordinador**: GitHub READ-ONLY; las escrituras se reservan al Owner operador.

## 1. Verificación observada de P5

- El Owner confirmó haber inspeccionado los cinco controles de P5 y aceptado su evidencia: `OWNER REVIEW — PCM-G2B-P5`.
- `KhaosMagnus/Project-Control`, ID `1465064417`, público.
- Rama `main`: `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb` (raíz, un README aprobado).
- `meta/project-control`: **ausente** antes de P6.
- `R-MAIN`, ID `27709862`, `active`, objetivo exacto `refs/heads/main`, sin bypass. Exige un PR, una aprobación y un historial lineal; solo admite `squash` y `rebase`; bloquea borrado y non-fast-forward.
- `PCM-GENESIS-SAFETY`, ID `27708103`, `active`, objetivos `refs/heads/main` y `refs/heads/meta/project-control`, sin bypass, prohíbe borrado y non-fast-forward.
- Instalación `162412374`: `selected`, 11 repositorios retenidos; **excluye** el ID `1465064417`.

## 2. Límite de la revisión humana y futura ruta de PR

El Owner es el revisor humano que examinó P5. En la **génesis** no existe ningún PR que requiera aprobación. Un eventual PR de actualización deberá tener autor GitHub diferente del usuario que emita la aprobación, pasar una revisión elegible en GitHub y obtener las autorizaciones de contenido/QA que correspondan. La cuenta `JormungandrMagnus`, controlada por la misma persona que `KhaosMagnus`, **no** acredita independencia de personas por sí sola. No se considera aprobada ninguna actualización futura ni una excepción general al estándar por esta revisión de la configuración.

**Disposición operativa de este informe**: los controles configurativos de P5 y la revisión del Owner están acreditados. Se prepara un único push P6 de la raíz documental autorizada; la viabilidad y separación de roles para **PR futuros** requieren evaluación y autorización antes de su primer uso. Si el Owner decide que la exigencia de independencia de personas ya bloquea P6 bajo el texto ejecutivo, debe prevalecer STOP y solicitar enmienda expresa; este documento no modifica contratos congelados.

## 3. Objeto exacto de P6

- Repositorio remoto: `https://github.com/KhaosMagnus/Project-Control.git`
- Rama nueva: `refs/heads/meta/project-control`.
- Commit local esperado: `cac838940e0e824a1f828ff660e422a6441a1da7`.
- Tree: `3e39ae46b9e1690604387452ee7283062a79e182`.
- Único archivo: modo `100644`, `README.md`; blob SHA-1 `2b30688846710fe73b89a537bb5a8cfb21e738eb`.
- Cero padres; no fetch/merge ni historia de `main`.
- `main` antes del push: `6d6f3639bc0cb84bc76845ad66f859e3fa1117bb`.

## 4. Preflight del Owner inmediatamente antes de P6

El Owner inspecciona localmente la identidad autor/committer publicada, verifica HEAD, tree y limpieza del workspace meta, y ejecuta `git ls-remote --heads` para comprobar que **únicamente** existe `main` en el SHA esperado. Se confirma que los dos rulesets siguen activos y que la instalación compartida conserva selección/exclusión. Cualquier anomalía o salida inconclusa: **STOP sin push**.

En PowerShell, desde la máquina Windows usada para P3:

```powershell
$ErrorActionPreference = 'Stop'
$meta = 'D:\Local\PCM-001_G2-B_EXECUTIVE_AUTHORIZATION_PACKET_2026-11-16\P3-WORK-META'
$url = 'https://github.com/KhaosMagnus/Project-Control.git'
$expectedMain = '6d6f3639bc0cb84bc76845ad66f859e3fa1117bb'
$expectedMeta = 'cac838940e0e824a1f828ff660e422a6441a1da7'
$expectedTree = '3e39ae46b9e1690604387452ee7283062a79e182'

if (!(Test-Path (Join-Path $meta '.git'))) { throw 'STOP: Workspace META ausente.' }
if ((git -C $meta rev-parse HEAD) -ne $expectedMeta -or $LASTEXITCODE -ne 0) { throw 'STOP: SHA META no coincide.' }
if ((git -C $meta rev-parse 'HEAD^{tree}') -ne $expectedTree -or $LASTEXITCODE -ne 0) { throw 'STOP: TREE META no coincide.' }
if ((git -C $meta rev-list --parents -n 1 HEAD) -ne $expectedMeta -or $LASTEXITCODE -ne 0) { throw 'STOP: META no es un commit raíz exacto.' }
$tree = @(git -C $meta ls-tree -r HEAD)
if ($LASTEXITCODE -ne 0 -or $tree.Count -ne 1 -or $tree[0] -notmatch '^100644 blob 2b30688846710fe73b89a537bb5a8cfb21e738eb\s+README\.md$') { throw 'STOP: Árbol META inesperado.' }
$changes = @(git -C $meta status --porcelain)
if ($LASTEXITCODE -ne 0 -or $changes.Count -ne 0) { throw 'STOP: Workspace META no limpio.' }
$refs = @(git ls-remote --heads $url)
if ($LASTEXITCODE -ne 0 -or $refs.Count -ne 1 -or $refs[0] -ne "$expectedMain`trefs/heads/main") { throw 'STOP: Remoto no coincide (solo main esperado). NO PUSH.' }
$remotes = @(git -C $meta remote)
if ($LASTEXITCODE -ne 0) { throw 'STOP: No se pudo leer remote local.' }
if ($remotes -contains 'origin') {
    $origin = git -C $meta remote get-url origin
    if ($LASTEXITCODE -ne 0 -or $origin -ne $url) { throw 'STOP: origin no coincide.' }
} else {
    git -C $meta remote add origin $url
    if ($LASTEXITCODE -ne 0) { throw 'STOP: No se pudo configurar origin local.' }
}
# ÚNICO PUSH P6. No force, no retry, no otro ref.
git -C $meta push origin HEAD:refs/heads/meta/project-control
if ($LASTEXITCODE -ne 0) { throw 'STOP: Push fallido/ambiguo. NO REINTENTAR; reportar para readback.' }
Write-Host 'P6 reportado; detener toda escritura y solicitar readback.'
```

**Después del único intento**, incluso si reporta éxito, el Owner detiene escrituras. PCM-001 debe releer ambas refs, árbol/commit nuevo, reglas, instalación, y decidir P6 PASS/STOP. Solo entonces puede solicitar al Owner P7: `R-META` (misma rama, PR, 1 aprobación elegible, historial lineal, sin bypass); QA de infraestructura P8 solo después de P7. `G3/G4/G5` continúan prohibidos.

## 5. Jerarquía y alcance

Este handoff es **un procedimiento de operación y evidencia**, no una nueva concesión ni una enmienda que anule G2-B, R3, R4 o R5. Si su aplicación resultase incompatible con el requisito de independencia del contrato ejecutivo, prevalece el contrato congelado y el STOP. No se autorizan modificaciones de otros repositorios, de la instalación, force-push, borrado, publicación de archivos extras ni experimentos CAS.
