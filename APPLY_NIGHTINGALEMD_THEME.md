# Apply NightingaleMD Theme

**Portable branding shortcut.** Paste this into any LLM when building a NightingaleMD deck, document, or UI — or point the model at this file's raw URL:
`https://raw.githubusercontent.com/omarzsalah1/nightingale-brand-assets/main/APPLY_NIGHTINGALEMD_THEME.md`

Authoritative as of **2026-07-14**. Self-contained (no fetch needed except the logo images). Free to reuse.

> **What changed from the old theme:** the single "Brand Red `#E45740`" is **RETIRED** and split into **Brand Coral** (human accent) + **Deep Alert Red** (negatives only). The palette is now a 15-color *semantic* set. **A color must be used for its assigned job — on-palette but wrong-role is a branding error.**

---

## LOGOS
- **Full logo (Shield + Name):** `https://raw.githubusercontent.com/omarzsalah1/nightingale-brand-assets/main/logos/full-logo.png`
- **Shield only:** `https://raw.githubusercontent.com/omarzsalah1/nightingale-brand-assets/main/logos/shield-only.png`

Placement: **Shield-only** bottom-right (~50px) on content slides; **Full logo** (~100px) centered on title + closing slides. Never stretch, recolor, add effects, or place the logo on a busy background.

---

## COLORS — 15-color semantic set

**Primary / structure**
- Brand Teal `#55B5B8` — primary anchor: headers, nav, trusted/system states, primary data series
- Neutral Dark `#49545E` — icons, axes, dividers, structured UI
- Text Primary `#31393F` — all body text
- Text Secondary `#5A6872` — captions, footnotes, supporting copy

**Human / accent** *(replaces the retired red)*
- Brand Coral `#F26E67` — primary HUMAN accent: engagement, momentum, featured callouts
- Soft Coral `#F48B80` — secondary accent: member-facing highlights, supporting data series
- Rose Tint `#F5A2A2` — soft backgrounds, quote panels, subtle emphasis

**Signal**
- Deep Alert Red `#C9473D` — risks, clinical warnings, refusals, negative outcomes **ONLY** (never decoration)
- Brand Yellow `#F8CA44` — KPIs, financial highlights, priority moments (use sparingly)
- Sage Green `#8FA56A` — positive progress, completion, secondary success
- Olive Green `#6F7E43` — grounding accent, supporting charts, mature clinical context
- Lavender Gray `#B9AEC8` — governance, data, secondary info, comparison series

**Surfaces**
- Warm Ivory `#F8F4EC` — primary slide/page background
- Brand Gray Light `#F2F3F4` — tables, cards, alternate backgrounds
- Warm White `#FFFDFC` — high-contrast content surfaces

**RETIRED — do NOT use:** Brand Red `#E45740` (→ use Brand Coral for human accent, Deep Alert Red for negatives).

---

## FONTS
- **Headlines:** Merriweather Bold (H1 48–60pt, H2 40–44pt)
- **Body / labels:** Lato Regular/Semibold (body 16–20pt, captions 11–14pt)
- **KPIs / big numbers:** Lato Bold
- **Minimum size:** 10pt — never smaller

---

## LAYOUT
- 16:9 aspect ratio (1280×720 or 1920×1080)
- 64px margins, 24px gutters, 12-column grid
- Content in **2–3 columns** (avoid vertical stacking)
- Backgrounds: **Warm Ivory** default; **Warm White** for high-contrast content; **Brand Gray Light** for cards/tables
- Footer: `© NightingaleMD 2026 | NightingaleMD.com` in Text Secondary
- Logo per the placement rule above

---

## STYLE
- Clean, flat design — no gradients, no 3D, no drop shadows on light surfaces
- Line-art icons (Neutral Dark, 1–2px stroke) — no filled/duotone mixing, no emoji
- Data labels directly on charts (no legends)
- One idea per slide
- Horizontal layouts for timelines/processes
- Sentence case everywhere; lead with real numbers, set bold

---

## THE ONE RULE
Every color must do its assigned job. **Teal = trust/structure. Coral = human warmth. Deep Alert Red = danger only. Yellow = KPI spotlight (sparingly). Green = progress. Lavender = data/governance.** On-palette but wrong-role reads as off-brand.

---

## CSS variables (drop into any HTML/CSS deck)
```css
:root{
  /* structure */
  --nm-teal:#55B5B8; --nm-neutral:#49545E; --nm-text:#31393F; --nm-text-2:#5A6872;
  /* human accent */
  --nm-coral:#F26E67; --nm-coral-soft:#F48B80; --nm-rose:#F5A2A2;
  /* signal */
  --nm-alert:#C9473D; --nm-yellow:#F8CA44; --nm-sage:#8FA56A; --nm-olive:#6F7E43; --nm-lavender:#B9AEC8;
  /* surfaces */
  --nm-ivory:#F8F4EC; --nm-gray-light:#F2F3F4; --nm-white:#FFFDFC;
}
```
Headlines `font-family:"Merriweather",serif;font-weight:700` · Body `"Lato",sans-serif`.
