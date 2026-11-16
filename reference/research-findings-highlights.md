# Research findings — highlights and open items

The distilled output of Phase 1, kept separate from both `AGENTS.md` (persona and writing rules)
and `STORYLINE.md` (the question chain). This file holds **what we believe and what
we still need to check**.

Both sections become live at the **core question** (why the solutions are physically hard) and the
**payoff** (Energy Group). They are not needed while writing the runway.

---

## Working hypotheses — the five things most likely to drive the core and the payoff

These came out of reading the three MGI reports. Each is a claim about where India's situation
differs from the global picture the reports describe.

1. **The grid is the world's #1 bottleneck.** 1.65 TW of solar and wind sits waiting for
   connection globally; transformer costs are up 35%; lead times have doubled to 2–3 years. In the
   MGI 2025 scorecard the grid is the only Level 1/2 challenge scored *negative*. This is the
   strongest possible set-up for the Energy Group transmission argument.

2. **India's peak is inverted** compared with the report's assumption. MGI's peak problem is
   winter-morning and heating-driven. India's is summer-evening and cooling-driven. India's
   equivalent of "heat pump efficiency collapses in the cold" is the **solar sunset ramp** — solar
   output dies exactly as the evening cooling load arrives.

3. **India is greenfield, not brownfield**, in steel and cement. MGI's framing is an asset-turnover
   window — roughly 60% of the world's blast furnaces need relining before 2030, so the chance to
   switch technology comes only when a plant is rebuilt. India is not waiting for that window; it
   is deciding right now what to build. Best position in the world, and the highest lock-in risk if
   it builds the wrong thing.

4. **India's EV story is 2- and 3-wheelers**, not cars. MGI's India finding is pessimistic because
   at roughly 841 gCO₂-e/kWh a battery car on today's Indian grid may never break even against
   petrol. That analysis does not transfer to the segment India is actually electrifying, which is
   far lighter and far less energy-hungry per kilometre.
   > ⚠️ **The 841 figure is wrong for India's grid.** CEA's own CO₂ Baseline Database (v21.0,
   > Nov 2025) puts the grid at **~710 g/kWh (FY 2024-25)** and ~715–719 g/kWh in 2022. The 841
   > matches CEA's *thermal-only* series, which excludes renewables. **Rebuild the breakeven
   > calculation on 710**, and correct `module-1C` and `module-1E` when either is next used.
   > Full series in `india-power-snapshot-2026.md`.

5. **Critical minerals are India's genuinely weak hand.** Lithium demand rises around 7× by 2030,
   roughly 40% of it unmet in the base case, and the top three countries control more than half of
   extraction. India has no strong position here. Be honest about it in the final deck rather than
   arguing around it.

Detail behind all five is in the `module-1*` files — see `00-INDEX.md`.

---

## Open items — figures believed but not yet verified against a primary source

The user plans to cross-question these during the India work, so treat the list as a checklist
rather than a blocker.

- ~~India peak demand ~250 GW, May 2024 — CEA / Grid-India~~ **VERIFIED 7 Aug 2026** against CEA's
  Executive Summary, June 2026: FY 2024-25 peak was **249,856 MW**. Current figure is
  **270,832 MW** (FY 2026-27 up to May 2026), up 15.1% year on year. Detail in
  `india-power-snapshot-2026.md`
- ~~India added >20 GW solar + wind in H1 2025, more than the US~~ **SUPERSEDED 7 Aug 2026** by a
  better figure: India added **54.6 GW of renewables in FY 2025-26**, including a record 6.05 GW
  of wind (MNRE). Over five years, 134 GW of RE against 21 GW net coal
- ~~India crossed 50% non-fossil installed capacity ahead of the 2030 NDC target~~ **VERIFIED
  7 Aug 2026** against CEA's own installed-capacity file (`Website_June.pdf`, as on 30.06.2026):
  total 548,858 MW · non-fossil **297,369 MW = 54.18%** · coal 224,158 MW (40.84%) · solar
  162,152 MW · wind 57,443 MW. The 500 GW target is **not** met — 297 GW built, roughly 60% of
  the way
- National Steel Policy target ~300 Mt crude steel by 2030 — Ministry of Steel
- National Green Hydrogen Mission target 5 MMT/yr by 2030 — MNRE
- **Exhibit 2 per-domain stock percentages in the MGI 2025 report — the row-to-value mapping came
  out of the PDF garbled. Do not quote until checked against the chart.**
- Exhibit 5 grid-intensity pairings, and the Germany Exhibit 3 panel labels (MGI Apr-2025 report)
- Whether Energy Group has a steel position at all

The 196-page Aug-2024 MGI full report has not been read. It is the authoritative source behind
most of the above.
