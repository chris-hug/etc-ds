---
name: etc-human-designsystem
description: Use this skill whenever building any UI, page, component, or app for ETC Solutions. Contains the complete Human ETC Design System — all color scales, typography, spacing, components, SVG illustrations, and usage rules. Read this before writing any code.
---

# Human ETC Design System

**Version:** 1.2
**For:** ETC Solutions — all web interfaces, marketing pages, apps
**Character:** Warm, editorial, international, confident understatement. Inspired by claude.com/blog and claude.com/platform. Not startup-flashy, not German Mittelstand — a precise, human, internationally-minded tech company.

---

## 0. How to Use This File

Read this entire file before writing any code. Apply every value, rule, and component pattern exactly as specified. Do not substitute fonts, invent new colors, or deviate from spacing primitives. When in doubt, do less — restraint is the system's core principle.

---

## 1. Logo

The real ETC logo is a square navy rectangle (`#00216C`) with three white letterforms (E, T, C). Use the full SVG everywhere — in the nav at 36×36px, and in the footer at 72×72px. Never use a simplified or abbreviated mark.

### Full Logo SVG

```svg
<svg width="472" height="471" viewBox="0 0 472 471" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path d="M0 0H472V470.775L358.742 470.728H141.939H46.048L15.9651 470.74C11.5053 470.742 4.25758 470.975 0 470.617V0Z" fill="#00216C"/>
  <path d="M19.8302 276.237C39.6346 276.455 59.4404 276.512 79.2454 276.407C101.141 276.5 123.036 276.45 144.931 276.257C144.951 286.235 144.698 297.132 144.928 306.987L56.9974 307.04C56.5131 310.455 56.7511 321.437 56.7324 325.192C56.7134 329.022 56.9989 339.982 56.9989 343.497C60.4592 343.497 67.1574 343.505 71.7651 343.497H118C122.686 343.49 134.167 343.497 138.119 343.497C138.119 352 138.095 363.737 138.091 372.412L63.1871 372.48C61.1239 372.5 59.0611 372.545 56.9989 372.612C56.5791 375.532 56.6709 386.362 56.7386 390.042C56.8816 397.817 56.4354 407.175 56.8619 414.795C60.9854 415.102 65.8564 414.962 70.0734 414.957L90.4976 414.952C109.136 414.952 128.346 415.182 146.953 414.857C146.575 424.41 146.819 435.845 146.784 445.577C104.704 445.102 61.9981 445.605 19.8551 445.547C19.5009 424.86 19.8054 403.247 19.8039 382.512L19.8302 276.237Z" fill="#FEFEFE"/>
  <path d="M379.902 272.108C382.524 271.803 386.724 272.263 389.417 272.498C403.434 273.723 416.914 278.128 428.387 286.445C440.124 294.935 448.547 307.243 452.209 321.258C453.174 324.905 453.732 328.913 454.329 332.66C450.524 333.333 443.242 333.243 439.359 333.255C432.982 333.275 426.264 333.335 419.909 332.95C418.054 327.565 416.479 322.65 412.894 318.13C406.322 309.855 397.897 304.44 387.319 303.288C357.862 299.868 339.862 320.368 336.677 348.42C333.872 373.1 337.709 401.805 362.307 414.87C366.114 416.893 372.044 418.065 376.232 418.535C386.007 419.635 397.064 418.348 404.892 411.888C413.817 404.528 418.687 394.423 419.867 383.058C419.907 382.925 420.109 381.29 420.139 381.058C431.894 380.828 443.867 381.205 455.547 380.898C454.377 397.695 449.024 412.735 438.049 425.575C411.267 456.913 356.907 456.295 327.109 429.633C310.027 414.348 301.322 391.753 299.774 369.083C298.104 344.593 304.457 317.458 320.899 298.673C337.252 280.258 355.884 273.593 379.902 272.108Z" fill="#FEFEFE"/>
  <path d="M288.412 276.377L298.497 276.255L298.532 306.955C287.942 307.12 277.227 306.895 266.627 306.982C260.35 307.035 254.31 306.807 248.033 307.347C247.625 311.95 247.816 318.795 247.821 323.537L247.828 350.9C247.833 382.257 248.1 414.127 247.725 445.445C235.675 445.567 223.624 445.577 211.573 445.475C211.749 431.98 211.592 418.147 211.591 404.625L211.594 342.555C211.594 331.075 211.821 318.675 211.467 307.267C206.665 306.732 198.396 306.987 193.273 306.987L160.824 306.965C161.106 304.117 160.971 299.007 160.973 296.057L160.971 276.485C176.326 276.367 191.681 276.337 207.037 276.39L288.412 276.377Z" fill="#FEFEFE"/>
</svg>
```

### Nav usage (36×36px)

```html
<a href="#" class="logo">
  <svg class="logo-etc-svg" viewBox="0 0 472 471" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
    <!-- paste full SVG paths here -->
  </svg>
  ETC Solutions
</a>
```

```css
.logo { font-family: var(--font-ui); font-size: 15px; font-weight: 600; color: var(--text); text-decoration: none; letter-spacing: -0.02em; display: flex; align-items: center; gap: 10px; }
.logo-etc-svg { display: block; flex-shrink: 0; width: 36px; height: 36px; } /* no border-radius, no overflow:hidden */
```

### Footer usage (72×72px)

Render the same SVG at `width="72" height="72"` inside an `<a class="logo-full">` wrapper.

**Logo rules:**
- Navy `#00216C` is the logo's own color — do not replace with `--blue-500`
- Always use the full ETC SVG — no simplified, abbreviated, or geometric substitute marks
- Never add `border-radius` or `overflow: hidden` to the logo SVG wrapper
- Never stretch, recolor, or add effects to the logo SVG

---

## 2. Fonts

Always load from Google Fonts:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Google+Sans:wght@400;500;600&family=Lora:ital,wght@0,400;0,500;1,400;1,500&display=swap" rel="stylesheet">
```

### Roles

| Role | Font | Usage |
|------|------|-------|
| Editorial | **Lora** (serif) | All headlines (H1–H3), body copy, testimonial quotes, pull quotes, section titles, blog card titles |
| UI | **Google Sans** (sans-serif) | Nav links, buttons, badges, labels, overlines, stats labels, captions, footer text, body copy in UI contexts |

### Text Styles

```css
/* H1 — Hero headline */
font-family: 'Lora', serif;
font-size: clamp(42px, 5.5vw, 68px);
font-weight: 400;
line-height: 1.1;
letter-spacing: -0.022em;

/* H2 — Section title */
font-family: 'Lora', serif;
font-size: clamp(28px, 3.8vw, 44px);
font-weight: 400;
line-height: 1.2;
letter-spacing: -0.02em;

/* H3 — Card title / Feature title */
font-family: 'Lora', serif;
font-size: 19px;
font-weight: 500;
line-height: 1.25;
letter-spacing: -0.01em;

/* H4 — List title / Why item title */
font-family: 'Lora', serif;
font-size: 19px;
font-weight: 500;
letter-spacing: -0.01em;

/* Body — editorial long-form */
font-family: 'Lora', serif;
font-size: 17px;
font-weight: 400;
line-height: 1.65;

/* Body UI — descriptive copy in cards, UI contexts */
font-family: 'Google Sans', sans-serif;
font-size: 15px;
line-height: 1.65;

/* Overline */
font-family: 'Google Sans', sans-serif;
font-size: 16px;
font-weight: 500;
color: var(--orange-500); /* always orange */
/* NO uppercase, NO letter-spacing, no decoration */

/* Quote */
font-family: 'Lora', serif;
font-size: clamp(19px, 2.5vw, 27px);
font-weight: 400;
font-style: italic;
line-height: 1.55;
letter-spacing: -0.01em;

/* Label / Caption */
font-family: 'Google Sans', sans-serif;
font-size: 11px–12px;
font-weight: 400–500;
color: var(--text-light);

/* Badge */
font-family: 'Google Sans', sans-serif;
font-size: 10px;
font-weight: 500;
letter-spacing: 0.01em;

/* Nav link */
font-family: 'Google Sans', sans-serif;
font-size: 15px;
font-weight: 400;
color: var(--text-mid);

/* Button */
font-family: 'Google Sans', sans-serif;
font-size: 15px; /* lg: 16px; sm: 13px */
font-weight: 500;
letter-spacing: -0.01em;

/* Link — feature-link, blog-link, link-arrow, inline */
font-family: 'Google Sans', sans-serif;
font-size: 14px; /* blog-link and feature-link: 14px; link-arrow: 15px */
font-weight: 400; /* ALWAYS regular — never 500 or 600 */
color: var(--blue-500);
text-decoration: none;
```

### Rules
- Headlines: **400 or 500 weight only** — never bold. Size creates hierarchy, not weight.
- Use italic (`<em>`) in hero headlines for one key phrase — never underline or color.
- Overlines are **never uppercase**, no extra letter-spacing.
- Body copy in editorial sections: Lora. Body copy in UI components: Google Sans.
- **Links are always regular weight (400), always `--blue-500`, no underline by default.**

---

## 3. Color System

### Full CSS Custom Properties (paste into `:root`)

```css
:root {
  /* ── BLUE SCALE ── */
  --blue-50:  #EEF2FF;
  --blue-100: #D8E2FC;
  --blue-200: #B4C6F8;
  --blue-300: #7EA3F2;
  --blue-400: #4D7AEB;
  --blue-500: #1F3FD8; /* PRIMARY BRAND BLUE */
  --blue-600: #1933B8;
  --blue-700: #142898;
  --blue-800: #0F1E78;
  --blue-900: #0A1558;
  --blue-950: #060D38;

  /* ── NAVY SCALE (brand dark blue #00216C) ── */
  --navy-50:  #E8EDF8;
  --navy-100: #C8D4EE;
  --navy-200: #A0B4E2;
  --navy-300: #7090D2;
  --navy-400: #4470C0;
  --navy-500: #1C50A8;
  --navy-600: #163E8C;
  --navy-700: #102E72;
  --navy-800: #00216C; /* BRAND NAVY — use ultra-sparingly */
  --navy-900: #001550;
  --navy-950: #000C34;

  /* ── ORANGE SCALE ── */
  --orange-50:  #FEF4EE;
  --orange-100: #FCE4D0;
  --orange-200: #F8C8A0;
  --orange-300: #F4A870;
  --orange-400: #EF8448;
  --orange-500: #E8592A; /* PRIMARY DECORATIVE ORANGE */
  --orange-600: #CC4418;
  --orange-700: #A83410;
  --orange-800: #82260C;
  --orange-900: #5C1A08;
  --orange-950: #360F04;

  /* ── SAGE SCALE ── */
  --sage-50:  #F4F8F2;
  --sage-100: #E4F0DE;
  --sage-200: #C8E0BC;
  --sage-300: #A8CC98;
  --sage-400: #88B474;
  --sage-500: #6A9854;
  --sage-600: #527A40;
  --sage-700: #3C5E2E;
  --sage-800: #28421E;
  --sage-900: #182810;
  --sage-950: #0C1608;

  /* ── ROSE SCALE ── */
  --rose-50:  #FDF4F2;
  --rose-100: #FAE4DE;
  --rose-200: #F4C8BC;
  --rose-300: #ECA898;
  --rose-400: #E08474;
  --rose-500: #D06254;
  --rose-600: #B44840;
  --rose-700: #90322C;
  --rose-800: #6C2018;
  --rose-900: #481008;
  --rose-950: #280804;

  /* ── SLATE SCALE ── */
  --slate-50:  #F2F5FA;
  --slate-100: #E0E8F4;
  --slate-200: #C4D4EC;
  --slate-300: #A0BCE0;
  --slate-400: #7CA0D0;
  --slate-500: #5C84BC;
  --slate-600: #4468A0;
  --slate-700: #304E80;
  --slate-800: #203860;
  --slate-900: #122440;
  --slate-950: #081428;

  /* ── BERRY SCALE (editorial/blog only) ── */
  --berry-50:  #F5EEF9;
  --berry-100: #E8D4F2;
  --berry-200: #D0A8E4;
  --berry-300: #B478D0;
  --berry-400: #9450B8;
  --berry-500: #72329A;
  --berry-600: #582480;
  --berry-700: #3D1152; /* PRIMARY BERRY */
  --berry-800: #2C0C3C;
  --berry-900: #1C0828;
  --berry-950: #0E0414;
  --berry: var(--berry-700);

  /* ── NEUTRAL SCALE (warm, slightly beige-tinted) ── */
  --neutral-0:   #FFFFFF;
  --neutral-50:  #FAFAF7;
  --neutral-100: #F4F3EE;
  --neutral-200: #EDEAE4;
  --neutral-300: #E2DED6;
  --neutral-400: #D0CBC2;
  --neutral-500: #B8B2A8;
  --neutral-600: #96908A;
  --neutral-700: #706A62;
  --neutral-800: #4A4640;
  --neutral-900: #2E2C27;
  --neutral-950: #1A1814;

  /* ── SEMANTIC TOKENS ── */
  --bg:           var(--neutral-50);
  --bg-card:      var(--neutral-0);
  --bg-section:   var(--neutral-100);
  --text:         var(--neutral-950);
  --text-mid:     var(--neutral-700);
  --text-light:   var(--neutral-600);
  --border:       var(--neutral-200);
  --border-light: var(--neutral-100);
  --blue:         var(--blue-500);
  --blue-hover:   var(--blue-600);
  --orange:       var(--orange-500);
}
```

### Color Usage Rules

| Color | Role | Where |
|-------|------|--------|
| `--blue-500` `#1F3FD8` | Primary brand / CTA | Buttons, logo mark bg, active nav, all links |
| `--orange-500` `#E8592A` | Decorative accent only | Overlines, stat `+` suffix, SVG accents. **Never buttons or links.** |
| `--navy-800` `#00216C` | Logo + ultra-sparse accent | Logo fill, integration icon strokes, CTA card circle. Max 2–3 per page. **Never as background.** |
| `--berry-700` `#3D1152` | Editorial special | Blog/insight cards only — max one per view |
| Sage/Rose/Slate 100 | Icon bubbles, blog card bgs | 100-level only |
| `--neutral-50` | Page background | Body bg |
| `--neutral-0` | Card surface | Feature cells, nav |

---

## 4. Spacing & Layout

```css
--section-gap: 104px;
--container:   1160px;
--r-card:      16px;
--r-btn:       10px;
--r-icon:      11px;
```

```css
.container { max-width: var(--container); margin: 0 auto; padding: 0 40px; }
@media (max-width: 600px) { .container { padding: 0 20px; } }
```

### Internal Spacing Primitives

| Where | Value |
|-------|-------|
| Icon bubble → title | 24px margin-bottom |
| Title → body | 10px margin-bottom |
| Body → badges | 14px margin-bottom |
| Badges → link | 16px margin-bottom |
| Why item padding | 22px top/bottom |
| Why icon wrap | 44×44px |
| Nav height | 64px |
| Card padding | 36px top · 30px sides · 32px bottom |

### Responsive Breakpoints

| Breakpoint | Width | Card behavior |
|------------|-------|---------------|
| Mobile | < 640px | 1 column |
| Tablet+ | ≥ 640px (`sm`) | 3 columns |
| Desktop | ≥ 960px | Full layout |

**Always use `@media (min-width: 640px)` or Tailwind `sm:` for card grid breakpoints.**

---

## 5. Icon Bubble Color Pairings

| Context | Bubble bg | Icon stroke | Orange accent |
|---------|-----------|-------------|---------------|
| ITCS / operations | `--sage-100` | `--sage-700` | Yes |
| Quality / analysis | `--rose-100` | `--rose-700` | Yes (needle) |
| Integration / tech | `--slate-100` | `--navy-800` | No |
| Why — expertise | `--sage-100` | `--sage-700` | No |
| Why — solutions | `--slate-100` | `--navy-800` | No |
| Why — technology | `--rose-100` | `--rose-700` | No |

Icon bubble: 60×60px (feature cards), 44×44px (why-items). SVG viewBox: 34×34 (feature), 20×20 (why). Stroke width: 1.0–1.8px. Max one orange accent per illustration.

---

## 6. SVG Illustrations (Reusable)

### ITCS / Bus (sage)

```svg
<svg width="34" height="34" viewBox="0 0 34 34" fill="none">
  <path d="M3.5 22Q3 11 4.5 10Q5.5 8.5 17 8Q28.5 8 29.5 10Q31 11 30.5 22Q30.5 23.5 29 24L5 24Q3.5 23.5 3.5 22Z" stroke="var(--sage-700)" stroke-width="1.55" stroke-linecap="round" stroke-linejoin="round"/>
  <path d="M3.5 17L30.5 17" stroke="var(--sage-700)" stroke-width="1.1" stroke-linecap="round"/>
  <path d="M9.5 8.5L9.5 17" stroke="var(--sage-700)" stroke-width="1.0" stroke-linecap="round"/>
  <path d="M17 8.5L17 17" stroke="var(--sage-700)" stroke-width="1.0" stroke-linecap="round"/>
  <path d="M24.5 8.5L24.5 17" stroke="var(--sage-700)" stroke-width="1.0" stroke-linecap="round"/>
  <circle cx="9.5" cy="27" r="2.6" stroke="var(--sage-700)" stroke-width="1.45" fill="none"/>
  <circle cx="24.5" cy="27" r="2.6" stroke="var(--sage-700)" stroke-width="1.45" fill="none"/>
  <circle cx="28" cy="4.5" r="1.3" fill="var(--orange-500)" opacity="0.9"/>
  <path d="M25.5 4.5Q25.5 2.2 28 2.2Q30.5 2.2 30.5 4.5" stroke="var(--orange-500)" stroke-width="1.1" stroke-linecap="round" fill="none" opacity="0.6"/>
  <path d="M23.5 4.5Q23.5 0.2 28 0.2Q32.5 0.2 32.5 4.5" stroke="var(--orange-500)" stroke-width="0.9" stroke-linecap="round" fill="none" opacity="0.35"/>
</svg>
```

### Gauge / Quality (rose)

```svg
<svg width="34" height="34" viewBox="0 0 34 34" fill="none">
  <path d="M4 20Q4 7 17 7Q30 7 30 20" stroke="var(--rose-700)" stroke-width="1.55" stroke-linecap="round" fill="none"/>
  <path d="M4 20L6 20" stroke="var(--rose-700)" stroke-width="1.55" stroke-linecap="round"/>
  <path d="M28 20L30 20" stroke="var(--rose-700)" stroke-width="1.55" stroke-linecap="round"/>
  <path d="M17 7L17 9" stroke="var(--rose-700)" stroke-width="1.55" stroke-linecap="round"/>
  <path d="M9.5 10.5L10.7 11.7" stroke="var(--rose-700)" stroke-width="1.3" stroke-linecap="round"/>
  <path d="M24.5 10.5L23.3 11.7" stroke="var(--rose-700)" stroke-width="1.3" stroke-linecap="round"/>
  <path d="M17 20L25 11" stroke="var(--orange-500)" stroke-width="1.8" stroke-linecap="round"/>
  <circle cx="17" cy="20" r="2.5" fill="var(--rose-700)"/>
  <path d="M10 28L14.5 33L27 22" stroke="var(--rose-700)" stroke-width="1.7" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
```

### Circuit / Integration (slate, navy)

```svg
<svg width="34" height="34" viewBox="0 0 34 34" fill="none">
  <rect x="1.5" y="12" width="10" height="10" rx="2.2" stroke="var(--navy-800)" stroke-width="1.55" fill="none"/>
  <rect x="22.5" y="12" width="10" height="10" rx="2.2" stroke="var(--navy-800)" stroke-width="1.55" fill="none"/>
  <path d="M11.5 17L22.5 17" stroke="var(--navy-800)" stroke-width="1.55" stroke-linecap="round" stroke-dasharray="2.5 2"/>
  <circle cx="17" cy="17" r="1.8" fill="var(--navy-800)" opacity="0.45"/>
  <path d="M6.5 12L6.5 6L17 6" stroke="var(--navy-800)" stroke-width="1.05" stroke-linecap="round" stroke-linejoin="round"/>
  <path d="M27.5 12L27.5 6L17 6" stroke="var(--navy-800)" stroke-width="1.05" stroke-linecap="round" stroke-linejoin="round"/>
  <path d="M6.5 22L6.5 28L17 28" stroke="var(--navy-800)" stroke-width="1.05" stroke-linecap="round" stroke-linejoin="round"/>
  <path d="M27.5 22L27.5 28L17 28" stroke="var(--navy-800)" stroke-width="1.05" stroke-linecap="round" stroke-linejoin="round"/>
  <circle cx="17" cy="6" r="1.7" fill="var(--navy-800)"/>
  <circle cx="17" cy="28" r="1.7" fill="var(--navy-800)"/>
</svg>
```

---

## 7. Badge Vocabulary

Do not invent new labels without reason.

| Category | Approved labels |
|----------|----------------|
| Operations | Betrieb, Echtzeit, Fahrgastinfo, Leitstelle |
| Quality | Qualität, Analyse, Monitoring, KPI |
| Integration | Integration, Planung, Infrastruktur, Schnittstellen |
| Editorial | Fallstudie, Technologie, Perspektive, Insight |

```css
.feature-badge {
  font-family: var(--font-ui); font-size: 10px; font-weight: 500;
  color: var(--neutral-700);
  background: var(--neutral-100);
  border: 1px solid var(--neutral-300);
  border-radius: 20px; padding: 3px 9px;
  letter-spacing: 0.01em; white-space: nowrap;
}
```

---

## 8. Components

### 8.1 Navigation

```css
nav { position: sticky; top: 0; z-index: 100; background: rgba(250,250,247,0.88); backdrop-filter: blur(18px); border-bottom: 1px solid var(--border-light); }
.nav-inner { display: flex; align-items: center; justify-content: space-between; height: 64px; }
.logo { font-family: var(--font-ui); font-size: 15px; font-weight: 600; color: var(--text); text-decoration: none; letter-spacing: -0.02em; display: flex; align-items: center; gap: 10px; }
.logo-etc-svg { display: block; flex-shrink: 0; width: 36px; height: 36px; } /* full ETC SVG — no border-radius */
.nav-links { display: flex; align-items: center; gap: 28px; list-style: none; }
.nav-links a { font-family: var(--font-ui); font-size: 15px; font-weight: 400; color: var(--text-mid); text-decoration: none; transition: color 0.15s; }
.nav-links a:hover { color: var(--text); }
```

### 8.2 Buttons

```css
.btn { font-family: var(--font-ui); font-size: 15px; font-weight: 500; padding: 10px 20px; border-radius: var(--r-btn); cursor: pointer; text-decoration: none; transition: all 0.18s ease; display: inline-flex; align-items: center; gap: 8px; border: none; letter-spacing: -0.01em; white-space: nowrap; }
.btn.sm { font-size: 13px; padding: 7px 14px; border-radius: 8px; gap: 6px; } /* for nav — stays within 64px bar */
.btn.lg { font-size: 16px; padding: 13px 26px; border-radius: 12px; }
.btn-primary { background: var(--blue); color: white; }
.btn-primary:hover { background: var(--blue-hover); transform: translateY(-1px); } /* no box-shadow */
.btn-secondary { background: var(--bg-card); color: var(--text); border: 1px solid var(--border); box-shadow: 0 1px 3px rgba(0,0,0,0.05); }
.btn-secondary:hover { background: var(--bg-section); transform: translateY(-1px); box-shadow: 0 4px 12px rgba(0,0,0,0.07); }
.btn-white { background: white; color: var(--blue); font-weight: 600; }
.btn-white:hover { background: rgba(255,255,255,0.92); transform: translateY(-1px); box-shadow: 0 6px 20px rgba(0,0,0,0.12); }
.btn-ghost-white { background: transparent; color: white; border: 1.5px solid rgba(255,255,255,0.38); }
.btn-ghost-white:hover { background: rgba(255,255,255,0.1); border-color: rgba(255,255,255,0.65); }
```

### 8.3 Links

**All links: weight 400, color `--blue-500`, no underline. Use inline SVG arrows — no external icon libraries.**

```css
.feature-link { font-family: var(--font-ui); font-size: 14px; font-weight: 400; color: var(--blue); text-decoration: none; display: inline-flex; align-items: center; gap: 6px; transition: gap 0.15s; }
.feature-link:hover { gap: 9px; }

.link-arrow { font-family: var(--font-ui); font-size: 15px; font-weight: 400; color: var(--text-mid); text-decoration: none; display: inline-flex; align-items: center; gap: 6px; transition: color 0.15s; }
.link-arrow:hover { color: var(--text); }

.blog-link { font-family: var(--font-ui); font-size: 14px; font-weight: 400; color: var(--text-mid); text-decoration: none; display: inline-flex; align-items: center; gap: 5px; transition: color 0.15s; }
.blog-link:hover { color: var(--text); }

/* Arrow icon micro-animation — apply to all inline SVG arrows */
.arrow-icon { display: inline-flex; align-items: center; justify-content: center; flex-shrink: 0; transition: transform 0.18s ease; }
.feature-link:hover .arrow-icon,
.link-arrow:hover .arrow-icon,
.blog-link:hover .arrow-icon { transform: translateX(4px); }
```

**Arrow SVG to use** (inline, no CDN dependency):
```html
<span class="arrow-icon">
  <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
    <path d="M5 12h14"/><path d="m12 5 7 7-7 7"/>
  </svg>
</span>
```

### 8.4 Overline

```css
.overline { font-family: var(--font-ui); font-size: 16px; font-weight: 500; color: var(--orange); margin-bottom: 12px; display: block; }
```

### 8.5 Feature Cards

```css
.features-grid { display: grid; grid-template-columns: 1fr; gap: 1px; background: var(--border); border: 1px solid var(--border); border-radius: var(--r-card); overflow: hidden; }
@media (min-width: 640px) { .features-grid { grid-template-columns: repeat(3, 1fr); } }
.feature-cell { background: var(--bg-card); padding: 36px 30px 32px; display: flex; flex-direction: column; transition: background 0.15s, transform 0.18s; }
.feature-cell:hover { background: #F9F8F4; transform: translateY(-2px); } /* midpoint between --neutral-0 and --neutral-100; lighter than page bg */
.icon-bubble { width: 60px; height: 60px; border-radius: var(--r-icon); display: flex; align-items: center; justify-content: center; flex-shrink: 0; margin-bottom: 24px; }
.feature-title { font-family: var(--font-editorial); font-size: 19px; font-weight: 500; color: var(--text); line-height: 1.25; letter-spacing: -0.01em; margin-bottom: 10px; }
.feature-body { font-family: var(--font-ui); font-size: 15px; line-height: 1.65; color: var(--text-mid); flex: 1; margin-bottom: 14px; }
.feature-badges { display: flex; flex-wrap: wrap; gap: 5px; margin-top: auto; margin-bottom: 16px; }
```

### 8.6 Why / Feature List

```css
.why { padding: var(--section-gap) 0; border-top: 1px solid var(--border-light); }
.why-grid { display: grid; grid-template-columns: 5fr 7fr; gap: 72px; align-items: start; }
@media (max-width: 960px) { .why-grid { grid-template-columns: 1fr; gap: 48px; } }
.why-left p { font-family: var(--font-ui); font-size: 17px; color: var(--text-mid); line-height: 1.75; }
.why-items { display: flex; flex-direction: column; }
.why-item { display: grid; grid-template-columns: 44px 1fr; gap: 18px; align-items: start; padding: 22px 0; border-bottom: 1px solid var(--border-light); }
.why-item:first-child { border-top: 1px solid var(--border-light); }
.why-icon-wrap { width: 44px; height: 44px; border-radius: 10px; display: flex; align-items: center; justify-content: center; flex-shrink: 0; }
.why-item-title { font-family: var(--font-editorial); font-size: 19px; font-weight: 500; color: var(--text); margin-bottom: 4px; letter-spacing: -0.01em; }
.why-item-body { font-family: var(--font-ui); font-size: 15px; color: var(--text-mid); line-height: 1.65; }
```

### 8.7 Blog / Insight Cards

Allowed backgrounds: `--slate-100`, `--rose-100`, `--sage-100`, `--neutral-100`, `--berry-700` (max one, add class `dark`).

```css
.blog-grid { display: grid; grid-template-columns: 1fr; gap: 12px; }
@media (min-width: 640px) { .blog-grid { grid-template-columns: repeat(3, 1fr); } }
.blog-card { border-radius: var(--r-card); padding: 28px 26px; display: flex; flex-direction: column; transition: transform 0.18s; }
.blog-card:hover { transform: translateY(-3px); }
.blog-illus { margin-bottom: 24px; }
.blog-meta { font-family: var(--font-ui); font-size: 12px; color: var(--text-mid); margin-bottom: 8px; }
.blog-title { font-family: var(--font-editorial); font-size: 19px; font-weight: 400; line-height: 1.4; color: var(--text); letter-spacing: -0.01em; flex: 1; margin-bottom: 18px; }
.blog-card.dark .blog-title { color: rgba(255,255,255,0.9); }
.blog-card.dark .blog-meta { color: rgba(255,255,255,0.5); }
.blog-card.dark .blog-link { color: rgba(255,255,255,0.6); }
.blog-card.dark .blog-link:hover { color: white; }
```

### 8.8 Testimonial

No background color — floats on `--bg`.

```css
.testimonial { padding: var(--section-gap) 0; border-top: 1px solid var(--border-light); text-align: center; }
.quote-mark { font-family: var(--font-editorial); font-size: 88px; line-height: 0.75; color: var(--orange); opacity: 0.25; margin-bottom: 14px; display: block; }
.quote-text { font-family: var(--font-editorial); font-size: clamp(24px, 3.2vw, 36px); font-weight: 400; font-style: italic; line-height: 1.5; color: var(--text); max-width: 760px; margin: 0 auto 32px; letter-spacing: -0.015em; }
.author-avatar { width: 38px; height: 38px; border-radius: 50%; background: var(--slate-100); border: 1px solid var(--border); display: flex; align-items: center; justify-content: center; font-family: var(--font-ui); font-size: 12px; font-weight: 600; color: var(--blue); margin: 0 auto 8px; }
.author-name { font-family: var(--font-ui); font-size: 15px; font-weight: 600; color: var(--text); display: block; }
.author-role { font-family: var(--font-ui); font-size: 13px; color: var(--text-light); display: block; margin-top: 2px; }
```

### 8.9 CTA Card

Never full-bleed. Always a rounded blue card inside `--bg`. Navy circle is one approved decorative use of `--navy-800`.

```css
.cta-wrap { padding: var(--section-gap) 0 0; }
.cta-card { background: var(--blue); border-radius: 20px; padding: 72px 56px; text-align: center; position: relative; overflow: hidden; }
.cta-card::before { content: ''; position: absolute; top: -100px; right: -100px; width: 320px; height: 320px; border-radius: 50%; background: var(--navy-800); opacity: 0.2; pointer-events: none; }
.cta-card h2 { font-family: var(--font-editorial); font-size: clamp(30px, 4.5vw, 50px); font-weight: 400; color: white; letter-spacing: -0.025em; line-height: 1.12; margin-bottom: 16px; position: relative; }
.cta-card p { font-family: var(--font-ui); font-size: 16px; color: rgba(255,255,255,0.7); margin-bottom: 36px; max-width: 420px; margin-left: auto; margin-right: auto; line-height: 1.65; position: relative; }
.cta-buttons { display: flex; justify-content: center; gap: 12px; flex-wrap: wrap; position: relative; }
@media (max-width: 600px) { .cta-card { padding: 48px 24px; border-radius: 16px; } .cta-card::before { display: none; } }
```

### 8.10 Footer

Same background as page. Only a border-top. Never dark.

```css
footer { background: var(--bg); padding: 56px 0 32px; border-top: 1px solid var(--border-light); margin-top: var(--section-gap); }
.footer-top { display: grid; grid-template-columns: 1.6fr 1fr 1fr 1fr; gap: 48px; padding-bottom: 40px; border-bottom: 1px solid var(--border-light); }
@media (max-width: 960px) { .footer-top { grid-template-columns: 1fr 1fr; gap: 32px; } }
@media (max-width: 600px) { .footer-top { grid-template-columns: 1fr; } }
.footer-col h4 { font-family: var(--font-ui); font-size: 12px; font-weight: 500; color: var(--text); margin-bottom: 12px; }
.footer-col ul { list-style: none; display: flex; flex-direction: column; gap: 8px; }
.footer-col a { font-family: var(--font-ui); font-size: 13px; font-weight: 400; color: var(--text-mid); text-decoration: none; transition: color 0.15s; }
.footer-col a:hover { color: var(--text); }
.footer-bottom { display: flex; justify-content: space-between; align-items: center; padding-top: 24px; }
.footer-bottom p { font-family: var(--font-ui); font-size: 12px; color: var(--text-light); }
```

### 8.11 Hero Stats

Google Sans numbers (intentionally breaks the serif headline rhythm). No animation.

```css
.hero-stats { display: flex; align-items: center; justify-content: center; gap: 48px; flex-wrap: wrap; padding-top: 40px; border-top: 1px solid var(--border-light); }
.hero-stat { display: flex; align-items: baseline; gap: 10px; }
.hero-stat-number { font-family: var(--font-ui); font-size: 32px; font-weight: 400; color: var(--text); letter-spacing: -0.03em; line-height: 1; }
.hero-stat-number .suffix { color: var(--orange); }
.hero-stat-label { font-family: var(--font-ui); font-size: 15px; color: var(--text-light); }
.hero-stat-divider { width: 1px; height: 24px; background: var(--border); }
@media (max-width: 960px) { .hero-stats { gap: 32px; } .hero-stat-divider { display: none; } }
```

**KPI countup:** Numbers animate from 0 on page load (350ms delay, 1600ms cubic ease-out). Use `data-target` attribute and capture `performance.now()` *before* the first `requestAnimationFrame` call — not inside it.

```js
(function () {
  var els = document.querySelectorAll('.countup');
  if (!els.length) return;
  function easeOut(t) { return 1 - Math.pow(1 - t, 3); }
  var DURATION = 1600;
  function animateCount(el) {
    var target = parseInt(el.getAttribute('data-target'), 10);
    el.textContent = '0';
    var startTime = performance.now();
    function step(ts) {
      var p = Math.min((ts - startTime) / DURATION, 1);
      el.textContent = Math.round(easeOut(p) * target);
      if (p < 1) requestAnimationFrame(step);
      else el.textContent = target;
    }
    requestAnimationFrame(step);
  }
  setTimeout(function () {
    els.forEach(function (el) { animateCount(el); });
  }, 350);
})();
```

---

## 9. Animation Spec

| Element | Animation |
|---------|-----------|
| Feature cards | `background: #F9F8F4` + `transform: translateY(-2px)` on hover |
| Blog cards | `transform: translateY(-3px)` on hover |
| Buttons | `transform: translateY(-1px)` on hover — **no box-shadow on btn-primary** |
| Arrow icons (all links) | `transform: translateX(4px)` on parent hover, `transition: transform 0.18s ease` |
| Feature link gap | `6px` → `9px` on hover, `transition: gap 0.15s` |
| Colors / borders | `transition: color 0.15s` or `transition: background 0.15s` |
| Buttons (all) | `transition: all 0.18s ease` |
| KPI numbers | Count up from 0 on page load, 350ms delay, 1600ms cubic ease-out |

No scroll animations, entrance animations, or parallax.

---

## 10. Design Principles (The Don'ts)

| ❌ Never | ✓ Instead |
|----------|-----------|
| Uppercase overlines | Lowercase, Google Sans 500 |
| Bold headlines (700+) | Regular/Medium — size creates hierarchy |
| Full-bleed colored section blocks | Border separation, same bg with 1-step tint |
| Dark footer | Same `--bg` as page, only a top border |
| Orange on buttons or links | Orange: overlines, stat suffixes, illustration accents only |
| Navy as a background or button | Navy: logo, icons, CTA card circle only |
| Berry outside blog/insight cards | Editorial only, max one per view |
| Multiple color blocks in sequence | Max one colored transition at a time |
| Box-shadows on cards | Border + background contrast only |
| Box-shadow on btn-primary hover | Only `translateY(-1px)` — the lift is enough |
| Feature card hover same as page bg | Use `#F9F8F4` — midpoint between card white and page bg |
| Simplified or abbreviated logo mark | Always use the full ETC SVG, even at small sizes |
| border-radius or overflow:hidden on logo | The SVG is already a square — render it as-is |
| External icon CDNs for arrows | Use inline SVGs — no Lucide, no FontAwesome |
| Gradient backgrounds | Flat color only |
| More than 2 typefaces | Lora + Google Sans only |
| Versalsatz / ALL CAPS | Always sentence case |
| Semibold or medium weight links | Links always font-weight: 400 |
| Underlined links | No underline by default |

---

## 11. Quick-Start HTML Shell

```html
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ETC Solutions</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Google+Sans:wght@400;500;600&family=Lora:ital,wght@0,400;0,500;1,400;1,500&display=swap" rel="stylesheet">
<style>
  /* 1. Paste full :root from Section 3 */
  /* 2. Add reset, body, container */
  /* 3. Add component styles from Section 8 as needed */
</style>
</head>
<body>
<!-- NAV -->
<!-- HERO -->
<!-- [PAGE SECTIONS] -->
<!-- CTA CARD -->
<!-- FOOTER -->
</body>
</html>
```

---

## 12. Version History

| Version | Changes |
|---------|---------|
| 1.0 | Initial system — colors, typography, all components |
| 1.1 | Added full logo SVG + nav mark, berry scale (50–950), icon bubble pairings table, all 3 SVG illustrations as reusable code, badge vocabulary, animation spec, internal spacing primitives, responsive breakpoints table, link weight corrected to 400 throughout all components |
| 1.2 | Full logo SVG used everywhere (nav 36×36px, footer 72×72px) — abbreviated mark retired. No border-radius on logo. Overline 12px→16px. Body UI 14px→15px. H4/why-item-title 17px→19px. Nav links 14px→15px. Buttons: base 14px→15px, lg 15px→16px, new `.btn.sm` 13px for nav. btn-primary hover: box-shadow removed, lift only. Feature card hover: `#F9F8F4` + `translateY(-2px)` instead of neutral-50. All card links (feature-link, blog-link) unified at 14px. link-arrow 15px. Arrow icons: inline SVG with `translateX(4px)` animation — no external CDN. KPI countup animation added (350ms delay, 1600ms cubic ease-out). Hero stat number 28px→32px, label 13px→15px. Testimonial quote larger: `clamp(24px, 3.2vw, 36px)`. Author name 13px→15px. |

*Human ETC Design System — March 2026. Read fully before writing any code.*
