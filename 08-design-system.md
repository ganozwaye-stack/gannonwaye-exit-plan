# Design System

## Colors (HSL tokens)

### Light / Dark (same values — dark theme)

| Token | HSL | Hex | Usage |
|-------|-----|-----|-------|
| `--background` | 220 15% 6% | #0F1116 | Page background |
| `--foreground` | 40 20% 92% | #EBE4D4 | Body text |
| `--card` | 220 12% 9% | #161920 | Cards, panels |
| `--primary` | 40 85% 58% | #F5D06E | CTAs, accents |
| `--accent` | 40 75% 52% | #C9A84C | Gradient pairs |
| `--secondary` | 220 10% 14% | #23262D | Secondary elements |
| `--muted` | 220 10% 14% | #23262D | Muted backgrounds |
| `--muted-foreground` | 220 10% 50% | #7A7E88 | Secondary text |
| `--border` | 220 10% 16% | #262A33 | Borders, dividers |
| `--destructive` | 0 84% 60% | #E5484D | Errors, delete |

### Gold Gradient

```css
background: linear-gradient(90deg, #c9a84c 0%, #f5d06e 40%, #ffe08a 50%, #f5d06e 60%, #c9a84c 100%);
```

## Typography

| Role | Font | CSS |
|------|------|-----|
| Display/Headings | Playfair Display | `'Playfair Display', serif` |
| Body/UI | Inter | `'Inter', sans-serif` |

### Google Fonts Import

```css
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500&family=Inter:wght@300;400;500;600;700&family=Dancing+Script:wght@400;600&family=Poppins:wght@300;400;500;600;700&display=swap');
```

## CSS Utility Classes

```css
.gradient-gold-text    /* Gold gradient text with clip */
.gradient-gold-glow    /* Gold gradient with glow shadow */
.gradient-gold-button  /* Gold gradient button style */
```

## Border Radius

- `--radius: 0.5rem` (8px)
- lg: 8px, md: 6px, sm: 4px

## Installed Packages

React, Tailwind CSS, shadcn/ui, lucide-react, moment, recharts, react-quill-new, react-hook-form, react-router-dom, date-fns, lodash, react-markdown, framer-motion, three.js, react-leaflet, @hello-pangea/dnd, @tanstack/react-query, @stripe/react-stripe-js, @stripe/stripe-js, zustand, zod, cmdk, canvas-confetti, gsap, html2canvas, jspdf, posthog-js, sonner, vaul
