# Reference Notes — Apple Web Design Science v0.1

## Supplied screenshot observations

The supplied references show a unified design vocabulary across iPhone/iPad
and macOS-style interfaces.

Recurring visual patterns:
- translucent floating functional surfaces
- strong background/content visibility beneath controls
- large continuous rounded shapes
- capsule/pill controls
- selected states represented by nested translucent pills
- minimal dark iconography on light surfaces
- bright semantic accent colors
- floating navigation
- sidebars and contextual menus
- grouped settings lists
- toolbar controls floating over content
- media controls with layered transparency
- soft edge highlights and inset specular reflections
- light and dark variants
- product/editorial pages using whitespace, large imagery, and card rails
- macOS-style traffic lights and window controls

## User-requested interaction direction

The user specifically wants a "jelly/flexible" pointer interaction:
- cursor hover causes subtle surface flexibility
- glass behaves like a thin liquid surface
- active/drag states stretch and deform
- lens/refraction can follow the pointer
- release settles with controlled elasticity

This should be treated as an interaction layer, not as a permanent page-wide
effect.

## Supplied code-derived implementation patterns

The supplied code includes reference implementations for:
- Liquid Glass Lens Button
- liquid toggle
- slider thumb with liquid glass lens
- theme switcher
- generic frosted/liquid glass filter

Notable implementation concepts:
- `backdrop-filter`
- `-webkit-backdrop-filter`
- SVG filter primitives
- `feDisplacementMap`
- radial normal-map-like input
- Gaussian blur
- color matrix
- morphology/composite
- inset specular highlights
- active-state transparency changes
- scale/stretch deformation
- pointer/touch dragging
- GSAP timeline/state control
- CSS custom properties
- view-transition-aware theme changes

Reference code is a source of implementation techniques, not evidence of
official Apple token values.

## Improvement policy

Each new screenshot batch should be compared against this file.

Add:
- new components
- new state patterns
- new material tiers
- new motion patterns
- new layout rules
- new responsive behaviors

Only generalize a pattern when it appears consistently across references or
is supported by official guidance.
