# The Creative Coding Compendium

A comprehensive collection of high-end design patterns, motion concepts, and visual effects for modern web design.

## 1. Kinetic Typography
Text is no longer static, but acts as a fluid material or physical object within the digital space.

*   **Velocity-Based Skew:** Typography that leans or distorts based on scroll speed. Fast scrolling creates a sharp italicized skew; stopping causes an elastic snap-back effect, adding physical weight to the interface.
*   **Infinite Marquee:** A seamlessly looping band of text (horizontal or vertical) that creates constant momentum. Advanced versions reverse direction based on scroll behavior.
*   **Variable Font Animation:** Dynamic interpolation of font weight, width, or slant triggered by scroll position or mouse proximity, making the text feel alive and responsive.
*   **Path Typography:** Text that flows along complex SVG paths—spirals, waves, or custom shapes—often animating along the path to guide the user's eye.
*   **Glyph Substitution / Hacker Text:** Characters randomly cycle through numbers, symbols, or alternative glyphs before locking into the final legible word, simulating a digital decoding process (Matrix-style).
*   **Mix-Blend-Mode Typography:** Text positioned over imagery using difference, exclusion, or overlay blending modes, dynamically inverting colors based on the background beneath it.
*   **Masked Text:** Heavy typography acting as a window or stencil, revealing video or animated imagery inside the character shapes while masking the rest.
*   **Outlined to Fill Transition:** Typography that exists initially as a delicate stroke (outline) and fills with solid color or gradient upon interaction or scroll entry.

## 2. Immersive Scrolling
Scrolling controls the timeline and narrative flow of the experience, rather than just vertical position.

*   **Lenis / Locomotive Scroll (Smooth Scroll):** Decouples scrolling from standard browser physics, adding inertia and damping for a heavy, luxurious, and cinematic feel.
*   **Pinning / Sticky Sections:** A central visual element (e.g., a 3D product render) locks into the center of the viewport while narrative text sections scroll over or around it.
*   **Horizontal-Vertical Hybrid:** A seamless transition where vertical scrolling translates into horizontal movement (often used for galleries or timelines) before returning to a vertical flow.
*   **Parallax Stack:** Sections stack on top of one another like a deck of cards. The previous section remains stationary and slightly darkens as the new section slides up to cover it.
*   **Scrubbing Video/Animation:** The scroll wheel acts as a playback head for a video or 3D sequence. Scrolling down advances the frame; scrolling up rewinds it.
*   **Mask Reveal on Scroll:** Visuals enter the viewport through expanding geometric masks (circles, wipes, or custom shapes) controlled directly by scroll progress.

## 3. Micro-Interactions & Cursor
The tactile connection between the user and the digital interface.

*   **Custom WebGL Cursor:** The cursor is replaced by a fluid simulation, light source, or distortion field that physically alters the background content in real-time.
*   **Magnetic Elements:** Interactive buttons or links that have a gravitational pull. As the cursor approaches, the element physically moves toward the mouse, creating a feeling of attraction.
*   **Trailing Cursor:** The primary cursor is followed by visual artifacts—lines, dots, or ghosts—that catch up with a smooth linear interpolation (Lerp) delay.
*   **Contextual Cursor:** The cursor morphs its shape or displays text labels based on the element underneath (e.g., transforming into a "View" eye icon over a gallery or a "Play" button over video).
*   **Hover Displacement:** Images that behave like liquid or jelly when hovered, distorting in the direction of the cursor movement using displacement maps.
*   **Spotlight Reveal:** The interface is shrouded in darkness, and the cursor acts as a torch or spotlight, revealing content only within its immediate radius.

## 4. WebGL & 3D
Utilizing shaders and 3D contexts to create depth, atmosphere, and realism.

*   **Fluid Simulation:** Interactive smoke, water, or oil simulations that swirl and mix based on cursor velocity and direction.
*   **Grain & Noise Shaders:** A fine, animated film grain overlay applied globally to break digital sterility and add tactile texture to the screen.
*   **Refraction / Glassmorphism:** 3D objects rendered with glass properties that physically refract, blur, and distort the background elements behind them.
*   **Particle Systems:** Images or forms composed of thousands of individual points that disperse, explode, or morph into new shapes upon interaction.
*   **Depth Map Parallax:** Using grayscale depth maps to fake 3D dimensionality on 2D images, causing foreground and background elements to shift at different rates based on mouse movement.
*   **Chromatic Aberration (RGB Split):** A post-processing effect that separates red, green, and blue channels at the edges of the screen or during rapid motion, mimicking lens distortion or digital glitching.
*   **Blobs & Organic Shapes:** Abstract, constantly morphing geometries (metaballs) in the background that resemble lava lamps or biological forms.

## 5. Layout & Grid Systems
A departure from standard columns towards artistic, architectural, and editorial grids.

*   **Bento Grid:** A modular layout style inspired by bento boxes, where content is organized into varied, rounded rectangular distinct cells.
*   **Neo-Brutalism:** A raw aesthetic featuring high contrast, thick black strokes, visible grid lines, monospace typography, clashing colors, and a lack of shadows or smoothing.
*   **Broken Grid / Asymmetry:** Elements that deliberately ignore the column structure, overlapping other elements, bleeding off the screen, or placed with calculated randomness.
*   **Whitespace Maximization:** The aggressive use of negative space to force extreme focus on a single, often small, central element.
*   **Rule Lines / Technical UI:** The use of fine 1px lines, crosshairs, and coordinate numbers as decorative elements to create a technical, blueprint, or HUD (Heads-Up Display) aesthetic.

## 6. Transitions & Loading
The journey from point A to point B treated as a standalone visual experience.

*   **Preloader Count-Up:** A loading screen featuring oversized typography counting from 0% to 100%, often stylized or strictly monospace.
*   **Curtain Transition:** A solid color or image that sweeps up like a theater curtain to cover the old page and reveal the new one.
*   **Morphing SVG Transitions:** The shape of the current viewport or image fluidly reshapes into the container of the next page's hero element.
*   **WebGL Distortion Transition:** The current view transitions to the next by shattering, pixelating, or liquefying the screen content.
*   **Staggered Entry:** Elements do not appear all at once but cascade in with slight delays (line by line), often combining a soft Y-axis translation with an opacity fade.

## 7. Visual Effects
Visual nuances that signal high production value.

*   **Dithering:** A retro-inspired shading technique using dot patterns to simulate gradients and shadows, evoking a nostalgic or lo-fi tech aesthetic.
*   **Backdrop Blur / Frosted Glass:** UI elements (like navigation bars) that blur the content scrolling beneath them, mimicking frosted glass materials.
*   **Invert Filters:** Specific zones or images that invert their color values instantly when hovered or scrolled over.
*   **Isometric Illustration:** 3D representations rendered without perspective convergence (parallel lines), often used for technical diagrams or abstract miniature worlds.
