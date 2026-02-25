# Architecture & Conventions

## Dependency Verification [MANDATORY]
Before importing ANY 3rd party library (e.g. `framer-motion`, `lucide-react`, `zustand`), check `package.json`. If missing, output the installation command before providing code. **Never** assume a library exists.

## Framework & Interactivity
- React or Next.js. Default to Server Components (`RSC`).
- **RSC SAFETY:** Global state works ONLY in Client Components. Wrap providers in `"use client"`.
- **INTERACTIVITY ISOLATION:** If motion/glass effects are active, extract interactive UI as isolated leaf component with `'use client'`. Server Components render static layouts only.

## State Management
- Use local `useState`/`useReducer` for isolated UI.
- Use global state strictly for deep prop-drilling avoidance.

## Styling Policy
- Tailwind CSS (v3/v4) for 90% of styling.
- **TAILWIND VERSION LOCK:** Check `package.json` first. Do not use v4 syntax in v3 projects.
- **T4 CONFIG GUARD:** For v4, do NOT use `tailwindcss` plugin in `postcss.config.js`. Use `@tailwindcss/postcss` or Vite plugin.

## Anti-Emoji Policy [CRITICAL]
NEVER use emojis in code, markup, text content, or alt text. Replace with high-quality icons (Radix, Phosphor) or clean SVG primitives.

## Responsiveness & Spacing
- Standardize breakpoints: `sm`, `md`, `lg`, `xl`.
- Contain layouts: `max-w-[1400px] mx-auto` or `max-w-7xl`.
- **Viewport Stability [CRITICAL]:** NEVER use `h-screen` for full-height Heroes. ALWAYS use `min-h-[100dvh]` to prevent layout jumping on mobile (iOS Safari).
- **Grid over Flex-Math:** NEVER use complex flexbox percentage math (`w-[calc(33%-1rem)]`). ALWAYS use CSS Grid (`grid grid-cols-1 md:grid-cols-3 gap-6`).

## Icons
Use exactly `@phosphor-icons/react` or `@radix-ui/react-icons`. Standardize `strokeWidth` globally (e.g., `1.5` or `2.0`).

## Forms
- Label MUST sit above input.
- Helper text optional but should exist in markup.
- Error text below input.
- Use standard `gap-2` for input blocks.
