# EPISODE RUNDOWNS — GCP IR #1–#5

## EP01 — Identidad primero
- **Code:** GCP-IR-01
- **Duración target:** 45–50s
- **Hook:** `Una SA de storage acaba de robar código. Esto miro primero en GCP`
- **Objetivo viewer:** Empezar triage por `principalEmail`, no por el bucket
- **Artifact hero:** `authenticationInfo.principalEmail`
- **Takeaway:** SA helper haciendo acción sensible = prioridad abuso de identidad
- **CTA:** Guárdalo · Parte 2: IP + user-agent
- **A-roll:** 0–2s + 42–50s
- **Screen %:** ~85%

## EP02 — Origen y herramienta
- **Code:** GCP-IR-02
- **Duración:** 45–55s
- **Hook:** `callerIp + userAgent: cómo separo ruido de compromiso`
- **Objetivo:** Correlacionar IP/geo/UA con la SA
- **Artifacts:** `callerIp`, `callerSuppliedUserAgent`
- **Takeaway:** SA + IP rara + UA Macintosh/CLI ≠ workload normal
- **CTA:** Parte 3: el primer fail que delata al atacante

## EP03 — Primer fail
- **Code:** GCP-IR-03
- **Duración:** 40–50s
- **Hook:** `El primer fail importa más que el primer success`
- **Objetivo:** Usar errores como señal de recon
- **Artifact:** `ServiceUsage.EnableService` (denied/error)
- **Takeaway:** Failed EnableService antes de exfil = sondeo de privilegios
- **CTA:** Parte 4: del enum al robo
- **Nota productor:** episodio “save magnet”

## EP04 — Cadena de exfil
- **Code:** GCP-IR-04
- **Duración:** 50–55s
- **Hook:** `storage.objects.get no es leer un archivo. En IR es exfil candidate`
- **Objetivo:** Armar cadena enum → get → objeto → tool
- **Artifacts:** `importantbucket`, `storage.objects.get`, `gsutil`, `secretcode.java`
- **Takeaway:** Si solo buscas download exitoso, llegas tarde
- **CTA:** Guárdalo para tu playbook de GCS
- **Nota productor:** episodio “share magnet”

## EP05 — Attack → Detect
- **Code:** GCP-IR-05
- **Duración:** 50–55s
- **Hook:** `Cómo debió alertar esto antes de perder secretcode.java`
- **Objetivo:** Traducir la cadena a detecciones accionables
- **Takeaway:** No detectes “GCS read”; detecta desviación identidad+origen+tool
- **CTA:** Comenta `GCP` y te paso el checklist de queries
