# Design Tokens - AI Flow Studio
> P03 High-Fidelity Mockup & Design System | AI Workflow App
> Format: AI-readable, Figma-ready, code-translatable

## 1. Color Palette

### Primary - Indigo (5-7 shade)
- primary-50: #EEF2FF - bg subtle
- primary-100: #C7D2FE - hover bg
- primary-300: #818CF8 - border active
- primary-500: #6366F1 - MAIN primary action
- primary-700: #4338CA - pressed state
- primary-900: #312E81 - text on light

### Neutral
- neutral-0: #FFFFFF
- neutral-100: #F8FAFC
- neutral-300: #CBD5E1
- neutral-500: #64748B
- neutral-700: #334155
- neutral-900: #0F172A

### Semantic
- success: #10B981
- warning: #F59E0B
- error: #EF4444
- info: #0EA5E9

## 2. Typography - 6 Level (Font: Inter)

| Token | Size | Weight | LineHeight | Usage |
|---|---|---|---|---|
| display | 48px | 700 Bold | 52px | Hero |
| h1 | 32px | 700 Bold | 40px | Page Title |
| h2 | 24px | 600 Semibold | 32px | Section |
| body | 16px | 400 Regular | 24px | Default |
| body-sm | 14px | 400 Regular | 20px | Secondary |
| label | 12px | 500 Medium | 16px | Uppercase 8% tracking |

## 3. Spacing Scale

- space-4: 4px
- space-8: 8px
- space-16: 16px
- space-24: 24px
- space-32: 32px
- space-48: 48px

Rules: Component padding 16/24, Section gap 32, Page margin 24 desktop / 16 mobile, Card gap 16.

## 4. Radius & Shadow

- radius-sm: 8px (buttons, badges)
- radius-md: 12px (inputs)
- radius-lg: 16px (cards)
- radius-full: 9999px (FAB, avatar)

- shadow-sm: 0 1px 2px rgba(15,23,42,0.05)
- shadow-md: 0 4px 12px rgba(15,23,42,0.08)
- shadow-lg: 0 12px 24px rgba(15,23,42,0.12)

## 5. Reusable Components (6+)

1. Button Primary: bg primary-500, text neutral-0, h 44px, radius-sm, typo body-sm semibold
2. Button Secondary: bg neutral-0, border neutral-300, text neutral-700
3. Button Ghost: transparent, text primary-500
4. Input Field: h 44px, border neutral-300, radius-md, focus primary-500, padding 16
5. Card Workflow: bg neutral-0, radius-lg, shadow-md, padding 24, gap 16
6. Badge/Tag: bg primary-50, text primary-700, radius-full, padding 4 12
7. Navbar: h 64px, bg neutral-0, border-b neutral-100
8. Avatar + State: 32px, radius-full

All components use tokens, no hard-coded hex.

## 6. Tokens Export JSON

```json
{
  "color": {
    "primary": { "50": "#EEF2FF", "100": "#C7D2FE", "300": "#818CF8", "500": "#6366F1", "700": "#4338CA", "900": "#312E81" },
    "neutral": { "0": "#FFFFFF", "100": "#F8FAFC", "300": "#CBD5E1", "500": "#64748B", "700": "#334155", "900": "#0F172A" },
    "semantic": { "success": "#10B981", "warning": "#F59E0B", "error": "#EF4444", "info": "#0EA5E9" }
  },
  "typography": {
    "display": { "family": "Inter", "size": "48px", "weight": "700", "lineHeight": "52px" },
    "h1": { "family": "Inter", "size": "32px", "weight": "700", "lineHeight": "40px" },
    "h2": { "family": "Inter", "size": "24px", "weight": "600", "lineHeight": "32px" },
    "body": { "family": "Inter", "size": "16px", "weight": "400", "lineHeight": "24px" },
    "bodySm": { "family": "Inter", "size": "14px", "weight": "400", "lineHeight": "20px" },
    "label": { "family": "Inter", "size": "12px", "weight": "500", "lineHeight": "16px", "letterSpacing": "0.08em", "transform": "uppercase" }
  },
  "spacing": { "4": "4px", "8": "8px", "16": "16px", "24": "24px", "32": "32px", "48": "48px" },
  "radius": { "sm": "8px", "md": "12px", "lg": "16px", "full": "9999px" }
}
```

## 7. Prototype Flow

Login -> Home -> Detail -> Form -> Success (no broken link)

## 8. AI Prompt Ready

"Gunakan color.primary.500 #6366F1 untuk primary action, spacing scale 4/8/16/24/32/48, typography Inter 6 level, komponen Button/Input/Card/Badge/Navbar/Avatar. Semua layar konsisten token, tidak ada hex acak."

---
Medan, 15 Okt 2026
