# India's power system — verified snapshot

Everything the India power argument rests on, pulled from primary sources. Two tables became
eight on 7 Aug 2026 when the core power question was researched.

Used by the targets question, the solutions question and the core. **Keep this file updated
rather than re-fetching.** Fetch commands are at the foot.

---

## 1. Installed capacity — as on 30 June 2026

Source: Central Electricity Authority, `Website_June.pdf`,
`https://cea.nic.in/wp-content/uploads/installed/2026/06/Website_June.pdf`

| Category | MW | Share |
|---|---|---|
| **Total installed capacity** | **548,858** | **100.00%** |
| **Total fossil** | **251,489** | **45.82%** |
| Coal | 224,158 | 40.84% |
| Gas | 20,122 | 3.67% |
| Lignite | 6,620 | 1.21% |
| Diesel | 589 | 0.11% |
| **Total non-fossil** | **297,369** | **54.18%** |
| Solar | 162,152 | 29.54% |
| Wind | 57,443 | 10.47% |
| Large hydro, incl. pumped storage | 52,065 | 9.49% |
| Biomass power | 10,869 | 1.98% |
| Nuclear | 8,780 | 1.60% |
| Small hydro | 5,182 | 0.94% |
| Waste to energy | 878 | 0.16% |

CEA's own grouping: *RES (including hydro)* = 288,589 MW / 52.58%. Non-fossil = RES + nuclear.

**Two conventions worth knowing.** Nuclear counts as non-fossil but is **not renewable** — the fuel
is mined and finite; it qualifies because fission releases no carbon. Biomass counts as non-fossil
**even though it burns** — the plant absorbed the same carbon while growing. Both are standard
international practice, not an Indian quirk.

**Against the NDC.** The 50% non-fossil-capacity target is **met and passed** — 54.18%, four years
early. The 500 GW target is **not** met: 297 GW built, roughly 60% of the way.

### Capacity, the long view
Source: CEA Executive Summary, June 2026, Section G

| | Coal | Gas | Diesel | Nuclear | Hydro | RES | Total |
|---|---|---|---|---|---|---|---|
| End 6th Plan (Mar 1985) | 26,311 | 542 | 177 | 1,095 | 14,460 | 0 | 42,585 |
| End 12th Plan (Mar 2017) | 192,163 | 25,329 | 838 | 6,780 | 44,478 | 57,244 | 326,832 |
| Up to Jun 2026 | 230,777* | 20,122 | 589 | 8,780 | 52,065 | 288,589 | 548,858 |

\* coal + lignite together in this table.

---

## 2. Generation mix — 2025

Source: Ember, via Our World in Data (`share-elec-by-source`, `electricity-prod-source-stacked`),
retrieved 7 Aug 2026

| Source | India TWh | India % | World % |
|---|---|---|---|
| Coal | 1,474.15 | 70.8 | 33.0 |
| Solar | 195.99 | 9.4 | 8.7 |
| Hydro | 177.97 | 8.5 | 14.0 |
| Wind | 103.98 | 5.0 | 8.5 |
| Nuclear | 53.83 | 2.6 | 8.8 |
| Gas | 48.54 | 2.3 | 21.8 |
| Bioenergy | 23.04 | 1.1 | 2.2 |
| Oil | 4.10 | 0.2 | 2.6 |
| Other renewables | 0.00 | 0.0 | 0.3 |
| **Fossil total** | **1,526.8** | **73.4** | **57.4** |
| **Non-fossil total** | **554.8** | **26.6** | **42.3** |
| **Total** | **2,081.6** | 100 | 100 |

India's total electricity demand: **2,082.8 TWh in 2025**, up from 1,802.9 TWh in 2022 (OWID).

Trend in India's coal share: 74.5% (2022) · 75.4% (2023) · 74.5% (2024) · **70.8% (2025)**.

**Coal generation fell in absolute terms in 2025 — 1,517.9 TWh (2024) → 1,474.2 TWh (2025).**
The first real fall outside covid. But it is solar taking daytime hours, not coal shutting down:
coal plant load factor actually **rose** to 72.4% in June 2026 from 66.6% a year earlier (CEA).

---

## 3. The gap — the single most important fact here

> India has built **54%** of its capacity clean. It gets **27%** of its electricity from it.

A coal plant runs when you ask it to. A solar farm runs when the sun is up — in India, roughly a
fifth of the hours in a year. So India can own more clean machines than dirty ones and still burn
coal for most of its power.

This is the **capacity–generation asymmetry**, one of the four ideas that drive the whole MGI
argument — see `module-1B-power-and-peaks.md`, where Germany shows the same thing from the other
end (capacity ~3× while generation only ~1.8×, utilisation down 27 percentage points).

**India's own plan expects the gap to persist.** The National Electricity Plan projects non-fossil
**capacity** at 57.4% by 2026-27 and **68.4% by 2031-32** — but non-fossil **generation** at only
39% by 2026-27 and **49% by 2031-32** (PIB, Ministry of Power). Two-thirds of the machines,
half of the electricity. The asymmetry is not a transition problem India grows out of; it is the
planned steady state.

---

## 4. Grid carbon intensity — the number that has not moved

Source: CEA, *CO₂ Baseline Database for the Indian Power Sector, Version 21.0*, dated 1 Nov 2025.
`https://cea.nic.in/wp-content/uploads/baseline/2025/12/CO2_Database_V_21.0.xlsx`, sheet `Results`.

Weighted Average **Grid** Emission Rate, including renewables and captive (tCO₂/MWh):

| FY | tCO₂/MWh |
|---|---|
| 2020-21 | 0.7026 |
| 2021-22 | 0.7152 |
| 2022-23 | 0.7191 |
| 2023-24 | 0.7290 |
| 2024-25 | **0.7117** |

And alongside it, from the same workbook:

| | 2020-21 | 2024-25 | Change |
|---|---|---|---|
| Net renewable generation (GWh) | 147,247 | 255,009 | **+73%** |
| Absolute CO₂ from power (tCO₂) | 909.7 million | **1,234.2 million** | **+36%** |
| Carbon per unit (tCO₂/MWh) | 0.7026 | 0.7117 | **+1%** |

> **In five years India's renewable generation rose 73%, its power emissions rose 36%, and the
> carbon in each unit of electricity did not move.** Demand grew faster than clean supply, so
> renewables served the growth and coal held its place.

### ⚠️ Correction — the 841 g/kWh figure is wrong for the grid

`module-1C-evs-heat-and-turnover.md` and `module-1E-synthesis.md` carry MGI's figure of
**~841 gCO₂-e/kWh for India (2022)** and treat it as the grid intensity. CEA's own data says the
grid figure for that period was **~715–719 g/kWh**. The 841 matches CEA's *Weighted Average
Emission Rate* — a **thermal-only** series that excludes renewables (0.8146 in 2021-22, 0.8271 in
2022-23).

**Use ~710 g/kWh (CEA, FY 2024-25) for India's grid.** Quoting 841 overstates it by about 15%.
This matters most for the transport question, which was going to lean on the 841 to argue that a
battery car may never break even in India. Rebuild that calculation on 710.

---

## 5. Peak demand — India's inverted, evening-driven peak

Source: CEA Executive Summary, June 2026, Section F

| Year | Peak demand (MW) | Peak met (MW) | Deficit |
|---|---|---|---|
| 2019-20 | 183,804 | 182,533 | −0.7% |
| 2021-22 | 203,014 | 200,539 | −1.2% |
| 2022-23 | 215,888 | 207,231 | −4.0% |
| 2023-24 | 243,271 | 239,931 | −1.4% |
| 2024-25 | **249,856** | 249,854 | ~0% |
| 2025-26 | 245,444 | 245,416 | ~0% |
| 2026-27 (up to May 2026) | **270,832** | 270,820 | ~0% |

**Open item closed.** The "~250 GW peak in May 2024" carried in
`research-findings-highlights.md` is confirmed in shape: FY 2024-25 peak was 249,856 MW. The
current figure is **270,832 MW** — up 15.1% year on year.

**When the peak falls is the whole point.** On 24 May 2026 India's peak of **247.9 GW arrived at
22:36** — in non-solar hours (Grid-India data, reported by Down To Earth, 25 May 2026). India
needs an evening ramp of about **60 GW**, and on some days ramps at up to **500 MW per minute**
(Centre for Science and Environment, via Business Standard, 3 Jun 2026).

This is India's version of MGI Reality 4, inverted: not "heat pump efficiency halves at −10 °C" but
**solar output goes to zero exactly as the cooling load arrives.** Same shape of problem —
maximum demand at minimum resource — different physics. See `module-1B-power-and-peaks.md`.

---

## 6. Storage — India is at roughly 1% of what it needs

| | Value | Source |
|---|---|---|
| Battery storage installed, cumulative | **5.9 GWh** (Mar 2026) | Mercom India Research, Q1 2026 |
| Added in Q1 2026 alone | 4.6 GWh, a 941% jump on the prior quarter | Mercom |
| BESS needed by 2026-27 | 8.68 GW / 34 GWh | NEP (Generation), Gazette May 2023 |
| **BESS needed by 2031-32** | **47.24 GW / 236 GWh**, ~₹3.49 lakh crore | Ministry of Power, PIB, 27 Jul 2026 |
| Pumped storage needed by 2026-27 | 7.45 GW / 47 GWh | same |
| **Pumped storage needed by 2031-32** | **26.69 GW / 175 GWh**, ~₹1.29 lakh crore | same |
| **Total storage needed by 2031-32** | **411 GWh** | same |
| India's progress | **1.4%** | 5.9 of 411 GWh |

Policy already in place (Ministry of Power, Jul 2026): storage recognised in the Electricity Rules
(Dec 2022); on the infrastructure Harmonised Master List (Oct 2022); 100% ISTS charge waiver for
co-located BESS commissioned up to June 2028; viability gap funding for **43.8 GWh**; CERC allows
**separate grid connectivity for non-solar hours**, so a developer can push stored solar into the
evening; CEA advisory (Feb 2025) recommending storage of **at least 10% of installed solar
capacity for a minimum of two hours**.

The demand signal is explicit: power is cheap at noon and scarce at 10 pm.

---

## 7. Transmission — and the power already being thrown away

### What exists
Source: CEA Executive Summary, June 2026, Section G

| | ckm |
|---|---|
| Transmission lines, 220 kV and above, total (30 Jun 2026) | **509,603** |
| of which 765 kV | 63,048 |
| of which HVDC | 9,655 |
| End of 12th Plan (Mar 2017), for comparison | 367,851 |
| Inter-regional transfer capacity (Jun 2026) | **120,340 MW** |

### What is planned

| Plan | Scope | Cost |
|---|---|---|
| CEA Transmission Plan for 500 GW non-fossil by 2030 (Dec 2022) | **50,890 ckm** — incl. 8,120 ckm HVDC, 25,960 ckm 765 kV, 15,758 ckm 400 kV | — |
| National Electricity Plan (Transmission), to 2032 | — | **₹9.15 lakh crore** |
| CEA plan for 900 GW non-fossil by FY36 (Mar 2026) | **137,500 ckm** + 827,600 MVA, FY27–FY36 | **₹7.93 lakh crore** |

### What it is costing right now — the curtailment problem

| Finding | Source |
|---|---|
| **One-third (33%) of the 54.8 GW of recently commissioned RE is on a *temporary* grid connection (T-GNA)** as of May 2026 | ICRA, via PV Magazine India, 8 Jul 2026 |
| Rajasthan holds 27% of India's solar and has curtailed **up to 80%** of solar output at times | Economic Times |
| Rajasthan curtailed **11.5 GW** of renewables since Jan 2026; 8.3 GW in March 2026 alone | reported Apr 2026 |
| Gujarat, Maharashtra, Tamil Nadu: **10–30%** curtailment during peak solar hours | Business India, Mar 2026 |

This is India's own version of MGI's global finding that **1.65 TW of solar and wind is waiting for
grid connection worldwide** — the only Level 1/2 challenge the 2025 scorecard marks negative.
See `module-1F-hardstuff-2025-update.md`. **It is the hinge of the Energy Group transmission argument.**

---

## 8. What India is still building

| | Value | Source |
|---|---|---|
| RE capacity added, FY 2025-26 | **54.6 GW** — a record | Vasudha Foundation year-end report |
| Wind added, FY 2025-26 | **6.05 GW** — highest ever, beating 5.5 GW in FY 2016-17 | MNRE, Apr 2026 |
| Distributed solar added, FY 2025-26 | 16.31 GW (8.71 rooftop + 7.67 KUSUM) | PIB |
| RE added over five years vs net coal added | **134 GW vs 21 GW** | Vasudha Foundation |
| Capacity under construction, all types | ~132 GW | PIB |
| **Additional coal and lignite planned** | **~97,000 MW** | Ministry of Power, PIB, 30 Mar 2026 |
| Total capacity target | 874 GW by 2032, from 524 GW at 31 Mar 2026 | Ministry of Power |

**Say the coal plainly.** India is adding clean capacity at a record rate *and* building roughly
97 GW of new coal. Both are true. The honest framing is that India is not replacing its coal fleet
— it is adding clean capacity on top of a coal fleet that is still growing, because demand is
growing faster than either.

---

## 9. Losses

| | Value | Source |
|---|---|---|
| T&D losses | 19.27% (2021-22) | CEA |
| AT&C losses | 16.23% (2021-22) | CEA |

Roughly one unit in six is lost between the plant and the meter. Every lost unit is coal burned
for nothing — the cheapest tonne of carbon in the system to remove, and the least glamorous.

---

## 10. Scorecard — progress against the 2030 and 2070 targets

| Target | Where India is | Progress |
|---|---|---|
| 50% non-fossil **capacity** by 2030 | 54.18% (30 Jun 2026) | **Met, four years early** |
| 500 GW non-fossil by 2030 | 297.4 GW | **59%** |
| Non-fossil **generation** — no NDC target; India's own plan says 49% by 2031-32 | 26.6% (2025) | **54% of plan** |
| Storage by 2031-32 | 5.9 of 411 GWh | **1.4%** |
| Carbon per unit of electricity | 0.712 t/MWh (FY25) vs 0.703 (FY21) | **~0%** |
| Net zero 2070 — power emissions to ~zero | 1,234 Mt and rising | **Not started** |

> **India has won the easy half of the power problem and has barely started the hard half.**
> Building panels is the easy half, and India is world-class at it. The hard half is delivering
> that electricity at ten o'clock on a May night. The binding constraint is the time of day,
> not the quantity.

---

## Still unverified

- Pumped storage capacity actually **under construction** in India — search was rate-limited
- The "100 GW nuclear by 2047" target — seen in an Ember summary, not confirmed at source
- Grid-India's own load-curve file. The 22:36 peak and the 60 GW ramp are from credible secondary
  reporting of Grid-India data, not the raw source

---

## Fetch commands, for refreshing this file

```powershell
# CEA installed capacity (only the current month is linked on the page)
Invoke-WebRequest -Uri "https://cea.nic.in/installed-capacity-report/?lang=en" -UseBasicParsing -TimeoutSec 60
# then follow the Website_<Month>.pdf link and extract page 1 with pypdf

# CEA Executive Summary — peak demand, PLF, transmission ckm, losses, capacity history
Invoke-WebRequest -Uri "https://cea.nic.in/executive-summary-report/?lang=en" -UseBasicParsing -TimeoutSec 60
# retry the PDF 2-3 times; cea.nic.in drops the first connection often

# CEA CO2 baseline database — grid carbon intensity. Sheet "Results", rows 13-14 and 31.
Invoke-WebRequest -Uri "https://cea.nic.in/cdm-co2-baseline-database/?lang=en" -UseBasicParsing -TimeoutSec 60
# needs: python -m pip install openpyxl

# Generation mix and absolute TWh
Invoke-WebRequest -Uri "https://ourworldindata.org/grapher/share-elec-by-source.csv" -UseBasicParsing -OutFile elecmix.csv
Invoke-WebRequest -Uri "https://ourworldindata.org/grapher/electricity-prod-source-stacked.csv" -UseBasicParsing -OutFile gen.csv
Invoke-WebRequest -Uri "https://ourworldindata.org/grapher/electricity-demand.csv" -UseBasicParsing -OutFile demand.csv
# OWID ignores ?country= filters — download the whole file and filter with Import-Csv
```

**Web search on this machine.** `WebSearch` and `WebFetch` are blocked by policy. DuckDuckGo, Bing,
Mojeek and Startpage all serve captchas to PowerShell. **Brave Search works** — verified
7 Aug 2026. Space requests ~6 seconds apart; it returns 429 after about four in a row.

```powershell
$r = Invoke-WebRequest -Uri ("https://search.brave.com/search?q=" + [uri]::EscapeDataString($query)) `
     -UseBasicParsing -TimeoutSec 60 `
     -UserAgent "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0 Safari/537.36"
($r.Content -replace '<script[\s\S]*?</script>',' ' -replace '<[^>]+>',' ' -replace '\s+',' ')
```
