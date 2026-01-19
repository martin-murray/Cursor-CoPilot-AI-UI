# Design System Documentation

## Overview

The Cursor CoPilot AI UI design system provides a minimal, consistent foundation for building user interfaces. It includes design tokens, base components, and automated QA to help teams build client-ready UIs efficiently.

## Design Tokens

Design tokens are the atomic values that define the visual style of the system. They ensure consistency across all components and interfaces.

### Typography

#### Font Families
- **Base**: System font stack for optimal performance and native feel
- **Mono**: Monospace font stack for code and technical content

#### Font Sizes (Modular Scale - 1.250 Major Third)
- `--font-size-xs`: 0.64rem (10.24px)
- `--font-size-sm`: 0.8rem (12.8px)
- `--font-size-base`: 1rem (16px)
- `--font-size-md`: 1.25rem (20px)
- `--font-size-lg`: 1.563rem (25px)
- `--font-size-xl`: 1.953rem (31.25px)
- `--font-size-2xl`: 2.441rem (39.06px)
- `--font-size-3xl`: 3.052rem (48.83px)

#### Font Weights
- `--font-weight-regular`: 400
- `--font-weight-medium`: 500
- `--font-weight-semibold`: 600
- `--font-weight-bold`: 700

#### Line Heights
- `--line-height-tight`: 1.2 (for headings)
- `--line-height-base`: 1.5 (for body text)
- `--line-height-relaxed`: 1.75 (for comfortable reading)

### Spacing

Based on an 8px grid system for consistent vertical rhythm and horizontal spacing:

- `--space-1`: 0.25rem (4px)
- `--space-2`: 0.5rem (8px)
- `--space-3`: 0.75rem (12px)
- `--space-4`: 1rem (16px)
- `--space-5`: 1.25rem (20px)
- `--space-6`: 1.5rem (24px)
- `--space-8`: 2rem (32px)
- `--space-10`: 2.5rem (40px)
- `--space-12`: 3rem (48px)
- `--space-16`: 4rem (64px)
- `--space-20`: 5rem (80px)
- `--space-24`: 6rem (96px)

### Colors

#### Neutral Colors
- Gray scale from 50 (lightest) to 900 (darkest)
- White and Black

#### Primary Colors (Blue)
- Primary scale from 50 (lightest) to 900 (darkest)
- Used for primary actions, links, and emphasis

#### Semantic Colors
- **Success** (Green): For success states and positive feedback
- **Warning** (Yellow): For warnings and cautions
- **Error** (Red): For errors and destructive actions

#### Semantic Tokens
- `--color-background`: Main background color
- `--color-surface`: Surface elements (cards, panels)
- `--color-text-primary`: Primary text color
- `--color-text-secondary`: Secondary text color
- `--color-text-tertiary`: Tertiary text color
- `--color-border`: Border color
- `--color-border-hover`: Border color on hover

### Other Tokens

#### Border Radius
- `--radius-sm`: 0.25rem (4px)
- `--radius-base`: 0.375rem (6px)
- `--radius-md`: 0.5rem (8px)
- `--radius-lg`: 0.75rem (12px)
- `--radius-xl`: 1rem (16px)
- `--radius-full`: 9999px (fully rounded)

#### Shadows
- `--shadow-sm`: Subtle shadow
- `--shadow-base`: Default shadow
- `--shadow-md`: Medium shadow
- `--shadow-lg`: Large shadow
- `--shadow-xl`: Extra large shadow

#### Transitions
- `--transition-fast`: 150ms
- `--transition-base`: 200ms
- `--transition-slow`: 300ms

## Base Components

### Typography Components

#### Headings
- `.heading-1`: Page title (3xl, bold)
- `.heading-2`: Section title (2xl, bold)
- `.heading-3`: Subsection title (xl, semibold)
- `.heading-4`: Component title (lg, semibold)

#### Text
- `.text-body`: Standard body text (base size)
- `.text-small`: Small text for captions
- `.text-muted`: Muted text color for less emphasis

**Usage:**
```html
<h1 class="heading-1">Main Page Title</h1>
<h2 class="heading-2">Section Title</h2>
<p class="text-body">Body paragraph text</p>
<p class="text-small text-muted">Small muted caption</p>
```

### Button Component

Buttons come in two styles (primary and secondary) and three sizes (small, default, large).

**Classes:**
- `.button`: Base button class (required)
- `.button-primary`: Primary button style
- `.button-secondary`: Secondary button style
- `.button-small`: Small size variant
- `.button-large`: Large size variant

**Usage:**
```html
<button class="button button-primary">Primary Action</button>
<button class="button button-secondary">Secondary Action</button>
<button class="button button-primary button-small">Small Button</button>
<button class="button button-primary" disabled>Disabled</button>
```

**States:**
- Default
- Hover (automatic)
- Active (automatic)
- Disabled (use `disabled` attribute)

### Input Component

Text inputs for forms with consistent styling.

**Classes:**
- `.input`: Base input class
- `.form-group`: Container for label and input
- `.form-label`: Label styling

**Usage:**
```html
<div class="form-group">
  <label class="form-label" for="email">Email Address</label>
  <input type="email" id="email" class="input" placeholder="you@example.com">
</div>
```

**States:**
- Default
- Focus (automatic with blue ring)
- Disabled (use `disabled` attribute)

### Card Component

Container component for grouping related content.

**Classes:**
- `.card`: Base card container
- `.card-header`: Card header section
- `.card-title`: Card title
- `.card-description`: Card description
- `.card-content`: Main card content
- `.card-footer`: Card footer section

**Usage:**
```html
<div class="card">
  <div class="card-header">
    <h3 class="card-title">Card Title</h3>
    <p class="card-description">Card description text</p>
  </div>
  <div class="card-content">
    <p>Main content goes here</p>
  </div>
  <div class="card-footer">
    <button class="button button-primary">Action</button>
  </div>
</div>
```

### Layout Components

#### Container
`.container`: Centered container with max-width and responsive padding

#### Grid
- `.grid`: Base grid container
- `.grid-cols-1`: Single column
- `.grid-cols-2`: Two columns
- `.grid-cols-3`: Three columns

**Usage:**
```html
<div class="grid grid-cols-3">
  <div class="card">Column 1</div>
  <div class="card">Column 2</div>
  <div class="card">Column 3</div>
</div>
```

#### Flex Utilities
- `.flex`: Flex container
- `.flex-col`: Flex column direction
- `.items-center`: Align items center
- `.justify-between`: Space between items
- `.gap-2`, `.gap-4`, `.gap-6`: Gap sizes

### Spacing Utilities

Quick spacing utilities for common scenarios:
- `.mt-4`, `.mt-6`, `.mt-8`: Margin top
- `.mb-4`, `.mb-6`, `.mb-8`: Margin bottom
- `.py-8`, `.py-12`: Padding vertical

## Usage Guidelines

### Do's
✓ Use design tokens for all spacing, colors, and typography
✓ Use base components as building blocks
✓ Follow the spacing scale (8px grid)
✓ Use semantic color tokens for theme compatibility
✓ Maintain consistent typography hierarchy
✓ Prioritize clarity and usability

### Don'ts
✗ Don't add custom colors outside the token palette
✗ Don't use arbitrary spacing values
✗ Don't introduce new fonts
✗ Don't create custom components without using base components
✗ Don't override base styles unnecessarily

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- CSS Custom Properties (CSS Variables) required
- No IE11 support

## Getting Started

1. Include the CSS files in your HTML:
```html
<link rel="stylesheet" href="design-tokens.css">
<link rel="stylesheet" href="components.css">
```

2. Use the container and base components:
```html
<div class="container py-12">
  <h1 class="heading-1">Your Title</h1>
  <p class="text-body">Your content</p>
  <button class="button button-primary">Action</button>
</div>
```

3. Build your UI using only the defined tokens and components

## Examples

See `index.html` for a complete working example demonstrating all components and tokens.
