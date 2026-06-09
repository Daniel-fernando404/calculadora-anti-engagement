---
name: Anti-Deception Utility
colors:
  surface: '#faf8ff'
  surface-dim: '#d2d9f4'
  surface-bright: '#faf8ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f2f3ff'
  surface-container: '#eaedff'
  surface-container-high: '#e2e7ff'
  surface-container-highest: '#dae2fd'
  on-surface: '#131b2e'
  on-surface-variant: '#3d4a3d'
  inverse-surface: '#283044'
  inverse-on-surface: '#eef0ff'
  outline: '#6d7b6c'
  outline-variant: '#bccbb9'
  surface-tint: '#006e2f'
  primary: '#006e2f'
  on-primary: '#ffffff'
  primary-container: '#22c55e'
  on-primary-container: '#004b1e'
  inverse-primary: '#4ae176'
  secondary: '#b61722'
  on-secondary: '#ffffff'
  secondary-container: '#da3437'
  on-secondary-container: '#fffbff'
  tertiary: '#9e4036'
  on-tertiary: '#ffffff'
  tertiary-container: '#ff8b7c'
  on-tertiary-container: '#76231b'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#6bff8f'
  primary-fixed-dim: '#4ae176'
  on-primary-fixed: '#002109'
  on-primary-fixed-variant: '#005321'
  secondary-fixed: '#ffdad7'
  secondary-fixed-dim: '#ffb3ad'
  on-secondary-fixed: '#410004'
  on-secondary-fixed-variant: '#930013'
  tertiary-fixed: '#ffdad5'
  tertiary-fixed-dim: '#ffb4a9'
  on-tertiary-fixed: '#410001'
  on-tertiary-fixed-variant: '#7f2a21'
  background: '#faf8ff'
  on-background: '#131b2e'
  surface-variant: '#dae2fd'
typography:
  display-price:
    fontFamily: Inter
    fontSize: 48px
    fontWeight: '800'
    lineHeight: 48px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.01em
  headline-lg-mobile:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 32px
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '500'
    lineHeight: 28px
  label-mono:
    fontFamily: JetBrains Mono
    fontSize: 14px
    fontWeight: '600'
    lineHeight: 20px
    letterSpacing: 0.05em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 4px
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 40px
  container-margin: 16px
  gutter: 12px
---

## Brand & Style

The design system is built on a foundation of **Radical Functionalism**. It is designed for the high-friction environment of a supermarket: bright lights, physical movement, and cognitive load. The brand personality is honest, direct, and uncompromising—acting as a digital "bullshit detector" for deceptive pricing.

The visual style is **Ultra-Minimalist** with a focus on utility. It avoids unnecessary decoration, using heavy whitespace and high-contrast boundaries to ensure the user can find the cheapest unit price in seconds. The emotional response is one of clarity and empowerment against marketing tactics.

## Colors

The palette is strictly functional. 
- **Success Green (#22c55e):** Used exclusively to highlight the "Winner" (the lowest unit price). It serves as the primary action and validation color.
- **Deep Charcoal (#0f172a):** Used for primary text to ensure maximum legibility against the off-white background.
- **Off-White (#f8fafc):** The base background to reduce glare under harsh supermarket fluorescent lighting.
- **Error Red (#ef4444):** Used sparingly to denote the "Losing" price if a comparison is significantly worse value.
- **Muted Slate (#64748b):** Used for secondary information like unit labels (e.g., "per kg").

## Typography

This design system uses **Inter** for all primary interfaces due to its exceptional legibility and neutral, systematic tone. For technical data and unit types, **JetBrains Mono** is introduced to provide a clear visual distinction between descriptive text and raw data.

- **Scale:** Large, bold weights are prioritized. In a shopping aisle, users should be able to read the "Winner" price from a forearm's length while moving.
- **Contrast:** Level AA contrast is the minimum; Level AAA is the target for all price displays.

## Layout & Spacing

The layout utilizes a **Fixed-Width Mobile-First** approach, optimized for one-handed thumb use. 

- **Grid:** A simple 2-column grid is used for side-by-side product comparisons on larger screens, reflowing to a vertical stack on standard mobile devices.
- **Touch Targets:** Minimum touch target size is 48px. Inputs are full-width to accommodate quick taps while walking.
- **Visual Rhythm:** Generous vertical spacing (xl) between distinct comparison items to prevent visual crowding.

## Elevation & Depth

This design system rejects shadows in favor of **Tonal Layers and Bold Outlines**. 

- **Level 0:** Background (#f8fafc).
- **Level 1:** Cards/Plates (#ffffff) with a 1px solid border (#e2e8f0).
- **Level 2 (Active/Winner):** High-contrast border (2px solid #22c55e) to pull the element forward.

Depth is communicated through thickness and color, not light source simulation. This maintains the "Utility" aesthetic and ensures clarity in high-brightness environments.

## Shapes

The shape language is **Soft (0.25rem)**. While the brand is "Anti-Deception" and direct, sharp corners are avoided to keep the tool feeling modern and professional. 

- **Inputs:** Use standard `rounded` (0.25rem).
- **Comparison Cards:** Use `rounded-lg` (0.5rem) to distinguish the main container from internal elements.
- **Winner Badge:** Uses `rounded-xl` (0.75rem) to create a distinct, almost pill-like callout for the best value choice.

## Components

### Input Fields
Large-scale numeric inputs. Backgrounds are slightly grey (#f1f5f9) to indicate "Editability." Labels are placed inside the top-left corner in `label-mono` to maximize space for the numbers.

### Comparison Cards
The core component. A white container with a 1px border. When a product is determined to be the "Winner," the border thickens to 2px Success Green, and a "BEST VALUE" label appears in the top right.

### Buttons
- **Primary:** Solid Deep Charcoal with White text. High-impact, no-nonsense.
- **Secondary:** Transparent with a 1px Charcoal border.
- **Action:** Floating Action Button (FAB) for "Add New Comparison" uses Success Green with a white icon.

### Results Display
The final unit price (e.g., "$1.24 / kg") is displayed in `display-price`. It is the largest element on the screen.

### Logic Chips
Small, high-contrast badges used to tag items (e.g., "Bulk Pack", "Special Offer") to help the user remember which item is which during the comparison.