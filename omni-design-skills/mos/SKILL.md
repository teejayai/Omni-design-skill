---
name: omni-mos
description: OmniONE — MOS (Manufacturer OS) design skill. Desktop B2B web app — sidebar shell, data tables, stepper flows, BRAND-BLUE primary + teal accents, 6px control radius. Extends the shared omni-design-system base.
---

# OmniONE — MOS

Desktop B2B web app (1440px) for manufacturers — Targets, Roles, Sales Process, Order Creation, Product upload, Customer Mgt. Extends [omni-design-system](../base/SKILL.md). Gordita throughout. Currency ₦. "Powered by OmniONE" footer on every screen.

## Voice / personality
Operational and businesslike. Plain, task-led labels ("Add New Target", "Pending Validation"). Guided, multi-step (stepper flows + form-with-live-Preview). Trust/clarity over flair — status via soft-tinted badges, not loud color.

## Preferred components & variants
- **Buttons**: Primary = filled **brand blue `#173E87`** (Create, Search, Action ▾). Secondary = white + gray stroke (Cancel/Export/Filter). Tertiary destructive = red text "Delete".
- **Fixed left sidebar** (288px) with dropdown nav groups + company-switcher card + Demo Account toggle.
- **Top utility bar**: language dropdown, search, settings, notification badge, avatar initials.
- **Data tables**: sortable header chevrons, per-row "View Details" link, **status badges** (Pending/Failed/Uploaded), footer "Rows per page" + pager.
- **Stat/summary cards** in 3-up rows; active card = teal border `#1AA179` on `#DEF7EF`.
- **Tabs**: underline-active.
- **Form controls**: labeled inputs with red `*`, "Please select" dropdowns, segmented day-pickers (active = teal fill), multi-select chips with `×`, date inputs w/ calendar icon, radio groups.
- **Live Preview panel** (right rail, `#F8F9FA`) mirroring form values under all-caps labels.

## Density & spacing
4px grid, **dominant gap = 8px**, then 4/12/16/24, section 30. Padding `px-16 py-8`, card `p-32`. Content max width 1152 (1440 − 288 sidebar). Table rows ~56px, input/button rows 38–44px. Medium-dense.

## Layout patterns
**App shell**: fixed sidebar (288) + top utility bar (60) + scroll main (1152) + global footer (60). Circular brand-blue back button + "Back" top-left; primary actions top-right. **Create flows** = 60/40 form + Preview split. **List page**: Back → stat-card row → tabs → titled table card + Action ▾ → search/filter toolbar → table → pager. Stepper strip above multi-stage flows.

## Token usage & deviations
- **Primary = brand blue `#173E87`** (the one product that keeps blue as primary). Teal `#20C997`/`#1AA179`/`#158362`/`#DEF7EF` = success/active. Amber `#FFC107` = pending; Soft Red `#DC3545`/`#8F222D` = failed/delete.
- **Default control radius = 6px** (`radius-sm`), not base 4px. Use 6px for MOS inputs/buttons/cards; pills `rounded-full`.
- **Surface bg = `#F8F9FA`** (not base `#F0F0F1`); Preview rail also `#F8F9FA`.
- Text drifts: `#343841`/`#353F50`/`#202124` headings, `#999BA0`/`#999999` sub-text.
- Stray greys: table-line `#EAECF0`, stroke `#D0D5DD`, button-stroke-active `#E1E6ED`.
- Shadow md: `0 2 4 -2 #1018280F, 0 4 8 -2 #1018281A`. Lime Green `#13CF19` present.

## Anti-patterns
- ❌ Hardcoding raw hex across competing namespaces (`Color/Secondary/Teal/*` vs `Secondary 1/*` vs raw `#20C997`) — use semantic `Specific/*` + `Border/*` aliases.
- ❌ **Inter / Untitled-UI token bleed** — a borrowed table component leaks Inter + `text-xs`; MOS font is **Gordita**, ignore the Inter leakage.
- ❌ Inventing a third surface bg — `#F8F9FA` (page) / `#FFFFFF` (card) only.
- ❌ Radius drift (12px/75px strays) — standardize on 6px control/card.
- ❌ `lineHeight:1` cramped body styles — prefer the lh20 14px variants.
- ❌ Mobile/bottom-sheet patterns — MOS is desktop sidebar-shell.

## Example patterns
**List/management page** (`17669:75534`): shell → circular back + "Back" → 3 stat cards (white, r6, 1px `#F0F0F1`, active = teal border on `#DEF7EF`) → underline tabs → card: `H6-20/Bold #343841` title + subdued desc + primary "Action ▾" (`#173E87`, r6) → toolbar [Search input + Search btn | Export + Filter tertiary] → table (header `#F8F9FA`, sort chevrons, Body-14, status badge, "View Details" link in blue) → footer pager.

**Create flow with live preview** (`1:91377`): header (back+title left, [Cancel][Create Target] right) → 60/40 split. Left = labeled fields (`Body-14/Medium` label + red `*`, inputs h38–44 r6 border `#D0D5DD`), segmented day-picker (active teal `#20C997`), multiselect chips w/ `×`, paired date inputs. Right = `#F8F9FA` Preview: all-caps `Caption-12` labels + `Body-16/Bold` values.

**Stepper table flow** (`1:129440`): top stepper "Step n/4" → two-pane: scrollable product grid (cards, 64px icon, name + ₦price) + sticky Cart panel (line items, Sub-Total/Discount/Total dividers, primary Checkout). 8px gaps.
