# Apply NightingaleMD Theme — v3 (canonical)

**Portable branding shortcut.** Paste into any LLM when building a NightingaleMD deck, document, or UI — or point the model at this file's raw URL:
`https://raw.githubusercontent.com/omarzsalah1/nightingale-brand-assets/main/APPLY_NIGHTINGALEMD_THEME.md`

Authoritative **2026-07-16**. Reconciled with the canonical NightingaleMD Design System — fonts, the full color spec, and the real SVG logos. Self-contained except the logo images. Free to reuse.

> **v3 changes:** logos now point to the **canonical SVG** marks (were PNGs). Colors updated to the canonical spec — **Deep Teal `#3E8E91`** for text/buttons, **Paper White `#FBFAF7`** as the default background (Warm White for cards), ivory demoted to occasional tints. Fonts confirmed **Fraunces / Hanken Grotesk / IBM Plex Mono / Newsreader**.
> **Retired — do NOT use:** Legacy Teal `#2BA79C`, Legacy Red `#E45740` (red survives **only** as the logo mark), and Merriweather/Lato. A color must be used for its assigned job — on-palette but wrong-role is a branding error.

---

## LOGOS (canonical SVG)
- **Shield mark:** `https://raw.githubusercontent.com/omarzsalah1/nightingale-brand-assets/main/logos/nightingale-icon-red.svg`
- **Full lockup:** `https://raw.githubusercontent.com/omarzsalah1/nightingale-brand-assets/main/logos/nightingale-logo-full.svg`

Placement: **Shield** bottom-right (~44px) on content slides; **full lockup** — or shield + a lettered "NightingaleMD" wordmark (Hanken Grotesk Light, "MD" in a red chip) — on title/closing. The mark is brand red `#E45740`; that is the one sanctioned heritage use of that hue. Never stretch, recolor, add effects, or place on a busy background.

**Canonical wordmark lockup** (shield + Hanken Grotesk Light wordmark + "MD" in a Brand Red chip). Reference: `logos/nightingalemd-lockup.html`. Set one knob — `font-size` on `.nm-lockup` — and it scales; spacing is locked (wordmark clears the shield):
```css
.nm-lockup{display:inline-flex;align-items:center;gap:.05em;line-height:1;
  font-family:'Hanken Grotesk','Helvetica Neue',sans-serif;font-size:60px}
.nm-lockup img{height:1.72em}
.nm-lockup .nm-wm{font-weight:300;letter-spacing:.005em;color:#31393F}   /* .on-dark -> #EDEFF0 */
.nm-lockup .nm-wm .md{font-weight:700;font-size:.76em;background:#E45740;color:#fff;
  border-radius:.2em;padding:.05em .24em;margin-left:.16em;vertical-align:.06em}
```
```html
<span class="nm-lockup"><img src=".../logos/nightingale-icon-red.svg" alt="NightingaleMD"><span class="nm-wm">Nightingale<span class="md">MD</span></span></span>
```

---

## COLORS — canonical palette

**Primary / structure**
- Brand Teal `#55B5B8` — signature color: large headers, trusted states, primary data series
- Deep Teal `#3E8E91` — accessible text, buttons, lines, small data elements
- Ink `#222A2E` — dark covers and high-authority sections
- Neutral Dark `#49545E` — icons, axes, dividers
- Text Primary `#31393F` — body copy
- Text Secondary `#5A6872` — captions and supporting text

**Human / accent**
- Brand Coral `#F26E67` — Florence, engagement, momentum, featured callouts / CTAs
- Soft Coral `#F48B80` — member-facing highlights and secondary data
- Rose Tint `#F5A2A2` — subtle backgrounds and quote panels

**Signal**
- Deep Alert Red `#C9473D` — risks, refusals, warnings, negative outcomes ONLY
- Brand Yellow `#F8CA44` — KPI and financial emphasis, used sparingly
- Sage Green `#8FA56A` — progress and completion
- Olive Green `#6F7E43` — grounded clinical context
- Lavender Gray `#B9AEC8` — governance and secondary data

**Surfaces**
- Paper White `#FBFAF7` — default background
- Warm White `#FFFDFC` — cards and elevated surfaces
- Warm Ivory `#F8F4EC` — occasional tinted sections only
- Brand Gray Light `#F2F3F4` — tables and alternate surfaces
- Border `#DDE2E5` — card and table boundaries

**Retired:** Legacy Teal `#2BA79C`, Legacy Red `#E45740` (mark only).

---

## FONTS
- **Headlines / display:** **Fraunces** (serif), tracking `-0.015em` — H1 48–60pt, H2 40–44pt on slides
- **Body / UI / data:** **Hanken Grotesk** — body 16–20pt, captions 11–14pt
- **Eyebrows / labels / footers:** **IBM Plex Mono**, UPPERCASE, letter-spaced `0.2em`
- **Pull quotes:** **Newsreader** italic
- **Minimum size:** 10pt

```html
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400..700&family=Hanken+Grotesk:wght@300..700&family=IBM+Plex+Mono:wght@400;500;600&family=Newsreader:ital,opsz@1,6..72&display=swap" rel="stylesheet">
```

---

## LAYOUT
- 16:9 (1280×720 or 1920×1080), 64px margins, 24px gutters, 12-column grid
- Content in 2–3 columns (avoid vertical stacking)
- **Backgrounds:** Paper White `#FBFAF7` default; Ink `#222A2E` for covers/section dividers (subtle low-opacity teal/coral radial glows, never busy gradients)
- **Cards:** Warm White `#FFFDFC`, 1px `#DDE2E5` border, 16px radius, soft cool shadow `0 2px 8px rgba(31,57,73,.08)`, optional 3px colored top rule
- Footer: `© NightingaleMD 2026 | NightingaleMD.com` in Text Secondary, IBM Plex Mono
- Logo per placement rule above

---

## STYLE
- Warm, editorial, clinical-but-human — a well-made health publication, not a SaaS dashboard
- Flat surfaces + soft cool-tinted low-opacity shadows on cards (never hard/dark drops)
- Icons: Font Awesome 6 solid in Neutral Dark or on colored tiles — no emoji
- Sentence case for all headlines; mono eyebrows UPPERCASE
- Lead with real numbers, cite sources inline; state guardrails proactively
- Data labels directly on charts (no legends); one idea per slide; horizontal timelines/processes
- No gradients (except subtle radial glows on dark covers), no 3D, no stock photography

---

## THE ONE RULE
Every color must do its assigned job. **Teal = trust/structure. Coral = human warmth. Deep Alert Red = danger only. Yellow = KPI spotlight (sparingly). Sage = progress. Lavender = governance.** On-palette but wrong-role reads as off-brand.

---

## CSS variables (drop into any HTML/CSS deck)
```css
:root{
  /* structure */
  --nm-teal:#55B5B8; --nm-teal-deep:#3E8E91; --nm-ink:#222A2E; --nm-neutral:#49545E;
  --nm-text:#31393F; --nm-text-2:#5A6872;
  /* human accent */
  --nm-coral:#F26E67; --nm-coral-soft:#F48B80; --nm-rose:#F5A2A2;
  /* signal */
  --nm-alert:#C9473D; --nm-yellow:#F8CA44; --nm-sage:#8FA56A; --nm-olive:#6F7E43; --nm-lavender:#B9AEC8;
  /* surfaces */
  --nm-paper:#FBFAF7; --nm-white:#FFFDFC; --nm-ivory:#F8F4EC; --nm-gray-light:#F2F3F4; --nm-line:#DDE2E5;
  /* type */
  --font-serif:'Fraunces',Georgia,serif; --font-sans:'Hanken Grotesk','Helvetica Neue',sans-serif;
  --font-mono:'IBM Plex Mono',monospace; --font-quote:'Newsreader',Georgia,serif;
}
```
Headlines `font-family:var(--font-serif);font-weight:600;letter-spacing:-.015em` · Body `var(--font-sans)` · Eyebrows `var(--font-mono);text-transform:uppercase;letter-spacing:.2em`. Page background `var(--nm-paper)`; cards `var(--nm-white)`.
