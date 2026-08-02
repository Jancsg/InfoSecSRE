# GCP-IR-01 — SCRIPT FINAL (palabra por palabra)

**Duración:** ~48s  
**VO pace:** calmado, 1.05x si hace falta  
**Cold open visual:** log con `principalEmail` ya resaltado

---

## VO
Una service account de storage acaba de tocar código sensible.

No empiezo por el bucket.
Empiezo por la identidad.

En Cloud Audit Logs busco
`authenticationInfo.principalEmail`.

Aquí aparece:
`cloud-storage-helper@cryptostartup.iam.gserviceaccount.com`.

Una SA “helper” haciendo actividad sensible
no se trata como ruido de workload.

Se trata como hipótesis de abuso de identidad.

Guárdalo.
Parte dos: IP y user-agent.

---

## ON-SCREEN TEXT (timed)
| t | text | style |
|---|------|-------|
| 0.0–2.0 | `SA ≠ HUMANO` | hero / accent |
| 0.0–2.0 | `GCP IR #1` | label |
| 2.0–6.0 | `IDENTIDAD PRIMERO` | hero |
| 6.0–18.0 | `authenticationInfo.principalEmail` | mono highlight |
| 18.0–30.0 | `cloud-storage-helper@...` | mono + green underline |
| 30.0–40.0 | `SA HELPER + ACCIÓN SENSIBLE` | alert soft |
| 30.0–40.0 | `= PRIORIDAD` | accent |
| 40.0–48.0 | `CRITERIO: abuso de identidad` | outro |
| 44.0–48.0 | `Guárdalo · Parte 2` | CTA |

## CAPTIONS (línea por línea)
```
una SA de storage
tocó código sensible
no empiezo
por el bucket
empiezo
por la identidad
principalEmail
cloud-storage-helper
SA helper
actividad sensible
no es ruido
es abuso
de identidad
guárdalo
parte 2
```
