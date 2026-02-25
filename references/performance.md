# Performance Guardrails

## DOM Cost
Apply grain/noise filters exclusively to fixed, pointer-event-none pseudo-elements:
```css
fixed inset-0 z-50 pointer-events-none
```
NEVER apply to scrolling containers to prevent continuous GPU repaints and mobile performance degradation.

## Hardware Acceleration
Never animate `top`, `left`, `width`, or `height`.

Animate exclusively via:
- `transform`
- `opacity`

## Z-Index Restraint
NEVER spam arbitrary `z-50` or `z-10` unprompted.

Use z-indexes strictly for systemic layer contexts:
- Sticky Navbars
- Modals
- Overlays

---

## Pre-Flight Checklist

Before outputting code, evaluate against this matrix:

- [ ] Is global state used appropriately to avoid deep prop-drilling rather than arbitrarily?
- [ ] Is mobile layout collapse (`w-full`, `px-4`, `max-w-7xl mx-auto`) guaranteed for high-variance designs?
- [ ] Do full-height sections safely use `min-h-[100dvh]` instead of the bugged `h-screen`?
- [ ] Do `useEffect` animations contain strict cleanup functions?
- [ ] Are empty, loading, and error states provided?
- [ ] Are cards omitted in favor of spacing where possible?
- [ ] Did you strictly isolate CPU-heavy perpetual animations in their own Client Components?
