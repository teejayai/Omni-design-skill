# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose
Builds reusable **design skills** for the **Omni Retail** design system, distributed via skills.sh. Not a code app — output is `SKILL.md` prompt-context files + `tokens.json`.

## Source of truth
- All tokens, components, and patterns come from **Figma**, read via the connected **Figma MCP server** (`mcp__claude_ai_Figma__*` tools). Authenticate via `/mcp` if disconnected.
- Use **exact** Figma token names/values. Never invent or hardcode values.
- ONE shared design system (`omni-design-skills/SKILL.md` + `tokens.json`); each product extends it and never deviates.

## Structure
```
omni-design-skills/
├── SKILL.md        # shared base: tokens + global rules
├── tokens.json     # machine-readable tokens (colors, typography, effects, spacing, radius, components)
├── {dos,mos,agent,ros,omnipay}/SKILL.md   # per-product
└── README.md
```
Products: DOS, MOS, AGENT, ROS, OMNIPAY.

## Workflow
1. Read Figma design-system file via MCP → extract color/text/effect styles, spacing/radius tokens, component inventory → write `tokens.json` + base `SKILL.md`.
2. Per product file: identify tokens used, component preferences (e.g. filled vs outlined), density/spacing, layout patterns, deviations → fill product `SKILL.md`.
3. Each product `SKILL.md` includes: base reference, voice/personality, preferred components, anti-patterns, example patterns.

## Key Figma MCP tools
- `get_variable_defs` — color/spacing/token variables
- `get_metadata` / `get_design_context` — frames, components, structure
- `get_screenshot` — visual reference
- `search_design_system` / `get_libraries` — component inventory

## Constraints
- Skills are prompt context, not training — be explicit and detailed.
- Each `SKILL.md` must be self-contained enough to generate matching UI.
