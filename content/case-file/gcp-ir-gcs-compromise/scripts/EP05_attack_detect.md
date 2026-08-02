# GCP-IR-05 — SCRIPT FINAL

**Duración:** ~52s

---

## VO
¿Cómo debió alertar esto
antes de perder `secretcode.java`?

No detectes “lectura en GCS”.
Detecta desviación.

Uno:
SA con `objects.get`
desde IP no trusted.

Dos:
`EnableService` denied
en una SA que no administra servicios.

Tres:
`gsutil` o `gcloud`
desde identidad de workload.

Cuatro:
acceso a bucket high-value
fuera de baseline.

La detección útil
no es el event name.
Es identidad,
origen,
tool
y secuencia.

Comenta `GCP`
y te paso el checklist de queries.

---

## ON-SCREEN TEXT
| t | text |
|---|------|
| 0–2 | `ATTACK → DETECT` |
| 2–8 | `NO detectes "GCS read"` |
| 8–18 | `1 SA + objects.get + IP rara` |
| 18–26 | `2 EnableService DENIED` |
| 26–34 | `3 gsutil desde workload SA` |
| 34–42 | `4 bucket high-value off-baseline` |
| 42–48 | `identidad + origen + tool + secuencia` |
| 48–52 | `Comenta GCP · checklist` |

## CAPTIONS
```
cómo debió
alertar
antes de perder
secretcode.java
no detectes
lectura GCS
detecta
desviación
SA
objects.get
IP no trusted
EnableService
denied
gsutil
desde workload
bucket
off baseline
identidad
origen
tool
secuencia
comenta
GCP
```
