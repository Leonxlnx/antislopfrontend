---
name: design-taste-frontend
description: Enforces high-end frontend design patterns, anti-AI-slop rules, and motion specifications for React/Next.js. Use when building or reviewing UI components, dashboards, or landing pages.
---

# Design Taste Frontend

Senior UI/UX Engineer skill that overrides default LLM biases toward generic AI designs.

## Active Baseline

```
DESIGN_VARIANCE: 8 | MOTION_INTENSITY: 6 | VISUAL_DENSITY: 4
```

Adapt these dynamically based on user requests. See `references/dials.md` for definitions.

## Quick Reference

| Topic | File | Search |
|-------|------|--------|
| Architecture | `references/architecture.md` | `grep "CRITICAL" references/architecture.md` |
| Design Rules | `references/design-rules.md` | `grep "NO " references/design-rules.md` |
| Motion/Animation | `references/motion.md` | `grep "spring" references/motion.md` |
| Performance | `references/performance.md` | `grep "NEVER" references/performance.md` |
| Creative Arsenal | `references/creative-arsenal.md` | `grep "Grid\|Menu\|Card" references/creative-arsenal.md` |
| Dial Definitions | `references/dials.md` | — |

## Critical Rules (Always Apply)

### Banned Defaults
- **NO Inter font** → Use Geist, Outfit, Cabinet Grotesk, Satoshi
- **NO AI Purple/Blue** → Use Zinc/Slate with singular accent (Emerald, Electric Blue, Deep Rose)
- **NO `h-screen`** → Use `min-h-[100dvh]` for mobile safety
- **NO Emojis** → Use Phosphor/Radix icons or SVG primitives
- **NO 3-Column Card Layouts** → Use asymmetric grids or zig-zag

### Typography Defaults
```css
/* Headlines */
text-4xl md:text-6xl tracking-tighter leading-none

/* Body */
text-base text-gray-600 leading-relaxed max-w-[65ch]
```

### Motion (When MOTION_INTENSITY > 5)
```javascript
// Always use spring physics, never linear
type: "spring", stiffness: 100, damping: 20

// For magnetic/continuous animations: useMotionValue, NOT useState
```

### Performance
- Animate only `transform` and `opacity`
- Isolate perpetual animations in their own Client Component with `React.memo`
- Use CSS Grid over flex-math: `grid grid-cols-1 md:grid-cols-3 gap-6`

## Pre-Flight Checklist

- [ ] Mobile collapse guaranteed (`w-full`, `px-4`, `max-w-7xl mx-auto`)?
- [ ] Full-height uses `min-h-[100dvh]` not `h-screen`?
- [ ] `useEffect` animations have cleanup functions?
- [ ] Empty, loading, and error states provided?
- [ ] CPU-heavy animations isolated in Client Components?
