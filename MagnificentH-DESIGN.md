# MagnificentH - Design Guidelines

These guidelines define how MagnificentH looks, feels, and communicates. They apply to every view, component, and piece of copy in the product. When designing or reviewing any new view, each principle below must be considered and respected.

---

## 1. MagnificentH Figma Design Library First

All visual decisions must be based on the **[MagnificentH Figma Design Library](https://www.figma.com/design/z4YHGaWIWUFUnLw9CtYhDs/MagnificentH-library)**. Before building a custom component, style, or color, check whether the library already provides it. Custom solutions are only acceptable when the library has no equivalent, and must follow the library's visual conventions to remain consistent.

There are two key references inside the library file:

- **MH Design System page** — the design tokens that underpin everything: color system, typography (typefaces, weights, and usage), and shared effects (shadows). These must be used instead of arbitrary values in custom code.
- **Logos and symbols page** — the canonical logo, logomark, and symbol assets, including creative/test variations.

**When designing a new view:** open the Figma library first. For any visual decisions (color, typography, effects), use the tokens documented below (sourced directly from the library). Only reach for custom solutions when the library cannot meet the requirement.

---

## 2. Brand Typography

MagnificentH uses four typefaces, each with a distinct purpose. Together they balance an editorial, characterful brand voice (Fraunces, Lora) with a clean, structured interface (Libre Franklin, Alata).

| Typeface | Role | Weights used | Source |
|---|---|---|---|
| **Fraunces** | Logotype and selected highlight titles (e.g. login, marketing tool purpose) | Regular | [Google Fonts](https://fonts.google.com/specimen/Fraunces) |
| **Libre Franklin** | Body text, paragraphs, and all info boxes | Regular, Medium, SemiBold | [Google Fonts](https://fonts.google.com/specimen/Libre+Franklin) |
| **Alata** | All titles, buttons, and emphasis / interface elements | Regular | [Google Fonts](https://fonts.google.com/specimen/Alata) |
| **Lora** | Article subheadings, set in uppercase for a magazine/newspaper-style editorial tone | Regular, Medium | [Google Fonts](https://fonts.google.com/specimen/Lora) |

**Usage notes:**

- **Fraunces** is an "Old Style" soft-serif display face. It brings character, warmth, and print-era nostalgia to the brand. Use it sparingly — for the logo and standout highlight titles only — so it doesn't compete with the rest of the interface.
- **Libre Franklin** is the workhorse body typeface, chosen for clarity, readability, and neutrality. It complements the expressive Fraunces logo and the geometric Alata.
- **Alata** is a geometric, low-contrast sans used for titles, buttons, and navigation. Its clean structure echoes the brand's logomark and gives the UI a clear visual hierarchy.
- **Lora** is reserved for article subheaders, set in uppercase, to give long-form content a publication-style rhythm and hierarchy.

**When designing a new view:** pick the typeface based on role (logo/highlight → Fraunces, body → Libre Franklin, UI/titles/buttons → Alata, article subheads → Lora), not on personal preference. Never introduce a fifth typeface without updating the library first.

---

## 3. Color System

All colors below are defined as variables/tokens in the Figma library and must be referenced by token name, not by raw hex value, wherever the codebase supports design tokens.

### Primary palette

| Token | Hex | HSL |
|---|---|---|
| Yellow | `#FEBD27` | 42° 99% 57% |
| Brown | `#BD3D00` | 19° 100% 37% |
| Orange (`Accent Colors/Orange`) | `#F94700` | 17° 100% 49% |

### Accent palette

| Token | Hex | HSL |
|---|---|---|
| Blue | `#3685EA` | 214° 81% 56% |
| Green (`Accent Colors/Green`) | `#009448` | 149° 100% 29% |
| Light / Water Green (`Accent Colors/Water Green`) | `#D5FAE9` | 152° 79% 91% |

### Neutrals

| Token | Hex | HSL |
|---|---|---|
| Black 00 | `#000000` | 0° 0% 0% |
| Off Black (`Grey Scale/Off Black #333`) | `#333333` | — |
| Light Grey | `#F5F5F5` | 0° 0% 96% |
| White (`Grey/00`) | `#FFFFFF` | — |

### Semantic / status

| Token | Hex | HSL |
|---|---|---|
| Error | `#FF0000` | 0° 100% 50% |
| Error Light | `#FFCCCC` | 0° 100% 90% |

### Text colors

| Token | Hex | Usage |
|---|---|---|
| `Text Color/Dark` | `#2D3649` | Default body/heading text on light backgrounds |
| `Text Color/White` | `#FFFFFF` | Text on dark or colored backgrounds |

**When designing a new view:** use the Primary palette for brand moments (logo, hero accents), the Accent palette for highlights, tags, and secondary emphasis, Neutrals for backgrounds and structure, and the Error palette only for validation/error states. Never use raw error red or error light for anything other than error/destructive states.

---

## 4. Effects & Elevation

| Token | Definition | Usage |
|---|---|---|
| `For mockups` (drop shadow) | `drop-shadow(4.09px 3.74px 3.74px rgba(0, 0, 0, 0.45))` | Applied to mockup frames / elevated surfaces in presentations and marketing material |

**When designing a new view:** reuse this shadow definition for any elevated surface (cards, modals, mockup frames) rather than inventing a new shadow value. Keep shadow usage minimal and purposeful.

---

## 5. Logo & Brand Mark

The canonical logo, logomark, and symbol variations live on the **Logos and symbols** page of the [MagnificentH Figma Design Library](https://www.figma.com/design/z4YHGaWIWUFUnLw9CtYhDs/MagnificentH-library). This page also contains creative/test implementations (e.g. mockup explorations) — these are references for ideation only and are not approved for production use unless promoted to the core library.

**When designing a new view:** always pull the logo/logomark asset directly from the Figma library rather than re-exporting or recreating it, so updates to the brand mark propagate consistently.

---

## Using These Guidelines in Practice

When asked to design or review a view, apply this checklist:

1. Have you checked the [MagnificentH Figma Design Library](https://www.figma.com/design/z4YHGaWIWUFUnLw9CtYhDs/MagnificentH-library) for an existing token, style, or component before creating a new one?
2. Does typography follow the role mapping (Fraunces → logo/highlights, Libre Franklin → body, Alata → titles/buttons/UI, Lora → article subheads)?
3. Are colors referenced by token name from the palettes above, not arbitrary hex values?
4. Is the Error palette used only for error/validation states?
5. Does any elevated surface reuse the documented shadow token instead of a new one?
6. Is the logo/logomark pulled from the Figma library rather than recreated?
