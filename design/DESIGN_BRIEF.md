# Energy Transition Research — Report Design Specification

**Version** 1.0 · 2026-08-08
**Scope** Layout, typographic, colour and production system for converting a corpus
of question-and-answer Markdown files into a publication-grade report.

This document is self-contained and portable. Copy it into the build directory; it
carries every value needed to implement the design without reference to any other file.

---

## 0. Hard constraints

1. **No McKinsey / MGI reference anywhere in the output** — not in visible text, the
   colophon, PDF metadata, file names, CSS class names, or code comments. Any
   reference material used to inform this design is a private study only.
2. Consequently: **no McKinsey Sans, no Bower**, and no use of their signature blue
   `#2251FF`. All colour derives from Energy Group brand assets.
3. All typefaces must be **open-licensed and embeddable** in a distributed PDF.
4. Design to **external-publication grade** throughout, since final audience is undecided.

---

## 1. Agreed decisions

| # | Area | Decision |
|---|---|---|
| 1 | Content architecture | Themed chapters; each question a numbered subsection (`n.n`) |
| 2 | Toolchain | Markdown → HTML/CSS → PDF via **Paged.js** + headless Chrome |
| 3 | Brand treatment | **Restrained** — editorial-neutral; logo used sparingly |
| 4 | Exhibits | Generated from supplied data into a house chart system |
| 5 | Page format | **A4 portrait**, 210 × 297 mm |
| 6 | Typography | Open-source pairing — display serif + neutral grotesque |
| 7 | Audience | Mixed / undecided → build to the highest bar |
| 8 | Deliverables | Print-grade PDF **and** responsive HTML from one source |

---

## 2. Information architecture

```
Front cover .................. title · deck · entity · date · logo
Contents ..................... chapters + full question index
At a glance .................. 4–6 bullet synthesis of the whole report
Introduction ................. framing narrative, 1–2 pp

  Chapter opener ............. oversized numeral · title · chapter
                               "At a glance" · accent rule
    n.1  Question as subsection heading
         Answer body, two columns
         Exhibits · callouts · pull-quotes
    n.2  Question …
  [repeat per chapter]

Methodology and scope ........ question selection, data vintage, limitations
Notes and sources ............ continuously numbered endnotes
Back cover ................... logo · entity · date · disclaimer
```

### Pagination rules

- Every chapter opens on a **recto** (odd-numbered, right-hand) page.
- A question never begins within 12 lines of a page foot.
- A question never splits across a chapter boundary.
- Widows and orphans suppressed globally (`orphans: 3; widows: 3`).
- Exhibits may float to the top of the next page but never precede the question
  that introduces them.

---

## 3. Page grid

| Property | Value | Notes |
|---|---|---|
| Trim | 210 × 297 mm | A4 portrait |
| Margin top | 20 mm | |
| Margin bottom | 18 mm | |
| Margin inner | 20 mm | binding side; mirrored on verso |
| Margin outer | 18 mm | |
| Live area | 172 × 259 mm | |
| Columns | 2 × 82 mm | |
| Gutter | 8 mm | |
| Baseline grid | 4.7625 mm ≈ 13.5 pt | all leading is a multiple |
| Bleed | 3 mm | print PDF only; omit for screen PDF |

Conversion constant: **1 mm = 2.834646 pt**.

### Page furniture

- **Running footer** only. No running header.
- Footer content: short report title at the **outer** edge, page number at the
  **inner** edge, hairline rule (`rule` colour, 0.25 pt) above, set at 7.5 pt.
- Footer suppressed on: front cover, contents, chapter openers, back cover.
- Folio numbering begins at 1 on the cover but is first *displayed* on the
  Contents page.

---

## 4. Colour system

All values sampled directly from the Energy Group Renewables wordmark gradient.

### Brand spectrum — also the categorical chart palette

| Token | Hex | Role |
|---|---|---|
| `--brand-teal` | `#0581A8` | Series 1 · chapter accent |
| `--brand-blue` | `#1A50A0` | **Primary accent** — rules, numerals, links |
| `--brand-violet` | `#5A439E` | Series 3 |
| `--brand-magenta` | `#902B94` | Series 4 |
| `--brand-crimson` | `#C03D5B` | Series 5 · negative / decline indicator |

### Neutrals

| Token | Hex | Role |
|---|---|---|
| `--ink` | `#0E1C2B` | Body text, headlines |
| `--ink-secondary` | `#5A6B7A` | Decks, captions, axis labels |
| `--ink-muted` | `#8A97A3` | Notes, sources, footer |
| `--rule` | `#D8DEE4` | Hairlines, table borders |
| `--tint` | `#F4F6F8` | Exhibit grounds, callout fills |
| `--paper` | `#FFFFFF` | Page |

### Application rules

- **One accent colour per chapter**, cycling the spectrum in order (Ch 1 teal,
  Ch 2 blue, Ch 3 violet, Ch 4 magenta, Ch 5 crimson, then repeat).
- The full five-hue gradient appears **only** on the front cover, chapter openers,
  and as a chart palette. Never as ornament within body text.
- Body copy is always `--ink` on `--paper`. No coloured body text.
- Sequential ramp: `--brand-teal` → `--brand-blue`, five steps.
  Diverging ramp: `--brand-crimson` ↔ neutral ↔ `--brand-teal`.
- **Validate before use:** every chart colour must clear 3:1 contrast against
  `--paper` for large marks, and the categorical set must remain distinguishable
  under deuteranopia and protanopia simulation. Where it does not, differentiate
  additionally by shape, texture or direct labelling — never by hue alone.
- Print PDF: define as CMYK-safe equivalents or accept the RGB→CMYK shift; confirm
  with the print vendor before final output.

---

## 5. Typography

**Specified pairing** — both SIL Open Font License, both variable, both embeddable:

- **Display serif:** Source Serif 4
- **Body sans:** Inter

Approved alternates if a specimen review rejects the above:
serif — Newsreader, Source Serif 4; sans — IBM Plex Sans, Source Sans 3.

### Type scale

| Element | Size / leading | Face | Colour |
|---|---|---|---|
| Cover title | 40 / 44 pt | Serif regular | `--ink` |
| Cover deck | 13 / 19 pt | Sans light | `--ink-secondary` |
| Chapter numeral | 64 pt | Serif light | chapter accent |
| Chapter title | 28 / 32 pt | Serif regular | `--ink` |
| Question heading (`n.n`) | 16 / 21 pt | Serif regular | `--ink` |
| Lede / deck | 12 / 17 pt | Sans light | `--ink-secondary` |
| Body | 9.5 / 13.5 pt | Sans light | `--ink` |
| Body emphasis | 9.5 pt | Sans light italic | `--ink` |
| Bullet list | 9.5 / 13.5 pt | Sans light, em-dash markers | `--ink` |
| Big-number callout | 44 pt | Serif regular | chapter accent |
| Pull-quote | 15 / 21 pt | Serif italic | `--ink` |
| Exhibit title | 11 pt | Sans medium | `--ink` |
| Exhibit subtitle | 8.5 pt | Sans light | `--ink-secondary` |
| Exhibit labels | 7.5 pt | Sans medium, all-caps, +40 tracking | `--ink-secondary` |
| Notes / sources | 6.5 / 9 pt | Sans light | `--ink-muted` |
| Footer | 7.5 pt | Sans light | `--ink-muted` |

### Setting rules

- Body is **ragged right**, not justified — 82 mm columns are too narrow to justify
  without rivers.
- Hyphenation on; minimum 3 characters before and after a break; maximum 2
  consecutive hyphenated lines.
- **Figures:** lining throughout. Apply `font-feature-settings: "tnum"` in all
  exhibits, tables and any column of aligned numbers.
- Em-dashes unspaced. Non-breaking spaces between a number and its unit
  (`30 GW`, `2.5 °C`).
- Endnote markers as superscript lining figures, continuous across the whole report.

---

## 6. Component inventory

The system consists of exactly these modules. Anything not on this list requires a
deliberate addition to the spec.

| Module | Description |
|---|---|
| Cover | Title, deck, entity, date, logo |
| Contents | Chapter list + question index with folios |
| At-a-glance block | Em-dash bullet list, bold lead-in phrase per bullet |
| Chapter opener | Numeral, title, accent rule, chapter at-a-glance |
| Question block | `n.n` heading + two-column answer body |
| Exhibit | See §7 |
| Big-number callout | Figure in accent colour + caption below |
| Pull-quote | Serif italic, hairline rule above and below |
| Comparison table | Tinted header row, hairline body rules, no vertical rules |
| Tier / status chip | Small rounded label for recurring categorical devices |
| Trend indicator | Three-state glyph — improving · neutral · deteriorating |
| Endnote list | Numbered, 6.5 / 9 pt |
| Back cover | Logo, entity, date, disclaimer |

---

## 7. Exhibit system

### Anatomy — fixed for every exhibit

```
Exhibit 4                                      ← 7.5pt caps, accent colour
Curtailment rises non-linearly beyond 30% solar share.
Share of generation curtailed, %, 2020–2035    ← 8.5pt subtitle: units + scope
┌────────────────────────────────────────────────────────────┐
│  [chart]                                                   │
└────────────────────────────────────────────────────────────┘
Note: …                                        ← 6.5pt
Source: …                                      ← 6.5pt
```

### Rules

- **Titles are assertions, not labels.** "Curtailment rises beyond 30% share" —
  never "Curtailment vs solar share".
- Subtitle must state **unit and scope**. No exception.
- Numbered continuously through the report, independent of chapter numbering.
- Permitted widths: half-column (40 mm), column (82 mm), full-width (172 mm),
  full-page (172 × 230 mm).
- Every exhibit carries a `Source:` line. Every derived or estimated figure carries
  a `Note:`.
- Rendered as **inline SVG**, not raster — required for print quality and for the
  HTML deliverable.

### Prohibited

No 3-D. No decorative gradients. No drop shadows. No pie charts above three slices.
No dual axes without an explicit justification recorded in the `Note:`. No truncated
value axes on bar charts. No hue-only encoding of categorical data.

### Recurring devices

A report reads as *designed* rather than *assembled* when a small number of visual
devices repeat across it. Confirm the final set once the content corpus is available;
candidates are the tier chip, trend indicator, big-number callout, comparison table,
and a full-page framework grid used at each chapter opening.

---

## 8. Logo usage

### Asset status — action required

The supplied `group_logo.png` is **not production-ready**: 1248 × 832 px RGBA with a
**baked-in near-white background** (corner pixels `#F5F6F6` and `#FEFEFF`), so it
renders a visible grey box on any tinted or dark surface. As raster it caps at
approximately 4.2 in wide at 300 dpi.

**Required before final output:** vector logo (SVG / EPS / AI) with true
transparency, plus a reversed (white) variant.

### Placement

| Location | Treatment |
|---|---|
| Front cover | Bottom-left, 34 mm wide, on white |
| Back cover | Centred, 34 mm wide, on white |
| Chapter openers | Not used |
| Body pages | Not used |
| HTML header | 28 mm equivalent, on white |

### Rules

Minimum reproduction width 24 mm. Clear space on all sides equals the cap-height of
the `a`. Never recoloured, stretched, rotated, or placed on a tinted panel or over
photography. Until the vector asset is supplied, **white backgrounds only**.

---

## 9. Content contract

### Directory structure to create in the build directory

```
├── content/               one .md file per question
├── data/                  one .csv per exhibit
├── config/
│   └── structure.yaml     chapter order, titles, accent assignment
├── assets/
│   ├── logo.svg           ← pending
│   └── logo-reversed.svg  ← pending
├── styles/
│   ├── tokens.css         colour + type variables from §4 and §5
│   ├── print.css          @page rules, Paged.js
│   └── screen.css         responsive HTML
├── templates/
└── build/                 report.pdf + /docs HTML output
```

### Required front-matter — every question file

```yaml
---
id: q-2-03
chapter: grid-and-storage
order: 3
question: "Why does curtailment rise sharply above 30% solar penetration?"
summary: "One-sentence answer, reused in the contents index and chapter at-a-glance."
exhibits: [curtailment-curve]
tags: [grid, solar, curtailment]
---
```

This front-matter is what allows the contents page, question index, chapter
summaries and cross-references to generate automatically rather than being
maintained by hand. **It is a hard requirement of the build, not a convenience.**

### Build pipeline

```
content/*.md ──► parse + validate front-matter
                      │
                 order by config/structure.yaml
                      │
data/*.csv ────► render exhibits to inline SVG
                      │
                 Markdown → templated HTML
                      │
        ┌─────────────┴─────────────┐
   print.css                    screen.css
        │                            │
  Paged.js + headless Chrome    responsive HTML
        │                            │
    report.pdf                   build/docs
```

The build must **fail loudly** on: missing front-matter field, unknown `chapter`
value, exhibit referenced but absent from `data/`, or an exhibit lacking a
`Source:` line.

---

## 10. Acceptance criteria

The design is complete when all of the following hold.

- [ ] Every chapter opens on a recto page.
- [ ] No widow or orphan lines anywhere in the document.
- [ ] All body leading sits on the 13.5 pt baseline grid.
- [ ] Every exhibit has an assertive title, a unit-and-scope subtitle, and a source line.
- [ ] Categorical chart colours remain distinguishable under deuteranopia simulation.
- [ ] No text below 6.5 pt anywhere.
- [ ] Logo appears only in the four locations listed in §8, always on white.
- [ ] Contents page folios match actual page numbers.
- [ ] Endnote numbering is continuous and every marker resolves to an entry.
- [ ] PDF passes a preflight check: all fonts embedded, no RGB in a CMYK print target.
- [ ] HTML deliverable is readable at 375 px width without horizontal scroll.
- [ ] Full-text search of the PDF returns zero hits for the constrained terms in §0.

---

## 11. Open items — blocking

These must be resolved before implementation begins.

| # | Item |
|---|---|
| 1 | **Volume** — how many Q&A files; typical and maximum answer length |
| 2 | **Chapter themes** — do groupings already exist, and in what order |
| 3 | **Sample file** — one representative `.md`; resolves more than any other answer |
| 4 | **Metadata** — report title, subtitle, author line, publication date |
| 5 | **Publishing entity** — Energy Group Renewables, Energy Group Renewables, or Energy Group. The supplied logo is the Renewables lockup specifically |
| 6 | **Vector logo** and the Energy Group brand guidelines document |
| 7 | **Citation policy** — does the §0 constraint also cover *source citations* in endnotes? If the underlying research draws on third-party published data, normal attribution practice requires it, and omitting attribution while using the data is a separate problem from avoiding brand association. Needs an explicit decision |
| 8 | **Exhibit data** — arriving as inline Markdown tables or separate CSVs; approximate exhibit count |
| 9 | **Legal** — required disclaimer text, confidentiality marking, approval line |

## 12. Open items — non-blocking

| # | Item |
|---|---|
| 10 | Cover treatment — type-only, abstract brand gradient, or photography |
| 11 | Section divider pages between chapters — yes or no |
| 12 | Separate question index at the back, in addition to the contents page |
| 13 | Version numbering and stated data-vintage cut-off date |
| 14 | Whether this becomes a recurring series — if so, build the template for reuse |

---

## 13. Recommended first build step

Do not build the full pipeline first. Build a **specimen**: three pages only —
front cover, one chapter opener, and one worked question spread with a real exhibit,
using real content. Judge the design there and iterate. Only once the specimen is
approved should the automated pipeline be built around it.
