# 🎨 MONETEC BRAND SPECIFICATIONS

## COLOR SYSTEM

### Primary Colors
```css
/* Monetec Yellow */
--monetec-yellow: #F5A700;
--monetec-yellow-rgb: 245, 167, 0;
--monetec-yellow-hsl: 41, 100%, 48%;

/* Navy Blue */
--monetec-navy: #0A2647;
--monetec-navy-rgb: 10, 38, 71;
--monetec-navy-hsl: 212, 75%, 16%;

/* Black */
--monetec-black: #000000;
--monetec-black-rgb: 0, 0, 0;
```

### Usage Guidelines
- **Yellow**: CTAs, highlights, key metrics
- **Navy**: Headers, important text
- **Black**: Backgrounds, depth
- **White**: Body text on dark

## TYPOGRAPHY

### Font Family
```css
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@200;400;500&display=swap');

/* Headers */
.header {
  font-family: 'Montserrat', sans-serif;
  font-weight: 200; /* ExtraLight */
  text-transform: uppercase;
  letter-spacing: 0.1em;
}

/* Body */
.body {
  font-family: 'Montserrat', sans-serif;
  font-weight: 400; /* Regular */
  line-height: 1.6;
}

/* Numbers */
.number {
  font-family: 'Montserrat', sans-serif;
  font-weight: 500; /* Medium */
}
```

### Size Scale
- H1: 72px / 4.5rem
- H2: 48px / 3rem
- H3: 36px / 2.25rem
- Body: 18px / 1.125rem
- Small: 14px / 0.875rem

## VISUAL PATTERNS

### Hexagonal Grid
```svg
<pattern id="hex-pattern">
  <!-- Hexagon path coordinates -->
  <polygon points="30,10 50,10 60,30 50,50 30,50 20,30"/>
</pattern>
```

### Animation Principles
1. **Emergence** (not appearance)
2. **Slow and deliberate** (1.5-2s)
3. **Light halos** on key elements
4. **Smooth morphing** transitions

## SPACING SYSTEM

```css
/* 8px base unit */
--space-xs: 8px;
--space-sm: 16px;
--space-md: 24px;
--space-lg: 48px;
--space-xl: 96px;
```

## GERMAN FORMATTING

### Currency
- ALWAYS: €1.000.000
- NEVER: 1.000.000€

### Number Formatting
- Thousands: Period (.)
- Decimals: Comma (,)
- Example: €1.234.567,89