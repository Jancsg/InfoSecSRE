# SERIES BIBLE — GCP IR: GCS Compromise
**Show:** LAB SHORT · Case File  
**Series code:** `GCP-IR`  
**Episodes:** 5  
**Format:** TikTok / Reels / Shorts · 9:16 · 40–55s  
**Language:** Español (términos técnicos en inglés tal cual en logs)  
**Inspiration lab:** LetsDefend — Google Cloud Compromise (método/procedimiento; no Q&A)  
**Creator:** Jan Carlos Santillán García · DFIR / Cloud IR / Offensive→Defensive  

---

## 1. Logline
Una service account de storage abusa GCS. En Cloud Audit Logs reconstruimos la cadena: identidad → origen → primer fail → enum → exfil.

## 2. Promesa al viewer
Al terminar la serie puede hacer triage de exfil GCS por campos reales de Audit Logs, no por vibes.

## 3. Tono
- Documental forense, calmado, preciso
- Cero “qué es GCP”
- Cero clickbait de miedo
- Una idea dominante por episodio
- Criterio de experto al cierre

## 4. Personajes / entidades del caso (lab)
| Entidad | Valor |
|--------|--------|
| Project | `cryptostartup` |
| Compromised identity | `cloud-storage-helper@cryptostartup.iam.gserviceaccount.com` |
| Source IP | `178.132.108.38` |
| Geo | Romania |
| Device/UA family | Macintosh |
| First failed API | `ServiceUsage.EnableService` |
| Bucket | `importantbucket` |
| Exfil method | `storage.objects.get` |
| Tool | `gsutil` |
| Object | `secretcode.java` |

## 5. Arco narrativo de la serie
1. Identidad (quién)
2. Origen (desde dónde / con qué)
3. Primer fail (recon de privilegios)
4. Cadena de exfil (qué / cómo)
5. Attack → Detect (cómo debió alertar)

## 6. Brand system (Case File)
### Color
- BG: `#0B0F14`
- Text: `#E8EEF5`
- Accent evidence: `#3DDC97`
- Alert/mismatch: `#FF5A5F`
- Muted: `#8B95A5`

### Type
- UI/labels: Space Grotesk / Sora / IBM Plex Sans
- Logs/code: JetBrains Mono / IBM Plex Mono

### Persistent lower-third
`LAB SHORT · GCP IR` (small, top-left or top-center, always)

### Intro (1.0s)
Black → hard cut → `JAN · LAB SHORT` → cold open on artifact

### Outro (2.5–3.5s)
Dark card:
```
CRITERIO
[one line]

Guárdalo · Parte N
```

## 7. Gear lock
- Camera A (A-roll face): iPhone 15 Pro Max + DJI Osmo · 1x · 4K30 or 1080p60
- Audio: DJI Mic 2 (TX on lapel)
- Lights: Neewer RGB → white key 4500–5600K; optional low accent only
- B-roll: Osmo locked / slow push; no floaty gimbal
- Screen: native recording (OBS/CapCut), never filmed monitor

## 8. Editorial rules
- Max 1 accent color meaning at a time
- No emoji overlays
- No floating badges
- Captions 2–4 words/line
- Keep right ~15% and bottom ~20% clear of TikTok UI
- First frame must be readable muted

## 9. Legal / safety
- Lab/demo data only
- No employer/client data
- Credit method inspiration, not “this is a real breach walkthrough”
- Defensive framing: detection / IR / forensics

## 10. KPI targets (series)
- Save rate above account median
- Comments asking for queries/checklist
- Series watch-through (part N → part N+1)
- Search + profile traffic on “GCP IR / GCS / Audit Logs”
