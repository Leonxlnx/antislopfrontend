# 2026 AI Design Tells & Tool Signatures

A comprehensive breakdown of the most noticeable indicators ("tells") that instantly expose a design or codebase as AI-generated (especially from tools like v0.dev, Lovable.dev, and Claude), along with structural and behavioral patterns to avoid.

## 1. Visual Design Characteristics (The Most Noticeable "Tells")
*   **The Purple/Blue Gradient Obsession:** A purple-blue gradient with glowing effects, almost always running from top-left to bottom-right on a white background. This is the absolute #1 indicator for 2025/2026 AI outputs.
*   **Arbitrary Glowing Effects:** Subtle, neon-like glows applied to buttons, cards, or text without structural purpose.
*   **Purposeless Whitespace:** Massive gaps between elements that serve no strategic or optical purpose (the AI uses space decoratively rather than structurally).
*   **Predictable Perfect Symmetry:** Centered content, cookie-cutter cards, and standard grid layouts without any structural breaks or tension.
*   **Rounded Blocks + Blue/White Contrast:** Exceedingly common in outputs from Lovable.dev and Claude.
*   **Flat Solid Backgrounds:** A complete lack of depth. No noise textures, grain overlays, gradient meshes, layered transparencies, or dramatic shadows.
*   **The "Soulless" Vibe-Coded Aesthetic:** Technically clean, but universally recognizable as generic. Everyone spots it immediately.
*   **Lack of Tension:** Missing asymmetry, overlapping elements, diagonal flow, or grid-breaking components.
*   **Overly "Balanced" Aesthetics:** Timid, evenly distributed colors and elements rather than bold, dominant focal points.

## 2. Typography
*   **Inter/Roboto Default:** Relying on `Inter`, `Roboto`, `Arial`, `system-ui`, or `Space Grotesk` as the default typeface. Banning Inter is the fastest way to de-program the "AI look."
*   **Poor Font Pairing:** Lacking a character-rich display font paired with a refined body font.
*   **Robotic Hierarchy:** Mathematically perfect hierarchies without manual optical adjustments (line-height and letter-spacing left exactly at Tailwind defaults).
*   **Sterile Text:** Overly "clean" fonts lacking character (e.g., failing to use high-contrast serifs in minimalist designs).

## 3. Colors & Theme
*   **Clichéd Color Schemes:** Purple/pastel overload, particularly purple-on-white.
*   **Overly Balanced Palettes:** Lacking a dominant primary color complemented by a sharp, unexpected accent.
*   **Missing CSS Variables:** Color values hardcoded randomly rather than utilizing a cohesive, manually-feeling token system.

## 4. Layout & Composition
*   **Standardized Sections:** Predictable navbars, generic hero sections, and 3-column feature grids with zero element of surprise.
*   **No "Memorable Element":** Lacking a signature animation, a unique interactive detail, or a distinct focal point.
*   **Uncontrolled Density:** Either extremely packed layouts or overly generous negative space without contextual justification.

## 5. Animations & Interactions (Micro-Interactions)
*   **Purposeless Animation:** Motion "sprinkled everywhere" (random hover states, glowing buttons, unnecessary transitions) without choreographing the user's focus.
*   **Basic Hover States:** Lacking high-end Framer Motion-style physics, staggered reveals, orchestrated page-load sequences, or scroll-triggered reveals.
*   **Dead Micro-Interactions:** Missing tactile feedback (e.g., button scale on press, card border glow on hover, nav underline slide).
*   **Static Pages:** "Dead" designs without lift-shadows, transforms, or creative physical animations.

## 6. Icons, Assets & Components
*   **Default Icon Libraries:** Relying heavily on Lucide-react, Bootstrap Icons, or emojis instead of premium sets like Phosphor, Streamline, or custom SVGs.
*   **Uncustomized UI Kits:** Using default `shadcn/ui` components without heavy customization (leaving default border-radiuses, shadows, and hover states untouched).
*   **Missing Materiality:** Failing to implement complex effects like Liquid Glass or frosted refraction.
*   **Generative Image Artifacts:** Using AI-generated placeholder images with typical errors (extra limbs, awkward lighting, gibberish text).

## 7. Source Code Hints (Inspect Element / View Source)
*   **data-* Attributes:** Traces of AI generation tools or Notion copy-paste (e.g., `<p data-start="104" data-end="490">`).
*   **Descriptive Comments:** Comments saying *what* the code does rather than *why* (e.g., `// This is a button`, `// AI-generated`).
*   **Emojis in `console.log`:** Bizarre console logs like `console.log("Success ✅")` (human developers rarely do this).
*   **Useless Comments:** Over-commenting every single line of standard framework code.
*   **Over-Complicated Logic:** Turning a 3-line task into 20 lines with nested conditionals, redundant variables, and outdated patterns.
*   **Strange Meta-Tags:** Meta-tags with unusual spelling or AI-typical phrasing.
*   **Baroque Code Structure:** Overly verbose and overly structured code (150 lines where 50 would suffice).
*   **Encoding Oddities:** Smart quotes, weird capitalization, or `&nbsp;` artifacts from chat UI copy-pasting.

## 8. Text & Content Characteristics
*   **Em-Dash Overuse:** Excessive use of em-dashes (—) in standard body text.
*   **The "Perfect" Essay Structure:** Rigid structure using topic sentences, transition words ("Additionally", "In conclusion", "Ultimately"), and perfect intro/outro pairs.
*   **Overly Balanced Sentences:** "While X is true, Y is also important."
*   **Generic Brand Names:** Relying on names like "NaturalWrite", "SmartFlow", or "VibeCraft" (instantly recognizable as AI).
*   **Keyword Stuffing:** Cramming buzzwords without strategic intent.
*   **Vague Positivity:** User reviews that say "Great product, highly recommend" without providing specific details.
*   **Hallucinations & No Human Touch:** Lacking personal anecdotes, specific data points, or a grounded human perspective.

## 9. Tool-Specific Signatures (2025/2026)
*   **Claude / Anthropic:** The classic purple-gradient + Inter font combination.
*   **v0.dev (Vercel):** Stacked blocks, placeholder-heavy sections, generic UI kits, and often a disconnected / low-quality feel.
*   **Lovable.dev:** Rounded blocks, blue-white contrast, and the undeniable "lovable generated website" aesthetic.
*   **Bolt.new / Cursor:** The basic Tailwind + Shadcn look without any customization. A "vibecoded landing page" often translates to this exact AI slop stack.
*   **The General Rule:** If it looks like "v0 + Claude + shadcn without prompt optimization," it's AI slop.

## 10. Other / Behavioral & Meta Hints
*   **Missing Accessibility:** Poor contrast, missing ARIA tags, and terrible keyboard navigation (AI tools often skip this unless explicitly forced).
*   **"Generated" Responsiveness:** Flawless on desktop, but featuring purposeless or awkward adaptations on mobile.
*   **Strategically Empty:** Technically correct but entirely lacking a core idea (the "beautifully wrapped gift box with nothing inside").
*   **Cumulative Slop:** The result of rapid iteration and appending features without human refactoring or polishing.
*   **Zero Polish:** Built in 10 minutes without any manual refinement or optical adjustments.
