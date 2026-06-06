# Omni Retail — Design Skill Builder Prompt

Paste the prompt below into Claude Code to build the design skills.

---

You are helping me build a reusable design skill for our **Omni Retail**
design system, distributed via skills.sh to our product design team.

## Context
- We have ONE shared design system (Omni) used across multiple products.
- Each product has its own design patterns but never deviates from the
  shared system.
- Our products are: **DOS, MOS, AGENT, ROS, OMNIPAY**.
- Goal: a base `SKILL.md` (shared system) + one `SKILL.md` per product.
- Figma is connected via an MCP server — use it to read the actual files
  directly (no manual key entry).

## Task
1. Use the connected Figma MCP server to open the files via the links I
   provide. I'll give you a Figma file link for the design system and for
   each product — read each one through the MCP.
2. Extract from the shared design system file:
   - Color styles/variables (name + value + group)
   - Text styles (font, size, weight, line height)
   - Effect styles (shadows, blurs)
   - Spacing/radius tokens
   - Component inventory

   Output this as a structured `tokens.json`.
3. For each product file (DOS, MOS, AGENT, ROS, OMNIPAY), analyze frames
   and components to identify:
   - Which tokens are used and where
   - Component preferences (e.g. filled vs outlined buttons)
   - Density and spacing tendencies
   - Layout patterns
   - Any product-specific deviations within the system
4. Generate `SKILL.md` files in this structure:
   ```
   omni-design-skills/
   ├── SKILL.md            (shared base: tokens + global rules)
   ├── dos/SKILL.md
   ├── mos/SKILL.md
   ├── agent/SKILL.md
   ├── ros/SKILL.md
   ├── omnipay/SKILL.md
   └── README.md
   ```
5. Each product `SKILL.md` must include: design system base reference,
   product voice/personality, preferred components, anti-patterns to
   avoid, and example patterns.

## Constraints
- Skills are prompt context, not training — be explicit and detailed.
- Use exact token names/values from Figma, never invented ones.
- Keep each `SKILL.md` self-contained enough to generate matching UI.

Start by asking me for the Figma link to the Omni design system file.

---

## Figma file links (paste as you go)

| File | Link |
|---|---|
| Omni design system | |
| DOS | |
| MOS | |
| AGENT | |
| ROS | |
| OMNIPAY | |
