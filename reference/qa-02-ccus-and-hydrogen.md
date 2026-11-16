# Q&A 02 — CCUS and hydrogen
Raised after Module 1D.

---

## Q1. With CCUS, are we spending money to prolong fossil fuel reliance?

**Partly yes — and it depends entirely on where you apply it.**

Split CCUS into two very different uses:

**Use A — CCUS on power plants and enhanced oil recovery (EOR).** This *is* largely a life-extension
play. You spend capital to keep a coal or gas plant running, and in the EOR case the captured CO₂ is
literally pumped underground to push out more oil. The criticism lands here. Power exhaust is also
dilute — about **14% CO₂ at a coal plant and ~4% at a gas plant** — among the hardest and most
expensive cases there are. If a solar-plus-storage plant is cheaper than a
coal plant with capture, CCUS on power is a bad trade.

**Use B — CCUS on cement, steel, ammonia, refining.** Here the criticism does *not* land, because
**there is no fuel to switch away from.** About 60% of cement's emissions come from **calcination** —
heating limestone (CaCO₃) drives off CO₂ as a chemical product of the reaction. Even with a
100%-renewable-powered kiln, that CO₂ still comes out. Capture is not prolonging fossil use; it is
the only route.

**The honest framing:** CCUS is a tool for the emissions that *cannot* be electrified away, not a
substitute for electrifying the ones that can. Judge each project by asking: *is there a cheaper
clean alternative for this specific source?* If yes, CCUS is a delay tactic. If no, it's necessary.

The real risk is **political**, not technical — CCUS being used as a reason to defer decisions
elsewhere. That's an argument for discipline about where it's deployed, not against the technology.

---

## Q2. Where are we going to store the CO₂?

Four geological options, in rough order of maturity:

1. **Depleted oil and gas fields.** Best understood — we have decades of data, the seal is proven
   (it held hydrocarbons for millions of years), and the wells already exist. Limited in volume.
2. **Deep saline aquifers.** Porous rock filled with salty, non-potable water, typically >800 m down
   where CO₂ becomes a dense supercritical fluid. **This is where most of the world's capacity is.**
   Northern Lights (Norway) is the flagship.
3. **Basalt formations — mineralisation.** CO₂ reacts with basalt and turns into solid carbonate rock
   in a couple of years. Permanent, no leakage risk. Iceland's CarbFix proved it.
4. **Unmineable coal seams / other.** Niche.

**What actually gets stored:** CO₂ is compressed to a supercritical state (dense like a liquid, flows
like a gas), injected below a caprock, and trapped by four mechanisms — structural trapping under the
seal, residual trapping in pore spaces, dissolution into brine, and finally mineral trapping.
Security *increases* with time.

**India's position — this matters for Phase 3.**
- India has relatively **few depleted oil and gas fields** (Mumbai High, Cambay, Assam) — small volume.
- **Saline aquifer mapping is early.** This is the gap.
- **The Deccan Traps** are a huge basalt province covering much of Maharashtra, Gujarat and MP —
  potentially very large mineralisation capacity, and geographically close to India's cement belt.
  Still research-stage, but it is India's most interesting card.
- Practical constraint: storage has to be **near the emitter**, or you need a CO₂ pipeline network,
  which India does not have.

---

## Q3. Why is CCUS costly?

Four separate costs, and people usually only think about the first.

**1. Separation — the big one.** Cost scales inversely with CO₂ concentration:

| Source | CO₂ in exhaust | Capture cost, $/t |
|---|---|---|
| Gas processing | ~100% | ~20 |
| Ethanol | ~95% | ~24 |
| Ammonia | high | ~18 |
| Iron and steel | ~26% | ~70 |
| Cement | ~21% | ~65 |
| Pulp and paper | ~14% | ~80 |
| Coal power | ~14% | ~74 |
| Gas power | ~4% | ~85 |
| Cars, buildings | ~0.04% (air) | Not capturable at source |

Dilute capture is **3–4× more expensive**. You are moving an enormous volume of hot gas to extract a
small fraction of it.

*Figures read off MGI Exhibit 40 (full report, p. 170), 11 Aug 2026. The costs are chart bars, not
printed numbers. This table replaces an earlier one that mistook Exhibit 40's share-of-US-emissions
bubbles (`<5 / <10 / ~35 / >50`) for concentrations — see [[module-1D-ccus-hydrogen-minerals]].*

**2. The energy penalty.** Post-combustion capture uses an amine solvent that grabs CO₂, then must be
**heated to release it** and be reused. That regeneration heat consumes **15–25% of the plant's own
energy output**. So a captured plant burns more fuel to produce the same useful output — the "parasitic
load". You pay twice: for the capture kit, and for the lost output.

**3. Compression.** CO₂ has to be squeezed to ~100+ bar for pipeline transport and injection. More
energy, more equipment.

**4. Transport and storage.** Pipelines, wells, injection, and then **monitoring and liability for
decades** after injection stops. Someone has to own that risk, and there's no revenue attached to it.

**And the structural problem underneath all four:** CCUS produces **nothing saleable**. A solar farm
sells electricity. A capture plant sells only the avoidance of a cost that mostly isn't priced. Without
a carbon price or a subsidy like the US 45Q, there is no revenue line at all. That, more than the
engineering, is why deployment is at ~2.5 Mt/year against a >1 Gt/year target.

---

## Q4. How does hydrogen make sense — is it useful like CCUS?

**Yes, and in a similar way: it's for the jobs electricity physically cannot do.**

Hydrogen has three genuine advantages:
- **It's a molecule.** It can act as a **chemical feedstock** — the reducing agent that strips oxygen
  from iron ore, or the input to ammonia. Electricity cannot do this; electrons are not ingredients.
- **High energy per kilogram** — useful where weight matters and for long-duration storage.
- **It burns hot** — can reach the >1,000 °C industrial temperatures.

Its fatal weakness is **round-trip efficiency**. Every step loses energy: electrolysis (~30% lost),
compression or liquefaction, transport, then conversion back. **40–75% of the input energy is gone**
depending on the use case.

So the rule is simple:

> **Wherever direct electrification works, it wins. Hydrogen is the fallback for where it doesn't.**

The defensible uses:
1. **Feedstock** — replacing today's grey hydrogen in refineries and fertiliser (this is the biggest,
   cleanest, most immediate market and it already exists)
2. **Green steel** (H₂-DRI) — a chemistry problem electricity can't solve
3. **Very high-temperature heat** where electric options don't yet exist
4. **Long-duration seasonal storage** — weeks, not hours
5. **Long-range shipping and aviation**, usually as ammonia or e-fuels rather than pure H₂

The 2025 report update matters here: **50+ hydrogen projects were cancelled in 2024–mid-2025**, only
2% of announced pipelines reached financial close, and the IEA revised costs **upward**. Meanwhile
batteries and electric kilns took over use cases hydrogen was supposed to own. Be sceptical.

**The one big idea to remember: "move the product, not the hydrogen."** Hydrogen is horrible to
transport — tiny molecule, leaks, needs −253 °C to liquefy, embrittles steel pipes. So don't ship it.
Make hydrogen where power is cheapest, use it there to make **hot-briquetted iron** or **ammonia**,
and ship *that*. Iron and ammonia move easily in ordinary bulk carriers. This reframes green hydrogen
from a fuel-export business into an **industrial relocation** — heavy industry migrates to wherever
renewable electricity is cheapest. For India (cheap solar, existing ports) that is a real opportunity.

---

## Q5. Why shift to hydrogen cars at all?

**Short answer: mostly, you shouldn't. For passenger cars the argument has been lost.**

The efficiency comparison is brutal:

| Route | Electricity → wheels |
|---|---|
| Battery EV | **80–90%** |
| Hydrogen fuel-cell vehicle | **25–35%** |

A hydrogen car needs roughly **three times the renewable electricity** to drive the same kilometre.
On top of that you'd need a completely new refuelling network, and hydrogen stations cost far more
than chargers.

Hydrogen's original pitch was fast refuelling and long range. Both advantages have eroded — the 2025
report notes cars now charging **400–500 km in 5 minutes** in China, and electric trucks reaching
**500–600 km** with megawatt charging in 15–30 minutes. The report is explicit: **battery electric
trucks can now serve use cases previously thought to need hydrogen.**

**Where fuel cells might still survive:** very heavy, very-long-haul, high-utilisation vehicles where
battery weight eats the payload, mining and port equipment running continuously, and possibly some
long-haul freight corridors. Even there, batteries are closing the gap fast.

**Verdict for the India work:** treat hydrogen mobility as marginal. Point India's green hydrogen
story at **refineries, fertiliser and ammonia export** — real, existing, large demand — not vehicles.
