#  Apple Web Design Science

> **An AI-agent skill for building refined, Apple-inspired web applications with Liquid Glass, fluid interaction, and design science.**

<p align="center">
  <img src="https://img.shields.io/badge/Design-Apple%20Inspired-111111?style=for-the-badge&logo=apple&logoColor=white" alt="Apple Inspired">
  <img src="https://img.shields.io/badge/Liquid%20Glass-Enabled-0A84FF?style=for-the-badge" alt="Liquid Glass">
  <img src="https://img.shields.io/badge/Web-Responsive-34C759?style=for-the-badge" alt="Responsive">
  <img src="https://img.shields.io/badge/Accessibility-WCAG%202.2-FF9F0A?style=for-the-badge" alt="WCAG 2.2">
</p>

<p align="center">
  <b>Design the experience first. Add the glass second.</b>
</p>

---

## ✨ What is this?

**Apple Web Design Science** is a reusable skill for AI web-building agents.

Give an AI agent a normal prompt such as:

```text
Build a modern AI SaaS dashboard.
```

The skill pushes the agent to think beyond generic UI generation:

```text
Prompt
  ↓
User goal
  ↓
Information hierarchy
  ↓
Layout system
  ↓
Component system
  ↓
Material + Liquid Glass
  ↓
Interaction + Motion
  ↓
Responsive behavior
  ↓
Accessibility
  ↓
Final web experience
```

The result should feel **calm, precise, spatial, tactile and premium** instead of looking like a generic "AI dashboard".

---

## 🎯 Design Direction

This skill is designed for **web applications** inspired by:

- iOS 26 / modern Liquid Glass language
- macOS Tahoe visual language
- Apple-inspired interaction patterns
- Human-computer interaction principles
- Modern responsive web design
- WCAG 2.2 accessibility practices
- User-provided Apple UI references
- Liquid Glass lens / refraction experiments

> **Important:** This is an independent, Apple-inspired design skill. It is not an official Apple product, framework, API, or reproduction of Apple's private implementation.

---

# 🧠 The Design Philosophy

The skill follows this priority:

```text
1. User goal
2. Information hierarchy
3. Content clarity
4. Interaction ergonomics
5. Platform familiarity
6. Visual refinement
7. Material effects
8. Decorative detail
```

A beautiful effect that makes a product harder to understand is considered a **design failure**.

### The rule

> **Content first. Interface second. Glass third.**

---

# 🫧 Liquid Glass

Liquid Glass is treated as a **functional material layer**, not a decoration that gets placed on every element.

Use it primarily for:

```text
Navigation
Toolbar
Floating controls
Menus
Dialogs
Segmented controls
Important buttons
Search
Sliders
Switches
Contextual actions
```

Keep important content clear:

```text
Text
Charts
Tables
Forms
Images
Product information
Primary data
```

### Glass construction

A high-quality glass surface can be built from multiple layers:

```text
┌──────────────────────────────┐
│          Content             │
├──────────────────────────────┤
│      Specular highlight      │
├──────────────────────────────┤
│     Lens / refraction        │
├──────────────────────────────┤
│       Glass tint             │
├──────────────────────────────┤
│      Backdrop blur            │
├──────────────────────────────┤
│        Background            │
└──────────────────────────────┘
```

Instead of:

```css
background: rgba(255,255,255,.2);
```

the system encourages layered materials:

```text
transparency
+ blur
+ tint
+ edge response
+ specular highlight
+ depth
+ optional refraction
```

---

# 💧 Liquid Lens / Refraction

For selected components, the skill supports a more advanced optical treatment:

```text
glass
  +
localized distortion
  +
lens displacement
  +
specular response
```

Possible web techniques include:

- `backdrop-filter`
- `-webkit-backdrop-filter`
- SVG filters
- `feDisplacementMap`
- `feGaussianBlur`
- `feColorMatrix`
- `feMorphology`
- `feComposite`
- CSS custom properties
- pointer tracking
- GSAP or Web Animations where appropriate

The supplied reference implementation demonstrates a slider thumb using a
localized displacement map together with a translucent overlay and
specular layers.

---

# 🪼 Jelly / Flexible Interaction

One of the signature ideas in this skill is a **soft physical response**.

The interface should not feel like a static image.

### Hover

```text
Pointer enters
     ↓
surface subtly reacts
     ↓
highlight moves
     ↓
lens follows pointer
     ↓
component settles
```

### Press

```text
press
 ↓
small compression
 ↓
material becomes more active
 ↓
action feedback
 ↓
soft release
```

### Drag

```text
pointer movement
      ↓
continuous deformation
      ↓
lens follows movement
      ↓
surface stretches
      ↓
release
      ↓
small elastic settle
```

The interaction should feel like a **thin flexible membrane**, not a bouncing
toy.

---

# ⚙️ Component Language

The skill encourages a reusable component system instead of creating a
different glass effect for every component.

### Core components

```text
GlassButton
GlassIconButton
GlassCard
GlassToolbar
GlassSidebar
GlassTabBar
GlassSegmentedControl
GlassSearch
GlassMenu
GlassDialog
GlassSlider
GlassSwitch
GlassInput
```

Conceptually:

```text
                 APP
                  │
        ┌─────────┴─────────┐
        │                   │
   CONTENT SYSTEM      MATERIAL SYSTEM
        │                   │
   cards / tables       glass / lens
   charts / forms       blur / tint
   imagery / text       edge / shadow
        │                   │
        └─────────┬─────────┘
                  │
            MOTION SYSTEM
                  │
       hover / press / drag
       spring / transitions
```

---

# 🎨 Visual System

## Typography

Typography should feel system-native before it feels decorative.

The skill prefers:

```css
font-family:
  -apple-system,
  BlinkMacSystemFont,
  "Segoe UI",
  sans-serif;
```

Use hierarchy through:

- size
- weight
- spacing
- line height
- grouping

Not through excessive:

- gradients
- glow
- outlines
- shadows
- uppercase text

---

## ◯ Shape Language

The system uses **related radii**, not random rounded corners.

Example working scale:

```css
--radius-sm:   14px;
--radius-md:   20px;
--radius-lg:   28px;
--radius-pill: 999px;
```

The actual radius should adapt to component size and context.

---

## 🎨 Color

Color is semantic.

A typical palette structure is:

```text
Neutral base
      ↓
Primary accent
      ↓
Success / Warning / Error
      ↓
Supporting accents
```

The accent should guide attention instead of painting the entire interface.

---

# 📐 Layout Science

Before generating UI, the agent should answer:

```text
What is the user's primary task?
What is the most important content?
What action happens most often?
What is secondary?
What should be progressively disclosed?
What can stay hidden until needed?
```

Then it establishes:

- alignment
- spacing
- grouping
- content width
- density
- responsive behavior
- navigation
- action hierarchy

---

# 📱 Responsive by Transformation

The skill does **not** treat mobile as a smaller desktop.

### Desktop

```text
large content frame
+
multi-column layouts
+
floating tools
+
expanded navigation
```

### Tablet

```text
fewer columns
+
touch-first controls
+
adaptive panels
```

### Mobile

```text
stacked content
+
simplified navigation
+
larger touch targets
+
lower visual density
+
reduced optical complexity
```

---

# 🧪 Design Science

The skill combines visual design with interaction and cognitive principles.

### Gestalt

- Proximity
- Similarity
- Continuity
- Common region
- Figure / ground

### Interaction

- Fitts-style target accessibility
- Hick-style choice reduction
- Cognitive load
- Recognition over recall
- Progressive disclosure
- Clear cause and effect

### Visual

- Hierarchy
- Contrast
- Alignment
- Rhythm
- Balance
- Whitespace
- Density

---

# ♿ Accessibility

Premium visual design should not come at the cost of usability.

The skill includes:

- semantic HTML
- keyboard navigation
- visible focus
- readable text over glass
- proper control states
- accessible labels
- pointer + keyboard interaction
- reduced motion
- fallback behavior for complex effects

The web accessibility baseline is **WCAG 2.2**.

---

# ⚡ Performance

Liquid effects can be expensive.

The skill uses an **effect budget**:

### Tier 1 — Simple

```text
transparency
+
border
+
shadow
```

### Tier 2 — Enhanced

```text
Tier 1
+
backdrop blur
+
tint
```

### Tier 3 — Lens

```text
Tier 2
+
localized displacement
+
specular effects
```

### Tier 4 — Dynamic

```text
Tier 3
+
pointer tracking
+
drag deformation
+
advanced motion
```

Not every component should use Tier 4.

> **Use the strongest effect where it creates the most value.**

---

# 🚫 Anti-Patterns

The skill actively avoids generic "glassmorphism".

### Avoid

- Glass on everything
- Excessive blur
- Excessive glow
- Neon gradients everywhere
- Huge shadows
- Random 3D objects
- Endless pill buttons
- Random corner radii
- Tiny low-contrast glass text
- Constant cursor-following effects
- Unnecessary parallax
- Animation without purpose
- Desktop UI squeezed onto mobile
- Generic "AI dashboard" clichés

---

# 🧩 Supported Web Stacks

The design language can be implemented with:

```text
HTML / CSS / JavaScript
React
Next.js
Vue
Svelte
Tailwind CSS
Vanilla CSS
GSAP
Web Animations API
SVG filters
```

The design system is framework-independent.

---

# 🚀 Example

### User prompt

```text
Build a task-management web app with a clean Apple-inspired interface.
```

### Agent behavior

Instead of blindly producing cards, it reasons:

```text
User task
   ↓
Task hierarchy
   ↓
Sidebar + main workspace
   ↓
Floating toolbar
   ↓
Content-first task list
   ↓
Glass contextual actions
   ↓
Soft hover response
   ↓
Tactile drag / press
   ↓
Responsive mobile layout
   ↓
Accessibility
```

### Result

A reusable system such as:

```text
┌────────────────────────────────────────────┐
│              Glass Toolbar                 │
├─────────────┬──────────────────────────────┤
│             │                              │
│   Glass     │       Task Workspace         │
│   Sidebar   │                              │
│             │   Content-first cards        │
│             │                              │
│             │   Glass contextual actions  │
│             │                              │
└─────────────┴──────────────────────────────┘
```

---

# 📦 Installation

Copy the skill into the skills directory used by your AI agent:

```text
apple-web-design-science/
├── SKILL.md
├── REFERENCE_NOTES.md
└── README.md
```

Then instruct your agent to use:

```text
apple-web-design-science
```

as the design authority for web UI generation.

---

# 🛠️ How to Use

Simply give the agent your product request:

```text
Create a modern finance dashboard.
```

or:

```text
Build an e-commerce product page.
```

or:

```text
Turn this existing HTML into a premium Apple-inspired interface.
```

The skill should preserve the user's product requirements while applying the
shared design system.

---

# 🧠 Reference-Driven Learning

This project is designed to improve as more visual references are added.

New screenshots can teach the skill:

```text
new reference
    ↓
pattern extraction
    ↓
compare with existing rules
    ↓
identify recurring behavior
    ↓
update component recipes
    ↓
improve visual system
```

The goal is **not to collect screenshots**.

The goal is to extract the **design logic behind them**.

---

# 🗂️ Project Structure

```text
apple-web-design-science/
│
├── SKILL.md
│   └── Main AI-agent design instructions
│
├── REFERENCE_NOTES.md
│   └── Visual + implementation observations
│
└── README.md
    └── Project documentation
```

---

# 🔬 Roadmap

- [x] Apple-inspired web design foundation
- [x] Liquid Glass material rules
- [x] Lens / refraction concepts
- [x] Jelly interaction language
- [x] Responsive design rules
- [x] Accessibility baseline
- [x] Performance effect tiers
- [x] Reusable component language
- [ ] Expanded component recipes
- [ ] Larger screenshot reference library
- [ ] More advanced pointer physics
- [ ] More motion presets
- [ ] Design-token generator
- [ ] React component starter kit
- [ ] Tailwind implementation
- [ ] Automated UI critique checklist
- [ ] Visual regression examples

---

# 🤝 Contributing

Have a better Apple-inspired web interaction, component pattern, or material
implementation?

Contributions are welcome.

The strongest contributions should explain:

```text
What problem does it solve?
Why does the interaction work?
When should it be used?
When should it NOT be used?
How does it behave on mobile?
How does it behave with reduced motion?
```

---

# ⚠️ Philosophy

This project intentionally separates:

```text
Apple's design principles
        ≠
Apple's private implementation
```

The goal is to reproduce the **quality of the experience**, not to pretend
we have access to private Apple implementation details.

---

# ⭐ The Core Rule

> **Don't make a website look like Apple.**
>
> **Make it think like a well-designed Apple interface.**

Then add the glass.

---

<p align="center">
  <b>Apple Web Design Science</b><br>
  <sub>Purpose → Hierarchy → Material → Motion → Delight</sub>
</p>
