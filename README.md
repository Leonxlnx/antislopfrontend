# Design Taste (Frontend Engineering)

A skill for AI coding agents to build high-end, premium frontend interfaces. The goal is to eradicate generic "AI slop" (Probability Collapse) and enforce strict engineering metrics, CSS hardware acceleration, and balanced design architectures.

---

## How It Works

This repository contains the **Design Taste Frontend Skill** (`SKILL.md`), which serves as a hardcore prompt and rulebook for LLM-based coding agents (like Claude, Cursor, v0, etc.).

Instead of just telling the AI "don't make it look bad," this skill establishes a deterministic engineering framework:
- **Strict Component Architecture:** Prevents "God Components" by enforcing modular React trees and strict Layout vs. UI Primitive separation.
- **Deterministic Typography:** Bans default text pairing and enforces semantic spacing (e.g., `tracking-tighter` on massive Sans-Serif metrics like Vercel or Linear).
- **Interactive UI States:** Forces the AI to generate loading skeletons, empty states, and error validations instead of static "happy paths."
- **Performance:** Enforces CSS hardware acceleration (`transform`, `opacity`) and strict GPU-cost limits for grain/noise filters.

---

## The Configuration Dials
Before running the agent, you can configure internal variables (1-10) directly in the prompt to deterministically control the CSS output:

1. **DESIGN_VARIANCE:** Controls symmetry and structural layout offsets (from grid-perfect to masonry asymmetry).
2. **MOTION_INTENSITY:** Controls JS payload, CSS spring physics, and GSAP/Framer complexity. 
3. **VISUAL_DENSITY:** Controls spacing tokens (e.g., `py-32` vs `py-2`) and typography tracking.
4. **EXPERIMENTAL_AESTHETICS:** Controls texture, mesh gradients, and color boundaries.

---

## Configuration Profiles (Examples)
Use these presets to instantly toggle the visual character of the output:

### 1. High-End Creative (The "Showcase" Look)
**Best for:** Portfolios, Brand Launches, Experimental Landing Pages.
- **`DESIGN_VARIANCE: 9`** (Wilde Asymmetrie, Masonry-Layouts, überlappende Sektionen)
- **`MOTION_INTENSITY: 8`** (GSAP-Parallax, Staggered Orchestration, magnetische Buttons)
- **`VISUAL_DENSITY: 2`** (Extremer Weißraum, massive Headlines, Editorial-Stil)
- **Result:** Ein visuelles Erlebnis, das wie eine digitale Kunst-Installation wirkt.

### 2. Balanced Premium (The "Modern SaaS" Look)
**Best for:** Startups, Marketing-Pages, Professional Services.
- **`DESIGN_VARIANCE: 5`** (Leichte Offsets, subtile Überlappungen, aber klarer Flow)
- **`MOTION_INTENSITY: 5`** (Flüssige CSS-Transitions, sanfte Load-Ins, tactile Hover-States)
- **`VISUAL_DENSITY: 5`** (Standardisierte Abstände, sehr gute Lesbarkeit)
- **Result:** Hochmodern, vertrauenerweckend und extrem "polished" – wie ein Stripe- oder Linear-Produkt.

### 3. Minimalist Standard (The "Utility" Look)
**Best for:** Dashboards, Dokumentationen, Interne Tools.
- **`DESIGN_VARIANCE: 2`** (Strikte Symmetrie, klassischer 12-Spalten-Grid)
- **`MOTION_INTENSITY: 2`** (Nur essentielle Interaktionen, Fokus auf Geschwindigkeit)
- **`VISUAL_DENSITY: 8`** (Hohe Informationsdichte, kompakte Listen, Mono-Fonts für Daten)
- **Result:** Funktional, schnell und übersichtlich. Sieht "normal" aus, aber durch die Design-Taste Regeln ohne den billigen AI-Beigeschmack.

---

## Installation

You can clone this skill directly into your project's agent skills directory.

### Project-Level Installation
```bash
git clone https://github.com/Leonxlnx/taste-skill.git .agent/skills/taste-skill
```

### Global Installation (Mac / Linux)
```bash
git clone https://github.com/Leonxlnx/taste-skill.git ~/.agent/skills/taste-skill
```

### Global Installation (Windows PowerShell)
```powershell
git clone https://github.com/Leonxlnx/taste-skill.git "$HOME\.agent\skills\taste-skill"
```

---

## Usage

Simply point your agent to the skill file and configure your dials:

> "Read `.agent/skills/taste-skill/SKILL.md`. Set VISUAL_DENSITY to 8 and MOTION_INTENSITY to 5. Build a data-heavy Fintech Dashboard."

---

## Resources Included

The `resources/` folder acts as an internal knowledge base that the Skill relies on:
- `2026-ai-tells-signatures.md`: The definitive guide to spotting generated UI (Lovable, v0, Claude traits).
- `creative-coding-compendium.md`: High-end library of motion patterns and advanced CSS.
- `100-ai-tells-audit.md`: Aggregated anti-patterns and typography failures to avoid.

---

## License

MIT - use freely, remix aggressively.
