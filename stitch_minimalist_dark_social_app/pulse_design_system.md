---
name: "Pulse"
description: "A sleek, high-contrast dark mode design system for modern mobile social media featuring electric purple and neon pink accents with refined elevation and 8pt rhythm."
---

## Overview

Pulse is a modern, clean, and minimalist design system crafted for mobile-first social discovery and visual storytelling. The system embraces a sleek, deep dark aesthetic engineered to let high-resolution photography and digital art command primary attention. High-contrast vibrant accents—electric purple (`#8B5CF6`) and neon pink (`#EC4899`)—energize interactions, notification pings, story rings, and micro-interactions without causing visual fatigue or halation.

The interface adheres strictly to an 8pt grid system, disciplined elevation stepping, subtle rounded corners, and clean typography that balances legibility with contemporary edge.

## Colors

The palette operates on rich, layered dark neutrals with controlled vibrancy for interactive and expressive states.

- **Primary:** Electric purple evokes digital energy, creativity, and futuristic connection.
- **Secondary:** Neon pink provides high-contrast vibrancy for likes, live status, unread notifications, and expressive highlights.
- **Surface Tiers:** Built on tiered dark neutrals (`#0D0D12` root background stepping up to `#16161F` cards and `#22222E` containers), preventing pure `#000000` text halation while preserving OLED depth.

```yaml
colors:
  electric-purple: "#8B5CF6"
  neon-pink: "#EC4899"
  light:
    primary: "#6D28D9"
    on-primary: "#FFFFFF"
    secondary: "#BE185D"
    on-secondary: "#FFFFFF"
    surface: "#FAFAFC"
    on-surface: "#0F172A"
    surface-container: "#F1F5F9"
    on-surface-container: "#334155"
    outline: "#CBD5E1"
    outline-variant: "#E2E8F0"
  dark:
    primary: "#A78BFA"
    on-primary: "#1E1145"
    secondary: "#F472B6"
    on-secondary: "#4C0519"
    surface: "#0D0D12"
    on-surface: "#F3F4F6"
    surface-container: "#16161F"
    on-surface-container: "#E5E7EB"
    surface-container-high: "#22222E"
    on-surface-container-high: "#FFFFFF"
    outline: "#2E2E3E"
    outline-variant: "#1E1E2A"
```

## Typography

The type scale combines **Red Hat Text** for geometric, confident headings and branding with **Instrument Sans** for highly legible, fluid UI elements and body copy.

```yaml
typography:
  headline-xl:
    fontFamily: "Red Hat Text"
    fontSize: 36px
    fontWeight: 700
    lineHeight: 44px
    letterSpacing: -0.5px
  headline-xl-mobile:
    fontFamily: "Red Hat Text"
    fontSize: 28px
    fontWeight: 700
    lineHeight: 34px
    letterSpacing: -0.4px
  headline-lg:
    fontFamily: "Red Hat Text"
    fontSize: 30px
    fontWeight: 700
    lineHeight: 38px
    letterSpacing: -0.3px
  headline-lg-mobile:
    fontFamily: "Red Hat Text"
    fontSize: 24px
    fontWeight: 700
    lineHeight: 30px
    letterSpacing: -0.2px
  headline-sm:
    fontFamily: "Red Hat Text"
    fontSize: 18px
    fontWeight: 600
    lineHeight: 24px
  headline-sm-mobile:
    fontFamily: "Red Hat Text"
    fontSize: 16px
    fontWeight: 600
    lineHeight: 22px
  body-lg:
    fontFamily: "Instrument Sans"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 24px
  body-md:
    fontFamily: "Instrument Sans"
    fontSize: 14px
    fontWeight: 400
    lineHeight: 20px
  body-sm:
    fontFamily: "Instrument Sans"
    fontSize: 12px
    fontWeight: 400
    lineHeight: 16px
  label-lg:
    fontFamily: "Instrument Sans"
    fontSize: 14px
    fontWeight: 600
    lineHeight: 20px
  label-md:
    fontFamily: "Instrument Sans"
    fontSize: 12px
    fontWeight: 600
    lineHeight: 16px
  label-sm:
    fontFamily: "Instrument Sans"
    fontSize: 11px
    fontWeight: 600
    lineHeight: 14px
```

## Layout & Spacing

Pulse strictly enforces an **8pt grid system** with 4pt half-steps for micro-alignments, iconography margins, and avatar badge placements.

- **Mobile Viewport:** Standard 390px fluid mobile canvas with 16px horizontal screen gutters.
- **Card Spacing:** 16px vertical gap between feed cards; 12px internal card padding.
- **Bottom Navigation Dock:** Fixed 64px bar height + safe area inset padding, distributing 5 key navigation targets evenly across the 390px width.

```yaml
spacing:
  xs: 4px
  sm: 8px
  md: 12px
  base: 16px
  lg: 20px
  xl: 24px
  2xl: 32px
  gutter-mobile: 16px
  nav-height: 64px
```

## Elevation & Depth

Depth is established through subtle surface stepping and diffused ambient shadows rather than harsh borders or heavy outlines:
- **Surface Elevation:** Base canvas `#0D0D12` sits at elevation 0. Post cards sit at `#16161F` with a soft diffused ambient shadow (`0 8px 24px -4px rgba(0, 0, 0, 0.45)` and a micro 1px outline of `rgba(255, 255, 255, 0.05)`).
- **Navigation Dock & Header:** Elevation 2 with refined backdrop blur (`rgba(13, 13, 18, 0.85)`) providing clear separation over scrolling media feeds.
- **Accents:** Active elements glow with subtle localized drop shadows in matching chromatic tints (e.g. electric purple `0 4px 14px rgba(139, 92, 246, 0.35)`).

## Shapes

Shapes reflect modern mobile ergonomics: subtle rounded corners on content cards (`16px`), friendly rounded avatars (`full`), compact chips (`12px`), and action buttons (`12px` to `full`).

```yaml
rounded:
  sm: 6px
  md: 10px
  lg: 16px
  xl: 20px
  full: 9999px
```

## Motion & Micro-interaction

Micro-interactions feel crisp, snappy, and responsive:
- **Heart / Like Interaction:** Bouncy spring scale pop (`transform: scale(1.2)`) settling back to `1.0` within 180ms.
- **Story Ring / Gradient Glow:** Smooth chromatic pulse indicating live or unviewed stories.
- **Tab Switching:** Instant 120ms cross-fade with subtle 2px vertical icon bounce.

```yaml
motion:
  tap:
    duration: 120ms
    delay: 0ms
    timingFunction: cubic-bezier(0.4, 0, 0.2, 1)
  heart-pop:
    duration: 200ms
    delay: 0ms
    timingFunction: cubic-bezier(0.175, 0.885, 0.32, 1.275)
  drawer-slide:
    duration: 250ms
    delay: 0ms
    timingFunction: cubic-bezier(0.2, 0, 0, 1)
```

## Voice & Content Strategy

Pulse communicates with a modern, confident, and effortless tone:
- **Action Verbs:** Actionable and concise ("Follow", "Reply", "Share post", "Save").
- **Numbers & Metrics:** Tabular numerals with concise abbreviators (`14.2k`, `892`, `45m ago`).
- **User Focus:** Human-centric, empowering content discovery and genuine creator community interaction.

## Components

Component implementations live as individual HTML sticker sheet files in
`components/`. Each file contains the canonical, styled HTML components with
`<!-- COMPONENT: name -->` comment markers. Read each file before use.

- **Avatar** → `@components/avatar.html`: `avatar-image`, `avatar-editable`
- **Button** → `@components/button.html`: `button-primary`, `button-icon`, `button-with-icon`
- **Card** → `@components/card.html`: `card-elevated`, `card-action`, `card-interactive`, `card-interactive-2`
