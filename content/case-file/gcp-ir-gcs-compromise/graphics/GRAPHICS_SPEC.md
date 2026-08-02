# GRAPHICS SPEC — CASE FILE PACK

## Canvas
- 1080 x 1920
- Safe margins: top 120px, bottom 340px, right 180px, left 64px

## Persistent elements
### Lower-third / series chip
- Text: `LAB SHORT · GCP IR`
- Size: 28–32px
- Color: `#8B95A5`
- Position: x=64, y=100
- Opacity: 90%

### Episode chip (optional)
- `GCP IR #0N`
- Accent `#3DDC97` on number only

## Title cards
### Cold open
- BG `#0B0F14`
- Hero text centered slightly above middle
- Font bold sans 72–84px
- Subtext mono 32px muted

### Outro
```
CRITERIO
[one line max 60 chars]

Guárdalo · Parte N
```
- CRITERIO label: muted 28px
- Body: 44–52px
- CTA: accent 36px

## Highlight treatments (screen overlays)
1. **Field label tag** — small pill above field: `principalEmail`
2. **Underline** — 4px `#3DDC97` under value
3. **Alert box** — 2px `#FF5A5F` rectangle around failed method
4. **Dimmer** — rest of log at 40% brightness when focusing one line

## Timeline card (EP04)
Container:
- width 900px centered
- BG `#121821`
- radius 12 (ok here: interaction/readability board)
- padding 28

Rows:
```
FAIL  EnableService
ENUM  importantbucket
GET   storage.objects.get
OBJ   secretcode.java
TOOL  gsutil
```
- Left labels muted
- Right values white / mono
- FAIL row value in `#FF5A5F`
- GET row value in `#3DDC97`

## Do / Don’t
DO: one hero text max on screen besides captions  
DON’T: arrows flying, stickers, “POV”, neon grids, skulls, matrix rain

## Asset list to pre-render (PNG/WebM)
- [ ] `intro_jan_labshort.png`
- [ ] `chip_labshort_gcp.png`
- [ ] `card_sa_ne_humano.png`
- [ ] `card_fail_gt_success.png`
- [ ] `card_exfil_chain.png`
- [ ] `card_attack_detect.png`
- [ ] `timeline_ep04.png`
- [ ] `outro_template.psd/capcut` (editable)
- [ ] `detection_list_1to4.png` (EP05)
