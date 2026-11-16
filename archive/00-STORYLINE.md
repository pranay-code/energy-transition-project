# The Storyline — the question chain

**This file is the single source of truth for the chain**: which questions, in what order, from
what sources, into which file. Writing rules, persona and audience live in `CLAUDE.md` — they are
deliberately not repeated here.

Written one question at a time, in order. Draft in chat, get approval, then save.

**Numbering is not fixed.** Questions merge and split as the story tightens (the India
world-average scenario was folded into Q8 on 6 Aug 2026, taking the chain from 14 to 13). Refer to
questions by role — *runway*, *core*, *payoff* — in any rule or instruction, never by number.

## The Chapters

The 17 questions (plus two planned additions) are grouped into 8 story chapters, each with a tagline to guide the reader:

*   **Chapter 1: The Beginning** — *How the world got so hot, and why it matters right now.* (Q1–Q5)
*   **Chapter 2: Eye Opening and Getting Ready** — *How the world is finally coming together to face the challenge.* (Q6–Q7, plus new question on fairness)
*   **Chapter 3: Our Pathway to the Common Goal Gate** — *India’s big promises and the real targets we have to hit.* (Q8–Q9)
*   **Chapter 4: Action Time** — *Let's analyse what the real solutions and challenges are.* (Q10–Q11)
*   **Chapter 5: Big Problem, But What First?** — *Let's prioritize and hit the biggest ones.* (New question on solar + Q12 on Electricity)
*   **Chapter 6: Reality Check** — *The hard truth about building our cities and feeding our people.* (Q13–Q14: Industry and Farming)
*   **Chapter 7: Let's Get Moving** — *The hard reality of shifting from petrol pumps to power plugs.* (Q15: Transport)
*   **Chapter 8: Rewire, Redo, and Build the Nation (TWO VERSIONS)** — *Let's get practical and turn challenges into opportunities.*
    *   **Version A (General Audience):** Q16 + a strong concluding wrap-up for the nation.
    *   **Version B (Energy Group Edition):** Q16 + Q17 (The Energy Group Payoff).

---

## The chain

| # | The question, as a reader would ask it | Ends on (the hook into the next one) | Must cover | Main sources | Output file |
|---|---|---|---|---|---|
| **Q1** | **What is climate — is it the same thing as weather? What about this "climate change"?** | This is what we call rapid climate change | Weather vs climate, plainly. Natural timescales. Today's rate vs the deglacial rate (~1 °C/1,700 yrs then, ~1 °C/40 yrs since 1980) | IPCC AR6 WG1, NOAA GML, HadCRUT5, PAGES2k | `01-what-is-climate-change.md` |
| **Q2** | **Rapid climate change: is this bad? And why?** | It is speeding up on its own — which leaves one big question: who started it? | Speed, not warmth. Life adapts over millennia, not decades. Self-reinforcing loops (ice–albedo) | IPCC AR6 WG2, WG1 SPM, SR1.5 | `02-why-speed-matters.md` |
| **Q3** | **Who is responsible? And why is this called "human-induced" climate change?** | All the clues point back to us | Attribution in plain terms: the timing lines up, the amounts match, nature has an alibi. **No isotopic-fingerprint jargon** — it did not land with the reader | IPCC AR6 WG1 Ch.3, Global Carbon Project | `03-attribution.md` |
| **Q4** | **So how exactly are we doing it? What are all the ways?** | Now the real question — how do we stop it? | Burning ≈ 3 in 4 tonnes. Then deforestation, cattle and rice methane, fertiliser, cement | Global Carbon Budget, IPCC AR6 WG3, FAO, EDGAR | `04-mechanisms.md` |
| **Q5** | **So how do we stop it?** | No single country can fix this alone — a truly global challenge | Nature already absorbs some (forests, soil, **oceans**). Net zero = what we add fits what nature takes back. Cut burning, protect sinks, trap the rest. **No technical difficulty here** — that is the core's job | IPCC AR6 WG3 SPM | `05-how-to-stop-it.md` |
| **Q6** | **Since this is a world issue, did governments come together and try to fix it? Any solutions or plans?** | The Paris Agreement is where the real story of action begins | Rio 1992 → Kyoto 1997 (left out poorer countries) → Copenhagen 2009 (fell apart) → Paris 2015 (stuck) | UNFCCC, IEA | `06-global-response.md` |
| **Q7** | **What is the Paris Agreement? Is it just a simple net-zero target, or something more objective — does it get into the details of what to do?** | Which brings us to — who is doing most of the emitting, and where does India stand? | Objective at the top: well below 2 °C, aim 1.5 °C, measured against the late 1800s; global net zero ~2050. Not prescriptive below that — sets the destination, not the route. **Do not dwell on its weaknesses** — our whole analysis is built against these commitments | UNFCCC Paris text, IPCC SR1.5 | `07-paris-agreement.md` |
| **Q8** | **Carbon emissions country by country — where does everyone stand, and where does India fit in?** | India's own targets matter — so what are the hard, objective numbers? | China ~30%, US ~13%, India ~7–8%. Per person: India ~2 t vs world ~4.7 t. Historical: India 3–4%. **Then the what-if**: every Indian at world average → ~3 Gt becomes ~7 Gt | Global Carbon Project, IEA, Our World in Data, UN pop. | `08-emissions-by-country.md` |
| **Q9** | **So what exactly has India signed up for under the Paris Agreement?** | You cannot cut what you cannot find — where is all that carbon coming from? | Three numbers, stated as bullets: **net zero 2070, not 2050** · −45% carbon per unit of work by 2030 vs 2005 (worded as "work", not "rupee of GDP" — money did not land with the reader) · ~50% non-fossil capacity / ~500 GW by 2030, half-mark crossed in 2025. Plus the remaining global carbon budget. **Anchor the analysis on 2030 as the action window and 2070 as the destination** | India NDC (UNFCCC 2022), COP26 Panchamrit, CEA 2025, IPCC AR6 carbon budget | `09-targets.md` |
| **Q10** | **Fine — but where is all this carbon actually coming from?** | Nothing else can make up for power — so what actually replaces each of these? | World pie first, then India's, six slices each, **2023 data (Climate Watch stops there)**. India: power 37.5 · industry 21.7 · farming 19.5 · transport 9.2 · buildings 5.8 · rest 6.3. Punch: power is 37% against 22% for the next biggest, and cleaning all transport would only remove 9%. Exhibit table included for a pie chart | Climate Watch/WRI via OWID (2023), Ember (2025 coal share) | `10-emissions-by-source.md` |
| **Q11** | **Okay, we know the sources and the major ones among them — how are we going to reduce them and meet our targets?** ← **THE BRIDGE** | Almost every road leads back to the same place, so start where the carbon is thickest: electricity | One line of solution + one line of challenge per sector, nothing deeper. Two exhibits: the at-a-glance strip, and the dependency diagram showing industry, transport and buildings all pointing into power while farming stands alone. **No difficulty explained here** — that is the sector questions' job | IEA, MGI, NITI Aayog, Ember 2025 | `11-solutions-by-source.md` |
| **Q12** | **Electricity sector: emission sources, solutions, challenges, and progress against targets?** ← **CORE 1** | The grid is the gate everything waits at — but factories cannot wait, and not all of their carbon comes out of a socket | Five beats (rule 3.4). Coal 40.8% of capacity but 70.8% of generation · power emissions 1,234 Mt and up 36% in four years · **grid carbon flat at ~0.71 t/MWh for five years while renewables grew 73%** · peak 270,832 MW arriving at 22:36, a 60 GW evening ramp · storage at 5.9 of 411 GWh · one-third of new RE on a temporary grid connection, Rajasthan curtailing up to 80% · 1.65 TW globally awaiting connection · **say plainly: record 54.6 GW of RE added *and* ~97 GW of new coal planned** | `india-power-snapshot-2026.md` (all of it), `module-1B`, `module-1F` | `12-power.md` |
| **Q13** | **Industry — steel, cement, the things India is still building. Can they be made clean?** ← **CORE 2** | India is not retrofitting; it is deciding right now what to build | Five beats. Heat vs feedstock as two separate problems · cement's process CO₂ · 49% of industrial energy above 500 °C · H₂-DRI and the four real blockers · **India is greenfield, not brownfield** | `module-1C`, `qa-03-steel-and-coal.md`, Ministry of Steel | `13-industry.md` |
| **Q14** | **Farming — 20 percent of India's emissions and no factory to fix. What then?** ← **CORE 3** | The one sector electricity cannot solve | Five beats. Cattle methane and paddy methane · fertiliser N₂O · alternate wetting and drying · why crores of small decision-makers is the binding constraint, not the technology. **Be honest that this sector has no Energy Group route** | FAO, MoEFCC BUR-4, ICAR, IRRI | `14-farming.md` |
| **Q15** | **Transport — small today. Does that stay true?** ← **CORE 4** | The EV question is really a grid question | Five beats. **India's story is 2W/3W, not cars** · MGI's pessimistic India car finding at ~841 gCO₂-e/kWh and why it does not transfer to two-wheelers · freight and rail · charging load lands on the same evening peak | `module-1C`, `research-findings-highlights.md`, MoRTH Vahan, IEA | `15-transport.md` |
| **Q16** | **Buildings, cooling, waste and gas leaks — the 12.1 percent left over.** ← **CORE 5** | The fastest-growing source in this slice has no number at all | Five beats, seven items. Cooking connected but not converted · household sewage split from factory water · open-cast mine methane · the refrigerant India marks "not applicable". **Electricity deliberately excluded — it belongs to Q12** | MoEFCC BUR-4, ICAP, CPCB, MoHUA | `16-buildings-and-rest.md` |
| **Q17** | **Challenges in disguise — the Energy Group opportunity** ← **THE PAYOFF** | Energy Group | Five opportunities, ranked and already stress-tested: **the evening hour** · **piped gas into low-refill districts** · **waste into a pipe Energy Group already owns** · **the freight corridor, not the charger** · **ash, cement and the coming shortage**. Say plainly where there is no position — farming, refrigerants, open-cast mine methane, and minerals. Say plainly that coal is the declining leg. Nothing sits between the last sector question and this | `reference/energy-group-asset-map-2026.md` and `reference/energy-group-opportunity-analysis-2026.md` — both written 8 Aug 2026 | `17-energy-group-opportunity.md` |

**Deliberately kept out of the runway:** technical difficulty, engineering constraints, and any
"why fossil fuels are hard to replace" material. Put early, they make the story impossible to
follow. The runway stays narrative and light; **all difficulty is concentrated in the core.**

---

## Why the order matters

Q1–Q5 establish that the problem is real, fast, ours, and physical.
Q6–Q7 establish that the world has responded and set a firm shared goal.
Q8–Q10 narrow from the world to India to the specific tonnes.
Q11 is the bridge: names a solution and a challenge for every sector, then hands over to the sectors.
Q12–Q16 take one sector each, in order of size, all following the same five beats.
Q17 turns the accumulated constraints into a commercial position.

**The core is no longer one question.** It became five, one per sector, on 7 Aug 2026. The reason:
the Energy Group argument is much stronger made sector by sector, against a challenge the reader has just
had explained, than assembled all at once at the end. The five beats are rule 3.4 in `CLAUDE.md`.

Everything before the payoff exists to make the payoff unavoidable rather than promotional.

---

## Progress

| Q | Status |
|---|---|
| Q1 | ✅ Locked 6 Aug 2026 — `01-what-is-climate-change.md` |
| Q2 | ✅ Locked 6 Aug 2026 — `02-why-speed-matters.md` |
| Q3 | ✅ Locked 6 Aug 2026 — `03-attribution.md` |
| Q4 | ✅ Locked 6 Aug 2026 — `04-mechanisms.md` |
| Q5 | ✅ Locked 6 Aug 2026 — `05-how-to-stop-it.md` |
| Q6 | ✅ Locked 6 Aug 2026 — `06-global-response.md` |
| Q7 | ✅ Locked 6 Aug 2026 — `07-paris-agreement.md` |
| Q8 | ✅ Locked 6 Aug 2026 — `08-emissions-by-country.md` (what-if scenario folded in) |
| Q9 | ✅ Locked 7 Aug 2026 — `09-targets.md`. Confirmed India = net zero **2070**, no 2050 target. First answer to use bullets (rule 3.2 changed to allow them) |
| Q10 | ✅ Locked 7 Aug 2026 — `10-emissions-by-source.md`. First answer with an exhibit table |
| Q11 | ✅ Locked 7 Aug 2026 — `11-solutions-by-source.md`. The bridge. Two exhibits |
| Q12 | ✅ Locked 7 Aug 2026 — `12-power.md`. **The first core question, and the template for all five.** Heading style changed here: short and plain, naming the five beats in order, instead of a conversational question. Beats are numbered sections, list items are numbered `section.item`, and **beat 2 and beat 3 carry the same six items in the same order** so each solution is seen twice — once as a fix, once as an obstacle. Exhibits are folded inline, not appended |
| Q13 | ✅ Locked 8 Aug 2026 — `13-industry.md`. **Confirms Q12 as the template and fixes the five beat titles word for word.** Two things Q12 left open are settled here: beat 4 is the three-part ladder (built and working / started, not finished / proof the finished version works), **not** an item-locked six; and beat 5 closes with a "the number nobody set a target for" section. Built on two government roadmaps read in full — Ministry of Steel and NITI Aayog cement. The spine is **heat versus feedstock** |
| Q14 | ✅ Locked 8 Aug 2026 — `14-farming.md`. **The first sector where MGI's 25 challenges do not reach** — there is no agriculture domain in the seven, so beat 3's five challenges are ours, built MECE by naming a different missing input each time (material · price · infrastructure · logistics · time), and the reader is told openly that they are ours. Built almost entirely on **India's Fourth Biennial Update Report to the UNFCCC**, downloaded and read in full. The spine is **the gas is different** (methane and nitrous oxide, biological, untouched by clean electricity) and **the decision-maker is different** (crores of households, no boardroom). Load-bearing finding: **79% of every tonne India has cut in farming came from one factory-gate decision** — neem-coated urea — and 21% from every farmer-by-farmer scheme combined. Beat 5 re-sorts the five rows by progress instead of size, so the biggest prize shows up as the slowest mover |
| Q15 | ✅ Locked 8 Aug 2026 — `15-transport.md`. **The sector where MGI's list does reach India again** (mobility = challenges 7–11), so beat 3 is theirs, not ours. Spine: **transport's answer is written on the power question's page** — every solution here ends by handing its carbon to the grid, and the railway has already finished that handover (31.8 TWh of traction power ≈ 23 Mt booked to power stations, eight times its visible 3 Mt). MGI's pessimistic India EV finding was **rebuilt, not imported**: at 710 g/kWh the scooter pays off its battery in ~7,800 km (about a year) while the car needs 65,000 km and never breaks even against an efficient petrol car — which is why India's EV story is scooters and autos. Load-bearing finding, and the second sighting of Q14's pattern: **ethanol blending delivered 31.8 Mt of the 37.5 Mt India credits to transport measures — 85% — against 0.4 Mt from every EV purchase subsidy, about 75× less.** Upstream beat downstream in two sectors independently. Also carries the charging-delivery failure: 83 built of 2,877 approved under FAME-II, and **0 of 6,562 sanctioned under PM E-DRIVE, ₹0 spent** (Lok Sabha, Aug 2026) |
| Q16 | ✅ Locked 8 Aug 2026 — `16-buildings-and-rest.md`. **The fifth and last core question, and the "everything left over" slice — buildings, cooking, cooling, waste AND gas leaks, 12.1%.** Electricity was cut out entirely on instruction: buildings' 33.5% share of consumption belongs to Q12 and must not be double-told, so cooling enters through the **refrigerant** instead, which India marks "not applicable" and does not estimate at all. Household sewage (34.1 Mt) split from factory waste water (21.8 Mt) — two owners, two fixes. Seven beat-2/beat-3 items, not six. Three boxes total 141 Mt with **no scheme pointed at them**: shops and offices, mine methane, factory water |
| **All five sectors** | ✅ **Share-of-India retro-fit, 8 Aug 2026.** Every sector answer now opens with its share as a clear number, and every beat-1 table carries an **Of India** column. One denominator throughout — see "The sector-share rule" below |
| Q17 | ✅ **Locked, 8 Aug 2026 — "Challenges in disguise: the Energy Group opportunity."** Five opportunities in reader voice: the evening hour · piped gas into low-refill districts · rubbish into a pipe Energy Group owns · the freight corridor not the charger · cement, ash and the coming shortage. Four honest gaps named (farming, refrigerants, open-cast methane, steel) and **the coal tension stated plainly**. Built from `reference/energy-group-asset-map-2026.md` and `reference/energy-group-opportunity-analysis-2026.md`. **The rubric, the scoring and the three stress-test corrections were deliberately kept off the page** — rule 1.3. ~2,200 words, the longest answer in the chain, and **the only one with no forward hook**, since it closes the report |

**Q9 open check — now closed.** CEA's own installed-capacity file (as on 30 June 2026) confirms
non-fossil capacity at **297,369 MW of 548,858 MW = 54.18%**. Q9 updated to the verified figure and
the caution removed from its source line.

**Carried into the core — now used.** Power's share of India's *fuel-burning* emissions is 53%
(world 46%), a sharper figure than the 37% of total greenhouse gases used in Q10. It opens Q12's
section 1. Detail at the foot of `10-emissions-by-source.md`. **Never put 37.5%, 48% and 53% in the
same answer** — three different denominators, and the reader will think one of them is wrong.

**Found while writing Q12, and held back for the payoff.** Energy Group Renewables has **3.37 GWh of battery
storage operational at Khavda**, which is **57% of every battery on India's grid** (Mercom puts all
of India at 5.9 GWh), built in about **10 months** against the 18-month industry norm, and
contracted to reach **14 GWh** at that one site. Q12 states the 3.37 GWh as a plain fact and says
nothing commercial about it. The argument belongs to Q17. Full detail and sourcing in §5 of
`reference/india-storage-and-grid-flexibility-2026.md`.

---

# ▶ CHECKPOINT — start here (updated 8 Aug 2026)

**State: the chain is complete. Q1 to Q17 are all written and locked, 8 August 2026.** Runway,
five sector questions, and the payoff. Nothing is half-written and nothing is missing.

**What a new session should do now is no longer draft — it is check, close and shape.**

1. **Close the open items.** The full list is under "Still unverified" below. Two are marked ⭐
   because a deliverable turns on them: the map of Energy Group Power's plants against Energy Group Cement's
   grinding units, and ATGL's real biogas and charging counts.
2. **Read the 196-page MGI full report.** Still unread, and it is the authoritative source behind
   the entire reference library.
3. **Read the chain end to end as a reader would**, in file order 01 to 17, checking that every
   answer still hands cleanly to the next. The sector-share retro-fit and the Q13 steel correction
   both landed late, so the joins around Q12 to Q16 have never been read as one piece.
4. **Then the deck.** The written chain is the argument; the deck is a different artefact and has
   not been started.

**The two Energy Group reference files are the research base and are finished.** Do not re-research them
and do not re-argue their conclusions.

- `reference/energy-group-asset-map-2026.md` — company full names, the two-layer group structure,
  **how each company actually earns money**, verified footprint, term glossary
- `reference/energy-group-opportunity-analysis-2026.md` — the rubric, the five opportunities, what to
  decline. **Read §5 and §6 before quoting anything: three claims failed arithmetic and were
  rebuilt, and in two cases the corrected version is the stronger argument**

## The house style — kept for any rewrite, no longer a drafting instruction

Every question is written. This block records how, so a later edit or a rewritten section does not
drift from the rest of the chain.

1. Read `CLAUDE.md` (loads on its own), then this file, then **`storyline/13-industry.md` in full,
   including its working notes.** Q12 set the template; Q13 finished it; Q14 proved it survives a
   sector MGI never covered; Q15 proved it survives a sector MGI does cover. Read Q12 too if the
   beat-4 ladder or the beat-5 closing section is unclear.
2. **Copy the shape exactly.** Short plain heading naming the beats in order · five numbered
   sections with these titles word for word — *Where the carbon comes from · The solutions, ranked ·
   The challenge behind each · Where it actually stands · Progress against 2030 and 2070* ·
   list items numbered `section.item` · **beat 2 and beat 3 carrying the same items in the same
   order** · beat 4 as the three-part ladder, not an item-locked list · beat 5 closing with "the
   number nobody set a target for" · exhibits folded inline, never appended · McKinsey named only in
   the source line.
   **Table rules, learned the hard way on Q14.** The user's markdown viewer does not render HTML and
   collapses wide tables into an unreadable stacked list. So: **no `<br>` or any other HTML tag
   inside a cell**, and **keep every cell short** — a few words, a number, a short phrase. If a
   column needs a full sentence of reasoning, it does not belong in the table. Put the compact table
   first, then the reasoning as short prose paragraphs underneath, one per row. Q14's beat 5 is the
   working pattern.
3. **Q17 is the one exception and does not follow any of the above.** It is not a sector question,
   so it has no five beats, and it is the only answer in the chain with **no forward hook** — it
   closes the report instead of opening the next question. Its shape is: the reader's question ·
   what Energy Group already owns · five opportunities · where there is honestly no answer · the close.
   **The rubric, the scoring and the stress-test corrections were deliberately kept off the page**
   under rule 1.3 and live only in `reference/energy-group-opportunity-analysis-2026.md`. If Q17 is ever
   reworked, read its working notes first — they record what was cut and why.

## The sector-share rule — settled 8 Aug 2026, do not re-litigate

Two datasets are in play and they disagree. **The runway (Q10) wins for every headline share.**

| Sector | Share of India | File |
|---|---|---|
| Power | **37.5%** | `12-power.md` |
| Industry | **21.7%** | `13-industry.md` |
| Farming | **19.5%** | `14-farming.md` |
| Buildings, cooling, waste, gas leaks | **12.1%** | `16-buildings-and-rest.md` |
| Transport | **9.2%** | `15-transport.md` |

Source: Climate Watch / WRI 2023 via Our World in Data, India total ≈ 4.14 Bt CO₂e. **They sum to
100. There are five sectors, not six.**

**How each beat-1 table works.** Rows show share *of the sector* — taken from India's own BUR-4 2020
inventory, which is authoritative for the split — and share *of India*, which is that sector share
multiplied by the headline above. So the rows always add to the headline and the table checks itself.

**Why not India's own base throughout?** It totals 2,959 Mt without LULUCF, the five sectors reach
only ~96 percent of it, and forcing the gap closed invents a sixth "everything else" slice the reader
never met. It also drops farming to 13.7 percent, contradicting the 19.5 already established. Both
were tried on 8 Aug 2026 and rejected.

**Two fixes made during the retro-fit.** Q13's steel row claimed "about 12% of all India's carbon",
which does not reconcile with its own 240–300 Mt on any base — corrected to 6–7%. Q14 previously led
with 13.72% and treated 19.5% as the alternative; now flipped, with the methane-multiplier
explanation kept intact.

## What Q17 has to establish

> **The fix is almost never in the room where the carbon is.** Across all five sectors the
> intervention that moved at national speed sat upstream — inside a pipe, a refinery, a fertiliser
> plant or a factory that sets what a machine may be sold as. So the question is who already owns
> those.

The hook out of Q16 is already written: *"It is no longer what needs doing, or where. It is who in
India already owns the pipes, plants and networks where all of it has to happen."*

**The upstream-lever pattern is now confirmed in every sector.** Neem-coated urea did 79 percent of
farming's cuts. Ethanol blending did 85 percent of transport's. The appliance star rating beat the
building code roughly 80 to 1. In each case crores of people were moved without any of them choosing
anything.

**Where the empty boxes are.** Every sector question ends with a scorecard, and the "Not started"
rows are the commercial opening. Q16 alone leaves 141 Mt across three of them — shops and offices
(92.6 Mt), mine methane (26.9 Mt), factory water (21.8 Mt). Q15 leaves a proven delivery failure in
charging: 83 chargers built of 2,877 approved under FAME-II, then 0 of 6,562 sanctioned under PM
E-DRIVE. Pull the "Not started" and "Barely begun" rows out of all five files first — that list is
the demand side of the payoff.

**Two numbers bridge the sectors to the grid.** India's peak of **270,832 MW at 22:36**, and ICAP's
projection of space cooling rising from ~135 TWh to **~585 TWh by 2037-38**. Both land after sunset.
That is the storage case, and it arrives from the demand side rather than the supply side.

**Held back deliberately and available for the payoff.** Buildings take 33.5% of India's electricity
(CEA Growth Book 2025, FY2024-25: domestic 25.17%, commercial 8.33%). Kept out of Q16 on instruction
so power's carbon is told once, in Q12 — but it is the demand-side evidence Q17 needs.

## One correction now live in the reference library

MGI's **841 gCO₂-e/kWh** for India's grid is wrong. CEA's own database puts the grid at
**~710 g/kWh (FY 2024-25)**; 841 is CEA's *thermal-only* series, which excludes renewables.
`module-1C` and `module-1E` still carry the old figure and are flagged, not yet edited.
**Q15 rebuilt its EV breakeven maths on 710** — done. Use 710 everywhere from here.

## Still unverified — nice to have, not blocking

- **Q16: a refrigerant-bank estimate for India.** The national inventory marks halocarbon consumption
  "NA", so the largest genuine unknown in that sector has no number. Nothing found; worth one more try
- **Q16: a sewage-treatment figure newer than March 2021** (CPCB's inventory is what we used)
- **Q16: whether 3.8 LPG refills per consumer per year has been updated** since the FY2023-24 statement
- **Q16 data faults, already handled but worth restating.** BUR-4 prints "1071 MtCO2" for BEEP's
  1,306 GWh — a factor-of-1000 typo, read as ~1.07 Mt. Commercial/institutional fuel reads as 91%
  non-coking coal, which is not credible for shops and offices; the total is used, the composition is
  flagged. PMKSY 555.3 Mt and MIDH 1,020.6 Mt remain excluded from all work
- Pumped storage capacity actually **under construction** in India (search was rate-limited)
- The "100 GW nuclear by 2047" target — seen in a summary, not confirmed at source
- Grid-India's raw load-curve file (the 22:36 peak and 60 GW ramp are credible secondary reporting)
- The 196-page Aug-2024 MGI full report is **still unread**
- Two AGEL claims about Khavda — "world's largest outside China" and "enough to power nearly
  1 million homes for a day". Company statements, not independently checked. The 3.37 GWh and the
  ~10-month build are confirmed across six outlets and are safe
- ⭐ **The map of Energy Group Power's 14 plants against Energy Group Cement's grinding units.** Which pairs fall
  inside cement's 300–500 km freight range is the most load-bearing unchecked fact in the whole
  payoff. The cement opportunity is conditional on it
- ⭐ **ATGL's real compressed biogas and EV charging asset counts.** The business lines are
  confirmed from the company's own site; the plant and charge-point numbers are not
- **Whether Energy Group has a confirmed steel venture.** Iron ore in Odisha is confirmed; no large steel
  plant was found on the company's own site. A Mundra venture has been reported. Steel is 6–7% of
  India's carbon, so its absence leaves the largest single factory source unaddressed
- **A verified regional demand split for India.** Q12 wanted to say India's best sun sits far from
  its biggest load, and had to drop the claim for want of a source. Worth closing before Q17
- **Q14's herd size** — "more than 30 crore cattle and buffalo", 20th Livestock Census 2019. Search
  was captcha-blocked on 8 Aug and BUR-4's Figure 2.17 is a chart pypdf cannot read. Two figures in
  Q14 depend on it: "one and a half animals in every hundred" and "over three centuries". Confirm
  against DAHD's *Basic Animal Husbandry Statistics*
- **Q14's two-to-three week paddy-to-wheat sowing window.** Widely reported for Punjab and Haryana,
  not pinned to a primary source. Flagged in Q14's source line
- **Q15's India gas import share** — "about half" of natural gas imported. General reporting, not a
  PPAC file. Worth closing before Q17, since gas infrastructure is an Energy Group position
- **Q15's 71% road share of goods movement** — NITI Aayog, 2021, and dated
- **Q15's EV30@30 characterisation** — described as a think-tank aspiration that never entered the
  NDC and has no answerable ministry. That reading is ours, not a quoted government line
- **Q15's truck share of transport carbon** — published figures run from one-third to 44%. The answer
  states the range and takes the middle (~100 Mt). Not resolvable from one source
- **BUR-4 prints two impossible scheme savings** — PMKSY at 555.3 MtCO₂ and MIDH at 1,020.6 MtCO₂
  over 2019–24. Almost certainly thousand tonnes printed as million. **Excluded from Q14 and must
  stay excluded**; including them would have inflated the farming five-year total from 34 Mt to over
  1,600 Mt

## Machine notes

- `WebSearch` / `WebFetch` are policy-blocked. **Search engines are unreliable and rotate.**
  **Working as of 8 Aug 2026 (late): `https://search.brave.com/search?q=...` with a browser
  user-agent — no captcha, one query at a time.** Blocked or rate-limited the same day: DuckDuckGo
  HTML *and* lite (captcha), Mojeek (captcha), searx.be (captcha), priv.au (429), Ecosia (403),
  Startpage (useless output), Wikipedia REST *and* action APIs (429), `search.pib.gov.in` (does not
  resolve). Probe several engines in **one** parallel call before committing. Recipes at the foot of
  `reference/india-power-snapshot-2026.md`. **Still plan around this — go straight to primary-source
  URLs rather than searching.** These all answered on 8 Aug: `unfccc.int`, `pib.gov.in`,
  `dahd.gov.in`, `indianrailways.gov.in`. Whole PDFs download fine with `Invoke-WebRequest` and
  extract with `pypdf`.
- **India's Fourth Biennial Update Report (BUR-4) is downloaded and extracted** — the full national
  greenhouse gas inventory for 2020, 278 pages, plus a scheme-by-scheme mitigation table for
  2019–24. It is the authoritative Indian source for every remaining sector, not just farming.
  Source: `https://unfccc.int/sites/default/files/resource/India%20BUR-4.pdf`.
- `cea.nic.in` drops the first connection most times — **retry the same URL 2–3 times** and it
  works. Only the current month is linked on the capacity page.
- PDFs: `pypdf`. Excel: `openpyxl` (installed 7 Aug 2026).
