# Omni Design Skills

Reusable design skills for the **OmniONE Retail** design system, distributed via skills.sh.

## Structure
```
omni-design-skills/
├── base/SKILL.md       # shared base: tokens + global rules
├── base/tokens.json    # machine-readable design tokens
├── dos/SKILL.md
├── mos/SKILL.md
├── agent/SKILL.md
├── ros/SKILL.md
├── omnipay/SKILL.md
└── README.md
```

## Install
```
skills add teejayai/Omni-design-skill
```
Installs all 6 skills (base + 5 products). Read `base/SKILL.md` first, then a product skill.

## Model
ONE shared design system (`SKILL.md` + `tokens.json`). Each product extends it with its own voice, component preferences, and **documented deviations** — but never redefines base tokens. Read the base first, then the product skill.

## Product cheat-sheet
| Product | Platform | Primary action | Accent | Control radius | Layout signature |
|---|---|---|---|---|---|
| **DOS** | Mobile | Steel Gray `#4B5563` | Teal | 5px (sheets 30) | Bottom-nav + bottom-sheets; surface `#F8F9FA`, text `#333` |
| **MOS** | Desktop web | **Brand blue `#173E87`** | Teal `#1AA179` | **6px** | Sidebar shell (288) + data tables + form/preview split |
| **AGENT** | Mobile | **Teal `#158362`** | Blue (decorative) | 5 / 10 / 20 | Gamified card feed + sticky bottom CTA |
| **ROS** | Mobile | Steel near-black `#252A31`/`#161A1E` | Teal `#1AA179` | 5 / 10 (sheets 30) | Onboarding hero + input stack + bottom-sheet pickers |
| **OMNIPAY** | Web + Mobile | **Purple `#A682FF`** | Teal-tint shadows | web 12 / mobile 20 | Status chips + transaction tables; finance trust cues |

**Shared everywhere:** Gordita font, the OmniONE type scale, the color ramps & semantic tokens in the base. **Recurring deviations:** most products override brand-blue primary and use softer radii than the base 4px; several use surface `#F8F9FA` and text `#333`.

## Status
- ✅ Base: full Gordita type scale, color ramps, semantic tokens, core components (buttons, inputs, tags, badges, **modals, navigation, banners & toasts, popovers/selectors**).
- ✅ All 5 product skills (crawled from product Figma files via MCP).
- ⏳ Pending: mobile type-scale exact values; effect/shadow styles (correct Figma node needed).

Source: Figma via the connected Figma MCP server. Exact token names/values only.
