---
name: Tactile Core
colors:
  surface: '#f9f9fc'
  surface-dim: '#d9dadd'
  surface-bright: '#f9f9fc'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f3f3f6'
  surface-container: '#edeef1'
  surface-container-high: '#e8e8eb'
  surface-container-highest: '#e2e2e5'
  on-surface: '#1a1c1e'
  on-surface-variant: '#45474a'
  inverse-surface: '#2f3133'
  inverse-on-surface: '#f0f0f3'
  outline: '#75777a'
  outline-variant: '#c5c6ca'
  surface-tint: '#5d5e61'
  primary: '#5d5e61'
  on-primary: '#ffffff'
  primary-container: '#f0f0f3'
  on-primary-container: '#6b6d70'
  inverse-primary: '#c6c6c9'
  secondary: '#555f71'
  on-secondary: '#ffffff'
  secondary-container: '#d6e0f6'
  on-secondary-container: '#596376'
  tertiary: '#545f72'
  on-tertiary: '#ffffff'
  tertiary-container: '#ebf0ff'
  on-tertiary-container: '#626d81'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e2e2e5'
  primary-fixed-dim: '#c6c6c9'
  on-primary-fixed: '#1a1c1e'
  on-primary-fixed-variant: '#454749'
  secondary-fixed: '#d9e3f9'
  secondary-fixed-dim: '#bdc7dc'
  on-secondary-fixed: '#121c2c'
  on-secondary-fixed-variant: '#3d4759'
  tertiary-fixed: '#d8e3fa'
  tertiary-fixed-dim: '#bcc7dd'
  on-tertiary-fixed: '#111c2c'
  on-tertiary-fixed-variant: '#3c475a'
  background: '#f9f9fc'
  on-background: '#1a1c1e'
  surface-variant: '#e2e2e5'
typography:
  display-lg:
    fontFamily: Sora
    fontSize: 48px
    fontWeight: '700'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Sora
    fontSize: 32px
    fontWeight: '600'
    lineHeight: '1.2'
  headline-lg-mobile:
    fontFamily: Sora
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Sora
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Sora
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Sora
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-lg:
    fontFamily: Sora
    fontSize: 14px
    fontWeight: '600'
    lineHeight: '1.4'
    letterSpacing: 0.01em
  label-sm:
    fontFamily: Sora
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1.4'
    letterSpacing: 0.05em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  base: 8px
  xs: 4px
  sm: 12px
  md: 24px
  lg: 40px
  xl: 64px
  gutter: 24px
  margin-mobile: 16px
  margin-desktop: 48px
---

## Brand & Style
The design system is centered on the concept of "Indie Logic"—a philosophy that prioritizes intentional, physical-feeling interactions within a digital space. The aesthetic is purely Neumorphic (Soft UI), where the interface is treated as a single, continuous extrusion of a warm, premium surface. 

This design system avoids the traditional "layering" of digital paper; instead, it mimics the tactile sensation of molded plastic or soft-touch silicone. It is designed to evoke a sense of calm, precision, and high-end industrial design. Every element is either pushed out from or pressed into the base surface, creating an emotional response that is grounded, modern, and highly accessible through shadow-driven affordance.

## Colors
The color strategy for this design system is monochromatic and surface-driven. The base color (`#F0F0F3`) is the absolute foundation; it serves as the background, the component surface, and the neutral anchor. 

To maintain the Neumorphic illusion, components must never use a different background color than the page itself. Contrast is achieved exclusively through light and shadow. The typography utilizes deep charcoal and slate tones to ensure high legibility against the soft background, while a deep slate blue provides a sophisticated accent for active states or critical focus points.

## Typography
Sora is the exclusive typeface for this design system, chosen for its geometric clarity and generous x-height, which complements the rounded, physical nature of the UI. 

Headlines use a tighter letter-spacing and heavier weights to stand out against the soft-shadowed environment. Body text is kept clean with ample line height to ensure readability. Because the UI relies on shadows rather than lines for structure, typography plays a critical role in defining the hierarchy of information. All text uses high-contrast charcoal tones to offset the low-contrast nature of Neumorphic surfaces.

## Layout & Spacing
This design system utilizes a fluid grid with generous internal padding to allow the soft shadows room to "breathe." Elements should never be cramped; the Neumorphic effect requires white space to define the slopes and curves of the UI.

The layout philosophy follows a 12-column structure on desktop and a 4-column structure on mobile. A standard 24px spacing rhythm (3x base) is used for most component gaps. Margins are kept wide to emphasize the "object" feel of the interface within the viewport.

## Elevation & Depth
Elevation in this design system is not achieved through Z-index stacking, but through the simulation of light hitting a physical surface from the top-left.

**Raised State (Default):**
Components appear to rise out of the surface using dual shadows:
- Light: `-6px -6px 12px rgba(255, 255, 255, 0.7)`
- Dark: `6px 6px 12px rgba(163, 177, 198, 0.5)`

**Inset State (Active/Pressed):**
When interacted with, components appear to be pressed into the surface:
- Inner Light: `inset -4px -4px 8px rgba(255, 255, 255, 0.7)`
- Inner Dark: `inset 4px 4px 8px rgba(163, 177, 198, 0.5)`

Avoid using flat borders or solid dividers. Depth is the only way to separate sections.

## Shapes
The shape language is organic and soft. All containers must avoid sharp 90-degree angles. Standard cards and large containers utilize a 24px corner radius to maintain a friendly, molded appearance. Interactive elements like buttons and chips utilize a 50px pill-shape radius for maximum comfort and tactile appeal. This consistency in rounding ensures that every element feels like it belongs to the same unified surface.

## Components

**Buttons**
Buttons are pill-shaped (`50px` radius). In their default state, they use the "Raised" dual shadow. On hover, the shadow intensity increases slightly. On click (Active), they transition to the "Inset" shadow state to simulate a physical button press.

**Cards & Containers**
Large content areas use a `24px` radius. They should always match the background color (`#F0F0F3`). Content within cards should have a minimum of `24px` internal padding to ensure text does not clash with the curved edges.

**Input Fields**
Inputs are consistently "Inset" by default to indicate they are "hollow" areas ready to be filled. They use the `24px` radius for standard fields or `50px` for search bars.

**Chips & Tags**
Small pill-shaped elements (`50px` radius) that use the "Raised" state. For selected states, use the accent slate-blue for the text and a slightly deeper inset shadow.

**Selection Controls**
Checkboxes and radio buttons should be treated as small Neumorphic wells. When checked, a small raised "nub" or an icon appears within the well, using the "Raised" shadow logic at a smaller scale.

**Lists**
List items should be separated by vertical spacing rather than divider lines. Each item can be a subtle "Raised" surface or simply occupy the flat plane, using typography and icons to define the structure.