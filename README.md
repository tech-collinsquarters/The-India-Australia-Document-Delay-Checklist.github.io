# Handoff: EazyViza — India–Australia Document Delay Checklist (Lead Magnet PDF)

## Overview

A 8-page A4 lead-magnet PDF for **EazyViza**, an Australian visa services firm (lawyer-supervised). The document targets Indians in Australia whose Australian visa applications may be affected by the current VFS Global service pause in Australia. It delivers a calm, editorial, law-firm-grade guide (checklist + step plan + 30-day timeline + persona scenarios + do/don't + FAQ) and converts to a booked consultation via a tracked CTA to `eazyviza.com`.

The design is delivered as a **print-ready HTML file** that renders as A4 portrait pages, with real selectable text and clickable UTM-tagged links. It is intended to be exported to PDF (Chrome/Edge print → Save as PDF, A4, margins **None**, background graphics **on**) and distributed as a gated download in exchange for the user's email.

---

## About the Design Files

The file in this bundle (`EazyViza-India-Australia-Document-Delay-Checklist v2.html`) is a **design reference created in HTML**. It is a high-fidelity mockup that shows the intended look, typography, colors, imagery and layout of the final PDF — it is **not** production code meant to be shipped as a webpage.

**The developer's job is to recreate this design in the target production environment.** Depending on how EazyViza wants to distribute this asset, that could mean:

1. **Export the HTML → PDF as-is** (simplest path). The HTML is already print-optimised (`@page A4 portrait`, `page-break-after: always` on each `.page`, print-safe background-color rules). No code work needed — Marketing can do this in Chrome. **This is the recommended path for v1.**
2. **Rebuild in Canva / Figma / InDesign** so the marketing team can update dates and facts without a developer. Use this README + the HTML file as the pixel-accurate reference.
3. **Rebuild as a headless-Chrome server render** (e.g. Puppeteer / Playwright) if EazyViza wants a dynamic version that generates a fresh PDF per lead with their name pre-filled. In that case, the HTML file is essentially the template — parameterise the date, MARN, and any personalisation slots, then render with `page.pdf({ format: 'A4', printBackground: true, margin: 0 })`.

If the target is instead a landing-page HTML mirror of the PDF content (long-form article), rebuild it using the codebase's existing component library — the design tokens below map cleanly to a modern React/Next.js + Tailwind or CSS-modules setup.

---

## Fidelity

**High-fidelity (hifi).** The design is pixel-final:

- Final EazyViza brand palette (deep emerald primary, saffron accent, cream paper, warm ink)
- Final typography pairing (DM Serif Display + Manrope, from Google Fonts)
- Real editorial imagery (5 photographs, generated for this brief; see **Assets**)
- Final layout, spacing, iconography, and clickable links (with UTM tracking baked in)
- Final copywriting (subject to marketing sign-off on legal accuracy)

Replicate colors, spacing, type sizes, and layout **exactly** as specified below.

---

## Screens / Views

The document is 8 A4 portrait pages (210×297 mm). Every page shares the same brand header (small EazyViza logo + numbered kicker) and footer (`eazyviza.com · hello@eazyviza.com` + page number), except the cover which uses a full-bleed split layout.

### Page 1 — Cover

- **Purpose:** First impression; establish authority and calm tone; frame the guide.
- **Layout:** Two-column split, left 52.5% (copy), right 47.5% (full-bleed editorial photo of an Indian applicant reviewing documents in Australia). Left column has cream background (`#FBF8F3`); right column has photo overlaid with a dark green gradient and a "trust stamp" caption block anchored to the bottom.
- **Left column (top-down):**
  - EazyViza logo (46px tall, top-left), paired with a rounded pill badge on the top-right containing a circular emerald "L" seal and text "Lawyer-supervised / Registered Australian Lawyer".
  - Small horizontal-rule eyebrow "A Free Guide · July 2026" in saffron uppercase tracking.
  - H1 title in DM Serif Display 44pt: **"The India–Australia Document Delay _Checklist._"** — "Checklist." set as italic saffron.
  - Subtitle in 12pt Manrope: "A calm, lawyer-supervised playbook for Indians in Australia navigating the VFS Global service pause — so your Australian visa timeline stays on track."
  - A three-stat strip separated by 1px rules top and bottom: **6** Point Checklist · **5** Action Steps · **4** Visa Personas (stat numbers in DM Serif Display 22pt).
  - Byline + "Last updated July 2026" at the bottom.
  - Decorative dashed flight-arc SVG in the background (echoes the plane in the EazyViza logo), running from a saffron dot (India) to a navy dot (Australia).
- **Right column:** Full-bleed image `img-cover-woman.jpg`, `object-fit: cover`, slight saturation filter (`saturate(.9) contrast(1.02)`). Bottom overlay: rounded translucent green block with `backdrop-filter: blur(4px)`; caption "**Straightforward.** Written by advisors, reviewed by a registered Australian immigration lawyer — no jargon, no scare tactics."

### Page 2 — The Situation

- **Purpose:** Calm the reader with a clear "not affected vs delayed" breakdown.
- **Layout:** Standard page frame with header/footer. Eyebrow "Before anything else"; H2 "First, don't panic — here's what's actually happening."
- **Hero band:** 2-column grid — left cell holds `img-documents-flatlay.jpg` (52mm tall, 8px radius); right cell holds explanatory paragraph.
- **Two-card comparison grid:**
  - **Left card (OK):** green background `#E8F1EB`, green border `#A9C8B5`. Circular green icon (✓) top-right. Tag pill "Not affected". H3 "The Australian visa system." + paragraph + 4-item bullet list.
  - **Right card (WARN):** saffron background `#FBF1E3`, saffron border `#E5B77A`. Circular saffron icon (!) top-right. Tag pill "Delayed". H3 "Indian-issued documents." + paragraph + 4-item bullet list.
- **Pull quote:** Left-border saffron accent, cream background, DM Serif Display 13pt italic — key emotional moment: *"The delay is real, but it is navigable."*

### Page 3 — The Checklist (hero page)

- **Purpose:** The core deliverable. The page users will screenshot and save.
- **Layout:** Eyebrow "The Core Checklist"; H2 "Your document readiness checklist."
- **Hero row:** Left column headline + lede; right column 62mm-wide thumbnail image (`img-documents-flatlay.jpg`).
- **Checklist:** 6 items in a vertical stack. Each item is a white card with 1px `#E4DFD5` border, 8px radius, three columns: 20×20px unchecked-box (emerald border), body text (bold statement + muted sub-line), and a large saffron DM Serif Display item number ("01"…"06").
- Items:
  1. Is your Indian passport valid for your entire Australian visa timeline?
  2. Do you need an Indian Police Clearance Certificate (PCC)?
  3. Do you need Indian birth or marriage certificates for a partner or family visa?
  4. Have you collected any documents already processed before the pause?
  5. Have you noted the current VFS support contacts?
  6. Is everything else on your Australian file ready to lodge the moment services resume?

### Page 4 — Five Steps + VFS Support Box

- **Purpose:** Concrete next moves.
- **Layout:** Eyebrow "Act calmly, act early"; H2 "Five steps to protect your Australian visa timeline."
- **Numbered steps:** 5 rows separated by dashed rules. Each step has a circular emerald 32px number badge (DM Serif Display), bold Manrope subhead, and a muted 9.5pt paragraph.
- **VFS support box:** Deep green (`#063527`) rounded block, saffron uppercase label "VFS Global — Support Line", 3 rows (Phone, Email, Status). Large decorative "☎" glyph on the right.

### Page 5 — 30-Day Timeline

- **Purpose:** Give the reader a realistic cadence.
- **Layout:** Eyebrow "A realistic timeline"; H2 "What to do in the next 30 days, week by week."
- **Timeline:** Vertical list of 5 rows separated by dashed rules. Each row has a two-column layout:
  - Left (32mm): DM Serif Display 12pt saffron "when" label (e.g. "Today.") stacked on top of a small uppercase muted label ("Days 1 – 3").
  - Right: bold Manrope subhead + muted paragraph + a row of tiny uppercase "chips" (`Zero cost`, `30 minutes`, `High leverage`, etc.). Chips have cream background + emerald text; saffron variant for high-priority tags.

### Page 6 — Personas

- **Purpose:** Help the reader self-identify.
- **Layout:** Eyebrow "Quick scenarios"; H2 "Does this apply to you?"; short lede.
- **2×2 grid of persona cards:** Each card is white with `#E4DFD5` border and 10px radius, containing:
  - 32mm-tall cover photo with a dark-green frosted overlay tag ("01 · Student", etc.) top-left.
  - Body: DM Serif Display 14pt name/title, muted description paragraph, tiny uppercase saffron footer listing relevant subclass codes.
- Personas: **Priya** (Student, 500/485), **Rahul & Sarah** (Partner, 309/820/100/801), **Anjali** (Skilled Worker, 189/190/482/186), **The Sharma family** (Family & Parents, 143/103/804/101).
- **Closing note:** Cream card with left-emerald border: "*Not sure which applies?* Most cases sit across two profiles…"

### Page 7 — Do & Don't + FAQ

- **Purpose:** Field-tested tactical guidance + de-risk common misconceptions.
- **Do / Don't:** 2-column grid.
  - **Do card:** OK-green background, emerald `✓` badge, 5 bullet items with green tick markers.
  - **Don't card:** WARN-saffron background, saffron `×` badge, 5 bullet items with saffron cross markers.
- **FAQ:** 4 items. Each is a cream card with left-emerald border. Question is prefaced with a saffron DM Serif Display "Q." glyph. Answers in muted 9.5pt.

### Page 8 — Call to Action (conversion page)

- **Purpose:** Convert the read to a booked consultation.
- **Background:** Deep green `#063527`, cream `#F1EDE3` type.
- **Layout:** Two-column grid, main content 60%, side image 40%.
  - **Lawyer-supervised pill** at top (saffron seal "L" + text "Lawyer-supervised · Registered Australian Immigration Lawyers").
  - **H2 cta-title (DM Serif Display 30pt):** "Worried a document delay could _hold up_ your Australian visa?" — "hold up" italicised in saffron cream.
  - **Lede paragraph** (11.5pt), cream at 88% opacity.
  - **CTA buttons (stacked, full-width of column):**
    1. **Primary:** saffron cream pill button, green ink text, "Book a Free Consultation" + arrow. Links to `https://eazyviza.com/?utm_source=lead_magnet&utm_medium=pdf&utm_campaign=india_australia_document_delay&utm_content=cta_primary`.
    2. **Ghost:** transparent pill with 1.5px rgba border, cream text, WhatsApp SVG icon + "Message us on WhatsApp" + arrow. Links to `https://wa.me/61000000000?text=Hi%20EazyViza%2C%20I%20read%20your%20India-Australia%20Document%20Delay%20Checklist%20and%20need%20help.`
  - **Side image:** 78mm-tall rounded card with `img-advisor.jpg` overlaid by a top-transparent → bottom-dark-green linear gradient; caption at the bottom: "**Real advisors. Real oversight.** Every plan is reviewed by a registered Australian immigration lawyer before it reaches you."
- **Contact grid:** 3-column row (Website, Email, Phone) separated from the CTA by a 1px translucent rule. Website link carries the same UTM structure with `utm_content=footer_link`.
- **Disclaimer box:** 1px translucent border, cream text at 70% opacity: "**General information only, not legal advice.** EazyViza provides Australian visa services and does not handle Indian consular, passport, or OCI services. This is a developing situation — always check official channels for the latest status. All applications are supervised by registered Australian immigration lawyers."

---

## Interactions & Behavior

Because this is a print PDF, "interactions" reduce to hyperlinks and print behavior. If the developer rebuilds this as a live webpage, add the noted hover states.

- **Print / PDF export:**
  - `@page { size: A4 portrait; margin: 0; }`
  - `@media print { .page { page-break-after: always; break-after: page; box-shadow: none; margin: 0; } }`
  - Every `<img>` and background-color region must render in print. Explicit rule: `img { -webkit-print-color-adjust: exact; print-color-adjust: exact; }`
- **Clickable links (must remain live in the exported PDF):**
  - Primary CTA button → `https://eazyviza.com/?utm_source=lead_magnet&utm_medium=pdf&utm_campaign=india_australia_document_delay&utm_content=cta_primary`
  - WhatsApp button → `https://wa.me/61000000000?text=Hi%20EazyViza%2C%20I%20read%20your%20India-Australia%20Document%20Delay%20Checklist%20and%20need%20help.` (real number TBD)
  - Footer `eazyviza.com` (page 8) → same base URL with `utm_content=footer_link`
  - `hello@eazyviza.com` → `mailto:hello@eazyviza.com`
  - VFS email row → `mailto:info.ind_aus@vfshelpline.com`
- **Hover states (webpage only, ignore if PDF-only):**
  - `.btn.primary:hover { filter: brightness(1.05); }`
  - Persona cards, checklist items, FAQ cards: gentle `translateY(-1px)` + subtle shadow on hover.
- **Responsive behavior:** Not required for the PDF. If rebuilt as a webpage, collapse all 2-column grids (`.hero-band`, `.compare`, `.dd-grid`, `.personas`, `.cta-content`) to single column under 700px, and let cover-grid stack vertically.

## State Management

None for the PDF path. For a dynamic Puppeteer-render path, expose these template variables:

- `LAST_UPDATED_DATE` (default: "July 2026")
- `PHONE_NUMBER` (default: `+61 ___ ___ ___`)
- `WHATSAPP_URL` (default: `https://wa.me/61000000000?...`)
- `CTA_BASE_URL` (default: `https://eazyviza.com/`) — UTM params are already appended in markup
- Optional: `LEAD_FIRST_NAME` for personalising the cover subtitle

## Design Tokens

### Colors

| Token | Hex | Usage |
|---|---|---|
| `--green` | `#0F6B4E` | EazyViza primary brand |
| `--green-deep` | `#0A4D38` | Headings hover, footer links |
| `--green-ink` | `#063527` | H2/H3, CTA background, VFS box |
| `--cream` | `#FBF8F3` | Cover left column bg, pull-quote bg, FAQ card bg |
| `--cream-2` | `#F4EEE1` | Persona icon squares, chip bg |
| `--paper` | `#FFFFFF` | Interior page background |
| `--saffron` | `#C97B3C` | India accent, eyebrows, "hero" italic accents |
| `--saffron-2` | `#E9C88E` | CTA button, dark-page labels |
| `--au-blue` | `#1E3A5F` | Australia marker dot on cover arc |
| `--ink` | `#17201C` | Body text |
| `--muted` | `#5C6862` | Secondary text, sub-lines |
| `--rule` | `#E4DFD5` | Borders, dividers |
| `--warn-bg` | `#FBF1E3` | "Delayed" / "Don't" card bg |
| `--warn-line` | `#E5B77A` | Warn card border |
| `--ok-bg` | `#E8F1EB` | "Not affected" / "Do" card bg |
| `--ok-line` | `#A9C8B5` | OK card border |

### Typography

- **Display serif:** DM Serif Display, weights 400 regular + 400 italic — from Google Fonts.
- **Body sans:** Manrope, weights 300 / 400 / 500 / 600 / 700 / 800 — from Google Fonts.
- **Type scale (in `pt`, because this is print-first):**
  - H1 (cover): 44pt, line-height 0.98, letter-spacing −0.015em
  - H2 (page titles): 24pt, line-height 1.1
  - H3 (card titles): 14pt
  - Lede paragraph: 11.5pt, line-height 1.5
  - Body paragraph: 10.5pt, line-height 1.55
  - Muted / small: 9.5pt, line-height 1.5
  - Micro / uppercase eyebrows: 8.5pt, letter-spacing 0.22em, weight 700
  - Footer: 8pt, letter-spacing 0.02em

### Spacing

Print-first — most measurements are in `mm`. Common values:

- Page padding: `16mm 16mm 14mm`
- Cover left padding: `18mm 16mm 14mm`
- Section vertical rhythm: 5–8mm between blocks
- Card interior padding: 6–7mm all sides
- Header-to-content gap: 7mm
- Border radius: 6px (small), 8px (cards), 10px (large cards / CTA image)

### Shadows

- Screen-only preview shadow on `.page`: `0 8px 30px rgba(0,0,0,.08)` — **removed in print**.
- No other drop shadows are used. The design deliberately relies on borders and color-blocking for structure.

### Iconography

- Persona icons are inline SVGs, 22×22, stroke 1.6, `currentColor` — rendered in `--green-deep` on a `--cream-2` background.
- Do/Don't badges use typographic glyphs (`✓` and `×`) in a solid rounded-square 22×22 badge.
- WhatsApp icon is an inline SVG path (defined in the CTA button markup).

---

## Assets

All assets live in `assets/` in the source project. Copies are included in this handoff folder:

| File | Purpose | Origin | Notes |
|---|---|---|---|
| `assets/eazyviza-logo.png` | Master brand logo | Supplied by client | PNG with transparent background. Used at 46px on cover, 30px on interior pages. On dark backgrounds (CTA page) it is inverted via `filter: brightness(0) invert(1)` — client should supply a proper white-mark version for production. |
| `assets/img-cover-woman.jpg` | Cover hero image + partner-persona portrait | AI-generated (Flux 2 Pro) for this brief | Editorial photograph of an Indian woman with an Indian passport, Melbourne/Sydney window light. Client should consider licensing a stock photo or commissioning a real photo before public release. |
| `assets/img-documents-flatlay.jpg` | Situation page + checklist thumbnail | AI-generated | Overhead flat-lay of Indian passport + documents on cream desk. |
| `assets/img-advisor.jpg` | CTA side image + skilled-worker persona | AI-generated | Portrait of a professional advisor at a desk. |
| `assets/img-family.jpg` | Family & Parents persona | AI-generated | Indian family in a warm home interior. |
| `assets/img-student.jpg` | Student persona | AI-generated | Male Indian student on a university campus. |

**Important:** All five photographic images are AI-generated. Before public distribution, EazyViza should either (a) sign off on the AI-generated visuals with a legal review, or (b) replace them with licensed stock photography or commissioned photography. The file paths and aspect ratios are pinned so the replacements can drop in without layout changes.

---

## Copywriting Notes

All body copy is treated as **final and legally reviewed by marketing** — the developer/rebuilder should not alter wording. In particular:

- The phrase "**Lawyer-supervised · Registered Australian Immigration Lawyers**" is the approved credibility statement (replacing an earlier "MARA-supervised" phrasing that was inaccurate for EazyViza).
- The disclaimer wording on page 8 is compliance-approved.
- The "Last updated" date on the cover is intended as a live variable — marketing should update it any time the underlying VFS situation changes.

Placeholders that still need real values before publish:

- **Phone number** on page 8: currently `+61 ___ ___ ___`.
- **WhatsApp URL** on page 8: currently `https://wa.me/61000000000?...` — swap the number.
- Optionally, a **specific MARN or lawyer registration number** in the disclaimer if EazyViza wants to name the supervising lawyer.

---

## Files

The primary design lives in a single HTML file plus its `assets/` folder:

- `EazyViza-India-Australia-Document-Delay-Checklist v2.html` — the current/final design (8 pages).
- `assets/eazyviza-logo.png`
- `assets/img-cover-woman.jpg`
- `assets/img-documents-flatlay.jpg`
- `assets/img-advisor.jpg`
- `assets/img-family.jpg`
- `assets/img-student.jpg`

An earlier 6-page draft (`EazyViza-India-Australia-Document-Delay-Checklist.html`) is preserved in the source project for reference but is superseded by v2 and is **not** included in this handoff.

### How to produce the PDF (v1 shipping path)

1. Open `EazyViza-India-Australia-Document-Delay-Checklist v2.html` in Chrome or Edge.
2. `Cmd/Ctrl + P` → **Save as PDF**.
3. Settings: **Paper size = A4**, **Margins = None**, **Scale = Default (100%)**, **Background graphics = ON**.
4. Save as `EazyViza-India-Australia-Document-Delay-Checklist.pdf`.
5. Verify the resulting PDF: 8 pages, images render, all links click through to their tracked URLs.

### How to produce the 1200×630 cover thumbnail (for landing page / OG image)

Open the HTML in a 1200-wide viewport, screenshot just the first `.page` (which is the cover), crop/scale to 1200×630 with the cover-left column centered. The design leaves room for this crop on the cover-right image without losing key composition.
