---
name: omni-omnipay
description: OmniONE — OMNIPAY design skill. Payments/wallet/card product (web + mobile). PURPLE brand accent (#A682FF) replaces brand blue, signature status chips, data tables, finance-grade trust cues. Extends the shared omni-design-system base.
---

# OmniONE — OMNIPAY

Payments / wallet / card product, web (1440px) + mobile (375px). Extends [omni-design-system](../SKILL.md). Gordita is the system font. OmniPay overlays a distinct **purple** accent and (legacy) mixes in third-party kits — treat those as debt, not patterns.

## Voice / personality
Functional, transactional, finance-grade. Plain labels ("Wallet Balance", "Add Money", "Withdraw"). Explicit trust/compliance cues on money flows ("Powered by Victory MFB — Trusted, Secured, and CBN Licensed", "Terms and Conditions of OmniPay cards"). Warm onboarding microcopy on auth. Clear + reassuring, not playful.

## Preferred components & variants
- **Status chip** (signature): pill h-30, radius 12, px-16, tinted bg + matching text. Successful / Pending / Failed.
- **Data table**: card-wrapped (r16 + shadow), sortable uppercase headers (Gordita Medium 16/24 + sort icon), rows px-16 py-12 with 1px inset bottom divider. Used for all transaction lists.
- **Stat / balance cards**: ~264×125, r10, purple 1px border, faint teal shadow; selected = purple-tinted fill `rgba(166,130,255,.05)`.
- **Tabs**: text + 2px underline; active = purple `#A682FF` Medium, inactive grey `#6C757D` Regular.
- **Buttons** — web: Primary solid purple r12 h52; Secondary purple-outline r12. Mobile: Primary solid purple **r20** h48; Secondary purple-outline r20.
- **Input (auth)**: labeled, r8, 1px `#D0D5DD`, px-14 py-10, shadow-xs, trailing eye/mail icon (Untitled-UI kit).
- **Payment card visual**: 299×188 r16, purple `#9283BE` face, AfriGo + OmniPay branding, "DEBIT", expiry.
- **Info/feature row**: white, 1px `#ECECEC`, r4, icon + text.
- Charts: line + pie, purple-dominant with lime/yellow accents.

## Density & spacing
4px grid. Gaps 8/12/16/22/24/32. Web canvas 1440, content inset left 32, table width 1382. Table rhythm rows px-16 py-12, cells p-8, header pt-16 pb-8. Mobile canvas 375, padding 16, content 343, card r20. Medium density — roomy cards, 16/24 line-heights.

## Layout patterns
- **Web shell**: left sidebar + top app bar (h-82, faint teal shadow), page title Gordita Medium 24 `#232F49`, top-right action cluster.
- **List screen**: Tabs → search bar (h-62, purple-tinted border) → table card.
- **Dashboard**: stat-card row → line chart → pie charts in white cards.
- **Auth**: 50/50 split — left illustration, right centered 360px form column, gap-24.
- **Mobile**: fixed top bar (back / centered title / action, h-48) → swipeable card carousel → stacked info rows → checkbox consent → stacked buttons.

## Token usage & deviations
- **Primary = PURPLE, not brand blue.** `#A682FF` (buttons, active tabs, links, card borders). Card face `#9283BE`; link tint `#8A6CD4`; magstripe band `#1F4284`.
- **Status chip palette (own named set, NOT base success/error):** Success `#0B7719` on `rgba(11,119,25,.15)`; Pending `#979797` on `#E9EDF1`; Failed `#D10101` on `rgba(209,1,1,.15)`.
- **Text drift:** `#232F49` (web headings/body), `#2E2E2E`/`#313131` (mobile), `#667085`/`#344054` (auth kit) — not base `#101928`.
- **No single control radius:** buttons 8 (auth) / 12 (web) / 20 (mobile); cards 10/12/16/20. Standardize per platform: **web control 12px, mobile control 20px**.
- Effects: brand teal-tinted shadows `rgba(100,197,186,.11/.22)`; auth shadow-xs `0 1 2 rgba(16,24,40,.05)`.
- A stray Dashboard scale exists (Primary `#2A85FF`, Lime `#40C351`, Warning `#FFCD00`, full Neutral ramp) — legacy, do not propagate.

## Anti-patterns
- ❌ Three competing color systems (purple / Dashboard `#2A85FF` / auth Gray kit) — standardize on **purple primary + status palette**.
- ❌ Font drift — mobile card screens use Lato, one web button uses Rubik; keep **Gordita**.
- ❌ Treating status colors as base Soft Green/Soft Red — OmniPay status is its own named set.
- ❌ Random radii — web control 12px, mobile control 20px.
- ❌ Heading `#232F49` elsewhere expecting base `#101928`.

## Example patterns
**Transaction table row** (`29069:73124`): `flex gap-16 px-16 py-12` + inset bottom divider; 5 cells `flex-1 p-8` Gordita Regular 16/24 `#232F49`; final cell = Status chip. Header: Medium 16 uppercase + sort icon, pt-16 pb-8. Wrap in white card r16 shadow.

**Status chip** (`29069:73143`): `inline-flex h-30 items-center justify-center px-16 rounded-12`, Gordita Regular 16. Success `#0B7719`/`rgba(11,119,25,.15)`; Pending `#979797`/`#E9EDF1`; Failed `#D10101`/`rgba(209,1,1,.15)`.

**Balance / stat card** (`29069:73108`): `w-264 h-125 rounded-10 border-1 border-[#A682FF] bg-white shadow-[0_2_32_-4_rgba(100,197,186,.11)]`; amount Gordita Regular 18 `#232F49` (`₦ 27,500,468`), label Medium 14 `#A682FF` + icon. Selected variant fills `rgba(166,130,255,.05)`.
