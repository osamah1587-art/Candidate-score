# Candida Score Calculator

ICU clinical decision support tool for estimating the probability of invasive candidiasis in critically ill patients.

## Features

- **Leon 2006 (original)** — validated 4-variable model (max score 7, threshold ≥ 3)
- **Modified (expanded)** — adds 4 extra ICU-relevant modifiers (max score 11, threshold ≥ 4)
- **Side-by-side comparison** — both scores with full factor weight table
- Color-coded risk stratification (low / moderate / high)
- Antifungal recommendations with dosing guidance
- Clinical notes field per model
- Reset all button
- Dark mode support
- PWA-ready (add to home screen)

## Deploy to GitHub Pages

1. Create a new repository (e.g. `candida-score`)
2. Upload `index.html` and `manifest.json`
3. Go to **Settings → Pages → Source → main branch / root**
4. Your app will be live at `https://YOUR-USERNAME.github.io/candida-score/`

> **Note:** For full PWA icon support, add `icon-192.png` and `icon-512.png` to the repo (192×192 and 512×512 px).  
> If you skip this, the app still works — just without a custom home screen icon.

## Scoring

### Leon 2006 (original)
| Factor | Points |
|---|---|
| Surgery on ICU admission | +1 |
| Total parenteral nutrition | +1 |
| Multifocal Candida colonization (≥2 sites) | +3 |
| Severe sepsis | +2 |
| **Max** | **7** |

**Threshold:** Score ≥ 3 → consider empirical antifungal

### Modified (expanded)
Adds to the Leon variables:
| Extra factor | Points |
|---|---|
| ICU stay ≥ 7 days | +1 |
| Broad-spectrum antibiotics ≥ 3 days | +1 |
| Renal replacement therapy | +1 |
| Immunosuppression / steroids | +1 |
| **Max** | **11** |

**Threshold:** Score ≥ 4 → consider empirical antifungal

## Reference

Leon C et al. *Crit Care Med* 2006;34:730–737.

---

*For clinical decision support only — not a substitute for clinical judgement.*
