# Module 1C — EVs vs grid carbon, industrial high heat, and the turnover window

Source: MGI, *Ten physical realities the energy transition must tackle*, April 2025, pp. 12–16
(Realities 5, 6, 7; Exhibits 5, 6, 7).

---

## Reality 5 — For EVs to deliver on their potential, grids must get cleaner

### The mechanics

A BEV and an ICE car have **opposite emissions profiles over time**:

| | Manufacturing | Running |
|---|---|---|
| **ICE** | Lower | Higher, and fixed by the fuel |
| **BEV** | **Higher** (battery production is energy-intensive) | Lower — **but only as clean as the grid charging it** |

So a BEV starts life *in carbon debt* and pays it off as it drives. That gives you two metrics:

- **Carbon breakeven distance** — km driven before cumulative BEV emissions drop below the ICE
- **Lifetime emissions saved** — the gap at end of life (assumed ~**200,000 km**, from US odometer
  readings of 12-year-old cars)

The variable that decides both is **grid carbon intensity (gCO₂-e/kWh)**, including upstream
emissions from extracting, processing and transporting fuels.

### Grid intensity, 2022 (Exhibit 5)

| Grid | gCO₂-e/kWh |
|---|---|
| 100% green | 0 |
| European Union | ~275 |
| United States | ~429 |
| Global average | ~529 |
| China | ~658 |
| **India** | **~841** |

*(India under a decarbonising path averages ~640 over 2022–35. Exact pairing of the second-scenario
values is my reading of the exhibit — worth re-checking against the original chart.)*

### The results — and India is named explicitly

**European Union (~275 g):** a small/midsize BEV breaks even at **20,000–40,000 km** and saves
**45–65%** of lifetime CO₂ versus an average ICE — *even assuming the grid never decarbonises further*.

**India (~841 g), grid frozen at 2022 intensity:**
- A passenger BEV could **emit more than a top-performing ICE**
- And only **somewhat less** than an average ICE
- Carbon breakeven distance runs **beyond 250,000 km** — i.e. beyond the vehicle's life. It never
  breaks even.

**India, grid decarbonising per the scenario:** a midsize BEV bought *today* achieves lifetime
savings of up to **15%** versus even a top-performing ICE.

### The lesson

> **An EV is not a clean product. It is a claim on the grid.**

Its carbon performance is written by the generation mix, not by the vehicle. Which means:

1. **Sequencing matters.** Pushing EVs hard onto a coal-heavy grid buys little carbon benefit in
   the near term. Grid decarbonisation and EV rollout are not two independent programmes —
   the second is *derivative* of the first.
2. **But it is not an argument against EVs.** Note the framing: a car bought *today* is judged
   against the grid it will see over the *next 12–15 years*, not today's grid. Because the grid
   improves over the vehicle's life, EVs bought now get progressively cleaner while an ICE
   bought now never does. The ICE locks its emissions in on day one.
3. **Other reasons still hold** regardless of carbon — urban air quality, oil import bill, noise,
   and running cost.

### Two caveats to carry into Phase 2

- This analysis is **passenger cars only**. India's EV market is overwhelmingly **two- and
  three-wheelers**, with far smaller batteries and therefore far smaller manufacturing carbon
  debt — breakeven arrives much sooner. The report's pessimistic India finding does **not**
  transfer to the segment India is actually electrifying.
- India's ICE baseline is also different: smaller, lower-powered, more efficient cars than the
  US fleet the model is calibrated on.

---

## Reality 6 — The big four industrial materials need very high heat, and resist electrification

### The big four

**Steel, cement, plastics, ammonia** — Vaclav Smil's "four pillars of modern civilisation" —
account for roughly **two-thirds of industrial emissions**.

They are hard to decarbonise for **two separate reasons**, and it matters that they are separate:

1. **Fossil fuels as the source of very high-temperature heat** — an energy problem
2. **Fossil fuels as feedstock** — a *chemistry* problem. Oil is an ingredient in plastics; coal
   is the reducing agent that strips oxygen from iron ore. You cannot solve this with cleaner
   electricity, because electricity is not a molecule.

### The temperature split (Exhibit 6)

Global industrial final energy by temperature requirement:

| | High (>500 °C) | Medium (100–500 °C) | Low (<100 °C) | Cooling |
|---|---|---|---|---|
| **Iron and steel** | **83%** | 8% | 6% | 2% |
| **All industry, total** | **49%** | 21% | 22% | 7% |

The big four — steel, chemicals, cement — account for the **vast majority of very
high-temperature heat** in industry. By contrast, food and tobacco, pulp and paper get
~**90% of their heat at low or medium temperature**, which makes them comparatively easy.

**Read the total row carefully: about half of all industrial energy is *not* high-temperature.**
That is the good news buried in this exhibit — roughly half of industrial heat is already
addressable with technology that exists and works today.

### What works where

**Low and medium temperature (~43% of industrial energy) — solved, just needs deploying:**
- High-efficiency **industrial heat pumps**
- **Waste-heat recovery** (e.g. parts of the ammonia process)
- **Nuclear or geothermal** heat
- **Electric drives** replacing steam where the energy is doing mechanical work, not heating

**High temperature (~49%) — partially solved, mostly nascent:**
- **Electric arc furnaces** — mature, high temperature, already standard for scrap steel
- **Rotodynamic heaters** for cement calcination — new
- **Electro-cracking** for plastics — new
- **Alternative fuels** (biofuels) — can hit high temperatures and need *less* retrofitting, but
  securing reliable feedstock supply is the constraint

### The physical barrier most people miss

> **The form of heat transfer has to change.**

A flame heats by radiation and convection from a combusting gas. An electric element, plasma
torch or induction coil delivers heat by a completely different mechanism, with different
geometry and different distribution through the material. So you cannot simply unbolt the
burner and bolt on an electric one — **the vessel, the process and often the whole plant have
to be reconfigured.** That is why deployment is limited even where the technology exists.

**The counterexample that proves it's possible:** aluminium smelting needs >1,000 °C and is
**already almost entirely electric**. High temperature does not inherently mean unelectrifiable.

### The opportunity the report flags

Electrifying industrial heat can be **cost-effective**, and — critically — it creates **new
flexible demand**. An electrified furnace paired with **thermal energy storage** can heat when
power is cheap and abundant and coast when it isn't.

That is a direct bridge back to Module 1B: industrial electrification is not only a demand
problem for the grid, it is a potential **source of the flexibility the grid desperately needs.**

---

## Reality 7 — New technologies must be viable when the asset turnover window opens

### The steel example

- Global steel output ≈ **1.8 billion tonnes/year** — enough for 24,000 Golden Gate Bridges
- More than **1,400 high-emitting blast furnaces** operating worldwide
- Dominant route: **BF-BOF** (blast furnace–basic oxygen furnace), using coking coal to strip
  oxygen from iron ore into pig iron, then converting that to steel

Blast furnaces need **relining** — interior refractory lining replaced — roughly every
**10–20 years**. It is a major, capital-intensive reinvestment. And:

> **About 60% of the world's blast furnace capacity is due for relining before 2030.**

At that moment the operator faces a binary choice: **reline** (and lock in 10–20 more years of
high-emissions steel) or **replace** with a low-emissions route.

### Why the window is likely to be missed

The leading alternative — **hydrogen-based direct reduction plus an electric arc furnace
(H₂-DRI + EAF)** — is:
- not commercially scaled
- not cost-competitive
- capital-hungry up front
- and requires capabilities the operator may not have

If it isn't ready and bankable *at the moment the relining decision is taken*, the reline
happens by default. The window closes for another two decades.

### The generalisable insight — and it is the most important one in the report

> **The transition is lumpy, not continuous.**

Change does not happen when a clean technology becomes better. It happens when a clean
technology is **ready, affordable and financeable at the exact moment an existing asset comes
up for replacement.** Those moments are scarce, scheduled by engineering rather than by policy,
and they do not wait.

Three consequences:

1. **Timing beats superiority.** A technology that becomes excellent in 2032 loses to a relining
   decision taken in 2028. Being ready on time matters more than being best.
2. **The window is a deadline, not an opportunity.** Missing it doesn't delay the transition by a
   year — it delays that specific asset by a full lifecycle.
3. **This is the same logic as the household boiler** from our earlier Q&A, just at 1,000× the
   scale. Household boiler: 15–20 years. Car: 12–15 years. Blast furnace: 10–20 years. Power
   plant: 30–50 years. Building: 50–100 years. **The longer the asset life, the more urgent the
   decision** — because you get fewer chances.

---

## How Realities 5, 6 and 7 connect

- **R5** — the value of electrifying depends on what's in the wires. *Electrification is only as
  good as the grid behind it.*
- **R6** — some things resist electrification on physical grounds: too hot, or the fuel is an
  ingredient rather than an energy source.
- **R7** — even where electrification works, you can only act in narrow, scheduled windows.

Together they qualify the optimism of Module 1B. Yes, electrify everything — **but** the grid
must lead (R5), about half of industrial heat won't follow (R6), and you only get to act when
the asset lets you (R7).

---

## Check your understanding

1. Why does a BEV start life "in carbon debt," and what pays it off?
2. India's grid was ~841 gCO₂-e/kWh in 2022 and a BEV may never break even against a top ICE at
   that intensity. Why is that *not* a good argument against buying an EV in India today?
3. Name the two structurally different reasons the big four materials are hard to decarbonise.
   Why does the distinction matter?
4. About half of industrial energy is *not* high-temperature. Why is that the most encouraging
   number in Exhibit 6?
5. Why can't you simply replace a gas burner with an electric heater in a cement kiln?
6. Explain "timing beats superiority" using the relining window.

---

## India hooks (parked for Phase 2)

**R5 — grid intensity.** India's grid CO₂ intensity is falling and must be sourced properly from
the **CEA CO₂ Baseline Database** (combined margin, latest version) rather than the report's
2022 figure. Separately, rebuild the breakeven analysis for **electric 2W and 3W**, which is what
India is actually electrifying — small batteries change the answer completely.

**R6 — industry.** India is the world's **second-largest cement producer** and
**second-largest steel producer**, and the **largest producer of DRI (sponge iron)** — but mostly
*coal-based* DRI. India's industrial heat profile is therefore structurally different from the
OECD default, and the gas-to-electric substitution story doesn't map cleanly onto a coal-based
DRI economy. Direct Phase 3 relevance: Ambuja + ACC are Energy Group.

**R7 — turnover windows, and this is a genuinely favourable India finding.**
India is largely **building new capacity rather than replacing old**. The National Steel Policy
targets ~**300 Mt** of crude steel capacity by 2030 *(verify)*. That is a fundamentally better
position than Europe's or Japan's: a **greenfield choice**, not a brownfield retrofit. India
doesn't have to wait for a relining window — it is deciding *now* what to build. The flip side
is the risk: every conventional blast furnace commissioned this decade locks in emissions to
~2060. **India's window is open right now, and it is the only major economy where that is true.**
