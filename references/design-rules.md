# Design Engineering Rules

LLMs have statistical biases toward specific UI cliché patterns. Proactively construct premium interfaces using these engineered rules.

## Rule 1: Deterministic Typography

### Display/Headlines
```css
text-4xl md:text-6xl tracking-tighter leading-none
```

**ANTI-SLOP:** Discourage `Inter` for "Premium" or "Creative" vibes. Force unique character using `Geist`, `Outfit`, `Cabinet Grotesk`, or `Satoshi`.

**TECHNICAL UI RULE:** Serif fonts are strictly BANNED for Dashboard/Software UIs. Use exclusively high-end Sans-Serif pairings (`Geist` + `Geist Mono` or `Satoshi` + `JetBrains Mono`).

### Body/Paragraphs
```css
text-base text-gray-600 leading-relaxed max-w-[65ch]
```

## Rule 2: Color Calibration

- Max 1 Accent Color. Saturation < 80%.
- **THE LILA BAN:** "AI Purple/Blue" aesthetic is strictly BANNED. No purple button glows, no neon gradients. Use absolute neutral bases (Zinc/Slate) with high-contrast, singular accents (e.g. Emerald, Electric Blue, or Deep Rose).
- **COLOR CONSISTENCY:** Stick to one palette for the entire output. Do not fluctuate between warm and cool grays.

## Rule 3: Layout Diversification

**ANTI-CENTER BIAS:** Centered Hero/H1 sections are strictly BANNED when `LAYOUT_VARIANCE > 4`. Force:
- Split Screen (50/50)
- Left Aligned content / Right Aligned asset
- Asymmetric White-space structures

## Rule 4: Materiality, Shadows, and Anti-Card Overuse

**DASHBOARD HARDENING:** For `VISUAL_DENSITY > 7`, generic card containers are strictly BANNED. Use logic-grouping via `border-t`, `divide-y`, or purely negative space.

Use cards ONLY when elevation communicates hierarchy. When a shadow is used, tint it to the background hue.

## Rule 5: Interactive UI States

LLMs naturally generate "static" successful states. You MUST implement full interaction cycles:

- **Loading:** Skeletal loaders matching layout sizes (avoid generic circular spinners).
- **Empty States:** Beautifully composed empty states indicating how to populate data.
- **Error States:** Clear, inline error reporting (e.g., forms).
- **Tactile Feedback:** On `:active`, use `-translate-y-[1px]` or `scale-[0.98]` to simulate physical push.

---

# The 100 AI Tells (Forbidden Patterns)

To guarantee a premium, non-generic output, strictly avoid these common AI design signatures unless explicitly requested.

## Visual & CSS

```
NO Neon/Outer Glows: Do not use default box-shadow glows or auto-glows. Use inner borders or subtle tinted shadows.
NO Pure Black: Never use #000000. Use Off-Black, Zinc-950, or Charcoal.
NO Oversaturated Accents: Desaturate accents to blend elegantly with neutrals.
NO Excessive Gradient Text: Do not use text-fill gradients for large headers.
NO Custom Mouse Cursors: They are outdated and ruin performance/accessibility.
```

## Typography

```
NO Inter Font: Banned. Use Geist, Outfit, Cabinet Grotesk, or Satoshi.
NO Oversized H1s: The first heading should not scream. Control hierarchy with weight and color, not just massive scale.
NO Serif on Dashboards: Use Serif fonts ONLY for creative/editorial designs.
```

## Layout & Spacing

```
NO Misaligned Elements: Ensure padding and margins are mathematically perfect.
NO Floating Elements: Avoid awkward gaps.
NO 3-Column Card Layouts: The generic "3 equal cards horizontally" feature row is BANNED. Use 2-column Zig-Zag, asymmetric grid, or horizontal scrolling.
```

## Content & Data (The "Jane Doe" Effect)

```
NO Generic Names: "John Doe", "Sarah Chan", "Jack Su" are banned. Use creative, realistic-sounding names.
NO Generic Avatars: DO NOT use standard SVG "egg" or Lucide user icons. Use creative, believable photo placeholders.
NO Fake Numbers: Avoid 99.99%, 50%, or 1234567. Use organic, messy data (47.2%, +1 (312) 847-1928).
NO Startup Slop Names: "Acme", "Nexus", "SmartFlow". Invent premium, contextual brand names.
NO Filler Words: Avoid "Elevate", "Seamless", "Unleash", "Next-Gen". Use concrete verbs.
```

## External Resources & Components

```
NO Broken Unsplash Links: Do not use Unsplash. Use https://picsum.photos/seed/{random_string}/800/600 or SVG UI Avatars.
NO Default shadcn/ui: You may use shadcn/ui, but NEVER in generic default state. Customize radii, colors, shadows.
```
