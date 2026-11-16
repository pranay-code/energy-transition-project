# Layout plan — v2

**Status:** agreed 8 August 2026. This file replaces the page-geometry parts of
`DESIGN_BRIEF.md` (§3 page system, §5 type scale, §6 break-out module). Everything else in
the brief — colour tokens, exhibit anatomy, the no-attribution constraint, acceptance
criteria — still stands.

**Why v2 exists.** v1 set the text at 130 mm inside a 176 mm live area and let tables and
charts "break out" to the wider measure. Three different right edges appeared on one page
and it read as a fault. The fix is not better break-out code. The fix is to delete
break-out.

---

## 1 · The one rule

**Everything is the same width.** Body text, tables, charts, exhibits, notes, headings —
all start at the same left edge and stop at the same right edge.

No break-outs. No negative margins. No wide variant. No `full` / `col` / `half` widths. If a
table is too wide for the measure, the table gets fewer columns or smaller type — the page
does not get wider.

---

## 2 · Page geometry

A4, 210 × 297 mm. **Printed and bound**, so margins mirror.

| | Recto (right-hand, odd) | Verso (left-hand, even) |
|---|---|---|
| Inner (binding side) | 32 mm left | 32 mm right |
| Outer | 28 mm right | 28 mm left |
| Top | 25 mm | 25 mm |
| Bottom | 28 mm | 28 mm |

- **Measure: 150 mm.** Fixed. 210 − 32 − 28.
- **Live height: 244 mm.** 297 − 25 − 28.
- The footer sits inside the bottom margin, baseline 14 mm up from the trim edge.
- `* { box-sizing: border-box }` stays.

---

## 3 · Type

Source Serif 4 (`Report Serif`) and Inter (`Report Sans`), self-hosted variable woff2, both
OFL. Unchanged from v1.

| Use | Size / leading | Family, weight |
|---|---|---|
| Cover title | 40 / 44 pt | serif 400 |
| Cover deck | 13 / 19 pt | sans 300 |
| Chapter numeral | 64 pt | serif 200 |
| Chapter title | 28 / 32 pt | serif 400 |
| Question heading | 16 / 21 pt | serif 400 |
| Beat heading (`3.1 Solar and wind`) | 10.5 pt | sans 600, runs into the paragraph |
| **Body** | **10.5 / 15 pt** | sans 300 |
| Table | 9 / 13 pt | sans 300, header 500 |
| Exhibit title | 11 / 14 pt | sans 500 |
| Exhibit subtitle | 8.5 / 12 pt | sans 300 |
| Note, source, endnote | 8 / 11.5 pt | sans 300 italic for sources |
| Footer | 7.5 pt | sans 400 |

- 150 mm at 10.5 pt is about 80 letters a line. That is the comfortable reading width and
  the reason this measure was chosen.
- Ragged right everywhere. Never justify.
- Nothing below 8 pt. (v1 allowed 6.5 pt. It was unkind and it is now banned.)
- `tnum` and `lnum` on every table, exhibit and figure.

---

## 4 · Vertical rhythm — the baseline grid is gone

v1 locked every vertical measure to a 13.5 pt grid. It was fragile, Paged.js fought it, and
no reader ever noticed it. Deleted.

Replace with three spacing steps and nothing else:

| Token | Value | Used for |
|---|---|---|
| `--space-1` | 15 pt | between paragraphs |
| `--space-2` | 22 pt | above a beat heading, around a table |
| `--space-3` | 34 pt | above a question heading, around an exhibit |

- `orphans: 2; widows: 2` on every text block.
- No `margin-top` collapsing tricks. Set space on the top of a block, never the bottom,
  except the last-child reset.

---

## 5 · Page breaks

**Force a break in exactly five places, and nowhere else:**

1. Part divider — starts a new page
2. Chapter opener — starts a new **recto** (right-hand) page
3. Contents
4. Notes and sources
5. Back cover

Everything else flows. Never break a page to make a question, a chapter or a Q-and-A pair
fit neatly. A question that ends a third of the way down a page is correct.

**Bound printing means some blank pages.** When a chapter opener has to fall on a recto and
the previous chapter ended on a recto, a blank verso is inserted. That is intentional in a
bound document. Such a page must be **truly blank** — no footer, no folio, no running title.

### Paged.js trap — read this before touching break CSS

`break-before: page` is **ignored** on a flowing section in this setup. Every section in v1
that appeared to obey it was really a `height: <live-height>` block filling its own page.
`break-after: page` **does** work.

So: put the break on the element *before* the one you want to move, or make the target a
full-live-height block. Do not spend an hour rediscovering this.

Second trap: Paged.js rebuilds the DOM for every page, so `:first-of-type` and
`:last-of-type` cannot be trusted. Use adjacent-sibling selectors and the `data-split-from`
attribute Paged.js sets on continued elements.

---

## 6 · Tables

- Full measure, 150 mm. Always.
- 9 pt. Header row 500 weight, sentence case, no shading.
- One 0.5 pt rule under the header. 0.25 pt hairlines between rows. No vertical rules ever.
  No zebra striping.
- Number columns right-aligned with `tnum`. Text columns left-aligned.
- A long table may split across pages; repeat the header via `<thead>` and
  `display: table-header-group`.
- **No HTML tags inside a cell.** Keep every cell short. If a cell needs a sentence, it
  belongs in the prose, not the table.
- A table that will not fit 150 mm at 9 pt is a table with too many columns. Split it or
  cut a column. Do not shrink type below 8 pt and do not widen the page.

---

## 7 · Charts and exhibits

**Sourcing rule, from the user and not negotiable:** an exhibit exists only if the source
`storyline/*.md` file actually calls for one. Do not invent charts. If the `.md` draws a
table, it stays a table. If the `.md` draws a bar block, it becomes a bar chart with those
exact bars. If the `.md` just writes prose, there is no exhibit.

Anatomy, fixed and build-enforced:

```
Exhibit N          ← 7.5 pt tracked caps, chapter accent colour
Assertive title    ← 11 pt, a claim the reader could disagree with
Unit and scope     ← 8.5 pt subtitle
[ the chart ]      ← inline SVG, 150 mm wide
Note: …            ← 8 pt, required wherever any figure is ours or estimated
Source: …          ← 8 pt, required always. No exhibit renders without one.
```

- Every chart is **150 mm wide**. `tools/charts.py` loses its `WIDTHS` dictionary and its
  `half` / `col` / `full` / `page` options.
- Inline SVG only. No raster.
- **Banned:** 3-D, gradients, drop shadows, pies with more than three slices, dual axes,
  truncated bar axes, colour-only encoding.
- Exhibit gets `break-inside: avoid` when it fits in 244 mm; otherwise it is allowed to
  split.

---

## 8 · Page furniture

Running footer on body pages only. Chapter title on the outer side, folio on the inner
side, one 0.25 pt rule above, 7.5 pt, `--ink-muted`.

Suppressed on: cover, author page, contents, part dividers, chapter openers, blank pages,
back cover.

Page order:

1. Front cover
2. Author page — Drishti Verma (BSc Hons Computer Science, Delhi University); Dondeti Pranay
   Reddy (Energy Meteorologist, Energy Group Renewables Limited)
3. Contents, with real folios
4. Introduction
5. Part One divider → Chapter 1 opener → questions → Chapter 2 opener → questions
6. Part Two divider → Chapter 3 → Chapter 4
7. Part Three divider → Chapter 5
8. Methodology and scope
9. Notes and sources — endnotes, numbered continuously, single column, 8 pt
10. Back cover — carries the one permitted attribution

Chapter openers: the number, rule and title block sit about a third of the way down the
page, not hard to the top and not at the foot. Both extremes were tried in v1 and both left
a visible canyon of white.

---

## 9 · Colour

Unchanged from v1. One accent per chapter, no repeats.

| Token | Hex | Where |
|---|---|---|
| `--brand-teal` | `#0581A8` | Chapter 1 |
| `--brand-blue` | `#1A50A0` | Chapter 2 |
| `--brand-violet` | `#5A439E` | Chapter 3 |
| `--brand-magenta` | `#902B94` | Chapter 4 |
| `--brand-crimson` | `#C03D5B` | Chapter 5 |
| `--ink` | `#0E1C2B` | body text |
| `--ink-secondary` | `#5A6B7A` | subtitles, axis labels |
| `--ink-muted` | `#8A97A3` | notes, sources, footer |
| `--rule` | `#D8DEE4` | hairlines |
| `--tint` | `#F4F6F8` | teaching boxes |
| `--paper` | `#FFFFFF` | page |

Part dividers carry the full spectrum. Body pages carry one accent only.

---

## 10 · What to delete from the current code

Work through this list first. The layout will not come right while any of it survives.

**`styles/tokens.css`**
- `--col-w`, `--gutter` — no columns any more
- `--baseline`, `--baseline-2`, `--baseline-3`, `--baseline-4`, `--half-baseline` — replace
  with `--space-1/2/3`
- `--t-notes` 6.5 pt — nothing goes below 8 pt now
- `--measure` 130 mm → 150 mm; `--live-w` 176 mm → 150 mm; margins → 32/28/25/28

**`styles/print.css`**
- every negative-margin break-out rule (`.wide`, `.full-bleed`, `widen_tables` targets)
- every two-column leftover (`column-count`, `column-gap`, `column-span`)
- every rule that snaps a value to the baseline grid

**`tools/charts.py`**
- the `WIDTHS` dictionary and all width plumbing — one width, 150 mm, hard-coded

**`tools/build.py`**
- `widen_tables()` — deleted outright, it exists only to serve break-out
- keep `mark_source_lines()`, `number_columns()`, and the trailing-`<hr>` strip

**`config/exhibits.yaml`**
- the `width:` key on every entry

---

## 11 · Fixes from v1 that must be kept

These were real bugs, found and fixed, and must survive the rewrite.

- **Source lines.** The italic paragraph closing each answer has no `Source:` prefix in this
  corpus. It is found by shape — the last paragraph of the answer, italic end to end — not
  by a label. Matching on a prefix silently missed every one and they printed at body size.
- **Trailing rule.** The `---` separating an answer from its stripped working notes renders
  as a stray `<hr>` under the source line. Strip trailing `<hr>` from every answer.
- **Endnotes** are single column, 8 pt, `--ink-secondary`, with a coloured marker.

---

## 12 · Build and preview

```powershell
cd "D:\Energy Transition Project\report"
python tools/build.py --only 12 --out specimen
if ($?) {
  $s = Start-Process python -ArgumentList '-m','http.server','8899','--bind','127.0.0.1' -PassThru -WindowStyle Hidden
  Start-Sleep -Seconds 2
  node tools/preview.js "http://127.0.0.1:8899/build/docs/report.html" build/preview
  Stop-Process -Id $s.Id -Force
}
```

- Preview **must** be served over HTTP. Paged.js fetches the stylesheets itself and Chrome
  blocks that over `file://`.
- poppler / pdftoppm is not installed, so the Read tool cannot rasterise a PDF. Check pages
  by reading the PNGs in `build/preview/`.
- Close the PDF in any viewer before building, or the write fails with `WinError 32`.
- PowerShell 5.1 has no `&&`. Use `;` and `if ($?)`.

---

## 13 · Hard constraints carried forward

- **No attribution to the original analysis house anywhere in the output** — not in visible
  text, the colophon, PDF metadata, file names, CSS class names, or code comments. The one
  exception is the single credit on the back cover, agreed with the user. Acceptance
  criterion 12 in the brief therefore fails as literally written; that is deliberate and
  recorded, not an oversight.
- **Never write a file until the user has approved the text.**
- Web access: `WebSearch` and `WebFetch` are blocked by policy. Use
  `Invoke-WebRequest -Uri <url> -UseBasicParsing -TimeoutSec 30`.

---

## 14 · Open items only the user can settle

1. **Vector logo.** The current `group_logo.png` is 1248 × 832 with a baked-in near-white
   background, so a faint grey box shows on any tint. Needed: SVG with true transparency,
   plus a reversed white variant. Until then the logo appears on white grounds only, cover
   and back cover, 34 mm wide.
2. **Publishing entity** — Energy Group Renewables, Energy Group Renewables, or Energy Group. The
   supplied logo is the Renewables lockup.
3. **Legal text** — disclaimer, confidentiality marking, approval line. The back cover
   currently shows a visible placeholder rather than silently omitting it.
4. **Publication date** — the build date is used unless a date is set.

---

## 15 · Order of work for the fresh session

1. Delete everything in §10. Do this first and completely.
2. Rewrite `tokens.css` to the §2–§4 numbers.
3. Rewrite `print.css` — one column, five forced breaks, mirrored margins, recto chapter
   openers.
4. Rebuild Q12 alone as a specimen. Check every page PNG.
5. Re-derive the exhibit programme from what the `storyline/*.md` files actually specify.
   Q12 is the worked pattern: the section-1 table stays a table; the section-3.1 bar block
   becomes a bar chart; the third exhibit was dropped as a duplicate.
6. Only then: all 17 questions, contents with real folios, part dividers, chapter openers,
   introduction, methodology, endnotes, back cover.
7. Then the responsive HTML twin from the same source.
