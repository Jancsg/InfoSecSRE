# GCP-IR-02 — SCRIPT FINAL

**Duración:** ~50s

---

## VO
Ya tengo la identidad.
Ahora: ¿desde dónde y con qué?

Campo `callerIp`:
`178.132.108.38`.

Lo saco de baseline y lo paso por intel.
Sale Romania.

Luego `callerSuppliedUserAgent`.
Familia Macintosh.
Más adelante, herramienta CLI: `gsutil`.

Una service account de storage
desde IP rara
con UA de workstation
no parece automatización legítima.

Parece acceso abusado.

Parte tres:
el primer fail que delata al atacante.

---

## ON-SCREEN TEXT
| t | text |
|---|------|
| 0–2 | `IP + UA` |
| 2–8 | `callerIp` |
| 8–16 | `178.132.108.38` |
| 16–22 | `GEO · Romania` |
| 22–32 | `callerSuppliedUserAgent` |
| 32–38 | `Macintosh` |
| 38–44 | `tool · gsutil` |
| 44–50 | `SA + IP rara + UA workstation = abuso` |
| 47–50 | `Parte 3 · primer fail` |

## CAPTIONS
```
ya tengo
la identidad
ahora
desde dónde
y con qué
callerIp
178.132.108.38
intel
Romania
userAgent
Macintosh
después
gsutil
SA de storage
IP rara
workstation
no es normal
es abuso
parte 3
primer fail
```
