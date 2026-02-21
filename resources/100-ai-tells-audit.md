# The Comprehensive Audit: 100 Indicators of AI-Generated Design

This audit categorizes specific indicators ("Tells") that suggest a design may be AI-generated, along with the underlying causes and specific countermeasures to fix them.

## 6.1 Category: Visual Syntax (Colors, Gradients, Shadows)

| # | The "AI Tell" (Indicator) | Why it happens (Cause) | The Countermeasure (Fix) |
|---|---|---|---|
| 1 | Purple/Blue Gradient | Default "Tech" aesthetic in training data (SaaS boom). | Use semantic color tokens; derive palette from unique brand photos. |
| 2 | Neon Glow / Outer Glow | Excessive use of standard CSS box-shadow. | Use subtle border colors or inner shadows instead of outer glows. |
| 3 | Standard Tailwind Blue (`bg-blue-600`) | High frequency of this utility class in training codebases. | Define a custom primary color in `tailwind.config.js`. |
| 4 | Glassmorphism Blur | Trend in 2021-2022 data; AI mimics "modernity". | Use solid opacity or texture; use blur only when conceptually relevant. |
| 5 | Pure Black Shadows | Usage of `#000` with opacity (e.g., `rgba(0,0,0,0.1)`). | Use colored shadows (e.g., dark blue shadow on blue BG) for depth. |
| 6 | Perfectly Even Gradients | Linear gradient from top-left to bottom-right (`45deg`). | Use radial gradients, noise overlays, or mesh gradients. |
| 7 | Dark Mode = Pure Black | Standardization on `#000000` background. | Use "Off-Black" or dark Charcoal/Navy (`#121212`) for less eye strain. |
| 8 | Lack of Texture | AI generates flat vectors; texture is complex to code. | Add noise, grain, or subtle patterns to backgrounds. |
| 9 | Oversaturated Accents | AI selects colors with maximum saturation to "stand out". | Desaturate accent colors to blend them better with neutrals. |
| 10 | Inconsistent Lighting | Shadows suggest different light sources. | Audit all shadows to ensure a consistent light source. |
| 11 | "Standard" Gray Palette | Usage of the standard `gray-500` scale. | Tint grays with a hint of blue or warm yellow. |
| 12 | Excessive Gradient Text | Headers with Text-Fill-Gradient. | Use gradient text sparingly, only for 1-2 keywords. |

## 6.2 Category: Typography & Micro-Typography

| # | The "AI Tell" (Indicator) | Why it happens (Cause) | The Countermeasure (Fix) |
|---|---|---|---|
| 13 | Inter Font Everywhere | The most common Open Source UI font in datasets. | Use distinct pairing (e.g., Serif for Header, Sans for Body). |
| 14 | H1 "Screams" (Too big) | Logic assumes "Importance = Size" without nuance. | Use weight, color, or capitalization for hierarchy, not just size. |
| 15 | Missing Letter Spacing | Default `tracking-normal` on all text. | Use negative tracking for large headers; positive for Small Caps. |
| 16 | Standard Line Height | Default `leading-normal` (1.5) on headers. | Tighten leading for headers (1.1-1.2); loosen for body text. |
| 17 | Orphans (Widowed words) | AI doesn't check line breaks; leaves single words. | Use `text-wrap: balance` or `pretty` in CSS. |
| 18 | Only "Geometric" Sans | Bias towards geometric/modernist fonts (Poppins). | Explore Humanist or Grotesque fonts for more character. |
| 19 | No Serif Usage | Serifs are statistically rarer in SaaS UIs. | Introduce a serif font for editorial/elegant vibes. |
| 20 | Generic Font Weights | Usage of only 400 (Regular) and 700 (Bold). | Use 500 (Medium) and 600 (SemiBold) for subtlety. |
| 21 | All-Caps Subheaders | A very frequent pattern for "Eyebrow" text. | Use lowercase italics or sentence case for a softer look. |
| 22 | Missing Text Contrast | Gray text on gray background fails WCAG. | Check contrast ratios (Target: min. 4.5:1). |
| 23 | No Tabular Numbers in tables | Figures wiggle due to variable width. | Enable `font-variant-numeric: tabular-nums` for data. |

## 6.3 Category: Layout & Spatial Patterns

| # | The "AI Tell" (Indicator) | Why it happens (Cause) | The Countermeasure (Fix) |
|---|---|---|---|
| 24 | Bento-Grid Obsession | Modular code is easier to generate than overlaps. | Break the grid; use asymmetry or overlapping elements. |
| 25 | 3-Column Feature Row | The "Standard Model" for web design sections. | Use a 2-column Zig-Zag layout or horizontal scrolling. |
| 26 | Perfect Centering | `flex justify-center` is the safest alignment. | Try left-aligned content for better readability. |
| 27 | Uniform Border Radius | `rounded-lg` is applied indiscriminately to everything. | Vary radius: tighter for inner elements, softer for containers. |
| 28 | Full-Width Sections | Sections consistently span 100% width without whitespace. | Use "Container" constraints; allow whitespace on the sides. |
| 29 | Cards of Equal Height | Forced symmetry, even if content varies. | Allow masonry layouts or variable heights. |
| 30 | "Sticky" Headers | Default behavior in many Nav templates. | Make sticky optional or Hide-on-Scroll. |
| 31 | No Overlap/Depth | Elements sit next to each other, never on top. | Use negative margins (`-mt-10`) to create depth/overlap. |
| 32 | Symmetrical Padding | `py-20` (top/bottom) is always the same. | Adjust optical spacing; bottom often needs more space. |
| 33 | The "Sidebar" Rut | Dashboards always use a left fixed sidebar. | Try Top-Nav or floating Command Menus (Cmd+K). |
| 34 | Missing Whitespace | AI tends to pack info ("Horror Vacui"). | Double the whitespace. Let the design breathe. |

## 6.4 Category: Component Architecture

| # | The "AI Tell" (Indicator) | Why it happens (Cause) | The Countermeasure (Fix) |
|---|---|---|---|
| 35 | Generic "Card" Look | Border + Shadow + White BG = The universal card. | Remove border; use only background color or only spacing. |
| 36 | Primary/Secondary Buttons | Always one filled, one outlined (Ghost). | Use text links or tertiary buttons to reduce visual noise. |
| 37 | Pill-Shape Badges | "New" or "Beta" badges are always round pills. | Try square badges, flags, or pure text labels. |
| 38 | Accordion FAQs | The standard pattern for "FAQ" sections. | Use a side-by-side list or a searchable Help Center. |
| 39 | Carousel Testimonials | 3 cards visible, dots underneath. A classic. | Use a "Wall of Love" masonry grid or embedded tweets. |
| 40 | Pricing Table Towers | 3 columns, middle one "Recommended" and bigger. | Highlight the "Recommended" one with color, not just size. |
| 41 | Modals for Everything | Excessive use of popups for simple actions. | Use inline editing or slide-over panels instead. |
| 42 | Avatar Circles | User profiles are always perfect circles. | Try "Squircles" or rounded squares. |
| 43 | Toggle-Switch Cliché | Dark Mode toggles are always a Sun/Moon switch. | Use a dropdown or system preference detection. |
| 44 | Search Bar Top Right | Always located top right in the navigation. | Place search centrally or use a Command Palette overlay. |
| 45 | Footer "Link Farm" | 4 columns of links in the footer. | Simplify footer; focus on main paths and legal. |

## 6.5 Category: Iconography & Imagery

| # | The "AI Tell" (Indicator) | Why it happens (Cause) | The Countermeasure (Fix) |
|---|---|---|---|
| 46 | Lucide/Feather Icons | The "Times New Roman" of icons in React. | Use a unique set (Phosphor, Heroicons Micro, or Custom). |
| 47 | Rocketship Icon | Universal metaphor for "Launch" or "Speed". | Use a bolt, spark, or abstract motion line. |
| 48 | Shield Icon | Universal metaphor for "Security". | Use a lock, fingerprint, or vault graphic. |
| 49 | Floating 3D Objects | Abstract spheres/cubes (Spline style) are trendy. | Use real product photography or human-centered illustrations. |
| 50 | Stock "Diverse Teams" | Uncanny stock photos of people pointing at screens. | Use candid photos of the real team or black & white style. |
| 51 | Isometric Illustrations | The "Corporate Memphis" style (big limbs). | Avoid flat vector art; use collage or hand-drawn styles. |
| 52 | Generic Logo Placeholders | "Company Name" with generic geometric shape. | Create a simple typographic logo or use a monogram. |
| 53 | Inconsistent Stroke Width | Icons have different stroke weights (1px vs 2px). | Audit all icons for consistent stroke weight. |
| 54 | Missing Favicon | AI generates the page but forgets the tab icon. | Always generate a branded favicon. |
| 55 | Hallucinated Details | Illustrations with extra fingers or gibberish text. | Manually check every pixel of AI art. |

## 6.6 Category: Copywriting & "Tone of Voice"

| # | The "AI Tell" (Indicator) | Why it happens (Cause) | The Countermeasure (Fix) |
|---|---|---|---|
| 56 | "Unlock / Unleash" | Most likely next-token for "Potential". | Use specific verbs: "Build", "Create", "Scale", "Save". |
| 57 | "Seamless Integration" | The standard descriptor for APIs. | Describe how it integrates (e.g., "One-Click-Connect"). |
| 58 | "Elevate your..." | Vague, aspirational language. | Focus on outcome: "Double your revenue." |
| 59 | "Game-changer" | Overused superlative. | Use specific praise: "Saves us 10 hours a week." |
| 60 | "In the world of..." | Classic essay intro cliché. | Cut the preamble. Start with the problem. |
| 61 | "Delve" | A literary word overrepresented in LLMs. | Use "Explore", "Dive in", or "Analyze". |
| 62 | "Tapestry" | Poetic filler word. | Use "Network", "System", or "Collection". |
| 63 | Title Case Headers | "Writing Every Word Like This". | Use sentence case: "Just like a normal sentence." |
| 64 | Exclamation Marks! | Artificial enthusiasm in success messages. | Remove exclamation marks. Be confident, not loud. |
| 65 | "Oops!" Errors | Faux-polite anthropomorphization. | Be direct: "Connection failed. Please try again." |
| 66 | Passive Voice | "Mistakes were made." | Use active voice: "We couldn't save your changes." |

## 6.7 Category: Interaction & States

| # | The "AI Tell" (Indicator) | Why it happens (Cause) | The Countermeasure (Fix) |
|---|---|---|---|
| 67 | No Hover Status | Buttons don't change on mouse hover. | Add `hover:bg-opacity-90` or `transform: scale(1.02)`. |
| 68 | Instant Transitions | Changes happen with 0ms delay (abrupt). | Add `transition-all duration-200` to interactive elements. |
| 69 | Missing Focus Ring | No outline when tabbing (Accessibility Fail). | Ensure `focus-visible:ring` is active. |
| 70 | Dead Links | Buttons that click but do nothing (`href="#"`). | Link to real 404 pages or visually disable the button. |
| 71 | No "Active" Status | Nav links don't show which page you are on. | Style the current page link differently (bold/colored). |
| 72 | Scroll Jumping | Clicking anchor jumps immediately (no smooth scroll). | Add `html { scroll-behavior: smooth; }`. |
| 73 | Generic Loader | A spinning circle as the standard loader. | Use Skeleton Screens (Shimmer effect) or custom animation. |
| 74 | Missing "Empty State" | Dashboard with 0 items is simply empty. | Design a "Getting Started" illustration for empty views. |
| 75 | Alert Fatigue | Usage of system alerts (`window.alert`) for errors. | Use Custom Toast notifications (e.g., Sonner). |

## 6.8 Category: Code Structure & Semantics

| # | The "AI Tell" (Indicator) | Why it happens (Cause) | The Countermeasure (Fix) |
|---|---|---|---|
| 76 | Div Soup | `<div class="nav">` instead of `<nav>`. | Use Semantic HTML: `<main>`, `<article>`, `<aside>`. |
| 77 | Inline Styles | `style="margin-top: 20px"` mixed with classes. | Move all styling to CSS classes/Tailwind utilities. |
| 78 | Hardcoded Values | `width: 350px` (breaks on mobile). | Use relative units (`w-full`, `max-w-md`) or rem/em. |
| 79 | Missing Alt-Text | `alt=""` or `alt="image"`. | Describe image content for screen readers. |
| 80 | Z-Index Wars | `z-index: 9999` hacks. | Establish a clean Z-Index scale in the theme. |
| 81 | Commented-out Code | AI leaves artifacts behind. | Clean/remove all comments before deployment. |
| 82 | Import Hallucinations | Importing libraries that aren't installed. | Check if `package.json` matches imports. |
| 83 | Unused Classes | Classes that do nothing (e.g., `flex` on a block). | Lint CSS; remove redundant utilities. |
| 84 | Missing Meta Tags | No `og:image` or description. | Add clean SEO and Social Sharing meta tags. |

## 6.9 Category: Data Patterns (The "Jane Doe" Effect)

| # | The "AI Tell" (Indicator) | Why it happens (Cause) | The Countermeasure (Fix) |
|---|---|---|---|
| 85 | "Acme Corp" | The Wile E. Coyote of company names. | Use realistic fake names (e.g., "Lumina Logistics"). |
| 86 | "Jane/John Doe" | The laziest name placeholder. | Use a name generator for diversity (e.g., "Sarah Chen"). |
| 87 | +1 (555) 123-4567 | The standard fake phone number from US movies. | Use localized format or realistic fakes (555 is obvious). |
| 88 | 123 Main St. | Standard address. | Use a real-sounding address (e.g., "42 Market Street"). |
| 89 | Perfect Round Numbers | "$100.00" or "50% Growth". | Use realistic data: "$99.00" or "47% Growth". |
| 90 | Short Lorem Ipsum | One sentence of Lorem Ipsum repeated. | Use real draft text, never Lorem Ipsum. |
| 91 | Repetitive Dates | All blog posts dated "Jan 1, 2024". | Randomize dates to appear organic. |
| 92 | Duplicate Avatars | The same face for multiple users. | Ensure unique assets for every distinct user. |

## 6.10 Category: Strategic Omissions (What AI Forgets)

| # | The "AI Tell" (Indicator) | Why it happens (Cause) | The Countermeasure (Fix) |
|---|---|---|---|
| 93 | No Legal Texts | AI prioritizes features over compliance. | Always add Privacy/ToS links in the footer. |
| 94 | Missing "Back" Buttons | Dead ends in User Flows. | Ensure every page has a way to go back. |
| 95 | No 404 Page | Forgetting the "Page Not Found" experience. | Design a custom, helpful 404 page. |
| 96 | Missing Favicon | (Repeated for emphasis) Often forgotten. | Add `favicon.ico`. |
| 97 | No Loading Skeleton | Content jumps while loading. | Add loading states to prevent Layout Shift (CLS). |
| 98 | Missing Validation | Forms submit without email checks. | Add client-side validation (Zod/React Hook Form). |
| 99 | No "Skip to Content" | Vital for keyboard users. | Build in a hidden "Skip to content" link. |
| 100 | Cookie Banner Blindness | AI builds the page without GDPR compliance. | Add a compliant Cookie Consent Manager. |
