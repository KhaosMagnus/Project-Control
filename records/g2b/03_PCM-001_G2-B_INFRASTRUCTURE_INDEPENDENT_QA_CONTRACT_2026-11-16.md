# PCM-001 — G2-B Independent Infrastructure QA / Owner Acceptance Contract

**Assignment to propose at G2-B:** `PCM-G2B-IQA-INFRA-001`  
**Execution requires prior Owner G2-B GRANTED; this document itself is non-executable.**

Two independent reviewers (one ChatGPT and one Grok or separately designated independent persons) receive the **same** frozen evidence after P7, using distinct read-only sessions. No GitHub write credentials, no code merges, no app/permissions changes and no test pushes.

## Read-only acceptance tests

| ID | Expected condition | Required evidence | Fail/unknown handling |
|---|---|---|---|
| Q1 | Repo actual ID/owner correct; public; default `main`; no unintended extra public artifacts | GitHub readback and setting summary | FAIL/UNKNOWN |
| Q2 | `main` commit root (`parents=[]`) and exactly reviewed `README.md` mode `100644` | SHA, `ls-tree`, file bytes SHA-256 `e924a5791fae6d7cb4b380c351a77bb7982301b93cfa78455a2166d63121e340` | FAIL |
| Q3 | `meta/project-control` root (`parents=[]`), exactly reviewed README mode `100644` | SHA, `ls-tree`, SHA-256 `326f9ae9f119fa4319a0170565c8bd4d75d3000ebb329bdb28b5c7a0e52a0ae0` | FAIL |
| Q4 | Two lineages independent; full object retrieval and `git merge-base` no common ancestor, exit=1 | Full refs/tips and Git graph checks | UNKNOWN if incomplete; FAIL if shared |
| Q5 | Common guard ACTIVE **from before first push** covering both branches, with no bypass, anti-deletion + anti-force | Rule ID, creation timestamp, targeting/readbacks, operator record | FAIL/UNKNOWN |
| Q6 | `R-MAIN` and `R-META` ACTIVE; PR, independent reviewer eligibility and linear history, methods viable, no missing CI check | Rule ID, selectors, admin readback, user/role evidence | FAIL/UNKNOWN |
| Q7 | Installation `162412374` still `selected`, old approved set unchanged, new `repo_id` excluded | Administrative selected list before/after, API metadata, separate personal OAuth caveat | FAIL/UNKNOWN |
| Q8 | Only authorized repo-related operations, one push for each root; no G3 import, release, PCM activation or other project mutation | Logs, refs, selected readbacks; limits noted | FAIL/UNKNOWN |
| Q9 | Partial/ambiguous operations followed freeze/STOP/recovery rules, if any | Event/readback table | FAIL/UNKNOWN |

**Important:** Public GET access to the new repository does **not** prove app exclusion; selected-list admin evidence is required. No readback proves absence of every transient write, so state the actual confidence and observational limits.

Each report: `PASS / FAIL / INCONCLUSIVE`, with exact observed SHAs, effective controls, no-write attestation, limitations and claims graded `VERIFIED / PARTIAL / UNKNOWN`. Differing QA conclusions are reconciled by PCM-001 as a **proposal**; Owner independently decides G2-B acceptance. A `PASS` does not authorize G3, G4, G5, any autonomous publication, or adoption by Certificador AOI.
