# Portable bootstrap — staging workspace (NOT a release)

**Work branch:** `dev/portable`, created from `main@6d6f3639bc0cb84bc76845ad66f859e3fa1117bb` by Owner-approved `PCM-BRANCH-STRATEGY-001`.
**Historical source:** `KhaosMagnus/YU3DOH-Carder` @ `056adb5097b7ce067082782e8d8c92b42db9082a` (frozen source snapshot).
**Purpose:** preserve the exact historical `PROJECT_CONTROL_BOOTSTRAP-v1.0` package before designing and validating a successor.
**Status:** SOURCE IMPORTED FOR DEVELOPMENT / NO INDEPENDENT QA OR RELEASE ACCEPTANCE / NO ADOPTION BY PROJECTS.
**Authority record:** `meta/project-control:decisions/PCM-BRANCH-STRATEGY-001_OWNER_APPROVAL_2026-11-22.md` (resolve control HEAD at use).

## Historical frozen inputs

- `bootstrap/PROJECT_CONTROL_BOOTSTRAP-v1.0/`: original 11-file payload (one MANIFEST + 10 manifest-listed files), unchanged; protocol v1.0 SHA-256 `586cb4d8740e33ac8a3a6db65a5ce1506fe855ca1968adacd3034352106c70e3` / Git blob `1ac3689c1e811d1594291afee6b2c1c6efd093d0`.
- `bootstrap/dist/PROJECT_CONTROL_BOOTSTRAP-v1.0.zip`: original 62,955-byte ZIP, Git blob `13eae102d5aed553d4fb3a023ab77b71601306b2`, SHA-256 `c3c5cb0c896d7e11696948e7677d74ea077a87d27350064b1ad6d521ceb74f6e`. Sidecar bytes also unchanged.
- `bootstrap/legacy/build_package_yu3doh_v1.py`: unmodified historical builder, source blob `83a580f9d2339e566ea2a2ceddfa98b39f9ef07f`. **Do not execute as the master builder**: it runs `git show bd1840bf0b1dc8e294af1226ec6cfb0546f7bc89:protocols/GENERIC_PROJECT_CONTROL_PROTOCOL-v1.0.md` against the local repository; the referenced YU3DOH commit is not guaranteed to exist here.
- The frozen ZIP does not require the historical builder to be consumed. To produce a successor, write a new portable builder and validate a new package identity rather than altering v1.0 in place.

## Development sequence (NOT automatically authorized as a release)

1. Independently verify exact source Git blobs, manifest digests, ZIP members and CRC; compare against historical report. Import does not equal QA PASS.
2. Determine amendments for a successor separately: improvements to documenting decisions/evidence and retentions, conditional Git operations, and the proposed normative versioning model. `PCM-VERSIONING-001` is not yet adopted.
3. Design and implement candidate outside the frozen `v1.0` directory, e.g. `bootstrap/next/`, with new version chosen only after compatibility assessment.
4. Pin a candidate SHA, run agreed tests and QA, receive separate Owner integration authorization. `main` continues protected; no merge, tag or release created by this import.

**Return route:** DEVELOPMENT/PCM-001 → Owner / independent QA by future assignment. Keep source/history and local governance separate.
