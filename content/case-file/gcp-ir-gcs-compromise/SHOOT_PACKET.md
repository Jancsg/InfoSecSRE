# SHOOT PACKET — GCP IR #1–#5
**Úsalo el día de grabación.** Todo lo demás es referencia; esto es lo que ejecutas.

**Duración total de rodaje estimada:** 2.5–3.5 h (serie completa)  
**Gear:** iPhone 15 Pro Max + DJI Osmo + DJI Mic 2 + Neewer (key blanca)  
**Formato final:** 1080×1920 · 40–55s · Case File  

---

# 0) SETUP UNA VEZ (20 min)

## Luz
- Neewer key: **blanco 5600K**, 45° a tu izquierda, intensidad media
- Fill: rebote a pared o segunda luz al 30%
- Acento RGB: apagado o verde pared al **10–15%** máx
- Nada de modo fiesta

## Cara (A-roll)
- iPhone en Osmo, **vertical**, lente **1x**
- Altura: ojos
- Distancia: 1–1.5 m
- Osmo: **locked** (sin flotar)
- Encuadre **A1**: pecho-arriba, ojos en tercio superior, espacio libre arriba ~10%
- Encuadre **A2**: más cerrado (hombros/cabeza) solo para hooks

## Audio
- Mic 2 en solapa, 15–20 cm de la boca
- Prueba: di “uno dos tres prueba lab short” + 5s silencio
- Auriculares: confirma que no hay roce de cable

## Pantalla (B-roll técnico)
- Zoom OS 125–150%
- Tema oscuro
- Cursor grande
- Cierra tabs personales
- Deja listas las 10 escenas de log (abajo §1)

## Marcas en piso/escritorio
- Cinta donde pones los pies para repetir A1
- Misma silla/altura en todos los A-roll

---

# 1) ESCENAS DE LOG A TENER ABIERTAS

Graba cada una **3s quieta + 2s con cursor en el campo**.

| ID | Qué debe verse claro |
|----|----------------------|
| L1 | `authenticationInfo.principalEmail` = `cloud-storage-helper@cryptostartup.iam.gserviceaccount.com` |
| L2 | project / contexto `cryptostartup` (opcional) |
| L3 | `callerIp` = `178.132.108.38` |
| L4 | `callerSuppliedUserAgent` con **Macintosh** |
| L5 | UA / tool con **gsutil** |
| L6 | Vista filtrada de errores / denied |
| L7 | method fail: `ServiceUsage.EnableService` |
| L8 | bucket: `importantbucket` |
| L9 | method: `storage.objects.get` |
| L10 | object: `secretcode.java` |

**Nombres de archivo sugeridos:**  
`L1_principalEmail.mp4` … `L10_secretcode.mp4`

---

# 2) ORDEN DE RODAJE DEL DÍA (no grabes ep por ep)

Graba por **tipo de toma** (más rápido):

### Bloque A — Cards (CapCut/Canva, o iPhone a fondo negro)
1. Intro: `JAN · LAB SHORT`
2. Cold opens:  
   - `SA ≠ HUMANO`  
   - `IP + UA`  
   - `FAIL > SUCCESS`  
   - `EXFIL CHAIN`  
   - `ATTACK → DETECT`
3. Outros (fondo `#0B0F14`): ver cada ep abajo

### Bloque B — Cara (iPhone+Osmo+Mic)
Para cada ep: **2 takes** del hook + **2 takes** del cierre (ver guiones).

### Bloque C — Screen
Todas las L1–L10 (take limpio + take con cursor).

### Bloque D — B-roll opcional (10 min)
- Manos/teclado 1s  
- Over-shoulder monitor borroso 1s  

---

# 3) CÓDIGOS DE ENCUADRE (memoriza esto)

| Código | Qué es | Cómo se ve |
|--------|--------|------------|
| **A1** | Talking head MCU | Pecho-arriba, ojos tercio superior |
| **A2** | Hook tight | Más cerrado, más intensidad |
| **B1** | Screen full | Log centrado, márgenes laterales |
| **B2** | Punch-in | Recorte 120–130% al campo |
| **B3** | Highlight | Caja/underline en valor |
| **C1** | Cold open card | Texto hero en negro |
| **C2** | Timeline card | Lista de cadena |
| **C3** | Outro | Criterio + Guárdalo |
| **D1/D2** | B-roll | Teclado / over-shoulder |

**Zona segura móvil:** no pongas info crítica abajo del 20% ni a la derecha del 15% (UI TikTok).

---

# EP01 — IDENTIDAD PRIMERO (~48s)

## Estructura
```
0–1s   C1 intro marca
1–2s   C1/B2 hook visual SA ≠ HUMANO
2–6s   A2 o B1 setup
6–30s  B2/B3 principalEmail + valor
30–40s B1 criterio
40–48s C3 + A1 CTA
```

## Encuadres a grabar (cobertura)
- [ ] C1 `JAN · LAB SHORT`
- [ ] C1 `SA ≠ HUMANO` + label `GCP IR #1`
- [ ] A2 hook (texto abajo) — 2 takes
- [ ] A1 cierre CTA — 2 takes
- [ ] L1 screen limpio
- [ ] L1 screen con cursor al email
- [ ] C3 outro EP01

## Guion CARA — Hook (A2) — lee esto a cámara
> Una service account de storage acaba de tocar código sensible.  
> No empiezo por el bucket. Empiezo por la identidad.

## Guion CARA — Cierre (A1)
> Se trata como hipótesis de abuso de identidad.  
> Guárdalo. Parte dos: IP y user-agent.

## Guion VO sobre pantalla (si no usas cara en el medio)
> En Cloud Audit Logs busco `authenticationInfo.principalEmail`.  
> Aquí aparece: `cloud-storage-helper@cryptostartup.iam.gserviceaccount.com`.  
> Una SA helper haciendo actividad sensible no se trata como ruido de workload.

## Qué mostrar en pantalla
1. Zoom a campo `principalEmail`  
2. Underline verde al email completo  
3. Texto overlay: `SA HELPER + ACCIÓN SENSIBLE = PRIORIDAD`

## Outro card (C3)
```
CRITERIO
SA helper en acción sensible = abuso de identidad

Guárdalo · Parte 2
```

## Tomas exactas (orden en timeline final)
| # | t | Plano | Acción de cámara/edit |
|---|---|-------|------------------------|
| 1 | 0.0–1.0 | C1 | Intro |
| 2 | 1.0–2.5 | C1/B2 | `SA ≠ HUMANO` sobre crop del email |
| 3 | 2.5–6.0 | A2 | Hook a cámara |
| 4 | 6.0–18.0 | B2→B3 | Punch-in a `principalEmail` |
| 5 | 18.0–30.0 | B3 | Hold en valor email |
| 6 | 30.0–40.0 | B1 | Overlay criterio |
| 7 | 40.0–48.0 | A1/C3 | Cierre + CTA |

---

# EP02 — ORIGEN + UA (~50s)

## Estructura
```
0–2s    C1 IP + UA
2–16s   B2/B3 callerIp → Romania
16–38s  B2/B3 UA Macintosh → gsutil
38–50s  C3 fórmula
```

## Encuadres a grabar
- [ ] C1 `IP + UA` · `GCP IR #2`
- [ ] A2 hook (opcional) — 2 takes
- [ ] L3 callerIp
- [ ] L4 Macintosh UA
- [ ] L5 gsutil
- [ ] A1/C3 cierre — 2 takes

## Guion CARA — Hook
> Ya tengo la identidad.  
> Ahora: ¿desde dónde y con qué?

## Guion VO pantalla
> Campo `callerIp`: `178.132.108.38`.  
> Lo saco de baseline y lo paso por intel. Sale Romania.  
> Luego `callerSuppliedUserAgent`. Familia Macintosh.  
> Más adelante, herramienta CLI: `gsutil`.

## Guion CARA — Cierre
> Una service account de storage, desde IP rara, con UA de workstation,  
> no parece automatización legítima. Parece acceso abusado.  
> Parte tres: el primer fail que delata al atacante.

## Overlays
- `178.132.108.38`
- `GEO · Romania`
- `Macintosh`
- `tool · gsutil`
- Final: `SA + IP rara + UA workstation = abuso`

## Outro card
```
CRITERIO
SA + IP rara + UA workstation = abuso

Parte 3 · primer fail
```

## Tomas timeline
| # | t | Plano | Acción |
|---|---|-------|--------|
| 1 | 0–2 | C1 | Cold open |
| 2 | 2–8 | A2/B1 | Hook |
| 3 | 8–16 | B3 | IP + Romania chip |
| 4 | 16–28 | B3 | UA Macintosh |
| 5 | 28–38 | B3 | gsutil |
| 6 | 38–50 | C3/A1 | Fórmula + CTA |

---

# EP03 — PRIMER FAIL (~46s) ★ SAVE

## Estructura
```
0–2s   C1 FAIL > SUCCESS (rojo)
2–22s  B1→B3 errores → EnableService
22–42s interpretación
42–46s C3 CTA
```

## Encuadres a grabar
- [ ] C1 `FAIL > SUCCESS` en `#FF5A5F`
- [ ] A2 hook — 2 takes
- [ ] L6 filter errors
- [ ] L7 EnableService fail (caja roja en edit)
- [ ] A1/C3 cierre — 2 takes

## Guion CARA — Hook
> Error de analista: buscar solo llamadas exitosas.  
> Yo filtro primero los fails.

## Guion VO pantalla
> Aquí el primer failed API call: `ServiceUsage.EnableService`.  
> Traducción: el actor está sondeando si puede habilitar servicios y ampliar capacidad.

## Guion CARA — Cierre
> Una SA de storage fallando `EnableService` antes de tocar el bucket  
> es recon de privilegios.  
> El primer fail importa más que el primer success.  
> Guárdalo. Parte cuatro: del enum al robo.

## Overlays
- `ServiceUsage.EnableService` (rojo)
- `SONDEO DE PRIVILEGIOS`
- `SA storage → FAIL → luego bucket`

## Outro card
```
CRITERIO
Primer fail = recon de privilegios

Guárdalo · Parte 4
```

## Tomas timeline
| # | t | Plano | Acción |
|---|---|-------|--------|
| 1 | 0–2 | C1 | FAIL > SUCCESS |
| 2 | 2–8 | A2 | Hook |
| 3 | 8–16 | B1 | Filter errors |
| 4 | 16–28 | B3 | EnableService + caja roja |
| 5 | 28–42 | B1 | Interpretación |
| 6 | 42–46 | C3/A1 | CTA |

---

# EP04 — CADENA DE EXFIL (~54s) ★ SHARE

## Estructura
```
0–2s    C1 EXFIL CHAIN
2–28s   B2 secuencia bucket → get → tool → object
28–45s  C2 timeline card
45–54s  C3 busca la secuencia
```

## Encuadres a grabar
- [ ] C1 `EXFIL CHAIN` · `GCP IR #4`
- [ ] A2 hook — 2 takes
- [ ] L8 importantbucket
- [ ] L9 storage.objects.get
- [ ] L5 gsutil (reusa)
- [ ] L10 secretcode.java
- [ ] C2 timeline card
- [ ] A1/C3 cierre — 2 takes

## Guion CARA — Hook
> Esta es la cadena completa.

## Guion VO pantalla (sigue el cursor en este orden)
> Después del fail, enumera el bucket: `importantbucket`.  
> Luego el method de lectura: `storage.objects.get`.  
> En IR, eso no se archiva como “get”. Se trata como exfil candidate.  
> Tool: `gsutil`.  
> Objeto: `secretcode.java`.

## Guion CARA — Cierre
> Secuencia: fail de privilegios, enum del bucket, get del objeto sensible,  
> misma identidad, mismo origen.  
> Si solo buscas el download exitoso, llegas tarde. Busca la secuencia.  
> Guárdalo para tu playbook de GCS.

## Timeline card (C2) — crear tal cual
```
1 FAIL   EnableService
2 ENUM   importantbucket
3 GET    storage.objects.get
4 OBJ    secretcode.java
5 TOOL   gsutil
```
- FAIL en rojo  
- GET en verde acento  

## Outro card
```
CRITERIO
No busques solo el download. Busca la secuencia.

Guárdalo · Playbook GCS
```

## Tomas timeline
| # | t | Plano | Acción |
|---|---|-------|--------|
| 1 | 0–2 | C1 | EXFIL CHAIN |
| 2 | 2–6 | A2 | Hook |
| 3 | 6–12 | B3 | importantbucket |
| 4 | 12–20 | B3 | objects.get |
| 5 | 20–26 | B3 | gsutil |
| 6 | 26–32 | B3 | secretcode.java |
| 7 | 32–45 | C2 | Timeline full |
| 8 | 45–54 | A1/C3 | Cierre |

---

# EP05 — ATTACK → DETECT (~52s)

## Estructura
```
0–2s    C1 ATTACK → DETECT
2–42s   4 cards de detección (hard cuts)
42–52s  A1 CTA comenta GCP
```

## Encuadres a grabar
- [ ] C1 `ATTACK → DETECT`
- [ ] A2 hook — 2 takes
- [ ] Card det 1, 2, 3, 4 (gráficos o texto full-screen)
- [ ] A1 cierre CTA — 2 takes (mira a cámara)

## Guion CARA — Hook
> ¿Cómo debió alertar esto antes de perder `secretcode.java`?  
> No detectes “lectura en GCS”. Detecta desviación.

## Guion VO / cards (una por corte)
1. > SA con `objects.get` desde IP no trusted.  
2. > `EnableService` denied en una SA que no administra servicios.  
3. > `gsutil` o `gcloud` desde identidad de workload.  
4. > Acceso a bucket high-value fuera de baseline.

## Guion CARA — Cierre
> La detección útil no es el event name.  
> Es identidad, origen, tool y secuencia.  
> Comenta `GCP` y te paso el checklist de queries.

## Cards texto (full screen)
```
1  SA + objects.get + IP rara
2  EnableService DENIED
3  gsutil desde workload SA
4  bucket high-value off-baseline
```

## Outro card
```
CRITERIO
Identidad + origen + tool + secuencia

Comenta GCP · checklist
```

## Tomas timeline
| # | t | Plano | Acción |
|---|---|-------|--------|
| 1 | 0–2 | C1 | ATTACK → DETECT |
| 2 | 2–8 | A2 | Hook |
| 3 | 8–16 | C2 | Det 1 |
| 4 | 16–24 | C2 | Det 2 |
| 5 | 24–32 | C2 | Det 3 |
| 6 | 32–40 | C2 | Det 4 |
| 7 | 40–52 | A1 | Cierre + CTA |

---

# 4) CHEAT SHEET DE GRABACIÓN EN VOZ (teleprompter)

Copia esto a Notas del iPhone / teleprompter. Lee lento.

## EP01
Una service account de storage acaba de tocar código sensible.  
No empiezo por el bucket. Empiezo por la identidad.  
En Cloud Audit Logs busco authenticationInfo.principalEmail.  
Aquí aparece cloud-storage-helper arroba cryptostartup.  
Una SA helper haciendo actividad sensible no es ruido de workload.  
Es hipótesis de abuso de identidad.  
Guárdalo. Parte dos: IP y user-agent.

## EP02
Ya tengo la identidad. Ahora: desde dónde y con qué.  
CallerIp: 178.132.108.38. Intel: Romania.  
User agent: Macintosh. Tool: gsutil.  
SA de storage, IP rara, UA de workstation… no es automatización legítima.  
Parece acceso abusado.  
Parte tres: el primer fail que delata al atacante.

## EP03
Error de analista: buscar solo llamadas exitosas.  
Yo filtro primero los fails.  
Primer failed API call: ServiceUsage.EnableService.  
Está sondeando privilegios.  
SA storage fallando EnableService antes del bucket = recon.  
El primer fail importa más que el primer success.  
Guárdalo. Parte cuatro: del enum al robo.

## EP04
Esta es la cadena completa.  
Bucket: importantbucket.  
Method: storage.objects.get. En IR es exfil candidate.  
Tool: gsutil. Objeto: secretcode.java.  
Fail, enum, get, misma identidad, mismo origen.  
Si solo buscas el download, llegas tarde. Busca la secuencia.  
Guárdalo para tu playbook de GCS.

## EP05
Cómo debió alertar esto antes de perder secretcode.java.  
No detectes lectura en GCS. Detecta desviación.  
Uno: SA con objects.get desde IP no trusted.  
Dos: EnableService denied en SA no admin.  
Tres: gsutil desde identidad de workload.  
Cuatro: bucket high-value fuera de baseline.  
Identidad, origen, tool y secuencia.  
Comenta GCP y te paso el checklist.

---

# 5) CHECKLIST FINAL ANTES DE APAGAR LUCES

## Media capturada
- [ ] 5 cold opens  
- [ ] 5 outros  
- [ ] Intro marca  
- [ ] Timeline EP04  
- [ ] 4 detection cards EP05  
- [ ] A-roll hooks ×5 (mín 2 takes c/u)  
- [ ] A-roll cierres ×5  
- [ ] Screen L1–L10  
- [ ] B-roll D1/D2 (opcional)

## Calidad
- [ ] Audio limpio (sin roce)
- [ ] Ojos a foco en A-roll
- [ ] Logs legibles a pulgar en preview del iPhone
- [ ] Misma luz/encuadre en todos los A-roll
- [ ] Sin notificaciones en screen

## Siguiente paso (edit)
Abre CapCut → template Case File → ensambla en orden de tablas “Tomas timeline” de cada EP → captions de `scripts/` → exporta.

---

# 6) PLAN B SI VAS CORTO DE TIEMPO

Graba solo esto y aún cierras la serie:

1. Screen L1, L3, L7, L8, L9, L10  
2. VO completa teleprompter (sin cara)  
3. Cards cold open + outro  
4. Cara solo en EP01 hook + EP05 cierre  

Mínimo viable profesional: **terminal + VO documental + cards**. La cara es bonus.
