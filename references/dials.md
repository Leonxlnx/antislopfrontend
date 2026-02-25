# Design Dials

## Active Baseline

```
DESIGN_VARIANCE: 8
MOTION_INTENSITY: 6
VISUAL_DENSITY: 4
```

The standard baseline for all generations is strictly set to these values. Do not ask the user to edit this file.

**Always listen to the user:** Adapt these values dynamically based on what they explicitly request in their chat prompts. Use these baseline (or user-overridden) values as global variables to drive specific logic.

---

## DESIGN_VARIANCE (Level 1-10)

### 1-3 (Predictable)
- Flexbox `justify-center`
- Strict 12-column symmetrical grids
- Equal paddings

### 4-7 (Offset)
- `margin-top: -2rem` overlapping
- Varied image aspect ratios (e.g., 4:3 next to 16:9)
- Left-aligned headers over center-aligned data

### 8-10 (Asymmetric)
- Masonry layouts
- CSS Grid with fractional units (`grid-template-columns: 2fr 1fr 1fr`)
- Massive empty zones (`padding-left: 20vw`)

**MOBILE OVERRIDE:** For levels 4-10, any asymmetric layout above `md:` MUST aggressively fall back to strict, single-column layout (`w-full`, `px-4`, `py-8`) on viewports `< 768px` to prevent horizontal scrolling and layout breakage.

---

## MOTION_INTENSITY (Level 1-10)

### 1-3 (Static)
- No automatic animations
- CSS `:hover` and `:active` states only

### 4-7 (Fluid CSS)
```css
transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
```
- `animation-delay` cascades for load-ins
- Focus on `transform` and `opacity`
- `will-change: transform` sparingly

### 8-10 (Advanced Choreography)
- Complex scroll-triggered reveals or parallax
- Framer Motion hooks
- NEVER use `window.addEventListener('scroll')`

---

## VISUAL_DENSITY (Level 1-10)

### 1-3 (Art Gallery Mode)
- Lots of white space
- Huge section gaps
- Everything feels expensive and clean

### 4-7 (Daily App Mode)
- Normal spacing for standard web apps

### 8-10 (Cockpit Mode)
- Tiny paddings
- No card boxes; just 1px lines to separate data
- Everything is packed
- **Mandatory:** Use Monospace (`font-mono`) for all numbers
