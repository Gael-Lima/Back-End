---
name: Technical Architecture System
colors:
  surface: '#07122a'
  surface-dim: '#07122a'
  surface-bright: '#2f3952'
  surface-container-lowest: '#030d25'
  surface-container-low: '#101b33'
  surface-container: '#151f37'
  surface-container-high: '#1f2942'
  surface-container-highest: '#2a344e'
  on-surface: '#d9e2ff'
  on-surface-variant: '#c5c6cd'
  inverse-surface: '#d9e2ff'
  inverse-on-surface: '#263049'
  outline: '#8f9097'
  outline-variant: '#44474d'
  surface-tint: '#b9c7e4'
  primary: '#b9c7e4'
  on-primary: '#233148'
  primary-container: '#0a192f'
  on-primary-container: '#74829d'
  inverse-primary: '#515f78'
  secondary: '#b6c6ed'
  on-secondary: '#20304f'
  secondary-container: '#374767'
  on-secondary-container: '#a5b5db'
  tertiary: '#00dce5'
  on-tertiary: '#003739'
  tertiary-container: '#001d1f'
  on-tertiary-container: '#009096'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#d6e3ff'
  primary-fixed-dim: '#b9c7e4'
  on-primary-fixed: '#0d1c32'
  on-primary-fixed-variant: '#39475f'
  secondary-fixed: '#d8e2ff'
  secondary-fixed-dim: '#b6c6ed'
  on-secondary-fixed: '#091b39'
  on-secondary-fixed-variant: '#374767'
  tertiary-fixed: '#63f7ff'
  tertiary-fixed-dim: '#00dce5'
  on-tertiary-fixed: '#002021'
  on-tertiary-fixed-variant: '#004f53'
  background: '#07122a'
  on-background: '#d9e2ff'
  surface-variant: '#2a344e'
typography:
  display-lg:
    fontFamily: JetBrains Mono
    fontSize: 48px
    fontWeight: '700'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: JetBrains Mono
    fontSize: 32px
    fontWeight: '600'
    lineHeight: '1.2'
  headline-lg-mobile:
    fontFamily: JetBrains Mono
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.2'
  headline-md:
    fontFamily: JetBrains Mono
    fontSize: 24px
    fontWeight: '500'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Geist
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Geist
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-md:
    fontFamily: JetBrains Mono
    fontSize: 14px
    fontWeight: '500'
    lineHeight: '1.4'
    letterSpacing: 0.05em
  code-sm:
    fontFamily: JetBrains Mono
    fontSize: 13px
    fontWeight: '400'
    lineHeight: '1.5'
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 8px
  container-max: 1280px
  gutter: 24px
  margin-desktop: 48px
  margin-mobile: 16px
---

## Brand & Style

This design system is engineered to evoke the precision, logic, and structural integrity of back-end engineering. The brand personality is **authoritative, systematic, and highly functional**, catering to a professional developer audience that values efficiency over decoration.

The visual direction follows a **Modern Technical** aesthetic. It blends elements of **Minimalism** (to reduce cognitive load during learning) with **High-Contrast accents** that mirror terminal environments and IDE syntax highlighting. The UI should feel like a high-end development tool—stable, responsive, and meticulously organized. Layouts utilize subtle grid-inspired motifs and hairline borders to reference the "plumbing" of the internet.

## Colors

The palette is anchored in deep, architectural tones to provide a focused learning environment.
- **Primary:** A deep, midnight navy used for the foundational canvas.
- **Secondary:** A charcoal-tinted navy for surface layering and container backgrounds.
- **Tertiary (Accent):** An electric cyan, reserved strictly for calls-to-action, active states, and highlighting critical technical concepts.
- **Neutral:** A range of desaturated grays and slates used for secondary text and structural dividers.

The default state is **Dark Mode**, mirroring the preferred environment of professional developers. Light modes, if implemented, should maintain high contrast and avoid "warm" tints, staying within the cool-spectrum architectural grays.

## Typography

Typography plays a functional role in distinguishing between "concept" and "execution." 
- **JetBrains Mono** is utilized for headlines, labels, and metadata. This reinforces the technical nature of the content and provides an authoritative "code-first" voice.
- **Geist** is used for body text and instructional content. Its clean, humanist-influenced grotesque style ensures long-form readability without sacrificing the modern tech aesthetic.

Hierarchy is strictly enforced. All headings related to technical modules, API endpoints, or logic should use the monospace font. Large display sizes utilize tighter letter-spacing for a modern, compact look.

## Layout & Spacing

The layout is built on a **12-column fluid grid** for desktop and a **4-column grid** for mobile. We use an **8px base unit** to ensure consistent rhythm across all components.

- **Content Reflow:** On desktop, use a fixed-width central container (1280px) to prevent line lengths from becoming unreadable.
- **Logical Grouping:** Use generous vertical padding (64px to 128px) between major sections to emphasize the modularity of the curriculum.
- **Sidebar Navigation:** Documentation and lesson views should feature a fixed left-hand navigation rail for quick context switching between modules.

## Elevation & Depth

Depth is communicated through **Tonal Layering** rather than traditional shadows. In a dark environment, higher elevation is represented by lighter surface colors.

- **Level 0 (Background):** Primary deep navy (#0A192F).
- **Level 1 (Cards/Sidebar):** Secondary charcoal navy (#112240).
- **Level 2 (Popovers/Tooltips):** A slightly lighter navy/slate with a thin 1px border in the accent color at low opacity (15%).
- **Interactive States:** Use "Electric Cyan" glows (outer-glow/drop-shadow with 0 blur, 2px spread) to indicate focus or active states, mimicking a terminal cursor or energized circuit.

## Shapes

The shape language is **Soft but Precise**. While we avoid aggressive sharp corners to maintain a modern feel, we keep the radius tight to reflect structured logic.

- **Standard Elements:** Buttons and input fields use a 0.25rem (4px) radius.
- **Large Containers:** Cards and code blocks use a 0.5rem (8px) radius.
- **Interactive Indicators:** Small badges or chips may use a pill shape to distinguish them from structural UI elements.

## Components

- **Buttons:** Primary buttons are solid Electric Cyan with black text for maximum contrast. Secondary buttons use a Ghost style—thin 1px borders with the Cyan color.
- **Code Blocks:** Styled to resemble high-end IDEs. Background should be the darkest neutral, with a thin top-bar containing the file name in `label-sm` monospace.
- **Progress Indicators:** Use thin, horizontal bars. Completed lessons use the Cyan accent; current lessons use a pulse animation.
- **Cards:** No shadows. Use a 1px border of `#233554` (a lighter version of the secondary color) to define boundaries.
- **Input Fields:** Dark backgrounds with a 1px bottom-border that transforms into a full Cyan outline upon focus.
- **Terminal Component:** A specialized card variant for shell commands, featuring a simplified header with "traffic light" window controls to provide a familiar environment for back-end learners.