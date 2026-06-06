---
name: omni-ros
description: OmniONE — ROS (Retail Operating System) design skill. Mobile-first onboarding/retail app. Warm + guided, near-black STEEL-GRAY primary action, teal #1AA179 accent, soft radii (5/10/30). Extends the shared omni-design-system base.
---

# OmniONE — ROS

Mobile-first (375px, PWA + native) retail operating system. Extends [omni-design-system](../SKILL.md). Gordita throughout. **Biggest deviation: ROS uses near-black steel-gray as its action color, not brand blue.**

## Voice / personality
Warm, personable, low-friction. Headers address the user by name ("Hi Cece!") with reassuring sub-lines ("We need a bit more information. Please enter your business details"). Progress always shown ("1 / 3" + bar, or step dots) — onboarding framed as short and guided. Calm neutral chrome: black/white/grey + a single teal accent, no decorative color.

## Preferred components & variants
- **Omni_Inputs** (workhorse): label row (Gordita Medium 14, `#515151`/`#4B5563`) + red `*`, over white field `h-48`, border `#ECECEC`, radius **10px**, padding 16/12. Trailing chevron when it's a select.
- **Main Buttons**: full-width, radius **5px**, py-10/px-16, Gordita Medium 14 `#FEFEFE`. Active `#252A31` (steel-700), modal action `#161A1E` (steel-900), disabled `#C0C3C8`.
- **Mobile header**: iOS status bar + language selector pill (bordered, r4, `#C0C3C8`) + help icon. Persistent on every screen.
- **Bottom button dock**: white, sticky, pt-15 pb-60 px-16.
- **Modal — bottom sheet**: top corners radius **30px**, grab handle, header (Medium 16), search input, scrollable radio list, sticky action button.
- **Steps-Dot stepper**: dot + tail, active `#4B5563`, inactive `#D9D9D9`.
- **Radio (Form Control Element)**: 24px, active = filled black ring.

## Density & spacing
4px grid honored. Field stack gap **26px**, label→input **6–8px**, intra-group 12–20px. Mobile artboard 375, content column 343–344 (16px gutters). Inputs comfortable (48px); modal radio rows gap 32px. Generous hero whitespace above forms (top offset ~128–290px).

## Layout patterns
Single column: **Mobile header (fixed top) → centered hero (title + subcopy + progress) → scrollable input stack → fixed bottom CTA dock → home indicator.** Centered hero width 287px; progress under subcopy. Pickers route to **bottom sheets** (not inline dropdowns). Required fields flagged inline with a small red asterisk.

## Token usage & deviations
- **Primary action = steel-gray near-black** `#252A31` (active) / `#161A1E` (modal) / `#C0C3C8` (disabled). Brand blue `#173E87` **not used** on product screens.
- **Teal accent = `#1AA179`** (progress fill) — darker than base `#20C997`.
- **Radii**: inputs **10px**, buttons **5px**, bottom-sheet top **30px** (not base 4/8).
- **Input border `#ECECEC`** — custom, not in base ramp.
- Text: heading/focused `#333333`, body grey `#6E737F` (Neutral/60), label `#515151`/`#4B5563`, placeholder `#979797`/`#D9D9D9`. Icon focused `#808080`. Button label `#FEFEFE`.
- **Required asterisk red `#F62828`** — deviates from base error `#DC3545`.
- Type: Gordita R400/M500; hero title Medium 24/lh30; Sub Body 14, Web Body Small-14, Body 16.

## Anti-patterns
- ❌ Brand-blue primary CTAs — ROS is steel-gray-700/900 near-black.
- ❌ Base teal `#20C997` — ROS uses `#1AA179`.
- ❌ 4px/8px radii on inputs — ROS inputs 10px, buttons 5px.
- ❌ Inline-expanding selects — route pickers to a bottom-sheet (search + radio list).
- ❌ Omitting progress on multi-step flows — every step shows count/dots.
- ❌ Dropping the persistent Mobile header (status bar + language/help).

## Example patterns
**Onboarding form step** (`26612:17617`): mobile header → centered hero (greeting `M24 #333`, subcopy `R14/lh20`) → progress (teal `#1AA179` bar on `#F0F0F1` + "n / N", or step dots `#4B5563`/`#D9D9D9`) → Omni_Inputs stack (gap 26; fields h48 r10 border `#ECECEC`, label `M14 #4B5563` + red `#F62828` `*`) → fixed bottom dock, full-width CTA (r5, `#252A31` active / `#C0C3C8` disabled, `M14 #FEFEFE`).

**Selection bottom sheet** (`25602:36554`): white sheet, top r30, grab handle, header `M16 #333`, search input (r8, border `#F0F0F1`, placeholder `#D9D9D9`), scrollable rows of `label (R14 #6E737F) + 24px radio (active black ring)`, sticky full-width action button (r5, `#161A1E`).

**Select-type input** (`26615:12716`): Omni_Input rendered as a button showing current value (`R14 #333`) + trailing 24px chevron; tap opens the bottom sheet above.
