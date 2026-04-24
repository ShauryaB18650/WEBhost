---
name: Technical Editorial
colors:
  surface: '#fdf8f8'
  surface-dim: '#ddd9d9'
  surface-bright: '#fdf8f8'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f7f3f2'
  surface-container: '#f1edec'
  surface-container-high: '#ebe7e7'
  surface-container-highest: '#e5e2e1'
  on-surface: '#1c1b1b'
  on-surface-variant: '#46464a'
  inverse-surface: '#313030'
  inverse-on-surface: '#f4f0ef'
  outline: '#77777b'
  outline-variant: '#c7c6ca'
  surface-tint: '#5f5e5f'
  primary: '#000000'
  on-primary: '#ffffff'
  primary-container: '#1c1b1c'
  on-primary-container: '#858384'
  inverse-primary: '#c8c6c7'
  secondary: '#515f74'
  on-secondary: '#ffffff'
  secondary-container: '#d5e3fc'
  on-secondary-container: '#57657a'
  tertiary: '#000000'
  on-tertiary: '#ffffff'
  tertiary-container: '#1d1b19'
  on-tertiary-container: '#878380'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e5e2e3'
  primary-fixed-dim: '#c8c6c7'
  on-primary-fixed: '#1c1b1c'
  on-primary-fixed-variant: '#474647'
  secondary-fixed: '#d5e3fc'
  secondary-fixed-dim: '#b9c7df'
  on-secondary-fixed: '#0d1c2e'
  on-secondary-fixed-variant: '#3a485b'
  tertiary-fixed: '#e7e2dd'
  tertiary-fixed-dim: '#cac6c2'
  on-tertiary-fixed: '#1d1b19'
  on-tertiary-fixed-variant: '#494643'
  background: '#fdf8f8'
  on-background: '#1c1b1b'
  surface-variant: '#e5e2e1'
typography:
  display-xl:
    fontFamily: Inter
    fontSize: 120px
    fontWeight: '900'
    lineHeight: 110px
    letterSpacing: -0.04em
  headline-lg:
    fontFamily: Inter
    fontSize: 64px
    fontWeight: '800'
    lineHeight: 72px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-caps:
    fontFamily: Space Grotesk
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.1em
spacing:
  page-margin: 8vw
  section-gap: 160px
  gutter: 32px
  component-padding: 24px
---

## Brand & Style

This design system centers on the intersection of high-end editorial publishing and precise mechanical engineering. The brand personality is authoritative, meticulous, and sophisticated, aiming to evoke the feeling of a premium technical journal or an aerospace blueprint. 

The aesthetic leverages **High-Contrast Minimalism**. It relies on the tension between massive, aggressive typography and vast amounts of negative space. The inclusion of floating SVG technical sketches—such as airfoil cross-sections, fluid dynamics vectors, and stress-test diagrams—acts as the primary decorative language, softening the starkness of the layout while reinforcing the engineer’s domain expertise.

## Colors

The palette is intentionally restrictive to maintain an editorial "ink-on-paper" feel. 

- **Primary**: A deep, "Rich Black" (#0A0A0B) used for all primary headings, body text, and structural borders.
- **Secondary**: A muted "Steel Grey" (#475569) reserved for technical metadata, labels, and secondary supporting text.
- **Background**: Absolute white (#FFFFFF) to maximize contrast and provide a clean canvas for SVG elements.
- **Accent**: A very light "Blueprint Grey" (#E2E8F0) used for subtle divider lines and background fills for technical data blocks.

## Typography

Typography is the structural backbone of this design system. We use **Inter** for its neutral, utilitarian clarity, but push it to extremes in weight and scale. 

- **Display & Headlines**: Use the "Black" (900) and "ExtraBold" (800) weights with tight letter spacing to create a physical "mass" on the page.
- **Body**: Set with generous line height to ensure readability against the high-contrast background.
- **Technical Metadata**: **Space Grotesk** is used for labels, captions, and data points. Its geometric, technical construction provides a visual "flavor" that hints at engineering software interfaces and blueprints.

## Layout & Spacing

The layout utilizes a **Fixed 12-Column Editorial Grid** with exceptionally wide margins (8vw) to force content into a central, focused column. 

- **Vertical Rhythm**: High-density information is avoided. Massive gaps (160px+) between sections create a "gallery" feel, allowing each project or engineering concept to breathe.
- **The "Floating" Layer**: Technical SVGs should be placed on a separate z-index layer. They do not adhere to the grid; they should overlap grid lines and occasionally bleed off the edge of the viewport, mimicking loose sketches on a workbench.

## Elevation & Depth

This design system is strictly flat. Depth is achieved through **Layering and Transparency** rather than shadows or blurs.

- **Z-Indexing**: Text sits on the top layer. SVG sketches sit on the middle layer (often at 20-40% opacity). The white background sits on the bottom.
- **High-Contrast Outlines**: Instead of shadows, use 1px or 2px solid black borders to define elements. 
- **Overlays**: When elements must overlap, use hard cuts and sharp edges to maintain the "cut-and-paste" editorial aesthetic.

## Shapes

To reinforce the mechanical engineering theme, this design system uses **Sharp (0px)** corners for all UI elements. 

The absence of rounded corners evokes the precision of machined parts and technical drawings. This applies to buttons, image containers, form fields, and cards. Any "softness" in the UI should come exclusively from the organic curves of the decorative SVG sketches (like the curve of an airfoil) rather than the UI containers themselves.

## Components

### Buttons
Buttons are either solid black blocks with white text or "Ghost" buttons with a 2px black stroke. They use `label-caps` typography. The hover state should invert the colors instantly with no transition easing, emphasizing a mechanical, binary response.

### Technical Cards
Cards are defined by a 1px `accent_color_hex` border. They should feature a `label-caps` category at the top and may include a small "Fig. 01" style numbering system in the corner to mimic textbook diagrams.

### Technical SVGs (Floating Elements)
These are not just icons; they are architectural elements. They should be rendered in `primary_color_hex` or `secondary_color_hex` with varying stroke weights (0.5px to 1.5px). They should be set to `pointer-events: none` so they do not interfere with the user's ability to interact with the text.

### Lists & Specifications
Engineering specs should be presented in a two-column list format. The left side (label) uses `label-caps` in the secondary color, while the right side (value) uses `body-md` in the primary color. A dotted leader line should connect the two.

### Input Fields
Inputs are simple bottom-border only (1px black). Labels should float above the line in the `label-caps` style. Focus states are indicated by the border thickening to 3px.