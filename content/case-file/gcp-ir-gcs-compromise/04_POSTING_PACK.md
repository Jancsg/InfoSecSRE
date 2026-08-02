# POSTING PACK — COPY + HASHTAGS + PIN STRATEGY

## Cadencia sugerida
| Día | Ep |
|-----|----|
| Lun | EP01 |
| Mié | EP02 |
| Vie | EP03 |
| Dom | EP04 |
| Mar (sem 2) | EP05 |

Horario: cuando tu audiencia tech está activa (prueba 12:00–14:00 o 19:00–21:00 CT).

---

## EP01 caption (TikTok)
```
En GCP no empiezo por el bucket. Empiezo por la identidad.

Cloud Audit Logs → authenticationInfo.principalEmail
Lab short de triage real (GCS compromise).

Guárdalo. Parte 2: IP + user-agent.

#GCP #CloudSecurity #DFIR #BlueTeam #CloudIR #LabShort
```

## EP02
```
Misma SA. Ahora origen y herramienta.

callerIp + callerSuppliedUserAgent
IP rara + UA workstation = hipótesis de abuso.

Parte 3: el primer FAIL que delata recon de privilegios.
```

## EP03
```
Error de analista: solo mirar successes.

El primer fail — ServiceUsage.EnableService —
suele ser el sondeo antes de la exfil.

Guárdalo para tu playbook.
Parte 4: la cadena completa.
```

## EP04
```
Cadena de exfil en GCS:

EnableService FAIL
→ importantbucket
→ storage.objects.get
→ gsutil
→ secretcode.java

Si solo buscas el download, llegas tarde.
Busca la secuencia.
```

## EP05
```
Attack → Detect

No alertes “GCS read”.
Alerta desviación:
identidad + origen + tool + secuencia.

Comenta GCP y te paso el checklist de queries.
```

---

## Pinned comment (cada ep)
EP01–04: `Serie GCP IR · lab defensivo · sin relleno`
EP05: `Checklist: SA objects.get off-baseline · EnableService denied · gsutil en workload SA · bucket high-value`

## Highlights / playlist
- Highlight TikTok: `GCP IR`
- Orden: 1→5
- Cover frame: timeline card EP04 o `SA ≠ HUMANO`

## Crosspost
- LinkedIn: EP04 o EP05 con 5 líneas de criterio senior (sin hashtags spam)
- No cambies el look entre plataformas; recorta captions sí

## Reply strategy (crece serie)
Si preguntan “qué query uso?”, responde:
`Parte 5 lo cubre — y si quieres te suelto el checklist completo`
