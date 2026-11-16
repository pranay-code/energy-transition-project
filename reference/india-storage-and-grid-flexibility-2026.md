# India storage and grid flexibility — verified snapshot

Everything learned from the **IIT Bombay "Advanced Battery Energy Storage Systems" short course,
6–7 April 2026**, plus the two industry decks handed out there. Written up on 7 Aug 2026 so the
250-odd slides never have to be re-read.

Companion to `india-power-snapshot-2026.md`. That file answers *how big is India's power problem*.
This one answers *what actually closes the evening gap, how fast, at what cost, and who is
already doing it.* Feeds the power question, the transport question and the Energy Group payoff.

---

## 0. The three sources, and how to cite them

| Deck | Author | What it is |
|---|---|---|
| `Advanced BESS_presentation material_IITB (1).pdf` | Prof. Zakir H. Rather, **Grid Integration Lab, Dept. of Energy Science & Engineering, IIT Bombay** | 201 slides. The main course deck. Grid integration, storage technology comparison, control, degradation, Indian and global case studies |
| `Advanced BESS_IndiGrid.pdf` | **IndiGrid Investment Managers Ltd** (India Grid Trust), April 2026 | 25 slides. A live developer's view — real project list, technical specification, safety, standards |
| `VR_BMS_Battery_Modelling_Apr_2026 (1).pdf` | Prof. **Venkatasailanathan Ramadesigan**, Dept. of Energy Science & Engineering, IIT Bombay | 21 slides. Battery modelling, BMS functions, degradation physics |

> ### ⚠️ Sourcing rule for this file
> The IITB deck carries an explicit restriction: contents *may be used for the benefit of the
> participant's employer* but **must not be shared with any third party** without written
> permission from the Grid Integration Lab.
>
> **So: use the facts, never reproduce the slides.** Almost every number below traces to a public
> original — Grid-India, CAISO, IEX, CEA, MNRE, PIB, IRENA, USGS, Ember. **Cite the original.**
> Only a handful of engineering facts have no public original (round-trip loss ranges, the
> container temperature gradient, pumped-hydro lead times, the technology comparison table). Those
> are credited to the course itself, which the restriction permits. IndiGrid's deck is a listed
> InvIT's investor material about publicly announced projects — normal attribution is fine.

---

## 1. The single most useful thing in the workshop — India's grid runs out of room in both directions on the same day

Source: **Grid-India**, operational data for **26 May 2025**, presented in the IITB deck.

| Hour of that day | What the grid ran out of |
|---|---|
| Five **mid-day** hours | **Downward reserves near zero.** Too much solar, nothing left the operator could turn *down* |
| Three **late-night** hours | **Upward reserves near zero.** Nothing left the operator could turn *up* |
| Roughly one hour | **No AGC down-reserve at all** (automatic generation control) |

Same day, same grid, two opposite emergencies. **This is the sharpest single piece of evidence
that India's binding constraint is the time of day, not the quantity of clean capacity.** It is
better evidence than the peak-hour statistic, because it is the system operator's own margin
running to zero rather than an inference from a demand curve.

### The market says exactly the same thing
Source: **Indian Energy Exchange**, day-ahead market, 26 May 2025.

Market clearing price **collapses in the middle of the day** (surplus solar) and **spikes at
night**. Thermal generators bid high after dark to recover their costs. The commercial signal and
the physical signal point the same way: *power is worthless at noon and precious at 10 pm.*

### And the grid's pulse is already wobbling
Source: **Grid-India** frequency profile, 26 May 2025. Frequency swung between **49.65 Hz and
50.35 Hz** against a 50 Hz standard — a wider band than a stable synchronous grid would show.

---

## 2. Inertia — the physical challenge nothing else in the reference library covers

**Nowhere in modules 1A–1F is this named.** It is a genuine gap that this workshop fills.

**The physics.** Coal, gas, hydro and nuclear plants all make electricity by spinning a very heavy
metal rotor. Every rotor on the grid turns in step. Because they are heavy, they cannot change
speed quickly, and that stored kinetic energy is what holds frequency steady in the first seconds
after a fault. Solar PV and wind connect through **inverters** — no synchronous rotating mass at
all. They are *non-synchronous*.

**The consequence, as RE share rises:**

| Effect | What it means |
|---|---|
| System inertia falls | Measured in MW·s; the IITB deck plots it falling directly against RE penetration |
| **RoCoF** rises | Rate of Change of Frequency — the grid's frequency moves faster after a disturbance |
| **Frequency nadir** deepens | The dip after a plant trips goes lower before it recovers |
| Short-circuit ratio falls | A "weak grid" — inverters themselves start to become unstable |
| Voltage rises at high-PV nodes | Rooftop solar on radial feeders pushes local voltage up until inverters trip themselves off |

**Why this matters for the argument:** it is a *physical* reason India cannot simply keep adding
panels. Beyond a certain share, more inverters make the grid less stable, not more clean. It is
independent of cost, land and transmission.

**The resolution, and it is commercially important.** A battery inverter can be run in
**grid-forming (GFM)** mode instead of the usual **grid-following (GFL)** mode. GFL behaves like a
controlled current source and needs the grid to already exist. GFM behaves like a controlled
*voltage* source — it sets its own frequency and voltage, provides **synthetic inertia**, works in
a weak grid, and can **black-start** a network with no outside supply.

| Service | GFL BESS | GFM BESS |
|---|---|---|
| Energy arbitrage | Proven, widely deployed | Same |
| Frequency regulation | Fast, accurate | Fast, accurate **+ weak-grid stability** |
| Virtual inertia | Limited | **Yes** |
| Black start | Needs external voltage reference | **Independent grid energisation** |
| Islanding | No | Seamless islanding and resync |
| 100% inverter-based grid | Challenging | **Possible** |

GFM control families: droop, Virtual Synchronous Machine (VSM), Synchronverter, Virtual Oscillator
Control (VOC), dispatchable VOC, matching control.

**Proven in the field, not theory:**
- **Dalrymple BESS, South Australia** — 30 MVA / 8 MWh, VSM grid-forming, commercial since
  Dec 2018. Delivered inertial response to a positive-RoCoF event on 16 Nov 2019 (Heywood
  interconnector trip) *before* the high-speed recorder even registered the frequency rise.
- **Hornsdale Power Reserve, South Australia** — 100 MW / 129 MWh at commissioning in 2017, later
  150 MW / 194 MWh, Virtual Machine Mode. Tested for real on 25 May 2021 when a coal plant
  exploded and neighbouring units tripped.
- **Dersalloch wind farm, Scotland** — grid-forming BESS black-starts the local 33 kV network.
- **St. Eustatius island** — 5 MVA / 5.9 MWh GFM battery picked up the whole island load
  automatically when every diesel generator shut down simultaneously.

> **Energy Group hook.** A grid-forming battery sitting inside a transmission network is worth more than
> the same battery sitting anywhere else, because it sells inertia, black-start and weak-grid
> support on top of arbitrage. That is a *transmission owner's* product, not a generator's.

---

## 3. Storage technology comparison — the numbers that decide the ranking

Source: IITB course deck, consolidated table.

| | Lead acid | **Li-ion** | Vanadium flow (VRFB) | Flywheel | **Pumped hydro** | Supercapacitor | Hydrogen |
|---|---|---|---|---|---|---|---|
| Cycle life | 250–500 | **3,000–5,000** | **10,000+** | 100,000+ | ~40 yr life | 100,000+ | 10,000+ |
| Energy density (Wh/kg) | 30–75 | **100–300** | 10–50 | 50–300 | 0.5–3 | 2.5–70 | 33,400 |
| **Round-trip efficiency** | 75–85% | **85–95%** | 60–80% | 80–85% | **70–80%** | >98% | **40–50%** |
| C-rate | 0.1–0.5C | 0.5–4C | 0.1–1C | 100C+ | 0.1–1C | 10–100C | 0.1–0.5C |
| Discharge duration | sec–hour | min–hour, <10 h | sec–min | **1–24 h+** | ms–min | sec–24 h | — |
| Maturity | Mature | Mature | Mature | Mature | Mature | Immature | Mature |

**Li-ion vs VRFB, the two that matter for the grid:**

| Parameter | Li-ion | VRFB |
|---|---|---|
| Round-trip efficiency | 90–95% | 70–85% real-world |
| Cycle life | 3,000–5,000 | 10,000 commercial, 12,000–15,000 in research |
| Depth of discharge | 10–90% typical, to protect life | **0–100%, no ill effect** |
| Lifespan | 10–15 years | **20+ years** |
| Safety | Moderate — thermal runaway risk | **High — non-flammable electrolyte** |
| Scaling | Power and energy fixed ratio | **Power and energy scale independently** |
| Recycling | Complex, energy-intensive | **~100% electrolyte recovery, low cost** |
| LCOS in India | **$0.08–0.09/kWh** | ~$0.10/kWh |
| Capital cost | — | 1.5–2× Li-ion |

**Why every Indian grid project is Li-ion (LFP) anyway:** highest round-trip efficiency, lowest
capital cost, lowest auxiliary consumption, proven supply chain, and 18-month delivery. LFP
specifically because it is safer and longer-lived than NMC even though it is less energy-dense —
and energy density does not matter when the battery sits still in a field.

**Why the alternatives are ruled out for the evening-peak job:**

| Technology | Killer limitation |
|---|---|
| Pumped hydro | Geographically constrained, large minimum unit size, **4–6 year lead time** |
| Compressed air | Needs underground caverns; high capex; limited scalability |
| Flywheel | Short operational life, mechanical wear, **not for long duration** |
| Thermal (sensible/latent) | Low density, thermal losses over time, slow charge/discharge |
| Hydrogen | **40–50% round-trip efficiency**, 350–700 bar tanks, handling cost, safety |
| Supercapacitor | Very short discharge, high self-discharge, high cost per kWh |
| Superconducting magnetic | Continuous cryogenic cooling, low energy capacity |

**Sodium-ion is the one to watch.** 90–150 Wh/kg, 3,000–5,000 cycles, up to 4,000 W/kg,
**−20 °C to 60 °C operating range**, non-flammable electrolyte possible, no cobalt, abundant raw
material, easier recycling. It cannot replace Li-ion yet on energy density, cycle life, rate and
commercial maturity — but it removes the single-country supply risk, which is India's weakest
point on minerals.

---

## 4. Battery degradation — and why Indian heat is a genuine India-specific problem

Sources: IITB BMS deck (Ramadesigan) and course deck.

**Two ageing paths:**
- **Calendar ageing** — capacity lost simply through the passage of time, worse at high temperature
  and high state of charge.
- **Cycle ageing** — capacity lost through charging and discharging.

**What accelerates it:** high temperature (internal resistance rises with working temperature) ·
high C-rate (faster charge/discharge → faster fade) · deep depth of discharge (cycle count falls
sharply as DoD rises) · high state of charge (accelerates SEI layer growth at the
electrode/electrolyte interface).

**The India-relevant finding.** Inside a utility BESS container with HVAC running, temperature is
**not** uniform. There is a vertical gradient: the lowest row of packs sits at an annual average of
**23–24 °C** while the upper packs sit **above 32 °C**. Result — **cells in the same container age
at different rates**, and the pack is limited by its worst cells. India's ambient heat makes the
HVAC work harder and widens that gradient.

**Duty cycle drives which ageing path dominates:**

| Service | Cycling pattern | Dominant degradation |
|---|---|---|
| Frequency regulation | Dozens–hundreds of shallow cycles/day, ±5–10% SoC | Cumulative micro-cycling |
| **Energy arbitrage / peak shaving** | **Few deep cycles/day, 60–80% DoD** | Cycle ageing |
| Backup / reliability | Held at mid-SoC, rare deep cycles | Calendar ageing |

India's evening-peak use case is the middle row: one or two deep cycles a day. IndiGrid's Dhule
design assumes **4,000 cycles and 2.5% capacity loss per year**, with either upfront
over-sizing or mid-life augmentation to hold contracted capacity.

**Plain-English translations for the writing:**
- Round-trip efficiency → *"you get back about nine units for every ten you put in."*
- Degradation → *"a battery is not a wire. It wears out as you use it, and it wears out faster
  when it is hot."*
- The container gradient → *"the top shelf of the box runs nearly ten degrees hotter than the
  bottom, all year, so the same battery ages unevenly."*

---

## 5. What is actually built and under construction in India

### ⭐ Energy Group Renewables at Khavda — the largest single site in India, by a wide margin

**Not from the workshop decks.** Verified separately on 7 Aug 2026 via Brave Search, from the Energy Group
Group release of 26 May 2026 as carried by Energy-Storage.News, ESS News, New Indian Express, The
Hitavada and GKToday, plus the Economic Times of 13 Jun 2026.

| | Value |
|---|---|
| Cumulative operational storage, Khavda Renewable Energy Park, Kutch, Gujarat | **3.37 GWh** |
| Announced | 26 May 2026 |
| Of which commissioned in March 2026 | **1.37 GWh** |
| Build time, start of on-site construction to commissioning | **~10 months** |
| Claim made | World's largest single-location battery deployment outside China |
| Contracted target at the same site, by end FY 2026-27 | **14 GWh** (Rajat Seksaria, CEO, BESS and Green Hydrogen, Energy Group — Economic Times, 13 Jun 2026) |
| Renewable generation at Khavda | ~9.9 GW operational, 30 GW planned |

> ### ⭐⭐ The number to carry into the payoff question
> Mercom puts **all of India at 5.9 GWh** of battery storage as of March 2026.
> **Energy Group's 3.37 GWh is 57% of every battery on India's grid — at one site.**
> And 14 GWh at that single site would be more than **twice** everything India has today,
> against a national requirement of 411 GWh by 2031-32.
>
> **This also breaks the 18-month clock below.** Khavda was delivered in ~10 months. Use
> "roughly a year to eighteen months" as the general figure, and the 10 months as what a
> single owner controlling land, grid connection and procurement can actually do. That gap
> *is* the Energy Group argument — do not spend it early.

⚠️ **Two figures reported by AGEL and not independently checked:** the "world's largest outside
China" claim, and "enough to power nearly 1 million homes for a day". Treat both as company
statements. The 3.37 GWh, the March 1.37 GWh tranche and the ~10-month build are consistent across
six independent outlets and are safe to use.

### IndiGrid's own utility-scale pipeline (April 2026)

| Project | Size | Type | Contract signed | Build time | Commissioning |
|---|---|---|---|---|---|
| **Gujarat BESS Pvt Ltd** | 180 MW / **360 MWh** | Standalone | 26 Jan 2024 | 18 months | **25 Feb 2026** |
| **Rajasthan BESS Pvt Ltd** | 250 MW / **500 MWh** | Standalone | 23 Dec 2024 | 18 months | **22 Jun 2026** |
| **SJVN – Uttar Pradesh** | 187.5 MW / **750 MWh** | Standalone | 16 Jul 2025 | 18 months | 15 Jan 2027 |
| **NVVN – Uttar Pradesh** | 125 MW / **500 MWh** | Standalone | 26 Aug 2025 | 18 months | 25 Feb 2027 |
| **Kilokari BESS (KBPL), Delhi** | 20 MW / **40 MWh** | DISCOM-integrated | — | 10+2 months | Built |

> ### ⭐ The 18-month clock
> **Every one of these runs to an 18-month contract-to-commissioning schedule.** This is the single
> most useful fact in the IndiGrid deck. It gives the solution ranking a *sourced* basis:
> solar months → **battery ~18 months** → transmission years → pumped hydro 4–6 years →
> nuclear 10+ years. Speed, not just cost, is why storage outranks firm clean power for 2030.

**Kilokari, Delhi** is worth noting separately: 20 MW / 40 MWh, **two cycles per day of two hours
each**, sited inside the distribution network of a major city, BOOT model, 12-year term from COD,
tariff-based revenue, technology-agnostic tender. That is the load-centre storage template.

**Dhule, Maharashtra** — a smaller but instructive case. IndiGrid's 765/400 kV, 3,000 MVA
substation was paying >₹50 lakh a year for auxiliary supply. Ground-mounted solar under
Maharashtra net metering could not offset **25%** of consumption, because the state **excludes the
6 pm–10 pm evening peak from net-metering set-off**. The fix was a 100 kW / 230 kWh battery
charged off-peak and discharged 6–10 pm. Design points: 250 kWp PV at 17% CUF · 230 kWh DC usable
/ 188 kWh AC usable · max charge/discharge 0.5C · PCS efficiency >97% · BESS auxiliary 2.5 kW.
**The regulatory definition of India's evening peak is 6 pm–10 pm.**

### Where the money sits in a BESS
- **Battery cells ≈ 70% of total system cost** (IndiGrid).
- Full cost split (course deck): storage block 35% · storage balance-of-system 15% ·
  power equipment 10% · control & communication 10% · system integration 5% · EPC 15% ·
  project development and grid integration 10%.

---

## 6. Costs, revenue and why this suddenly works

Source: Ember and IRENA, via the IITB deck.

- **BESS costs have fallen ~80% in a decade**, which has driven a **five-fold increase in BESS
  revenue** over the same period.
- **Batteries installed in India after 2024 are projected to be profitable** on market
  participation alone — annual revenue exceeding annualised cost.
- LCOS in India: **$0.08–0.09/kWh for Li-ion**.
- Revenue stacking is the model, not arbitrage alone: energy arbitrage in the wholesale market
  **plus** SRAS and TRAS ancillary services **plus** capacity/reliability payments.

*(A figure of "Rs 1.77 lakh per MW" appears on the Ember revenue slide without a stated basis —
per month? per year? — so it is **not** usable until confirmed.)*

**The five value-stacking use cases (IndiGrid's framing):**
1. **Storage with generation** — firms up RE, makes it dispatchable, cuts curtailment.
2. **Storage with transmission** — optimises line capacity, relieves congestion, defers
   network augmentation.
3. **Storage with distribution** — peak shaving and load shifting at the load centre; DISCOM
   portfolio optimisation; defers infrastructure upgrades.
4. **Storage for ancillary / balancing services** — frequency control, voltage control, fast
   response, black start.
5. **Storage as a service** — merchant asset, capex or opex model, leased or auctioned.

> **Energy Group hook.** Items 1, 2 and 3 are each a *different existing asset base* — generation,
> transmission, distribution. A group that owns all three can stack value in a way a pure-play
> storage developer cannot.

---

## 7. Policy and money already in place

| Instrument | Detail |
|---|---|
| **PLI, Advanced Chemistry Cell** | **₹18,100 crore** to support **50 GWh** of domestic manufacturing over five years |
| **Viability gap funding** | Up to **40%** of project cost for BESS |
| **Energy Storage Obligation** | **4% by 2030**; 85% of energy stored must come from renewables |
| **CEA advisory** | Future solar tenders to include **2-hour co-located storage equal to 10% of installed solar capacity** |
| **Critical minerals** | Customs duty exemption on **25 critical minerals**; National Critical Mineral Mission |
| **Recycling** | **₹1,500 crore** incentive scheme for critical-mineral and e-waste recycling |
| **Market access** | BESS allowed into the High Price Day-Ahead Market, SRAS and TRAS |

*(Cross-reference: `india-power-snapshot-2026.md` §6 also holds the ISTS waiver to June 2028, the
Harmonised Master List listing, VGF for 43.8 GWh, and CERC's separate non-solar-hour connectivity
rule. The two lists are complementary — read both.)*

### State targets and policies

| State | Target / policy |
|---|---|
| **Andhra Pradesh** | **25 GWh by 2029** — the largest single state target |
| **Rajasthan** | **10 GWh by 2028-29**; captive plants must store 20% of energy if generating above 100% of contract |
| **Telangana** | 3.8 GW by 2030, 7.9 GW by 2035 (BESS + PSP); land, charge and duty incentives |
| **Bihar** | 6.1 GWh by 2030 (4.5 GWh BESS + 1.6 GWh pumped hydro) |
| **Kerala** | Draft 2025 policy — storage covering ≥10% of new RE capacity, or 2 hours of peak power |
| **Uttar Pradesh** | Solar + BESS incentive; R&D focus |
| **Madhya Pradesh** | Special incentive for RE projects with an X/10 storage component |
| Assam · Odisha · Tamil Nadu | Procurement rules (AERC 2024), hybrid-with-storage priority, TANGEDCO-led build |

**Rajasthan BESS regulations, March 2026** — the first detailed state framework:
grid-scale sizing **≥1 MW and ≥2-hour duration** · services defined as frequency regulation,
reserves, voltage support, black start · **AGC-enabled with real-time telemetry to SLDC** ·
SLDC monitors SoC, round-trip efficiency and availability · four deployment models recognised
(standalone, co-located with RE, behind-the-meter, aggregator-based).

---

## 8. Proof it works — the destination, in other people's grids

**California (CAISO)** — the same evening problem, largely solved with batteries.

| Date | What happened |
|---|---|
| 20 May 2025 | BESS discharge hit **10 GW**, over **30% of the fuel mix**, matching gas + imports combined |
| 6 Aug 2025 | BESS discharge hit **11 GW**, ~**28% of the fuel mix** |
| 8 Jan 2026 | BESS *charging* hit **10.5 GW** — **49% of instantaneous RE generation** was going into batteries |
| **29 Mar 2026, 7 pm** | Batteries reached **12.29 GW, meeting 42.8% of total grid demand** |

CAISO's "duck curve" (lowest net-load day each spring) has steepened every year from 2019 to 2025.
Batteries charging at midday let gas units ramp off more efficiently **and** cut solar curtailment
— one asset solving both halves of the problem.

**South Australia** — textbook solar peak shifting: charge through the middle of the day on
surplus PV, discharge into the evening peak in non-solar hours.

**Spain** — nationwide blackout on **28 April 2025**; rapid BESS build-out since.
⚠️ **Do not attribute the blackout to low inertia.** The official cause is still contested. The
deck only shows the build-out that followed. Say what happened, not why.

---

## 9. Minerals and supply chain

- **~90% of rechargeable batteries worldwide are lithium-ion.** Demand growth is driven by grid
  storage and EVs together.
- LFP is displacing NMC in EV applications globally on cost, safety and improving density.
- **Vanadium** (for flow batteries): China ~70,000 t, then ~21,000 t, ~8,000 t, ~5,000 t for the
  next three producers. World resources exceed **63 million tonnes**. **India's vanadium comes
  from iron and steel slag and other industrial waste** — a by-product position, not a mining one.
- **Sodium** production is far more spread across countries than lithium — the core argument for
  sodium-ion as a supply-security hedge.
- Full battery material set: lithium, cobalt, nickel, manganese, graphite, copper, aluminium,
  iron/steel, vanadium, zinc, sodium.

This is the one area where the workshop **confirms India's weak hand** rather than its strong one.
Consistent with hypothesis 5 in `research-findings-highlights.md` and Reality 10 in `module-1D`.

---

## 10. Cross-check on sector emissions

Source: **JRC / IEA, "GHG emissions of all world countries", 2025 report**, CO₂ only, 2024.

| Sector | India | World |
|---|---|---|
| **Power industry** | **48%** | **39%** |
| Industrial combustion | 22% | 16% |
| Transport | 11% | 21% |
| Processes | 8% | 8% |
| Buildings | 7% | 8% |
| Fuel exploitation | 4% | 8% |

**A third independent confirmation that power is roughly half of India's carbon dioxide.**
Sits alongside the 37.5% of *all greenhouse gases* used in the emissions-by-source question
(Climate Watch/WRI, 2023) and the 53% of *fuel-burning* emissions held over from it. Three
different denominators, same conclusion — **do not put more than one of them in a single answer.**

---

## 11. Secondary India data from the deck (use the CEA snapshot instead where they overlap)

MNRE Akshay Urja Portal / CEA, as at **Feb 2026** — four months older than the CEA figures in
`india-power-snapshot-2026.md`, so **prefer that file**. Kept here only for the split it adds:

- RE installed 215.5 GW — **rooftop solar 24.86 GW (13%) · ground-mounted solar 109.49 GW (58%) ·
  wind 55.13 GW (29%)**. The rooftop/ground split is new and not in the snapshot file.
- Thermal capacity 248.54 GW (coal + gas + diesel), up from 219 GW in 2017 — roughly **+13% in
  nine years**, against RE going from 57 GW to 215 GW over the same period.
- RE-rich states ranked: Gujarat, Kerala, Rajasthan, Maharashtra, Tamil Nadu, Madhya Pradesh,
  Karnataka.

---

## 12. What this changes in the storyline

| Question | What to add |
|---|---|
| **Power (core 1)** | The 18-month build clock as the sourced basis for the solution ranking · Grid-India's two-directional reserve failure on 26 May 2025 · the IEX price curve for the same day · **inertia as a new, uncovered physical challenge** · round-trip loss and heat-driven degradation as real costs of storage · the Indian project pipeline, so storage reads as "1.4% built but started", not "1.4% and nothing happening" · CAISO at 42.8% as the finished picture |
| **Transport (core 4)** | Charging load lands on the same evening peak the reserves data exposes. Degradation, C-rate and fast-charge limits (lithium plating above 2C) belong here, not in power |
| **Buildings (core 5)** | Rooftop solar causes **over-voltage on radial LV feeders**, tripping inverters off. Behind-the-meter storage is the fix. New material, not previously in the library |
| **Energy Group payoff** | The five value-stacking use cases map onto generation, transmission and distribution separately — a group owning all three stacks value a pure-play cannot. Grid-forming batteries make a transmission network the *best* place to site storage. State targets (AP 25 GWh, Rajasthan 10 GWh, Telangana 7.9 GW) are the addressable market. Minerals remain the weak hand |

---

## 13. Still unverified / not usable

- **"Rs 1.77 lakh per MW"** on the Ember revenue slide — no stated basis or period. Do not use.
- Cause of the **28 April 2025 Iberian blackout** — contested. Do not attribute to inertia.
- **Pumped storage actually under construction in India** — still open from
  `india-power-snapshot-2026.md`. The 4–6 year lead time here is generic, not India-specific.
- Whether the **411 GWh by 2031-32** national figure reconciles with the sum of announced state
  targets. Not checked.
- The **Energy Storage Obligation of 4% by 2030** — seen on a slide, not confirmed against the
  Ministry of Power notification.
