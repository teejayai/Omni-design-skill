---
name: omni-design-system
description: Shared OmniONE Retail design system — exact tokens (Gordita type scale, full color ramps, semantic tokens), global rules, and components used across all products (DOS, MOS, AGENT, ROS, OMNIPAY). Reference this base before any product skill.
---

# OmniONE — Design System (Base)

Shared system for all Omni Retail products. Every product skill extends this base and **never deviates**. Use only the names/values below — never invent values. Machine-readable mirror: [`tokens.json`](./tokens.json).

Source: Figma `OmniONE Design system` (`RNBrFtlAUysqguEEm4AzyY`).

## Typography

- **Font: `Gordita`** everywhere. Weights: Regular 400 · Medium 500 · Bold 700 · Black 900 (every style has all four). Light 300 + italics also ship.
- Designed to a **4px grid**. Letter-spacing values are percentages (px = size × pct).

### Font files (self-hosted)
Brand `.otf` files live in [`fonts/`](./fonts/); `@font-face` declarations in [`fonts/gordita.css`](./fonts/gordita.css). Import once at the app root: `@import "./fonts/gordita.css";` (or `<link>`), then use `font-family: "Gordita"`.

| File | weight | style |
|---|---|---|
| Gordita-Light.otf / -LightItalic.otf | 300 | normal / italic |
| Gordita-Regular.otf / -RegularItalic.otf | 400 | normal / italic |
| Gordita-Medium.otf / -MediumItalic.otf | 500 | normal / italic |
| Gordita-Bold.otf / -BoldItalic.otf | 700 | normal / italic |
| Gordita-Black.otf / -BlackItalic.otf | 900 | normal / italic |

### Web type scale (exact)
| Style | Size | Line height | Tracking |
|---|---|---|---|
| H1 - 48 | 48 | 56 (Regular) / 48 (M,B,Bk) | 0% |
| H2 - 36 | 36 | 44 (48 Black) | -3% |
| H3 - 32 | 32 | 40 | -3% |
| H4 - 28 | 28 | 36 | -2% (M,B) / 0% (R,Bk) |
| H5 - 24 | 24 | 28 | -2% (0% Regular) |
| H6 - 20 | 20 | 24 | -2% (0% Regular) |
| Body Large - 18 | 18 | 28 | 0% |
| Body Medium - 16 | 16 | 24 (R) / auto | 0% |
| Body Small - 14 | 14 | 20 | 0% |
| Body XSmall - 12 | 12 | 18 | 0% |
| Caption - 12 | 12 | auto | 0% |
| Label - 10 | 10 | 18 | 0% |

Mobile scale (`Body Medium-14`, `Body Small-12`, + heading mirror) — names known, exact values pending.

## Icons

- **1,176 SVG icons** in [`icons/`](./icons/), grouped into 19 category folders. Index + full name list: [`icons/icons.json`](./icons/icons.json).
- Each icon is **24×24, `viewBox="0 0 24 24"`**, line/path-based. Recolor with `fill`/`stroke` — set `currentColor` so icons inherit text color. Size via `width`/`height` (use the 4px grid: 16/20/24).
- File path: `icons/<category>/<icon-name>.svg` (kebab-case). e.g. `icons/general/home-01.svg`, `icons/arrows/arrow-right.svg`.

| Category | # | Category | # | Category | # |
|---|--|---|--|---|--|
| general | 197 | media-and-devices | 108 | editor | 104 |
| arrows | 92 | finance-and-ecommerce | 78 | layout | 63 |
| communication | 58 | files | 58 | development | 57 |
| weather | 52 | charts | 49 | maps-and-travels | 43 |
| users | 42 | security | 36 | education | 31 |
| images | 29 | time | 28 | alerts-and-feedback | 26 |
| shapes | 25 | | | | |

Use only these icons — don't invent or pull from other sets. Country flags + file-type chips were excluded.

## Color

### Primitive ramps (25→900, `400 (Base)` is the anchor)
**Primary 1 — Dark Cornflower Blue** (brand): 25 #F6F7FA · 50 #DCE2ED · 75 #C5CFE1 · 100 #A2B2CF · 200 #94BFE9 · 300 #2E5193 · **400 #173E87** · 500 #0E2856 · 600 #0F2858 · 700 #0B1F43 · 800 #071329 · 900 #030914

**Primary 2 — Steel Gray**: 25 #F8F8F9 · 50 #E4E5E8 · 75 #DBDDE0 · 100 #C0C3C8 · 200 #9CA1A9 · 300 #666E7A · **400 #4B5563** · 500 #404854 · 600 #343C45 · 700 #252A31 · 800 #161A1E

**Secondary 1 — Teal**: 25 #F6FDFB … 200 #63D9B6 · 300 #36CEA1 · **400 #20C997** · 500 #1AA179 · 600 #158362 · 700 #10654B · 800 #0A3C2D · 900 #051E17

**Secondary 2 — Light Blue**: 25 #F9FBFE … 200 #94BFE9 · 300 #75ACE3 · **400 #66A3E0** · 500 #5282B3 · 600 #426A92 · 700 #335170 · 800 #1F3143 · 900 #0F1822

**Accent 1 — Soft Green**: 50 #DFF2E3 · 100 #C9E9D1 · 200 #68C17D · 300 #3EB058 · **400 #28A745** · 500 #208637 · … · 900 #06190A

**Accent 2 — Amber**: 50 #FFF6DA · 100 #FFE69C · 200 #FFD451 · 300 #FFC720 · **400 #FFC107** · 500 #CC9A06 · … · 900 #261D01

**Accent 3 — Soft Red**: 50 #FAE1E3 · 100 #F1AEB5 · 200 #E7727D · 300 #E04958 · **400 #DC3545** · 500 #B02A37 · … · 900 #21080A

**Neutral / Grey**: 25 #F8F9FA · 50 #F0F0F1 · 100 #F0F2F5 · 200 #D9D9D9 · 300 #CCCCCC · 400 #B3B3B3 · 500 #667185/#999999 · 700 #344054 · 900 #101928 · Black #010611 · White #FFFFFF

### Semantic tokens (use these in UI, not raw primitives)
- **Surface**: bg #F0F0F1 · bg-alt #FFFFFF · card-bg #FFFFFF · card-alt-bg #F8F9FA
- **Border**: Thick #B3B3B3 · bold #CCCCCC · mid #E5E5E5 · light #F0F0F1
- **Text**: default #101928 · subtitle #344054 · focused #333333 · subdued #999999 · disabled #D9D9D9
- **Icon**: focused #808080 · disabled #D9D9D9
- **Button**: primary #173E87 · hover #5D78AB · disabled #C5CFE1 · text #FFFFFF · *alt* primary #4B5563 / hover #9CA1A9 / disabled #DBDDE0
- **Brand**: primary #173E87 · hover #0B1F43 · secondary #20C997 · success #28A745 · alert #FFC107 · error #DC3545 · grey #D9D9D9

> A secondary brand palette also exists (`Primary - main #034DB1` / `Secondary - main #FFC120`, steps 01–06). See `tokens.json` → `alt_brand_palette`. Default to the Brand/Button semantic tokens above unless a product specifies otherwise.

## Layout

- **Radius**: control 4px · card/modal 8px · pill 30px
- **Spacing**: 4px grid — 4 · 8 · 12 · 16 · 20 · 24 · 32 …
- **Button heights**: sm 32 · md 36 · lg 44 · xl/2xl 48 · **Icon** 24×24
- **Effects**: see Shadows below.

### Shadows (exact — same scale web + mobile)
Untitled-UI elevation scale, base color `#101828`. Use for overlays/raised surfaces; default to borders for flat separation.

| Token | box-shadow |
|---|---|
| `xs` | `0px 1px 2px 0px rgba(16,24,40,0.05)` |
| `sm` | `0px 1px 2px 0px rgba(16,24,40,0.06), 0px 1px 3px 0px rgba(16,24,40,0.10)` |
| `md` | `0px 2px 4px -2px rgba(16,24,40,0.06), 0px 4px 8px -2px rgba(16,24,40,0.10)` |
| `lg` | `0px 4px 6px -2px rgba(16,24,40,0.03), 0px 12px 16px -4px rgba(16,24,40,0.08)` |
| `xl` | `0px 8px 8px -4px rgba(16,24,40,0.03), 0px 20px 24px -4px rgba(16,24,40,0.08)` |
| `2xl` | `0px 24px 48px -12px rgba(16,24,40,0.18)` |
| `3xl` | `0px 32px 64px -12px rgba(16,24,40,0.14)` |

Guidance: `xs/sm` inputs & cards · `md/lg` dropdowns & popovers · `xl/2xl` modals & toasts · `3xl` full-screen overlays.

## Components

**Button** — Types: Primary · Secondary gray · Secondary colour · Tertiary gray · Tertiary colour. Sizes sm/md/lg/xl/2xl/Long. States Default/Hover/Focused/Disabled. Colour themes Native blue · Omnibiz Orange · Warning Yellow. Optional left/right icon (24px), gap 10. Primary = bg #173E87, text #FFFFFF, radius 4px, lg padding 10×20.

**Input row / addons** — bg #F6F6F6, padding 12, gap 8, Gordita Regular 16/24 #747474. Addons: Trailing Icon, Leading/Trailing dropdown, Flag + number, Bank Icon, Tags.

**Modal** — radius 8, bg #FFFFFF, footer top-border #ECECEC + padding 24 + gap 11 + two equal pill buttons.

**Divider** — 1px, Grey/100 #F0F2F5.

**Tag** — radius **4**, padding 10×(5–6), gap 4, **Gordita Medium**. Sizes S 12/18 · M 14/20 · L 16/24. Optional 12px leading/trailing icon (recolor to text). Types:
| Type | bg | text |
|---|---|---|
| Default | transparent, border #E4E5E8 | #4B5563 |
| Error | #FAE1E3 | #8F222D |
| Warning | #FFF6DA | #624A02 |
| Success | #DEF7EF | #0E5B43 |

**Badge / Status** — pill (radius **24**), padding 20×(5–6), **Gordita Regular**. Sizes S 12/18 · M 14/20 · L 16/24.
| Type | bg | text |
|---|---|---|
| Blue | #E8F1FA | #2C517D |
| Red | #FFF0F1 | #8F222D |
| Yellow | #FFF8E3 | #624A02 |
| Green | #DEF7EF | #0E5B43 |
| Purple | #EDE6FF | #534180 |
| Orange | #FFF2EE | #962F10 |
| Grey | #F0F0F1 | #999999 |

**Badge / Dot, Count & notification** — *Dot* 6px in 10 colors (orange/teal/blue/yellow/red/dark-grey/light-blue/green/purple/gray). *Dot-on-icon* S 18 · M 20 · L 24. *Dot-on-text* leading dot before a label. *Count* sizes S 30 · M 32 · L 36, colors red/gray, digit Single/Double (+plus); hidden at 0, caps at 9+/99+. Mobile + Desktop variants.

## Logos

In [`logos/`](./logos/): a master sheet (`omni-logos-sheet.svg` / `.png`, 4000px) **plus 18 per-logo SVGs** — 6 brands × 3 forms.

- **Forms**: `wordmark` (horizontal lockup) · `app-icon` (white mark on #173E87 rounded square) · `mark` (standalone swirl).
- **Files**: `<brand>-<form>.svg`, e.g. `omnione-wordmark.svg`, `omnipay-app-icon.svg`, `omni-mark.svg`.
- **Brands & accent**: **Omni** (brand blue) · **OmniBiz** (orange) · **OmniPay** (purple) · **OmniHub** (green) · **OmniOne** (cyan/light-blue) · **OmniRetail** (bright green). The swirl mark is shared; only the accent stroke changes per brand.
- Each product skill uses its own brand lockup. SVGs are vector windows onto the master sheet (scale freely).

## Global rules
1. Type in **Gordita** only; pick from the scale above.
2. Use semantic tokens (Brand/Button/Surface/Border/Text/Icon) for UI; reach for raw ramps only when no semantic token fits.
3. Exact hex/names only — never approximate or introduce new colors.
4. Radius by role: controls 4px, surfaces 8px, pills 30px. Spacing on the 4px grid.
5. Separate flat content with borders + radius; use the **Shadows** scale only for raised/overlay surfaces (dropdowns, modals, toasts).
6. Product skills *select among* these tokens and set component preferences — they may not redefine tokens.

## Gaps
- Mobile type-scale exact values (names captured).
- Per-brand vector (SVG) logo files — sheet captured as PNG; vector export pending a re-issued Figma token.
