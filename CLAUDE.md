# Dual-GPU AI Workstation (pcsetup)

**What it is:** A single self-contained HTML build-plan document (case / cooling / power / desk-clearance) for Dominic's in-house 24×7 dual-GPU AI training workstation.
**Status:** **Rev 7 — USER PICKED THE O11 DYNAMIC EVO XL. GO-WITH-CONDITIONS after an 8-agent adversarial pre-purchase recheck (2026-07-25). index.html REBUILT around the EVO XL. Pre-purchase gate lives at `buy-checklist.html`.** Case comparison at `case-replacement.html`. **index.html is DONE (Rev 6/7). `layout.html` + `simple.html` + `build-picture.png` are STILL V3000 drawings and carry the 140mm rear-fan error — they need a from-scratch redraw for the EVO XL and must NOT be handed to a builder until then.**

**(Superseded) Rev 5 — WINNER = Lian Li V3000 Plus.** (2026-07-14) Ergosphere CONFIRMED a firmware min/max-height lock that can be set as default AND **survives a reset** → the crush problem is solved robustly. Combined with the user's 32" seated working height + a wheeled open-frame pedestal, the 674mm super-tower now fits under the desk. So the ≤560mm cap is REPLACED by the desk-lock approach. V3000 is the pick; EVO XL demoted to "foolproof fallback". Full doc rebuilt around the V3000 (new fan/rad layout, desk-lock section, pedestal, shopping list).
(Rev 4: super-towers eliminated on height + hotbox section + 1.8-ton O General. Rev 3: EVO XL after 5090=Astral LC. Rev 2: reopened after PRO 6000 = double-flow-through.)

## Live assets
- **Repo:** `opheliaclarke/pcsetup` (PUBLIC — user approved public visibility for Pages). Collaborators SilentAurora245 + mary3862jon added.
- **Pages:** https://opheliaclarke.github.io/pcsetup/ — verified HTTP 200.
- **Visual diagram:** https://opheliaclarke.github.io/pcsetup/layout.html — REALISTIC both-sides cutaway (user asked for both sides + more realism, 2026-07-14): Panel 1 BUILD side (cards/rads/fans/liquid-loops/motherboard, numbered 1-8), Panel 2 CABLE side (PSU/wiring/SSDs/hub, lettered a-e), Panel 3 under-the-desk context. Hand-authored SVGs with a reusable `#fan` symbol (blades), rad fins, colour-coded airflow. Linked from index.html. Editing tip: re-render with `google-chrome --headless=new --screenshot` + Read the PNG to visually verify after any edit (watch for label/arrow overlaps).
- **Plain-English version:** https://opheliaclarke.github.io/pcsetup/simple.html — the whole build in simple, non-technical words (user is non-technical, needs to explain to the assembler; 2026-07-14). Simplified plain-label diagram + "tell the builder" rule box + where-each-part-goes table. Linked from index.html + layout.html.
- **Downloadable picture:** https://opheliaclarke.github.io/pcsetup/build-picture.png — a clean PNG of the simple diagram (rendered from simple.html's SVG via headless Chrome + `convert -trim`), for print/WhatsApp/Canva-import. Regenerate: extract the SVG → minimal wrapper → chrome --screenshot → `convert -trim`.
- **CANNOT use Canva / no AI image-gen tool.** Images = hand-authored SVG → rendered to PNG. Told user not to share Canva login (can't use it + security). Layout verified against Lian Li's official V3000 interior diagram (v3k_plus_017-1.png) — matches (top/front/above-PSU-shelf/floor rad+fan positions).
- All pages carry `<meta robots noindex>`.
- SEPARATE related projects (NOT this folder): AC buying guide at https://opheliaclarke.github.io/ac-guide/ · desk research at https://opheliaclarke.github.io/standing-desk-india/

## Key facts
- **Rig (locked):** Ryzen 9 9950X3D · MSI X870E Carbon WiFi · 64GB DDR5 · GPU1 RTX PRO 6000 Blackwell 96GB (600W) · GPU2 RTX 5090 (AIO liquid, ~575W) · Corsair AX1600i · DeepCool LT720 360 AIO · ~1.4–1.45 kW peak.
- **Desk (constraint):** Ergosphere Balanced Desk PRO 340 L-Shape Corner, triple-motor, LOGICDATA/Bosch, **frame-only**. Published "63cm min" is to the DESKTOP TOP; the **underside bottoms out at ~605–615mm**. The PC goes UNDER it. **Rev 7 caveat: 605mm is the TABLETOP UNDERSIDE — the control box (~37mm) and crossbar hang BELOW it, and this has never been physically measured. Measure floor → lowest hard point with the bay empty before trusting any clearance number.**
- **USER'S WORKING DESK HEIGHT = 32 inches (813mm) surface** (chair at lowest, seated). Confirmed 2026-07-13. This is HIGH (std is 29"), which is GREAT for fit: at 32" the underside ≈ 788mm (25mm top) → clears even the 674mm V3000 Plus by ~114mm. So at working height BOTH cases fit easily. The only risk is the desk DROPPING below 32" toward its ~605mm-underside minimum.
- **CRUSH-SAFETY BY CASE (desk min underside ~605-615mm):** EVO XL (532mm) is SHORTER than the desk's lowest point → 73-83mm gap even at rock-bottom → CANNOT be crushed, needs NO limit (foolproof). V3000 Plus (674mm) is TALLER than the desk minimum → crushed by ~69mm if desk hits its min → REQUIRES a descent-cap (Ergosphere firmware limit at ~29.5-30" surface / ~724mm underside + physical steel hard-stops as backup). V3000 is now VIABLE (not dead) BECAUSE the user sits at 32".
- **WHEELED PEDESTAL PLAN (user idea, good):** put the V3000 on a 1-2" open-frame caster base so it rolls out for cleaning + lifts the bottom intake off floor dust/carpet. TWO rules: (1) pedestal height STACKS onto the 674mm case → raise the desk lock to match: 1" pedestal → lock ~30.5" surface, 2" → ~31.5" (user works at 32", so headroom exists). (2) Pedestal MUST be an OPEN frame (casters at corners, open middle), NEVER a solid board — a solid plate would seal the bottom intake and choke the flow-through 6000. Locking casters rated >50kg. V3000 has a built-in bottom dust filter already (no extra mesh needed; keep it clean — it's the 6000's air path). Feed = floor fans + "above-PSU" shelf fans (two-stage, straight up into the GPU).
- ~~V3000 Plus available offline~~ **STALE — user reported it unavailable again 2026-07-25 and it is now permanently out. See Rev 6/Rev 7.**
- **5090 CONFIRMED = ASUS ROG Astral LC** (user-stated). Verified specs: card 288.46×153.7×48mm (2.5-slot), radiator 400×120×**65mm with fans** (38mm bare core — THICKER than typical 5090 AIOs ~27mm), 600mm flexible tubes, 600W, 1×16-pin. India: sold ~₹5.25–7.4 lakh but mostly OOS/scarce at readable retailers. Roof-mount is the RECOMMENDED orientation (pump on card → rad above). The fat 65mm rad is the clearance to watch.

## THE BIG CORRECTION (Rev 1 was wrong — do not regress)
- **The RTX PRO 6000 Blackwell WS is NOT a rear-exhaust blower.** NVIDIA's datasheet: **double-flow-through** — draws air from BENEATH the card, vents UP into the case. All 600W stays in the chassis. Only the **300W Max-Q** is a blower. Rev 1's "exhausts out the back — a good citizen" was the load-bearing error under the whole case choice.
- Every liquid RTX 5090 is **2.5-slot** (not 2). The PRO 6000 is 2-slot but **extended height: 137mm** (vs standard 112mm).
- **PCI_E2 is PCIe 5.0 ×4** (not Gen4 ×4). Populating it drops PCI_E1 from ×16 to **PCIe 5.0 ×8**. No M.2/SATA lost. Slots are **4 pitches apart** (~81mm centres).

## Decisions made
- **CASE WINNER (Rev 3): Lian Li O11 Dynamic EVO XL** — ₹22,995 black, IN STOCK (Computech; also MD/PC Studio/Vedant/Amazon.in). **531.9mm tall** (28mm under the 560 cap). Chosen over the Flux Pro because: (a) user wants ROOM and felt the Flux Pro too small/tight; (b) 304mm WIDE + separate PSU chamber = wide-open main chamber for 2 cards + 2 rads; (c) roof takes an **81mm rad stack** so the Astral LC's fat 65mm rad drops in easy; (d) it STILL feeds the flow-through PRO 6000 via **3× 140mm FLOOR intake fans** (GN-verified effective — the card ingests from below, so floor intake is the correct direction). CONFIG: **Top** = 5090 Astral LC rad (exhaust) · **Side** = LT720 CPU rad (intake, needs the Lian Li MESH SIDE PANEL to breathe — GPU floor path needs nothing) · **Floor** = 3× 140mm fresh-air fans (feed the 6000) · PRO 6000 LOWER slot, 5090 TOP slot. Cons: needs mesh kit (cheap, confirm SKU/price); ~₹2k pricier than Flux Pro. **"Hotbox" reputation does NOT apply** — that's for front-fed air cards; a bottom-ingesting flow-through card sidesteps the glass-front weakness (this reverses my earlier 'avoid EVO XL' call).
- **CASE #2: Antec FLUX PRO** — ₹20,865 black, IN STOCK, Antec India store (MRP ₹25,999). Most DIRECT flow-through feed (shroud fans right under the lower GPU, GN chart-topper) but **245mm wide = tightest build** (the "feels small"); iShift PSU caps 180mm (use conventional bracket for 200mm AX1600i). Pick only if maximum cooling > room. **545mm tall with feet** (523mm without — Noctua publishes both; 70.77 L volume cross-checks). 8 slots; 455mm GPU-LENGTH limit vs 304mm card = huge margin. GPU HEIGHT/thickness clearance is UNPUBLISHED anywhere (Antec/Noctua/every reviewer — verification agent confirmed the spec field doesn't exist); the 137mm extended-height PRO 6000 is a measure-on-arrival, but a TALLER 150mm MSI RTX 5090 SUPRIM is spec'd into this case in the wild, so height is a non-issue in practice. Wins on the **PSU-shroud fan bank** that blows floor-ambient air straight UP into the GPU's underside — exactly what a flow-through card needs. GamersNexus noise-normalised thermal chart leader.
  - **PSU gotcha:** iShift 90° side mount caps at 180mm. The 200mm AX1600i needs the **conventional PSU bracket** + drive cage removed.
- **CASE #3: Corsair 6500D Airflow** — ~₹17,000, 496mm, cheapest/roomy dual-chamber BUT front⇄floor rad mounts OVERLAP: floor must hold GPU intake fans, so you can't also run a front rad → both rads forced to roof+side, and a 65mm rad in a mid-tower roof risks fouling the ATX board top. The cramped puzzle to avoid.
- **FAN/RAD LAYOUT (this is the performance):** LT720 360 → **FRONT, intake** (CPU only ~200W, +2–3°C). 5090's 360 AIO → **ROOF, exhaust**. **3× 120mm in the PSU shroud, pure intake, no rad** → feeds the PRO 6000. Rear → exhaust. **NEVER a radiator upstream of the PRO 6000** (GN measured 7–9°C penalty).
- **SLOT ORDER (important, corrected — was backwards in first draft):** **PRO 6000 in the LOWER slot PCI_E2** (sits over the shroud fans → fresh-air feed for the flow-through card) = **Gen5 ×4**; **5090 in the TOP slot PCI_E1** = **Gen5 ×8**. The ×4 is negligible for a 96GB card that keeps its job in VRAM; feeding the 600W air-cooled card 24/7 beats the bandwidth. This is the OPPOSITE of the "big card up top" habit, and it's correct here because the shroud fan bank is the whole reason for this case. Only keep the PRO 6000 up top (×8) if its jobs stream heavily from system RAM / NVMe offload — then feed it with a side intake fan instead. Both slots are CPU-direct.
- **DROP the vertical GPU kit AND the riser.** Cards seat natively 4 pitches apart (~40mm clear air). Vertical-mounting the PRO 6000 would face its intake into glass and choke it. (Lian Li VG4-4 V2 also isn't buyable in India — grey import at ~2.3× MSRP.) Saves ~₹15k and cools better. A plain GPU support stick is enough for a 2-slot card.
- **Fan-curve daemon is MANDATORY.** Stock NVIDIA VBIOS sits at ~30% fan at 85–90°C. Power-limited PRO 6000 under sustained LLM load: **85°C stock / 75–79°C at 80% / 66–67°C at 100%.** Use LACT or a pynvml daemon.
- **Angled 12V-2×6 adapter required** — the PRO 6000's connector is on the top middle edge.
- **DESK:** container stop at **700mm** (LOGICDATA: hold **"S" 10 s**, two clicks) + **2× steel hard-stop posts rated >2500N**. Gives 155mm air above the 545mm case; desk surface still 725mm. **Never reset the desk with the PC underneath** — reset drives BELOW the programmed limit and DISABLES anti-collision.
- Power-limit both GPUs ~80% on day one. Dedicated 16A circuit. ~3kVA online UPS.
- **AC = 1.8-ton O General inverter (user's chosen unit, GOOD pick).** Load math: room ~1.5 ton + PC ~0.4 ton = ~1.9 ton at full tilt (a hair over the unit's ~1.83-ton rating); the day-one ~80% power-limit drops total to ~1.83 ton = right at capacity. So 1.8-ton is adequate BECAUSE we power-limit (which we do anyway). O General = excellent 24×7/tropical-compressor brand. (Was 2-ton generic; now matched to their unit.)
- **UNDER-DESK HOTBOX = NOT A RISK (researched, §7 in doc).** Hotbox happens in CLOSED cubbies, not open L-corners. Floor-intake + top-exhaust is the RECOMMENDED under-desk layout: intake (cool floor air) and exhaust (top) are ~53cm apart → no short-circuit; ~168mm air gap above lets the plume spread. Do: keep L-corner sides open, desk off wall, aim exhaust at the AC return, sit upstream, case on a hard riser off carpet, keep floor filter clean. Optional clip fan as insurance.

## Dead ends — do NOT redo
- **Corsair 9000D: DEAD.** 664mm — 104mm taller than the desk's lowest point. (Good case otherwise; the only documented dual-PRO-6000 build uses it. Just cannot go under this desk.)
- **Lian Li V3000 Plus: DEAD.** 674mm (114mm over the 560 cap) — super-tower, won't fit under desk. Also OUT OF STOCK everywhere in India (EOL). Would've been near-ideal for the parts (filtered floor-intake + shroud fans straight up into the flow-through 6000, 8 slots, holds both rads). Height kills it.
- **ASUS ROG Hyperion GR701: DEAD.** ~659mm (verify: ASUS unlabeled "268×639×659"), ~100mm over. TWO fails: too tall AND no floor fan mount (solid PSU cover under card) → can't feed the flow-through 6000. In stock India ~₹39k but wrong case. Don't reconsider.
- **PC-BESIDE-DESK is OFF THE TABLE** (user 2026-07-13: wire problems + wastes the 6ft desk span). Under-desk is mandatory → never suggest a taller case by offering "put it beside instead".
- **Lian Li O11 EVO XL: was flagged DEAD in Rev 2, REINSTATED as WINNER in Rev 3.** The "hotbox" reputation is real ONLY for front-fed conventional air cards starved by the glass front. A bottom-ingesting flow-through card (PRO 6000) is fed from the FLOOR, so the glass front is irrelevant; run the top rad as exhaust and it breathes fine. Needs the mesh SIDE panel for the CPU rad only. Do NOT re-disqualify it on the generic hotbox reasoning.
- **Fractal Torrent: DEAD.** No top radiator mount at all (spec sheet confirms). Needs two rads.
- **Fractal North XL: DEAD.** "Bottom radiator: N/A", no floor fan mount → nothing feeds the PRO 6000 from below.
- **Phanteks NV7/NV9/Enthoo Pro 2 + Lian Li Lancool III: DEAD on availability** — out of stock at every Indian retailer.
- Do NOT merge both cards into one ~128GB trainer (no NVLink, mismatched VRAM/clocks). Two independent workers.
- Do NOT rely on the desk's anti-collision — LOGICDATA trips at ~40kg + desk load downward, and is OFF during reset.


## Rev 7 — pre-purchase recheck of the EVO XL (2026-07-25). READ THIS BEFORE TOUCHING THE CASE PLAN.

Bob picked the EVO XL and asked for a full recheck before buying. 8-agent adversarial workflow (7 lenses + go/no-go).
**Verdict: GO WITH CONDITIONS. No showstoppers.** Deliverable: `buy-checklist.html`.

**FOUR THINGS I HAD WRONG — do not regress to any of them:**
1. **THE "MESH SIDE PANEL BLOCKER" WAS A FALSE PREMISE.** Lian Li makes NO mesh side panel for the EVO XL because it
   does not need one — **top and right panels are aluminium fine mesh from the factory, 4 dust filters included.**
   Proof: Lian Li's own side-bracket figures (81mm main chamber / 40mm second chamber, 117.2mm outer) only reconcile
   if the fans blow across the case WIDTH through the side panel; two agents independently parsed Lian Li's 78MB CATIA
   STEP model and landed on the same geometry to ~1mm; Lian Li ships 2 side dust filters; GamersNexus benchmarked this
   case in a side-intake config. **DO NOT BUY any mesh kit** (esp. not the O11D EVO XL *Front* Mesh Kit O11DEXL-4X, and
   not any O11D EVO / EVO RGB kit — wrong case, widely stocked in India, the most likely money-wasting mistake).
   Residual unknown: manual p.13 captions two of four bracket styles "fans install toward the front panel" — unexplained,
   overruled on stronger evidence. Fallback is free (pull the clip-mounted front glass + ₹500–1,500 magnetic filter).
2. **Roof is 82mm, not 81mm** — and 81mm was the SIDE bracket figure misattributed. Roof and floor share a fixed
   **172mm budget split by tray position (manual p.28): Middle 82/90 (factory default, USE THIS), Low 118/54, Top 46/126.**
   The "118mm" seen elsewhere is real but is a mutually exclusive tray mode. Astral 65mm rad → 17mm spare in Middle.
3. **Rear fan is 120mm, NOT 140mm** — there is no 140mm rear mount ("Rear: up to 2×120mm"). The 2nd rear fan needs Low
   mode, which costs 36mm of floor plenum → use ONE 120mm.
4. **"Crush risk eliminated by geometry" is CONDITIONAL.** 605mm is the TABLETOP UNDERSIDE. The **control box hangs below
   it** (LOGICDATA COMPACT ~37mm deep → 48mm becomes 11mm on a 1" pedestal, COLLISION on 2"), crossbar depth unpublished,
   and "1 inch pedestal" = frame only; casters run 40–70mm plate-to-floor. **Measure floor → lowest hard point with the
   bay empty. Never a 2" pedestal.**

**KEY VERIFIED NUMBERS:** floor plenum **99–120mm** (CAD-derived; vs Antec C8's 62.8mm — the EVO XL's advantage is now
measured, not assumed) · GPU height clearance **169mm published** (PRO 6000 137mm → 32mm spare; Astral 153.7mm → **15.3mm**,
tightest in the build) · 531.9mm **includes feet** (CAD: pads at Y−39.4, top cover Y+492.0 = 531.4 vs published 531.9) ·
real depth **537mm** not 522 (PCI brackets 15mm past the published rear plane) → keep ≥100mm off the wall · slot pitch
20.33mm CAD-measured.

**SKU DISCIPLINE:** buy **O11DEXL-X** / code **G99.O11DEXL-X.IN**, BLACK. There is NO separate "EVO XL ARGB" product (base
case has the ARGB strip; listings titled ARGB print the standard SKU). **Near-miss to avoid: O11 Dynamic EVO RGB
(O11DERGBX)** — different MID-TOWER, 478×290×471, 7 slots, ₹17,990. Prices: ₹23,200 vishalperipherals · ₹25,000 MD Computers
(buy here if warranty path unresolved) · ₹24,990 pcstudio · ₹24,998 elitehubs · tpstech SOLD OUT · **amazon.in does NOT sell
this case** (old note saying it does is wrong). Box contains **ZERO fans**; GB-003 anti-sag IS included but only fits the
2nd expansion slot (useless for the PRO 6000 → buy a support stick); 2 seal plates included — FIT THEM or the side intake
short-circuits. All-in ₹29,400–31,200.

**LAYOUT LOCKED:** tray MIDDLE · ROOF = Astral 65mm rad EXHAUST (17mm spare, route BOTH EPS cables first) · SIDE = LT720
INTAKE, bracket INNER (29mm spare) · FLOOR = 3×140mm INTAKE pushed fully **REARWARD** (centred, one fan blows past the
card's nose into empty air) · REAR = 1×120mm exhaust · PRO 6000 lower slot / Astral top slot.
**Do NOT swap the rads:** only one rad can breathe outside air; making the Astral the intake dumps 600W into the chamber
the PRO 6000 breathes (600W→1200W case load). Swap is the FALLBACK only if the LT720's tubes don't reach from the side bay.

**THE REAL TOP RISK IS NOT THE CASE — it's the PRO 6000's stock fan firmware:** documented holding ~53% fan at 92°C then
dropping the card off the PCIe bus; power-limiting to 500W and 450W did NOT prevent it (Tyler Wall, 95k NVML samples;
corroborated by Ovidiu Dan's dual-PRO-6000 report). Fan daemon is a PREREQUISITE. Curve: ≤40°C→30%, 50→55%, 55→75%,
60→90%, ≥65→100%. Alarm on **core >85°C while fan <70%**.

**STILL UNKNOWN (flagged, not hidden):** where the Astral's power connector + coolant tubes exit (ASUS publishes nothing;
15.3mm is the tightest clearance in the build) · whether a 90° 12V-2x6 adapter exists thin enough for 15.3mm · NVIDIA
publishes NO thermal spec for the PRO 6000 · **nobody has ever documented a PRO 6000 in any O11-family case** (temp
projection 80–88°C core / 86–95°C memory is stitched, MEDIUM confidence ±5°C; memory is the binding constraint) · Lian Li
publishes no case weight and no ventilation clearance · Ergosphere's "63–128cm" block is boilerplate, not a spec for this
desk · Lian Li India after-sales = one phone line, "Abhijeet Singh 7042202227", no address/email/portal.

**DEVIL'S ADVOCATE LANDED ONE HIT:** "already documented for the assembler" was worth ZERO and is struck — layout.html,
simple.html and build-picture.png were all drawn for the V3000 Plus and carry the 140mm rear-fan error. **DO NOT hand them
to a builder.** They need a from-scratch redraw for the EVO XL — still outstanding.

**Switch to the Antec C8 only if ALL THREE:** Antec confirms in writing the side bay takes 65mm (100mm figure, not the
contradictory 50mm), AND confirms GPU height clearance ≥170mm, AND C4 comes back badly. Two of those nobody has ever asked
Antec. Performance 1 FT is dead on availability.

## Rev 6 — V3000 replacement research (2026-07-25)

**Deliverable:** `case-replacement.html` → https://opheliaclarke.github.io/pcsetup/case-replacement.html (noindex, favicon added; index.html also got a favicon + a red SUPERSEDED banner).

**Method:** 16-agent workflow (5 discovery sweeps → 63 unique candidates → 7 spec-verified → adversarial kill) then a 5-agent verification workflow (4 refuters + 1 completeness critic). Heights measured off manufacturer manual drawings at 600 dpi, calibrated on ATX PCIe pitch (20.32mm).

**RANKING — only 3 qualify:**
1. **HOLD Lian Li O11 Dynamic EVO XL (531.9mm)** — deepest plenum under the flow-through card + height-adjustable mobo tray, 65mm Astral rad goes in the ROOF conventionally, 304mm wide, broadest India stock, already documented for the assembler. ₹24,998 ARGB black IN STOCK at elitehubs (verified live 2026-07-25); ARGB white OOS.
2. **Antec C8 plain black (476mm, ₹9,599 antecindia.in, verified live)** — 56mm shorter, ₹15k cheaper, mesh top+right panels INCLUDED, 3× simultaneous 360 mounts, 8 slots, 303mm wide, full floor cut-out + pull-out filter. ~₹14,067 all-in (+ Arctic P14 ×5 ₹3,469, Antec I-Shape holder ₹999).
3. **Antec Performance 1 FT (522mm)** — BEST feed mechanism (3×120 on a perforated PSU shroud blowing straight up into the card = the V3000's two-stage feed), roof takes the 65mm rad offset beside the board, PSU bay 245mm. Killed to #3 by **230mm width** (narrower than the 245mm Flux Pro the user already rejected as too tight). OOS at elitehubs (₹13,595 plain / ₹16,550 ARGB); Computech ₹16,099 reported in stock.

**BIG CORRECTION — do not regress:** the first pass ranked the C8 **#1** on a claimed "~110mm floor plenum". An adversarial verifier measured Antec's own drawings: internal floor → bottom edge of mobo is only **62.8mm**, floor → lowest slot centre **47.0mm**, so the real plenum is **52.5mm** at 4 pitches down (73mm absolute best at 3 pitches). That is what demoted the C8 to #2. The C8 still physically fits everything.

**ALL THREE ARE ≤560mm → the Ergosphere desk firmware lock is NO LONGER LOAD-BEARING.** Gap at the desk's ~605mm minimum underside: C8 129mm bare / 78mm on a 2" pedestal; P1 FT 83/32; EVO XL 73/22. Crush risk gone by geometry alone.

**Rev 6 dead ends (verified, do NOT redo):** Corsair 9000D (re-opened on the new height cap, re-killed on floor feed) · Phanteks NV9/NV9 MkII (not buyable in India — Amazon.in "don't know when or if") · Enthoo Pro 2 (OOS ×9 listings, and it is **580mm** with feet, not 560) · Thermaltake CTE C750/C750 Air (rotated layout stands cards vertically → no underside for the floor to feed; roof caps at 240) · all Jonsbo (only roof+floor rad positions; floor is reserved) · Fractal Meshify 3 XL / Define 7 XL (no floor feed) · HYTE X50 (no roof mount at all) · **4U rackmount category closed** (SilverStone RM44 = front 360 only) · **open-frame category closed** (CM MasterFrame 700 ~702mm, unfiltered, OOS) · **2026 releases checked and empty** (Lancool 4, 207XL, V2000, O11D EVO RGB V2 — announced, not shipping, not in India) · **Indian domestic brands structurally absent** (Ant Esports flagship = 220mm wide, single 120mm bottom mount) · Lian Li O11 Dynamic XL ROG (513mm, 285mm, ₹19,299 — genuine find but Lian Li publishes NO rad thickness limit for it, builders report top+side interference, OOS at elitehubs).

**BLOCKED ON THE USER:** pick one of the three. Then rewrite index.html + layout.html + simple.html around it (Rev 6 proper).

**Rev 6 open items:**
- ~~EVO XL mesh side panel~~ **CLOSED 2026-07-25 — false premise, no such part exists and none is needed. See Rev 7.**
- C8: Antec publishes **two contradictory side-radiator numbers** — a 100mm thickness envelope (55+45 about a rail) and a separate "Clearance for Right Side Radiator Installation: 50mm (Depth max.)", no datum given for either. The 65mm Astral rad depends on which is real → ask Antec India in writing.
- C8: roof envelope is 70mm vs the Astral's 65mm (5mm) → the fat rad must go SIDE, LT720 in the roof.
- C8: PSU bay 210mm **excluding cable** vs the 200mm AX1600i → needs a 90°/short cable kit.
- C8 stock is thin: 2 sellers with plain black (antecindia.in, varietyinfotech.com), 3 already sold out (Computech/TheITDepot/Vishal). Buy early.
- P1 FT roof clearance is **measured, not published** (~28mm lateral to the board plane) → low-profile RAM.
- **Retailer access notes:** mdcomputers.in returns HTTP 403 to automated access; computechstore.in's `?s=` search returns the homepage regardless of query (its rows in the doc are agent-reported, not re-verifiable from here); elitehubs + antecindia are readable via headful Chrome (Playwright, channel="chrome").

## Open / next
- Confirm the exact Lian Li EVO XL mesh side-panel SKU + India price at purchase (needed for the CPU rad to breathe).
- ROG Astral LC is scarce/OOS in India — check live stock before committing the rest of the build.
- Read the label on the desk control box: **LOGICDATA or JieCang** — the container-stop procedure differs.
- Monitor motherboard VRM/PCIe temps, not just GPU temps. Documented failure mode: PCIe retimers hit 90°C and crash the fabric while the GPUs read "fine".
