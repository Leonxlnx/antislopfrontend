# Motion & Animation

## Creative Proactivity (Anti-Slop Implementation)

### Liquid Glass Refraction
When glassmorphism is needed, go beyond `backdrop-blur`:
```css
border-white/10
shadow-[inset_0_1px_0_rgba(255,255,255,0.1)]
```

### Magnetic Micro-physics (If MOTION_INTENSITY > 5)
Buttons that pull slightly toward the mouse cursor.

**CRITICAL:** NEVER use React `useState` for magnetic hover or continuous animations. Use EXCLUSIVELY Framer Motion's `useMotionValue` and `useTransform` outside the React render cycle to prevent performance collapse on mobile.

### Perpetual Micro-Interactions
When `MOTION_INTENSITY > 5`, embed continuous, infinite micro-animations (Pulse, Typewriter, Float, Shimmer, Carousel) in standard components.

Apply premium Spring Physics:
```javascript
type: "spring", stiffness: 100, damping: 20
```

No linear easing.

### Layout Transitions
Always utilize Framer Motion's `layout` and `layoutId` props for smooth re-ordering, resizing, and shared element transitions.

### Staggered Orchestration
Do not mount lists or grids instantly. Use:
- `staggerChildren` (Framer Motion)
- CSS cascade: `animation-delay: calc(var(--index) * 100ms)`

**CRITICAL:** For `staggerChildren`, the Parent (`variants`) and Children MUST reside in the identical Client Component tree. If data is fetched asynchronously, pass data as props into a centralized Parent Motion wrapper.

---

## Motion Intensity Levels (1-10)

### 1-3 (Static)
- No automatic animations.
- CSS `:hover` and `:active` states only.

### 4-7 (Fluid CSS)
```css
transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
```
- Use `animation-delay` cascades for load-ins.
- Focus strictly on `transform` and `opacity`.
- Use `will-change: transform` sparingly.

### 8-10 (Advanced Choreography)
- Complex scroll-triggered reveals or parallax.
- Use Framer Motion hooks.
- NEVER use `window.addEventListener('scroll')`.

---

## The Motion-Engine Bento Paradigm

For modern SaaS dashboards, enforce "Vercel-core meets Dribbble-clean" aesthetic.

### Core Philosophy
- **Aesthetic:** High-end, minimal, functional.
- **Palette:** Background `#f9fafb`. Cards `#ffffff` with `border-slate-200/50`.
- **Surfaces:** `rounded-[2.5rem]`. Diffusion shadow: `shadow-[0_20px_40px_-15px_rgba(0,0,0,0.05)]`.
- **Typography:** Geist, Satoshi, or Cabinet Grotesk. `tracking-tight` for headers.
- **Labels:** Place titles/descriptions **outside and below** cards.
- **Padding:** `p-8` or `p-10` inside cards.

### Animation Engine Specs
All cards must contain **Perpetual Micro-Interactions:**
- **Spring Physics:** `type: "spring", stiffness: 100, damping: 20`
- **Layout Transitions:** Heavy use of `layout` and `layoutId` props
- **Infinite Loops:** Every card has an "Active State" that loops infinitely
- **Performance:** Wrap dynamic lists in `<AnimatePresence>`

**PERFORMANCE CRITICAL:** Any perpetual motion or infinite loop MUST be memoized (`React.memo`) and isolated in its own microscopic Client Component. Never trigger re-renders in the parent layout.

### The 5-Card Archetypes

1. **The Intelligent List:** Vertical stack with infinite auto-sorting loop. Items swap positions using `layoutId`.

2. **The Command Input:** Search/AI bar with multi-step Typewriter Effect. Cycles through prompts with blinking cursor and "processing" shimmer gradient.

3. **The Live Status:** Scheduling interface with "breathing" status indicators. Pop-up notification badge emerges with "Overshoot" spring, stays 3 seconds, vanishes.

4. **The Wide Data Stream:** Horizontal "Infinite Carousel" of data cards. Seamless loop using `x: ["0%", "-100%"]`.

5. **The Contextual UI (Focus Mode):** Document view with staggered text highlight, followed by "Float-in" of floating action toolbar.

---

## GSAP / ThreeJS Usage

Default to Framer Motion for UI/Bento interactions.

Use GSAP (ScrollTrigger/Parallax) or ThreeJS/WebGL EXCLUSIVELY for:
- Isolated full-page scrolltelling
- Canvas backgrounds

**CRITICAL:** Never mix GSAP/ThreeJS with Framer Motion in the same component tree. Wrap in strict `useEffect` cleanup blocks.
