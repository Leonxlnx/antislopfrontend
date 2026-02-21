---
name: high-agency-frontend
description: Creative Technologist & Senior Frontend Engineer skill. Architect digital artifacts using measurable constraints, React-first architecture, specific Tailwind + Raw CSS separation, and strict interaction modes to eradicate generic templates.
---

# High-Agency Frontend Skill

## 1. DEFAULT ARCHITECTURE & TOOLING

**Framework & State:**
- React or Next.js (Server Components by default; `"use client"` strictly at the leaf level for interactive UI).
- Use local `useState`/`useReducer` for UI state. Global state is only for preventing deep prop-drilling across the component tree.
- Generate full interaction states proactively: Loading (Skeletons, not spinners), Empty (designed placeholders), and Error (inline feedback).

**Styling Separation:** 
- **Styling Rule:** Use Tailwind CSS for 90% of styling (layout, colors, spacing). Use raw CSS (or CSS Modules) ONLY for complex `@keyframes`, `clamp()` typography, and pseudo-element grain filters where Tailwind strings become unreadable.

**Animation & DOM:**
- No Vanilla JS DOM manipulation (e.g., `document.querySelector`, `el.addEventListener`). 
- For complex physics or DOM events, strictly use React patterns: `useRef` and `useEffect`. **Mandatory:** `useEffect` hooks implementing listeners MUST return a cleanup function to prevent memory leaks.
- Prefer `framer-motion` for complex physics and choreography.

---

## 2. THE ANTI-SLOP MANDATE (FORBIDDEN GENERIC PATTERNS)

Before writing any code, internalize these forced constraints. Do not output generic patterns; always default to the High-Agency alternative.

**Forbidden / Generic:** Purple-to-blue linear gradients.
**High-Agency Alternative:** Muted editorial tones, solid OLED blacks, or single-accent monochrome.

**Forbidden / Generic:** Glassmorphism (`backdrop-blur`) everywhere.
**High-Agency Alternative:** Solid opacity layers, or highly specific "Liquid Glass" (1px inner border + inset shadow).

**Forbidden / Generic:** Standard `box-shadow: rgba(0,0,0,0.1)`.
**High-Agency Alternative:** Tinted ambient shadows matching the background hue, or no shadow (use 1px borders).

**Forbidden / Generic:** Centered bento grids for everything.
**High-Agency Alternative:** Asymmetric layouts, brutalist HTML structures, or massive intentional whitespace (fallback to mobile column).

**Forbidden / Generic:** "Everything is a Card".
**High-Agency Alternative:** Rely on spacing, typography, and alignment to group data instead of boxed cards.

---

## 3. DESIGN ENGINEERING & CREATIVE PROACTIVITY

Do not wait for the user to explicitly ask for "creativity." Assume the user wants a premium, award-winning interface. Integrate these high-end coding concepts as your baseline:

### Typography Intent
- **Display Typography:** Make headers feel physical. Use `clamp()` for fluid sizing and enforce tracking adjustments (e.g., `tracking-tighter leading-none` on massive headers).
- **Contextual Selection:** Modern B2B tools excel with clean Sans-Serifs (`Inter`, `Geist`). For editorial, luxury, or portfolio aesthetics, default to highly refined Serif fonts (e.g., `Playfair Display`, `Cormorant Garamond`) and allow text to overlap images intentionally.

### Staggered Orchestration & Load States
- Do not mount lists or grids instantly. Use CSS cascades (`animation-delay: calc(var(--index) * 100ms)`) or Framer Motion `staggerChildren` to create sequential waterfall reveals.
- Loading states should be architectural (skeletons mapping the layout) rather than a generic centered spinner.

### Interactive Micro-Physics
- Buttons and interactive elements must feel tangible. On `:active`, use `-translate-y-[1px]` or `scale-[0.98]` to simulate a physical push indicating success/action.
- For high-end portfolios, implement buttons that pull slightly toward the mouse cursor using Framer Motion (mapping mouse coordinates to `useTransform` X/Y offsets).

### Performance-Safe Grain
- When a raw, "Lo-Fi High-Tech" texture is needed, dither the background.
- **Strict Execution:** Apply grain filters exclusively to fixed, pointer-event-none pseudo-elements (`fixed inset-0 z-50 pointer-events-none`) and NEVER to scrolling containers to prevent continuous GPU repaints.

---

## 4. EXECUTION SCENARIOS (Concrete Snippets)

### Scenario A: Complex Header (Tailwind + Raw CSS approach)
**Concept:** A massive headline scaling fluidly without huge Tailwind bracket strings.
```jsx
// HTML (Tailwind for layout)
<h1 className="fluid-headline text-zinc-900 tracking-tighter">
  Vanguard
</h1>
// CSS (Raw CSS for fluid math)
.fluid-headline { font-size: clamp(3rem, 8vw, 8rem); line-height: 0.9; }
```

### Scenario B: High-End Form Input
**Concept:** Predictable structure, explicit states, no guessing.
```jsx
<div className="flex flex-col gap-2 w-full max-w-md">
  <label className="text-sm font-medium text-zinc-800">Email</label>
  <input className="px-4 py-2 border border-zinc-200 focus:ring-2 focus:ring-zinc-900 rounded-none transition-all" />
  <span className="text-xs text-red-500">Error message placeholder</span>
</div>
```

---

## 5. RESPONSIVE & PERFORMANCE GUARDRAILS

- **Mobile Override:** Any asymmetric, staggered, or complex grid layout on desktop (`md:`) MUST collapse gracefully to a clean, single-column layout (`w-full`, `px-4`, `py-8`) on viewports `< 768px`. Do not allow horizontal overflow.
- **Hardware Acceleration:** Never animate `top`, `left`, `width`, or `height`. Animate exclusively via `transform` and `opacity`.

---

## 6. PRE-FLIGHT CHECKLIST

Before generating your final React output, verify internally:
- [ ] Is my styling separated correctly (Tailwind for 90%, CSS for complex clamps/keyframes)?
- [ ] Did I avoid Vanilla JS `el.addEventListener` in favor of React `useEffect` / `useRef`?
- [ ] If using `useEffect` for events or animations, is there a strict cleanup function?
- [ ] Is grain/noise applied ONLY to a `fixed inset-0 pointer-events-none` container?
- [ ] Are structural states (Loading skeletons, Empty, Errors) included?
- [ ] Has generic AI-Slop (purple gradients, standard shadows, bento grids) been purged in favor of high-agency design?
