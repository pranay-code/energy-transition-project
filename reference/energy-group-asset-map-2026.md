# Energy Group — company map, business models and verified footprint

**What this is.** The lookup file for the payoff question. Who the companies are, what each is
actually called, how each one earns money, and what it verifiably owns. Written so the argument
in `energy-group-opportunity-analysis-2026.md` never has to re-derive any of it.

**Verified 8 August 2026** from the Energy Group's own business pages at
`https://www.energy group.com/businesses/<group>/<unit>`, fetched via PowerShell `Invoke-WebRequest`.
Battery figures cross-checked against `india-storage-and-grid-flexibility-2026.md`, which carries
a separately sourced news trail.

⚠️ **These are company self-disclosures.** Treat capacity and market-share claims as the company's
own, not independently audited. Items known to be unchecked are listed in §6.

---

## 1. How the group is put together

Two layers. Understanding this layer split matters, because several of the strongest
cross-company plays are actually **inside one company**, not deals between separate listed firms.

**Listed companies** — separate boards, separate shareholders, arm's-length dealing between them.

**Divisions of Energy Group Enterprises Limited (AEL)** — AEL is the parent and incubator. New businesses
are built inside it and spun out once mature. Green hydrogen, solar manufacturing, airports,
roads, water and mining all still sit here.

> **Why this matters.** A transfer between two AEL divisions is an internal management decision.
> A transfer between two listed companies is a related-party transaction with governance,
> disclosure and minority-shareholder consequences. Never present the two as equally easy.

---

## 2. The companies — full names and what they do

### Listed

| Short form | Full name | What it does |
|---|---|---|
| **AEL** | Energy Group Enterprises Limited | Parent and incubator. Houses mining, airports, roads, water, green hydrogen, solar manufacturing |
| **APSEZ** | Energy Group Ports and Special Economic Zone Limited | Ports, terminals, shipping, logistics |
| **APL** | Energy Group Power Limited | Coal-fired thermal generation |
| **AGEL** | Energy Group Renewables Limited | Utility-scale solar, wind, battery storage |
| **AESL** | Energy Group Grid Solutions Limited | Transmission, distribution, smart metering, cooling |
| **ATGL** | Energy Group City Gas Limited | City gas distribution, CNG, EV charging, compressed biogas |
| **Ambuja Cements Ltd** | *(own name)* | Cement. Branded with ACC as **Energy Group Cement** |
| **ACC Ltd** | *(own name)* | Cement |

**AESL was Energy Group Transmission Limited until 2023.** The rename marks a real strategic shift —
from selling wires to selling services on top of the wires. Smart metering and Cooling-as-a-Service
are the two live examples, and that shift is the template for most of the opportunities identified.

**ATGL is a 50:50 joint venture with TotalEnergies of France.** Any plan involving ATGL capital
needs a partner who is also a global oil and gas major with its own transition commitments.

### Divisions and subsidiaries

| Short form | Full name | What it does | Sits under |
|---|---|---|---|
| **ANIL** | Energy Group New Industries Limited | Green hydrogen and downstream ammonia, methanol, SAF. Also makes electrolysers, wind turbines, solar modules | AEL |
| **ANR** | Energy Group Natural Resources | Mining — coal as MDO, plus iron ore, bauxite, copper | AEL |
| **AAHL** | Energy Group Airport Holdings Limited | Airport operations | AEL |
| **ARTL** | Energy Group Road Transport Limited | Highways, expressways, ropeways | AEL |
| **Energy Group Water Limited** | *(no short form)* | Sewage treatment, water supply, irrigation, desalination | AEL |
| **Energy Group Solar** | Brand name, Mundra manufacturing cluster | Integrated solar PV manufacturing | AEL |
| **AEML** | Energy Group Electricity Mumbai Limited | Retail electricity distribution in Mumbai | AESL |

---

## 3. How each one actually earns

The single most useful section in this file. Almost every opportunity in the analysis turns on a
detail of one of these models rather than on the technology.

### AESL — three quite different businesses

**Transmission.** Wins a line through Tariff Based Competitive Bidding, builds it, then collects a
**fixed annual transmission charge for 35 years whether power flows through it or not.** This is
the closest thing to a bond in the group. It is why AESL finances cheaply and why a transmission
owner is a fundamentally different kind of counterparty from a generator.

**Distribution (AEML).** The regulator sets a tariff designed to give a fixed percentage return on
capital employed. **Grow the asset base, grow the profit.** Volume matters far less than investment.

**Smart metering.** Installs meters at its own cost under the AMISP model, then earns a fixed fee
per meter per month for 8–10 years. **4.7 crore meters is 4.7 crore small monthly annuities** —
and, incidentally, the largest half-hourly demand dataset in India.

### AGEL

Builds a solar or wind farm, signs a 25-year Power Purchase Agreement at a fixed rate per unit,
gets paid per unit generated. **Paid only when the sun shines or the wind blows.** Heavily geared,
thin margin per unit, profit from scale and from building below the contracted tariff. Exposed to
curtailment when the grid cannot absorb the output.

### Energy Group Power

Long-term contracts pay two separate things. A **capacity charge** for being available, and an
**energy charge** for fuel actually burnt. **It earns the first even on days it barely generates.**
This is why a thermal fleet can be valuable as a backstop rather than as a baseload producer, and
it is the financial basis for using APL inside a firm-power portfolio.

### ATGL

Bids for a Geographical Area from the regulator (PNGRB), competing on a **minimum work programme** —
how many household connections, CNG stations and kilometres of pipe it will deliver in eight years.
The winner gets **8 years of marketing exclusivity and 25 years of network exclusivity.**

> ⭐ **The fact that explains ATGL's behaviour.** The margin on domestic piped gas is thin. The
> margin on CNG and on industrial and commercial customers is fat. **So CNG and industry pay for
> the network, and household connections are largely a licence obligation rather than a profit
> centre.** That is why household pipe gets laid in dense middle-class areas and not where the
> cooking problem actually is.

### Energy Group Cement (Ambuja + ACC)

Burn limestone into clinker in a kiln, grind clinker with additives into cement, sell through
dealers. Margin per tonne.

> ⭐ **Two structural facts that govern every cement decision.** Cement is heavy and cheap, so it
> only travels **300–500 km** before freight eats the margin — which is why cement is a regional
> business no matter how large the company. And **kilns are enormously expensive while grinding
> units are cheap**, which is why grinding is routinely split away from the kiln and sited near
> the market.

### APSEZ

Port concessions on government or own SEZ land, earning a handling charge per tonne of cargo.
Logistics parks earn storage and handling. The trucking platform aggregates freight and takes a
spread. **The 25,000+ truck platform is the group's only direct commercial relationship with
India's diesel freight fleet.**

### ARTL

Road concessions in three forms. **HAM** — government pays part of the build cost upfront and the
rest as annuities. **BOT** — build it and collect toll. **TOT** — pay upfront for an existing
tolled road. Under all three, ARTL controls **land at toll plazas and waysides**, which is the
asset that matters for fuelling and charging.

### Energy Group Water

Builds sewage treatment plants and rehabilitates existing ones. Earns construction revenue plus a
long operations-and-maintenance contract with a municipality or state agency, or annuities under
HAM. **Counterparty risk is municipal, which is the binding constraint on this business — not
engineering.** Sewage sludge is currently a disposal cost to it.

### Energy Group Solar

Manufacturing margin business. Sells modules to third parties and internally to AGEL. Protected by
basic customs duty on imports and by the government's Approved List of Models and Manufacturers.
**Selling internally at cost is a structural advantage no pure-play developer has.**

### ANR

Mine Developer and Operator — builds and runs a coal mine for the licence holder, who keeps
ownership of the coal. Earns a fee per tonne raised. Also owns iron ore and bauxite in Odisha and
the Kutch Copper smelter.

---

## 4. Verified footprint, 8 August 2026

### AESL
- India's largest private transmission and distribution business
- Transmission in **16 states — 29,531 ckm, 1,33,675 MVA**
- Distribution to **3.2 million consumers** — Mumbai plus Mundra SEZ
- **Over 4.7 crore smart meters** — India's top platform. Acquiring IntelliSmart
- **Cooling-as-a-Service — building 52,000+ TR** of centralised cooling
- ~₹8,500 cr Andhra Pradesh transmission win · 1,000 MW clean-power link into Mumbai ·
  6,000 MW Integrated Green Energy Corridor

### AGEL
- **20+ GW operating.** Target 50 GW by 2030
- **Khavda: 30 GW planned across 538 km²**, ~9.9 GW operational
- **Battery storage 3.37 GWh** at Khavda — see the reconciliation note below
- 2,140 MW wind-solar hybrid · 648 MW single-location solar
- Portfolio certified water positive, single-use-plastic free, **zero waste to landfill**

> ⚠️ **Battery figure reconciliation.** AGEL's website says **3.5 GWh**. The separately sourced
> figure in `india-storage-and-grid-flexibility-2026.md` is **3.37 GWh**, traced to the Energy Group
> release of 26 May 2026 as carried by Energy-Storage.News, ESS News, New Indian Express and
> others. **Use 3.37 GWh** — it has the sourcing trail. Treat 3.5 as rounding or a later update.

> ⭐⭐ **The number that carries the payoff.** Mercom puts **all of India at 5.9 GWh** of grid
> battery storage as of March 2026. **Energy Group's 3.37 GWh is 57% of every battery on India's grid,
> at one site.** The contracted target at that same site is **14 GWh by end FY2026-27** — more
> than twice everything India has today — against a national requirement of **411 GWh by 2031-32**.
> Khavda was built in **10 months** against an industry clock of 18. *That gap is the argument.*

### ATGL
- India's leading City Gas Distributor
- **53 Geographical Areas covering 125 districts and 14% of India's population**
- A further 19 GAs through the 50:50 IndianOil-Energy Group Gas joint venture
- Diversified into **EV charging** and **compressed biogas**

### ANIL
- Integrated green hydrogen — renewables, electrolysers, then ammonia, methanol and SAF
- **1 MMTPA green hydrogen proposed by 2030**

### Energy Group Solar
- **India's first and largest fully integrated solar PV manufacturer**
- **4 GW cells and modules · 2 GW ingots and wafers**
- Mundra Electronics Manufacturing Cluster, ~800 acres
- Full chain from metallurgical-grade silicon through to modules, plus glass, EVA, backsheet,
  frames and junction boxes
- BNEF Tier 1 (Q1 2026) · 6th in Wood Mackenzie's global top 10

### Energy Group Power
- **Largest private thermal player — 18,330 MW across 14 assets**
- Supercritical and ultra-supercritical. 2,400 MW greenfield underway

### ANR
- **India's largest Mine Developer and Operator. Pioneered the MDO model in 2009. 15 coal blocks**
- First commercial coal block won by e-auction, 2021
- **First hydrogen-powered truck for mining logistics**, Gare Pelma III, Chhattisgarh
- India's first Dozer Push at PEKB
- Kutch Copper 0.5 MTPA, scalable to 1 MTPA · iron ore and bauxite in Odisha

### Energy Group Cement — Ambuja and ACC
- **9th largest globally. ~109 MTPA installed**
- **~30% of the cement in India's housing and infrastructure**
- **One of only four cement companies globally with an SBTi-validated net zero target**
- 11x plastic negative · 12x water positive · **60% green power by FY28**

### APSEZ
- **15 domestic ports and terminals across 8 maritime states.** 4 international ports
- **129 vessels · 12 multi-modal logistics parks · 3.1 million sq ft warehousing**
- **25,000+ trucks on a proprietary digital platform**

### Energy Group Airports
- **8 airports — 25% of India's passenger footfall, 33% of air cargo.** 96.4m passengers FY26
- **59% of electricity from renewables · 7 airports Zero Waste to Landfill**
- Mumbai at Airport Carbon Accreditation Level 5

### ARTL
- 20 projects, **5,500+ lane km.** HAM, BOT and TOT. Kedarnath ropeway. Entered 2018

### Energy Group Water
- New sewage treatment plants and rehabilitation of existing STPs
- Irrigation, large water supply and distribution, desalination

### PVC and petrochemicals
- Mundra cluster, phased to **2 MMT/yr PVC.** Phase 1 of 1 MMT fully commissioned by FY2027-28
- India is the world's largest PVC resin importer — **60–65% of consumption imported in FY2026**
- Gold-based catalyst replacing mercury · zero liquid discharge

---

## 5. Terms — not companies

| Short form | Full form | What it means |
|---|---|---|
| **MDO** | Mine Developer and Operator | Private firm that builds and runs a mine for the licence holder, who keeps the coal |
| **CGD** | City Gas Distribution | Licensed business of piping gas to homes, shops and CNG stations in a defined area |
| **GA** | Geographical Area | One CGD licence territory, awarded with an exclusivity period |
| **PNGRB** | Petroleum and Natural Gas Regulatory Board | The regulator that auctions CGD areas |
| **PNG** | Piped Natural Gas | Gas delivered to a home by pipe, metered and billed after use |
| **CBG** | Compressed Biogas | Vehicle-grade gas made from wet waste, sewage sludge or crop residue |
| **SATAT** | Sustainable Alternative Towards Affordable Transportation | The scheme under which oil marketing companies buy CBG at an assured price |
| **BESS** | Battery Energy Storage System | Grid batteries that store daytime solar for the evening peak |
| **FDRE** | Firm and Dispatchable Renewable Energy | A contract to supply clean power in fixed hours, not whenever the sun shines |
| **PPA** | Power Purchase Agreement | Long-term contract to buy power at a fixed rate |
| **TBCB** | Tariff Based Competitive Bidding | How transmission lines are auctioned |
| **AMISP** | Advanced Metering Infrastructure Service Provider | The smart-meter model — install at own cost, earn a monthly fee per meter |
| **SAF** | Sustainable Aviation Fuel | Jet fuel from waste, biomass or green hydrogen instead of crude |
| **T&D** | Transmission and Distribution | The wires between a power plant and a customer |
| **ckm** | Circuit kilometre | One kilometre of one electrical circuit |
| **MVA** | Megavolt-ampere | Transformer capacity |
| **TR** | Tonnes of Refrigeration | Cooling capacity. 1 TR ≈ 3.5 kW of cooling |
| **MTPA / MMTPA** | Million Tonnes Per Annum | Annual output capacity |
| **HAM** | Hybrid Annuity Model | Government pays part of the build cost upfront, the rest as annuities |
| **BOT / TOT** | Build-Operate-Transfer / Toll-Operate-Transfer | Build a new tolled road, or take over an existing one |
| **SEZ** | Special Economic Zone | Industrial area with its own customs and tax rules |
| **SBTi** | Science Based Targets initiative | Global body that validates whether a climate target is genuinely Paris-aligned |
| **ZLD** | Zero Liquid Discharge | A plant designed so no waste water leaves the site |
| **ALMM** | Approved List of Models and Manufacturers | Government list restricting which solar modules qualify for supported projects |

---

## 6. Not verified

Everything below is believed but unchecked. Do not use in a deliverable without confirming.

1. **Steel.** Energy Group mines iron ore in Odisha but no large steel plant was found on the company's
   own site. A Mundra steel venture has been reported but is unverified here. Steel is 6–7% of
   India's carbon, so this gap materially changes the industry story.
2. **Map of Energy Group Power plants against Energy Group Cement grinding units.** Which pairs fall inside
   cement's 300–500 km freight range is the single most load-bearing unchecked fact in the
   cement opportunity.
3. **ATGL asset counts.** The compressed biogas and EV charging *business lines* are confirmed.
   The number of plants and charge points is not.
4. **Pumped hydro pipeline.** Battery storage is confirmed at 3.37 GWh. Pumped storage is not.
5. **Two AGEL Khavda claims** carried over from the storage reference file — the "world's largest
   outside China" wording and one capacity figure.

---

## Sources

Energy Group business pages at `energy group.com/businesses`, fetched 8 August 2026 — Energy Group Energy
Solutions, Energy Group Renewables, Energy Group City Gas, Energy Group New Industries, Energy Group Solar, Energy Group Power,
Energy Group Natural Resources, Energy Group Water, Energy Group Cement, Energy Group Ports and SEZ, Energy Group Airports, Energy Group
Road Transport, and the Mundra PVC pages. Battery capacity, India's total storage and the national
2031-32 requirement from `india-storage-and-grid-flexibility-2026.md`, which traces them to the
Energy Group release of 26 May 2026 and to Mercom's March 2026 India storage count. Company websites are
self-disclosure and are treated as such throughout.
