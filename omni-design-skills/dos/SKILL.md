---
name: omni-dos
description: OmniONE — DOS (Distributor Operating System) design skill. Mobile operational app for distributors. Utilitarian, neutral/STEEL-GRAY-forward primary, surface #F8F9FA, bottom-nav + bottom-sheets. Extends the shared omni-design-system base.
---

# OmniONE — DOS

Mobile app (375px, native iOS frames) for distributors/store operators. Extends [omni-design-system](../base/SKILL.md). Gordita throughout (native status-bar numerals use Inter — system only).

## Voice / personality
Operational, warehouse-floor utility tool — task-first, not a marketing surface. Calm and **neutral/grey-forward** (Steel Gray dominant, blue reserved). Friendly but terse: short headers, emoji greeting ("Hi John 👋🏼"), guided multi-step onboarding. Empty states push the next action.

## Preferred components & variants
- **Buttons**: Steel-Gray fill `#4B5563`, white Gordita Medium 14, ~46px tall.
- **Bottom nav bar**: 5 segments icon+label (12px), active = `#333`, inactive = `#666`.
- **Top app bar** ("Tab / Active", 107px incl. status bar): centered Bold 16 title in Steel Gray, leading back + trailing actions (cart w/ badge).
- **Segmented tab strip**: underline, active = `border-b-2 #333` Bold, inactive Regular.
- **Pill filter chips** `rounded-[40px]`: active = `#404854` fill + white, inactive = `#D0D5DD` border + `#333`.
- **Search input**: 32px tall, r4, `#F0F0F1` border, leading search icon + trailing filter icon.
- **Bottom-sheet modal**: `rounded-t-[30px]` + drawer grab-handle.
- **Stepper**: 32px numbered circles (grey-300 border) + tail line + description.
- Tags, Quick Actions grid, banner carousel with dot indicators.

## Density & spacing
4px grid, looser than base: screen H-padding **16px**, section gaps **20px**, content gaps **12px**, chip gaps **8px**. Modal padding 24H / 10 top, internal gap 30. Tab/chip rows 52–64px tall, horizontal scroll. Touch-target driven, moderately roomy.

## Layout patterns
Per-screen vertical stack: **status bar + app bar (107px)** → sub-header (greeting / warehouse-location selector with Tag) → **filter zone** (segmented underline tabs → pill chips → search, white bands separated by 8px `surface-bg` spacers) → **scroll body** (cards / list rows or centered empty-state + CTA) → **5-tab bottom nav** pinned + iOS home indicator. Dashboard adds banner carousel + Quick Actions.

## Token usage & deviations
- **Primary action = Steel Gray `#4B5563`** (de-facto primary), active chips Steel-Gray-500 `#404854`. Brand blue `#173E87` present but **reserved/rare**.
- **Surface bg = `#F8F9FA`** (not base `#F0F0F1`).
- **Text = `#333` focused** (not base `#101928`), subdued `#999`, grey-700 `#666`.
- Radii: buttons **5px**, modal sheet **30px** top corners, alongside standard 4px.
- New border greys: `#D0D5DD` (chip outline), `#ECECEC` (input divider).
- Button text often `#FEFEFE` (Bliss White), not pure white. Accents: Teal `#20C997`, Amber `#FFC107`, Success `#28A745`.
- Type: Gordita Mobile scale — H3-24/B, H4-20/M, H6-16/B, Body 16/14/12, Caption 12, Label 10.

## Anti-patterns
- ❌ Brand-blue primary CTAs — DOS uses Steel Gray.
- ❌ Base surface `#F0F0F1` — use `#F8F9FA`.
- ❌ Default text `#101928` — DOS text is `#333`.
- ❌ Desktop/sidebar layouts — mobile-only, 375px, bottom-nav driven.
- ❌ Top-attached dialogs — modals are bottom sheets (30px top radius + handle).
- ❌ Tight 8px gutters — keep 16px H-padding / 20px section gaps.
- ❌ Pure-white button labels — prefer `#FEFEFE`.

## Example patterns
**Primary button** (`2322:170470`): `bg #4B5563`, Gordita Medium 14 `#FEFEFE`, r4–5, px-24 py-12 (~46px), full-width.

**Filter/discovery row** (`2322:174644`): white band, py-15, horizontal scroll pill chips r40 px-16 py-8 gap-8; active `#404854` fill + white M14, inactive `#D0D5DD` border + `#333` R14; optional underline tab strip above.

**Bottom-sheet onboarding modal** (`2322:170453`): `bg-white rounded-t-30 px-24 pt-10 gap-30`, drawer handle, centered Medium 20 title `#333`, Steps list (32px numbered circles, grey-300 border + tail, 14px `#999` descriptions), full-width Steel-Gray CTA, iOS home indicator.
