---
name: apple-web-design-science
version: 0.1.0
description: >
  Design and implement web applications using an Apple-platform-inspired
  visual and interaction system derived from Apple HIG, current Liquid Glass
  guidance, macOS Tahoe/iOS 26 references, the user's supplied screenshots,
  and the supplied Liquid Glass CSS/JS experiments.
---

# Apple Web Design Science

## Mission

Create original web applications that feel at home in the Apple ecosystem:
calm, precise, content-first, spatial, responsive, tactile, and refined.

This is NOT an instruction to copy Apple's UI pixel-for-pixel or recreate
Apple trademarks. Use the principles, visual grammar, interaction patterns,
and material behavior as inspiration, then adapt them to the user's brand,
content, and web platform.

Primary target:
- Web applications
- Desktop web
- Tablet web
- Mobile web
- Responsive components
- HTML/CSS/JS, React, Next.js, Vue, Svelte, Tailwind, or another requested stack

Primary visual direction:
- iOS 26 / current Liquid Glass language
- macOS Tahoe 26 visual language
- Apple-style web composition
- Original "liquid glass + lens + responsive surface" behavior

## Core design doctrine

Priority order:

1. User goal
2. Information hierarchy
3. Content clarity
4. Interaction ergonomics
5. Platform familiarity
6. Visual refinement
7. Material effects
8. Decorative detail

Never reverse this order.

A beautiful effect that reduces readability or usability is a design failure.

---

# 1. Reference hierarchy

When designing, use references in this order:

1. User's current request and product requirements
2. User-provided screenshots and visual references
3. Official Apple HIG principles
4. Official Apple Liquid Glass guidance
5. Web accessibility standards
6. Supplied Liquid Glass code as implementation research
7. General visual-design heuristics

When new screenshots are supplied later, treat them as additional evidence.
Do not automatically overwrite existing rules; compare them and promote a
pattern only when it is consistent with the accumulated reference set.

User visual references supplied for v0.1 show:
- Liquid/frosted functional surfaces
- Translucent floating navigation
- Sidebars and grouped panels
- Pill-shaped controls
- Large whitespace and strong content hierarchy
- Rounded cards and continuous curves
- Bright semantic accent colors
- Dark and light functional layers
- Minimal iconography
- Contextual menus and sheets
- Toolbars that float above content
- Sliders/toggles with tactile deformation
- macOS-style window chrome
- Apple Store-style editorial product/card composition

---

# 2. Apple-inspired web language

Use the internal name:

APPLE-FLUID WEB

It consists of six visual layers.

### Layer A — Content
The actual product information, images, charts, forms, tables, text.

### Layer B — Structure
Grid, spacing, grouping, alignment, containers, navigation.

### Layer C — Functional glass
Navigation, toolbar, floating controls, segmented controls, dialogs,
tool palettes, important interactive surfaces.

### Layer D — Lens/refraction
Localized optical distortion, background displacement, soft refraction,
specular highlights and edge response.

### Layer E — Motion
Hover response, press compression, drag deformation, state morphing,
spring/bounce, view transitions.

### Layer F — Atmosphere
Subtle background gradients, photography, depth, blur, color ambience.

Do not make every object use all six layers.

---

# 3. Material rules

Liquid Glass is primarily a FUNCTIONAL LAYER.

Use glass most strongly for:
- Navigation
- Floating tab bars
- Sidebars
- Toolbars
- Floating controls
- Menus/sheets
- Primary interactive controls
- Sliders and toggles when actively manipulated

Do not cover the entire content layer in glass by default.

For content:
- Prefer solid, quiet, or standard material surfaces.
- Let cards, images, charts, and text remain visually clear.
- Use glass only where it creates hierarchy or interaction emphasis.

Clear glass:
- Use over visually rich backgrounds where background context matters.

Regular/thicker glass:
- Use when text legibility and separation matter more than transparency.

Dark glass:
- Use over dark immersive backgrounds; keep text contrast strong.

---

# 4. Glass construction

A glass surface is NOT simply:

background: rgba(255,255,255,.2);
backdrop-filter: blur(...);

Use a layered construction when the effect is important:

1. Base translucent material
2. Backdrop blur
3. Optional saturation / color adaptation
4. Edge/specular layer
5. Inner light/shadow
6. Optional localized lens/refraction
7. Content layer
8. Optional ambient shadow

Recommended conceptual structure:

.glass
  ├── glass-backdrop
  ├── glass-tint
  ├── glass-specular
  ├── glass-edge
  └── glass-content

The exact implementation may use pseudo-elements instead.

The optical treatment must remain subtle enough that the content is still
the visual priority.

---

# 5. Lens / refraction system

The supplied reference code demonstrates a more advanced "liquid lens"
approach rather than plain blur.

Important techniques observed in the supplied code:
- `backdrop-filter`
- `-webkit-backdrop-filter`
- SVG `feDisplacementMap`
- a radial normal-map style image
- blurred wrappers
- specular inset shadows
- active-state stretching
- local lens displacement
- a "liquid track" and shadow layer
- GSAP-driven drag and state changes

Reference code evidence:
- The slider lens applies a displacement filter using `feDisplacementMap`.
- The glass thumb combines a backdrop blur, translucent overlay, and
  multiple inset/specular shadows.
- Active interaction reveals the optical layers and stretches the control.
- The liquid toggle uses a filter stack, scale changes, drag progress,
  and a bounce-like state transition.
fileciteturn1file1L1-L1

For implementation:
- Use SVG filters only for components that benefit from real refraction.
- Prefer CSS-only glass for low-priority surfaces.
- Use localized distortion, never global page distortion.
- Keep displacement small enough to avoid visual chaos.
- Disable or simplify the effect on low-power/mobile contexts when needed.

Reference implementation ideas from the supplied code include:
- `feGaussianBlur`
- `feColorMatrix`
- `feDisplacementMap`
- `feMorphology`
- `feComposite`
- `backdrop-filter`
- `box-shadow` inset highlights
- CSS custom properties for progress/state
- GSAP for continuous drag/state orchestration

These values are implementation examples, not official Apple design tokens.

---

# 6. The "jelly / flexible surface" interaction

Use the user's requested concept:

When a pointer approaches or interacts with an important glass control, the
surface should feel slightly flexible, like a thin liquid membrane.

### Hover
Use low-amplitude response:
- 1–3 px translation
- tiny scale increase, usually <= 1.03
- local highlight shift
- optional pointer-relative lens movement
- icon may increase slightly
- never make the whole component wobble

### Pointer down
Use tactile compression:
- slight scale down
- optional horizontal/vertical squash
- stronger local highlight
- small shadow change

### Drag
Use continuous deformation:
- deformation follows pointer velocity
- lens location follows pointer
- amount of stretch depends on drag distance
- release returns to resting state with a short spring

### Release
Use:
1. settle
2. slight overshoot
3. return to 1.0 scale

The motion should communicate physical continuity, not decoration.

---

# 7. Motion science

Motion has a purpose.

Use motion to:
- communicate state
- preserve spatial continuity
- show cause/effect
- provide tactile feedback
- guide attention
- reveal/hide controls

Avoid motion that:
- repeats constantly
- delays common actions
- distracts from reading
- makes the UI feel like a demo page

Default interaction timing:
- hover response: ~120–220 ms
- press response: ~80–160 ms
- simple state transition: ~180–300 ms
- contextual material/state transitions: ~250–450 ms
- larger spring/bounce: only when it adds meaning

These are working ranges, not mandatory Apple values.

Use easing that feels:
- quick to react
- soft to settle
- slightly springy for tactile controls
- calm for navigation and layout

The supplied toggle reference uses a short initial state change and a
separate bounce/deformation mechanism; use that as an interaction pattern,
not as an exact timing requirement.
fileciteturn1file3L1-L1

Always support:
`@media (prefers-reduced-motion: reduce)`

Reduced-motion mode should:
- remove large transforms
- remove continuous parallax
- remove bouncing
- keep essential state changes visible
- preserve opacity/color transitions where appropriate

---

# 8. Layout science

Before styling, establish the hierarchy.

Ask:
- What is the primary task?
- What is the primary content?
- What is secondary?
- What actions are frequent?
- What actions are destructive?
- What can be progressively disclosed?
- What can remain hidden until needed?

Use:
- strong alignment
- consistent margins
- generous whitespace
- clear grouping
- readable text widths
- restrained card density
- responsive layout
- predictable control placement

Content should reach the edges when appropriate, while functional controls
can float over it as a distinct layer.

Do not use random card grids just because cards are easy to generate.

---

# 9. Responsive web system

The agent must design for:
- mobile
- tablet
- laptop
- large desktop

Do not merely shrink desktop.

Transform the composition.

### Desktop
- spacious content frame
- floating navigation / toolbar where useful
- multi-column information hierarchy
- side panels when useful
- larger interactive regions

### Tablet
- fewer columns
- stronger grouping
- adaptive sidebars
- touch-sized controls

### Mobile
- simplified navigation
- stacked content
- larger touch targets
- less visual density
- less optical distortion
- glass used primarily for important functional surfaces

Use fluid sizing where appropriate with:
- `clamp()`
- CSS Grid
- Flexbox
- container queries
- responsive typography

---

# 10. Typography

Typography must feel system-like before it feels decorative.

Preferred family strategy:
- Use the closest legally/technically available system UI font.
- For Apple-device contexts, use `-apple-system`, `BlinkMacSystemFont`,
  `SF Pro` when legitimately available, then system fallbacks.
- Never bundle or redistribute proprietary Apple font files unless the
  user has the proper license/source.

Hierarchy:
- Display
- Title
- Heading
- Body
- Secondary
- Caption
- Label

Use weight before decoration.

Do not create hierarchy with:
- excessive gradients
- glow
- giant shadows
- excessive uppercase
- decorative outlines

Typography should remain readable on glass.

---

# 11. Color

Color has semantic purpose.

Use:
- neutral base
- one primary action/accent
- semantic success/warning/error
- restrained supporting accents

The accent should guide attention, not paint every component.

For glass:
- let background content influence the material
- preserve readable foreground contrast
- avoid a muddy gray-on-gray UI
- use stronger material opacity where fine text or symbols need it

Dark mode:
- do not simply invert light mode
- rebalance contrast, hierarchy, glass opacity, and shadows
- keep semantic accents visible without excessive saturation

---

# 12. Shape language

Prefer:
- rounded rectangles
- pills
- circles for compact controls
- continuous, soft curvature
- nested radii that visually relate

Use radius as a system, not random values.

Example conceptual scale:
- micro: 10–12
- small: 14–16
- medium: 18–22
- large: 24–32
- capsule: 9999

Adapt radius to component size.

Do not make every element a giant pill.

---

# 13. Navigation

Functional navigation should visually float above content when the design
benefits from it.

Patterns:
- floating tab bar
- compact segmented control
- translucent sidebar
- toolbar
- search field
- contextual action group

Use selected-state treatment instead of heavy borders.

Selected state may use:
- lighter/darker material
- subtle pill background
- accent text/icon
- localized highlight

Avoid excessive dividers.

---

# 14. Buttons

Button hierarchy:

Primary
- strongest semantic accent
- high contrast
- simple label
- optional icon
- clear hover/press feedback

Secondary
- quiet neutral
- material or subtle background

Tertiary
- text/icon emphasis only

Glass button
- reserved for functional surfaces or rich-background contexts

On hover:
- subtle lift
- local lens
- icon response

On press:
- tactile compression
- material refraction becomes slightly more pronounced

Never make the interaction slower than the user's intent.

---

# 15. Cards

Card hierarchy:

1. Content
2. Surface
3. Boundary
4. Optional depth
5. Optional interaction

A card should not look like a plastic toy.

For content cards:
- prefer quiet surfaces
- strong typography
- meaningful imagery
- compact metadata
- sufficient whitespace

For interactive cards:
- add pointer response
- optional local lens
- subtle elevation or material change

---

# 16. Inputs, sliders, and switches

These are high-value candidates for tactile materials.

Slider:
- quiet track
- clear progress state
- enlarged but controlled thumb
- localized lens/refraction while interacting
- pointer and touch support
- keyboard support

Switch:
- obvious state
- tactile press
- continuous drag only when useful
- accessible `aria-pressed` or native semantic control
- avoid requiring drag to complete an action if a click can do it

The supplied examples show glass sliders and liquid toggles with:
- active optical layers
- stretching
- drag progress
- bounce-like feedback
- theme/state transitions
fileciteturn1file9L1-L1

---

# 17. Menus, sheets, dialogs

Use hierarchy:
- page/content
- dimming layer when needed
- floating menu/sheet
- primary action

Glass menus should:
- separate from background clearly
- keep text readable
- use grouping and spacing
- avoid excessive opacity
- support keyboard focus

Destructive actions should be visually clear without becoming visually
dominant.

---

# 18. Icons

Prefer:
- simple outline/glyph icons
- consistent stroke/weight
- visually balanced bounding boxes
- semantic familiar symbols

Do not invent complex icons when a standard familiar symbol exists.

On hover:
- tiny scale or weight change
- local color/accent response

Do not rotate icons unless rotation communicates a state.

---

# 19. Visual hierarchy rules

Use the following priority:

1. Task
2. Primary heading
3. Primary action
4. Key data
5. Supporting content
6. Secondary actions
7. Decorative effects

The eye should understand the interface before noticing the glass.

---

# 20. Design science checklist

Before finalizing, evaluate:

### Gestalt
- proximity
- similarity
- continuity
- common region
- figure/ground

### Interaction
- Fitts-style target accessibility
- Hick-style choice simplification
- cognitive load
- recognition over recall
- progressive disclosure
- clear cause/effect

### Visual
- hierarchy
- contrast
- alignment
- whitespace
- rhythm
- density
- visual balance

### Accessibility
- keyboard navigation
- visible focus
- sufficient contrast
- semantic HTML
- target sizing
- reduced motion
- readable text scaling

WCAG 2.2 should be the web accessibility baseline.

---

# 21. Accessibility is part of the visual system

Never let glass break accessibility.

Requirements:
- visible keyboard focus
- semantic HTML
- meaningful labels
- proper `aria-*` state when required
- pointer + keyboard support
- text remains readable over dynamic backgrounds
- controls remain distinguishable in reduced transparency/high contrast contexts
- motion can be reduced
- drag-only behavior has a non-drag alternative where applicable

Target sizes should satisfy WCAG 2.2 guidance and spacing must reduce accidental
activation.

---

# 22. Performance rules

Glass and SVG filters can be expensive.

Use the effect budget:

### Tier 1 — Simple
CSS translucent background + border + shadow.

### Tier 2 — Enhanced
Tier 1 + backdrop blur + saturation/tint.

### Tier 3 — Lens
Tier 2 + localized displacement/specular effects.

### Tier 4 — Dynamic
Tier 3 + pointer tracking + drag deformation + animation orchestration.

Use Tier 3/4 only on focal components.

Never apply expensive filters to hundreds of elements simultaneously.

Avoid:
- giant blurred layers covering the whole DOM
- multiple full-screen SVG filters
- continuous mousemove work that causes layout
- excessive `filter` chains

Prefer:
- transform/opacity for animation
- CSS variables
- `requestAnimationFrame` for pointer processing
- containment where useful
- progressive enhancement
- graceful fallback

---

# 23. Implementation contract

When generating a web app:

1. Define semantic HTML structure.
2. Define layout system.
3. Define design tokens.
4. Build content surfaces.
5. Build functional glass surfaces.
6. Add interaction states.
7. Add motion.
8. Add optional lens/refraction.
9. Add responsive transformations.
10. Add accessibility.
11. Add reduced-motion behavior.
12. Performance-check the visual effects.
13. Run a final Apple-inspired design critique.

Prefer reusable components.

Example component naming:
- `GlassButton`
- `GlassIconButton`
- `GlassTabBar`
- `GlassSidebar`
- `GlassToolbar`
- `GlassMenu`
- `GlassDialog`
- `GlassSlider`
- `GlassSwitch`
- `GlassSearch`
- `GlassCard`

Do not create separate, inconsistent glass implementations for every component.
Create one material system and parameterize it.

---

# 24. Design token foundation

Use tokens rather than hardcoded values everywhere.

Example:

```css
:root {
  --ui-radius-sm: 14px;
  --ui-radius-md: 20px;
  --ui-radius-lg: 28px;
  --ui-radius-pill: 999px;

  --ui-space-1: 4px;
  --ui-space-2: 8px;
  --ui-space-3: 12px;
  --ui-space-4: 16px;
  --ui-space-5: 20px;
  --ui-space-6: 24px;
  --ui-space-8: 32px;
  --ui-space-10: 40px;
  --ui-space-12: 48px;

  --glass-bg: color-mix(in srgb, white 16%, transparent);
  --glass-border: color-mix(in srgb, white 42%, transparent);
  --glass-highlight: color-mix(in srgb, white 72%, transparent);
  --glass-shadow: rgba(0,0,0,.12);

  --motion-fast: 140ms;
  --motion-base: 220ms;
  --motion-slow: 360ms;

  --ease-standard: cubic-bezier(.22,.61,.36,1);
}
```

These are a starting point for a web implementation, not Apple's official
tokens.

---

# 25. Cursor-reactive glass

For desktop pointer environments, the agent may add a local optical response.

Concept:

```text
pointer enters
  ↓
measure pointer position within component
  ↓
shift specular highlight toward pointer
  ↓
slightly alter lens origin
  ↓
tiny surface tilt/deformation
  ↓
pointer leaves
  ↓
settle smoothly
```

Do not translate the entire UI toward the cursor.

The response should feel like the material is reacting, not like the page is
following the mouse.

Touch devices:
- remove hover-only behavior
- preserve press/drag feedback

---

# 26. Dark-mode / light-mode strategy

Both modes are first-class.

Light:
- luminous neutral background
- visible translucent surfaces
- soft dark content
- bright accents

Dark:
- deep neutral background
- subtle translucent layers
- bright but controlled text
- semantic accents
- less obvious but still readable edges

Do not use pure black/white everywhere.

Use system-aware media queries where appropriate:

```css
@media (prefers-color-scheme: dark) {
  /* adapt material and contrast */
}
```

---

# 27. Apple-web editorial style

When the user asks for a landing page, marketing page, or product page,
switch from "dashboard density" to "editorial rhythm."

Use:
- oversized but restrained headlines
- very large whitespace
- full-bleed imagery
- short supporting copy
- strong product focal point
- horizontal content rails/carousels
- large rounded media panels
- simple CTA hierarchy

Think:
content first, interface second.

---

# 28. What NOT to do

Reject these by default:

- generic glassmorphism everywhere
- floating glass cards for every paragraph
- excessive neon gradients
- excessive glow
- huge drop shadows
- random 3D objects
- excessive border strokes
- fake "Apple" logos or proprietary assets
- tiny low-contrast glass text
- endless pill buttons
- random corner radii
- animations with no purpose
- cursor effects on every element
- constant parallax
- glass over every content surface
- desktop UI simply squeezed onto mobile
- "AI dashboard" visual clichés

---

# 29. Final design critique protocol

Before presenting the result, internally score each area from 1–5:

- Purpose
- Hierarchy
- Layout
- Typography
- Spacing
- Material
- Interaction
- Motion
- Responsiveness
- Accessibility
- Performance
- Originality

If Material scores high but Purpose/Hierarchy/Accessibility scores low,
reduce the effects before shipping.

---

# 30. Output behavior for an AI web builder

Given a user prompt such as:

"Build a task management web app."

Do NOT immediately produce random UI.

First internally determine:
- user goal
- information architecture
- platform density
- required components
- navigation model
- content hierarchy
- material tier
- interaction states
- responsive behavior

Then produce the web app.

The output should use the shared component system:

```text
Glass Navigation
Glass Toolbar
Glass Button
Glass Search
Content Surface
Content Card
Glass Menu
Glass Dialog
Glass Slider
Glass Switch
```

Only create custom visual treatment when the component needs a unique behavior.

---

# 31. Reference-driven improvement protocol

When the user supplies more screenshots:

1. Extract recurring patterns.
2. Separate Apple platform patterns from decorative artifacts.
3. Compare with existing skill rules.
4. Promote only consistent patterns.
5. Add new component recipes when evidence supports them.
6. Update tokens only when multiple references justify them.
7. Record exceptions instead of breaking global rules.
8. Increment the skill version.

New references should improve:
- geometry
- material construction
- motion
- component behavior
- responsive behavior
- typography
- hierarchy
- visual rhythm

The skill should become more accurate over time, not merely more decorative.

---

# 32. Source basis

Official Apple sources:
- Apple Human Interface Guidelines
- Apple Design Principles
- Apple Layout guidance
- Apple Materials / Liquid Glass guidance
- Apple Motion guidance
- Apple Accessibility guidance
- Apple Branding guidance
- Apple newsroom material describing iOS 26 and macOS Tahoe 26

Web sources:
- W3C WCAG 2.2
- MDN / WebKit documentation for web platform behavior

User-provided sources:
- Supplied Apple-style screenshots
- Supplied Liquid Glass CSS/JS reference file
- The reference file contains lens/displacement, backdrop-filter,
  specular layers, active stretching, drag behavior, and theme transitions.

---

# 33. Important distinction

This skill describes an Apple-inspired design SCIENCE for web applications.

It is not:
- a promise to reproduce native Apple APIs on the web
- a guarantee of identical Liquid Glass rendering
- a copy of Apple's private implementation
- a replacement for usability testing

When browser capabilities differ from native Apple rendering, reproduce the
perceived principles:
- translucent layering
- depth
- refraction
- hierarchy
- responsiveness
- tactility
- restraint
- clarity

not the exact internal implementation.
