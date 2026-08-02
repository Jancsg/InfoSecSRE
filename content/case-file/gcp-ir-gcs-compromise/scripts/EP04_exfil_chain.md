# GCP-IR-04 — SCRIPT FINAL (SHARE MAGNET)

**Duración:** ~54s

---

## VO
Esta es la cadena completa.

Después del fail,
enumera el bucket:
`importantbucket`.

Luego el method de lectura:
`storage.objects.get`.

En IR,
eso no se archiva como “get”.
Se trata como exfil candidate.

User-agent / tool:
`gsutil`.

Objeto:
`secretcode.java`.

Secuencia:
fail de privilegios,
enum del bucket,
get del objeto sensible,
misma identidad,
mismo origen.

Si solo buscas el download exitoso,
llegas tarde.

Busca la secuencia.

Guárdalo para tu playbook de GCS.

---

## ON-SCREEN TIMELINE CARD (mostrar 28–48s)
```
1 EnableService  FAIL
2 bucket enum    importantbucket
3 objects.get    EXFIL?
4 object         secretcode.java
5 tool           gsutil
```

## ON-SCREEN TEXT
| t | text |
|---|------|
| 0–2 | `EXFIL CHAIN` |
| 2–10 | `importantbucket` |
| 10–20 | `storage.objects.get` |
| 20–28 | `≠ read · = exfil candidate` |
| 28–40 | timeline card |
| 40–48 | `secretcode.java` |
| 48–54 | `Busca la secuencia · Guárdalo` |

## CAPTIONS
```
cadena completa
enumera
importantbucket
method
objects.get
en IR
es exfil candidate
tool
gsutil
objeto
secretcode.java
fail
enum
get
misma identidad
si solo ves
el download
llegas tarde
busca
la secuencia
guárdalo
```
