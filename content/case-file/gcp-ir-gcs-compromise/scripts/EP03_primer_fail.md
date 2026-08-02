# GCP-IR-03 — SCRIPT FINAL (SAVE MAGNET)

**Duración:** ~46s

---

## VO
Error de analista:
buscar solo llamadas exitosas.

Yo filtro primero los fails.

Aquí el primer failed API call:
`ServiceUsage.EnableService`.

Traducción:
el actor está sondeando
si puede habilitar servicios
y ampliar capacidad.

Una SA de storage
fallando `EnableService`
antes de tocar el bucket
es recon de privilegios.

El primer fail
importa más que el primer success.

Guárdalo.
Parte cuatro: del enum al robo.

---

## ON-SCREEN TEXT
| t | text | color |
|---|------|-------|
| 0–2 | `FAIL > SUCCESS` | red |
| 2–8 | `FILTRA ERRORES PRIMERO` | white |
| 8–22 | `ServiceUsage.EnableService` | mono + red |
| 22–34 | `SONDEO DE PRIVILEGIOS` | accent |
| 34–42 | `SA storage → FAIL → luego bucket` | white |
| 42–46 | `Guárdalo · Parte 4` | CTA |

## CAPTIONS
```
error de analista
solo ver successes
yo filtro
fails primero
EnableService
falló
está sondeando
privilegios
SA storage
fail primero
bucket después
recon
antes de exfil
guárdalo
parte 4
```
