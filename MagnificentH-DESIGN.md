# MagnificentH - Design Guidelines

These guidelines define how MagnificentH looks, feels, and communicates. They apply to every view, component, and piece of copy in the product. When designing or reviewing any new view, each principle below must be considered and respected.

---

## 1. MagnificentH Figma Design Library First

All visual decisions must be based on the **[MagnificentH Figma Design Library](https://www.figma.com/design/z4YHGaWIWUFUnLw9CtYhDs/MagnificentH-library)**. Before building a custom component, style, or color, check whether the library already provides it. Custom solutions are only acceptable when the library has no equivalent, and must follow the library's visual conventions to remain consistent.

There are two key references inside the library file:

- **MH Design System page** — the design tokens that underpin everything: color system, typography (typefaces, weights, and usage), and shared effects (shadows). These must be used instead of arbitrary values in custom code.
- **Logos and symbols page** — the canonical logo, logomark, and symbol assets, including creative/test variations.

For product philosophy and tone (see sections 2-4 below), the source of truth is the **[MagnificentH Social Playbook](https://www.figma.com/slides/x5aSgR44HSIbaLWZotN9Ub)**.

**When designing a new view:** open the Figma library first. For any visual decisions (color, typography, effects), use the tokens documented below (sourced directly from the library). Only reach for custom solutions when the library cannot meet the requirement.

---

## 2. Tone of Voice — Cultural, Calm, Intentional

MagnificentH's voice is closer to a museum label, an essay introduction, or a curator's note than to a social app. Every piece of copy should reinforce that this is a cultural space, not a feed.

**What "social" means here.** On MagnificentH, "social" does **not** mean constant interaction, real-time conversation, visible popularity, or frequency of engagement. It means: *shared cultural reference + public presence + indirect connection over time* — closer to books, exhibitions, essays, and architecture than to feeds or chats.

**Positioning statement:**

> "MagnificentH is an open social platform for art and culture designed for intentional visits, not compulsive scrolling."

**The social contract, by comparison:**

| Platform | Social contract |
|---|---|
| Instagram | "Stay here. Don't leave." |
| MagnificentH | "Come when you want. Leave enriched." |

> "MagnificentH is social in the way museums and books are social — people don't scroll them, they share them."

**When writing copy for a new view:** read it aloud. Does it sound like a curator introducing a piece, or like a growth-hacking notification? Avoid language that implies urgency, FOMO, streaks, "come back now," or "don't miss out." Favor calm, descriptive, editorial phrasing.

---

## 3. Design Principles — Minimal, Intentional & Cultural

> "You are deliberately designing a social network, not accidentally adding social features."

The product is built with restraint, legitimacy, and depth — not engagement hacking. Core values: **Open · Intentional · Non-Addictive · Cultural**.

**Translate values into interface decisions:**

| Instead of... | Use... |
|---|---|
| Feed | Search |
| Thumbnails | Typography |
| Cards | Chapters |
| "Next up" | Exit cues |
| Alerts | Silence |

> "Even where the page ends matters."

**Community without feeds.** Discovery is based on search, themes, curated collections, and editions (time-bound groupings) — there is no central feed. This deliberately removes urgency, FOMO, and comparison.

**Success looks different here.** Do not measure this product like Instagram. Track: completion rates, average reading time, number of reading sessions completed per visit, authors returning to publish again, external references/embeds, depth of engagement per visit, and time to return (not frequency).

> "If someone visits once a week for 20 minutes, that is success. If people come back later — not tomorrow — you're succeeding."

**When designing a new view:** ask whether it encourages a calm, intentional visit or pulls the user into a loop. Default to search, typography, chapters, exit cues, and silence over feeds, thumbnails, cards, "next up," and alerts.

---

## 4. Non-Addictive Design — No Dark Patterns, Ever

To genuinely reject addictive mechanics, certain patterns must never be built — this is UX architecture, not just philosophy.

**Explicit anti-patterns — never build these:**

- Infinite scroll
- Algorithmic feeds / algorithmic amplification
- Follower graphs
- Open comments enabled too early
- Likes / reactions as a core mechanic

> "These destroy early cultural coherence."

**Activation without a daily-active-user goal.** There is no "come back every day" loop. Re-engagement happens through genuine new cultural content:

1. A new micro-museum is published
2. It is featured as part of a theme or collection
3. It is shared externally (newsletter, museum partner, author)
4. Readers arrive intentionally, read, complete, and leave

> "No loop tries to pull them back immediately."

**When designing a new view:** if a feature's primary purpose is to maximize time-on-app, frequency of return, or compulsive re-engagement, it does not belong in MagnificentH. Re-engagement must come from new cultural content (micro-museums, collections, editions) — never from notifications, streaks, or algorithmic surfacing.

---

## 5. Brand Typography

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

## 6. Color System

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

## 7. Effects & Elevation

| Token | Definition | Usage |
|---|---|---|
| `For mockups` (drop shadow) | `drop-shadow(4.09px 3.74px 3.74px rgba(0, 0, 0, 0.45))` | Applied to mockup frames / elevated surfaces in presentations and marketing material |

**When designing a new view:** reuse this shadow definition for any elevated surface (cards, modals, mockup frames) rather than inventing a new shadow value. Keep shadow usage minimal and purposeful.

---

## 8. Logo & Brand Mark

The canonical logo, logomark, and symbol variations live on the **Logos and symbols** page of the [MagnificentH Figma Design Library](https://www.figma.com/design/z4YHGaWIWUFUnLw9CtYhDs/MagnificentH-library), under the **"Official Logos"** and **"For web"** sections.

| Asset | Variants |
|---|---|
| **Logo full** (full lockup) | `Color=Light`, `Color=Dark` |
| **Logo text** (wordmark only) | `Color=Light`, `Color=Dark` |
| **Logo mini** (compact mark) | `Color=Multi`, `Color=Color4`, `Color=Light`, `Color=Dark` |
| **Logomark** (symbol only) | single mark, used in "For web" medium logo lockups |
| **Favicon** | square icon + rounded "Faviconmini" tile |

The page also contains a **"Creative Implementation / Testing"** section (Rubik's Cube explorations, etc.) — these are ideation references only and are not approved for production use unless promoted into the "Official Logos" / "For web" sections.

**When designing a new view:** always pull the logo/logomark asset directly from the Figma library rather than re-exporting or recreating it, so updates to the brand mark propagate consistently. Choose the `Light`/`Dark`/`Multi` variant based on the background color per the Color System above (e.g. `Color=Dark` on light/white backgrounds, `Color=Light` on dark or saturated backgrounds).

---

## 9. Responsive Breakpoints — Search Results Card Grid

The card grid on browse/search views (e.g. [Architecture spaces](https://spaces.magnificenth.com/s?pub_categoryLevel1=architecture)) is mobile-first. The values below were read directly from the live production CSS on 12 November 2026 and are the de facto standard until they are formalized in the Figma library.

**Standard grid** (`SearchResultsPanel_listingCards`, search results without the map):

| Breakpoint | Min-width | Card-grid columns |
|---|---|---|
| Mobile | 320px (base styles, no media query) | 1 |
| Tablet | 550px | 2 |
| Desktop | 1024px | 4 |

**Map variant** (`SearchResultsPanel_listingCardsMapVariant`, search results shown next to the map):

| Breakpoint | Min-width | Card-grid columns |
|---|---|---|
| Mobile / Tablet | base styles | 1 |
| Desktop | 1024px | 2 |
| Very wide | 1921px | 3 |

> **Notes:** 320px is the conventional minimum supported mobile viewport; 550px, 1024px and 1921px are the media queries found in the live CSS. The labels "Mobile / Tablet / Desktop" are descriptive names added for this doc. An earlier version of this section listed 3 columns from 1024px and 4 columns from 1500px; the live CSS has no 1500px breakpoint and goes straight to 4 columns at 1024px. The **Responsive Breakpoints** page in the Figma library still shows the earlier values (768px / 3 columns / 1500px) and should be updated to match.

**When designing a new view:** for any card grid (search results, collections, editions), follow the standard progression — 1 column by default, 2 columns from 550px, 4 columns from 1024px — or the map variant when results sit next to a map. Do not introduce additional breakpoints or column counts without first checking the live implementation and updating the Figma library so this section stays accurate.

---

## 10. Components, Spacing & Grid

### Where components live

- **MagnificentH library** — the only source for components used in new work. Everything listed below is published from it.
- **[Magnificent Platform](https://www.figma.com/design/EIN5k2bE3SmkUQgcrCnqhT/Magnificent-Platform) file** — the product screens. Its screens use the library components. A few local components remain there on purpose as **previous versions**, named "… — previous (…)" (for example the story cards with the gold Favorite star, and the category chip with a coloured square). They are kept for reference only: do not use them in new work.

The library components sit under **🪜 Under Construction**. They are usable but still evolving, so check the library for the latest version before building. (Inventory as of 12 November 2026.)

### Buttons & inputs

| Component | Variants | Notes |
|---|---|---|
| `Button item` | Type: Yellow, Black, Circled, Circled + F, Circled + B · State: Default, Hoover, Disabled | Main action button. Boolean props show or hide the back/forward arrows. |
| `Button Category` | Status: Default, Hover, Selected · Color: Brown, Orange, Yellow, Blue, Green, Water Green | **The only category chip.** 50px high, width hugs the label, same size on desktop and mobile. Default = white with a black outline. Hover and Selected = filled with the category colour, outline in the same colour, black text. Pick the Color from the category mapping below. Replaces the former `Subcategory`, `Button Category / Mobile` and `Buttons Historical Style`. |
| `Button Load more` | Device: Desktop, Mobile · State: Default, Hover | "LOAD MORE" button; Desktop is 198px wide, Mobile 343px. |
| `See More` | Status: Default, Hover | "SEE MORE STORIES" button, desktop. |
| `Button More / Mobile` | Status: Default, Selected | "SEE MORE STORIES" button, mobile (343px). |
| `SearchBar` | Status: Default, Typing | |
| `TabsList` / `TabsList Mobile` | TabsList — State: 1, 2, 3 | Step tabs of the Create flow (Add details · Browse photos · Write your story). |
| `Block` | — | "Historical style" picker block (chips such as Eclectic, Neo-Renaissance). |

#### Category colours

Each category has one colour from the palette (Section 6). It is used for the category's chips (`Button Category`, Color property), its building on the interactive map, and any other category accent.

| Category | Color | Hex |
|---|---|---|
| Architecture, Cinema | Brown | `#BD3D00` |
| Fashion, Music | Orange | `#F94700` |
| Design, Photography | Yellow | `#FEBD27` |
| Culture, Science | Blue | `#3685EA` |
| Art, Gardens & Landscapes, Icons | Green | `#009448` |
| Venues | Water Green | `#D5FAE9` |

> **Accessibility notes.** Chip labels are black on every colour. Black on Brown has a contrast of 3.8:1, below the 4.5:1 that WCAG AA asks for 16px text; all other colours pass. On Water Green, the outline and fill are very close to white (1.1:1), so a hovered or selected Venues chip relies on its fill alone to stand out. Revisit both if accessibility becomes a requirement.
>
> **Live site (spaces.magnificenth.com), checked 12 Nov 2026.** Category IDs in the code: Design = `interior-design`, Culture = `lifestyle`, Gardens & Landscapes = `outdoor-garden`, Icons = `Centennial`, Venues = `dining`. The search-page chips match this table, with three small differences to fix in the code: Art chips use Water Green `#D5FAE9` instead of Green; Fashion and Music use `#FF4F02` instead of Orange `#F94700`; Science uses `#3785E9` (and some map shapes `#3582E4`) instead of Blue `#3685EA`.

### Icons

Search, Close, Exit, Create, Create Navbar, Message me, Bookmark, `Favorite` (status: Default, Selected, gold, brown), `Icon backward` / `Icon forward` (Default, Hoover), `Expand_down` (Down, Up), `Button Filter`. The **Old system** section holds earlier icons that must not be used for new work.

Icons keep their base size in the library (for example `Exit` is 33×33); resize the instance where a screen needs it rather than changing the main component.

### Footer / NavBar

| Component | Variants | Notes |
|---|---|---|
| `NavBar` | Desktop, Create, Bookmark, My Gallery | Platform top bar, 1440px. |
| `Navbar / Mobile` | Mobile, Open, Search | Platform mobile bar with menu. |
| `NavBar Mobile 3` | — | Mobile bar with back arrow, search and "Filter by". |
| `NavBar Mobile / Logo + Search + Filter` | — | Mobile bar with logo tile, search and "Filter by". |
| `Footer / Desktop` | Color: White, Dark | 1440px. |
| `Footer / Mobile` | color: White, Dark | 375px. |

### Components

| Group | Components |
|---|---|
| Story cards | `Component Story / Desktop` (Default, Hover), `Component Story / Mobile`, `Component Story Vertical M`, `Example Story / Desktop`, `Component XL` |
| Highlight cards | `Story Card / Selected for you`, `Story Card / Selected for you + Description` (orange and blue "Selected for you" blocks, reserved for upcoming use) |
| Browse cards | `Component Browse / Desktop` (Default, Hoover), `Component Browse / Mobile` |
| Create flow | `Image Upload Section / Desktop`, `Image Upload Section / Mobile` |
| Interactive category map | `Button Room` (Default, Hoover, You are here, Pin) and the Architecture, Fashion, Photography and Art building illustrations (Default, Hoover, You are here). A fourth Architecture state on this page is linked from another file, not from the library. |

**Naming clean-up still to do.** Several variants still use "Hoover" for hover (`Button item`, `Icon backward` / `Icon forward`, `Component Browse / Desktop`, `Button Room` and the building illustrations), and some sets still use the default property name "Property 1". Use the names as they appear in the library until they are renamed; renaming a variant in the library keeps existing instances linked.

### Marketing website (magnificenth.com) — not yet in the library

The WordPress homepage design in the [Wordpress-Website](https://www.figma.com/design/aHtOW36Wk1uUji87FDoN2Q/Wordpress-Website) file uses local components that have no library equivalent yet: a marketing site header (the library `NavBar` is the platform bar), value card, experience row, museum card, step card, creator card, institution card and article card. It also relies on a hard black offset shadow (8px / 10px, no blur), an eyebrow text style (Alata 14, +2.4 tracking, uppercase, Brown) and Fraunces highlight sizes, none of which exist in the library. These are candidates to add.

### Spacing & grid — not yet defined

The library does **not** yet define a spacing scale, corner-radius tokens, or a layout grid as variables. The card-grid breakpoints in Section 9 are the only documented layout rule, derived from the live site.

**When designing a new view:** reuse the components above before building anything custom. For category filters, always use `Button Category`. Do not invent ad-hoc spacing or component conventions in this document. If a spacing scale, grid, or new component is needed, define it in the Figma library first, then mirror it here so the doc stays a faithful reflection of the source of truth.

---

## Using These Guidelines in Practice

When asked to design or review a view, apply this checklist:

1. Have you checked the [MagnificentH Figma Design Library](https://www.figma.com/design/z4YHGaWIWUFUnLw9CtYhDs/MagnificentH-library) for an existing token, style, or component before creating a new one?
2. Does the copy sound like a curator's note, not a growth notification — calm, editorial, free of urgency/FOMO language?
3. Does the view favor search, typography, chapters, exit cues, and silence over feeds, thumbnails, cards, and alerts?
4. Does it avoid every banned anti-pattern (infinite scroll, algorithmic feed, follower graph, early open comments, likes-as-core-mechanic)?
5. Does typography follow the role mapping (Fraunces → logo/highlights, Libre Franklin → body, Alata → titles/buttons/UI, Lora → article subheads)?
6. Are colors referenced by token name from the palettes above, not arbitrary hex values?
7. Is the Error palette used only for error/validation states?
8. Does any elevated surface reuse the documented shadow token instead of a new one?
9. Is the correct logo variant (Light/Dark/Multi) used for the background it sits on, pulled from the Figma library rather than recreated?
10. Have you reused the library's existing components (Section 10) first — `Button Category` for every category filter, no "previous" components from the platform file — and raised any missing spacing/grid/component need to add to the Figma library rather than improvising it?
11. Does any card grid follow the responsive breakpoints in Section 9 (1 column by default, 2 from 550px, 4 from 1024px; map variant: 2 from 1024px, 3 from 1921px)?
