---
name: omni-agent
description: OmniONE — AGENT product design skill. Mobile field-sales-agent app. Gamified, encouraging, card-driven, TEAL primary action, soft radii (5/10/20). Extends the shared omni-design-system base.
---

# OmniONE — AGENT

Mobile-first (375px) app for field sales agents. Extends [omni-design-system](../base/SKILL.md) — use base Gordita type scale + token names; the overrides below are AGENT-specific.

## Voice / personality
Supportive coach, not a dashboard. Gamified and encouraging: greetings by name ("Hi Anike"), streak/booster framing ("178th", "Today's Booster Suggestion"), motivational copy, emoji mascots, friendly illustrated empty states. Spacious, card-driven, generous vertical rhythm — **never data-dense**.

## Preferred components & variants
- **Buttons**: filled, full-width, **Teal** `#158362`, Gordita Medium 14 `#FEFEFE`. Disabled = `opacity 0.5`. No outline/ghost primaries.
- **Inputs**: white, 1px `#F0F0F1` border, label-above-field, red `*` for required, placeholder `#999`.
- **Cards for everything** (plans, suggestions, progress) with soft shadow; **lists are card stacks, not tables**.
- **Bottom-sheet modals** with grab handle (rounded top ~20px), divider-separated rows.
- **Bottom tab bar** (Home/Customers/Inventory/Orders/Profile), active = teal.
- **Mobile header**: iOS status bar + back chevron + 18px Medium title.
- **Stepped wizard**: thin pill progress track (teal `#1AA179` fill) + "1 / 4" counter.

## Density & spacing
Roomy. Screen padding **16px**; field gap **26px**; section gap **30px**; label→input **6px**. Input height **48px** (14×8 padding); button height **46px**. Sticky bottom CTA bar: pt-20 / pb-60 / px-16.

## Layout patterns
`Mobile header → scroll body (16px padding) → sticky bottom CTA bar`. Home = vertical card feed: greeting → Target Progress card (brand-blue gradient, white text) → Booster Suggestion → "My Plans (x/12)" + horizontal day-picker → customer plan cards → bottom tab bar. Forms = single-column, label-above-input, stepper on top. Lists = card stacks with illustrated empty state + centered CTA.

## Token usage & deviations
- **Primary action = Teal**, NOT brand blue. Teal `#158362` (buttons), `#1AA179` (progress), `#F6FDFB` (25). Brand blue `#173E87` is **decorative/gradient only**.
- **Radii larger than base**: inputs **10px**, buttons **5px**, cards/sheets **20px**.
- **Button height 46px** (off the base 32/36/44/48 scale).
- Text: `#333333` (not base `#101928`), subdued `#999999`, label `#4D4D4D`.
- Extra colors seen: Purple `#8A6CD4`, Gold `#FFC800`, Amber ramp, Soft Red `#DC3545` (errors/asterisks). Button text `#FEFEFE` (Bliss White).
- Mobile headings use negative tracking (H3 -3%, H5/H6 -2%).

## Anti-patterns
- ❌ Brand-blue primary CTAs (primary is teal; blue is decorative).
- ❌ Data tables / dense grids in the app — use card stacks.
- ❌ Sharp 4px/8px radii — AGENT is soft (5/10/20).
- ❌ Outline/ghost primary buttons — they're filled, full-width.
- ❌ Terse/utilitarian copy — keep encouraging, progress/streak framing.
- ❌ Centered dialog modals — use bottom sheets with grab handle.
- ❌ Dropping the sticky bottom CTA on action screens.

## Example patterns
**Multi-step form** (`4603:82208`): mobile header → teal step progress + "1/4" → single-column inputs (gap 26): label `M14 #4D4D4D` + red `*` over 48px white field, 1px `#F0F0F1`, r10, 14×8 → sticky bottom bar with full-width teal `#158362` button, r5, h46, disabled opacity 0.5.

**Bottom-sheet selector** (`4603:83054`): white sheet, r-top 20, grab handle → 16px Medium title → vertical 14px text rows, 1px `#F0F0F1` dividers, ~54px rows.

**Home feed card** (`18696:67479`): 16px gutters; greeting H3-24 Bold → Target Progress card (brand-blue gradient, white, inner white pill button) → Booster card → "My Plans (0/12)" + day-picker (selected = teal pill) → plan cards → bottom tab bar.
