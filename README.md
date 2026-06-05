# ETC Design System

A living showcase of the ETC Solutions design system — typography tokens with fluid sizing, and the core components built from them. Every element references one shared token set (derived from the Figma "Flowbite-ETC" core file).

## Pages

- **[index.html](index.html)** — the full design-system showcase (everything on one page)
- **[etc-text-styles.html](etc-text-styles.html)** — typography overview (editorial styles + full type scale)
- **[etc-cards.html](etc-cards.html)** — card component variants
- **[etc-badges.html](etc-badges.html)** — badge component
- **[etc-content-block.html](etc-content-block.html)** — responsive content block

## Contents

- **Foundations** — typography: Lora (serif) for headings & Quote, Google Sans for everything else; size scale `xxs (11) → 9xl (128)` with fluid sizing on `≥ 2xl`.
- **Components** — Button (Primary / Secondary / Ghost, all sizes + hover/disabled states), Badge (neutral, with/without icon), Card (8 variants), Content Block (responsive).

## Tokens

All colours, spacing, radii, and type values live as CSS custom properties in a single `:root`. Components reference only semantic tokens — no hardcoded values.

## Run locally

```bash
python3 -m http.server 4321
# then open http://localhost:4321/
```
