# Dual-GPU AI Workstation (pcsetup)

**What it is:** A single self-contained HTML build-plan document (case / cooling / power / desk-clearance) for Dominic's in-house 24×7 dual-GPU AI training workstation.
**Status:** **Rev 12 — pedestal now has isometric + side-cutaway 3D views; ready-made trolley link retracted (solid deck), pedestal is build-only; mesh must be COARSE. Rev 11 — `build-guide.html` LIVE (standalone, no interlinking): parts+links, carpenter pedestal drawings in inches, labelled cabinet layout, 26-step install manual. Rev 10 — SLOT FITMENT SETTLED FROM PRIMARY SOURCES: 5090 above / PRO 6000 below = YES. Lian Li's own CAD proves the 8 expansion slots are children of the motherboard-tray assembly (they move WITH the tray), so tray position is irrelevant to card mounting; MSI's own manual proves PCI_E1/PCI_E2 are exactly 4 pitches apart at ATX positions 2 and 6. Cards land on case slots 2+3 and 6+7, ~33 mm clear air between, slot 8 free. One of our own reasons was wrong (the top-edge 12V-2x6 faces the SIDE PANEL, not the card above) — angled connector still mandatory. See Rev 10.** Rev 9 — `buy-checklist.html` is now a SHORT ranked 1-2-3-4 page (Bob found the long docs unusable). Rev 8 — CONFIRMED: BUY THE EVO XL (O11DEXL-X, black), and buy it SOON (EOL signals). 10-agent round-4 sweep incl. Reddit settled the alternatives. `buy-checklist.html` is now THE decision page (downsides + full sourced buy list + alternatives + CAD fitment proof + Reddit digest). Rev 7 — USER PICKED THE O11 DYNAMIC EVO XL. GO-WITH-CONDITIONS after an 8-agent adversarial pre-purchase recheck (2026-07-25). index.html REBUILT around the EVO XL. Pre-purchase gate lives at `buy-checklist.html`.** Case comparison at `case-replacement.html`. **index.html is DONE (Rev 6/7). `layout.html` + `simple.html` + `build-picture.png` are STILL V3000 drawings and carry the 140mm rear-fan error — they need a from-scratch redraw for the EVO XL and must NOT be handed to a builder until then.**

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
- **Angled 12V-2×6 native CABLE required — NEVER an angled ADAPTER** (CableMod angled adapters were CPSC-recalled 2024, 25,300 units / 272 incidents). The PRO 6000's connector is on the top middle edge; ~32 mm to the side panel vs the ~55 mm a straight plug + 35 mm bend radius needs. Target SKU: **Corsair Type-4 90° 12V-2x6, CP-8920348 (Style B, exits DOWN)**.
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







## Rev 12 — 2026-07-26. Pedestal: realistic 3D views (Bob couldn't read the flat drawing).

Bob: *"I want a realistic design layout of the pedestal... I don't understand this 1d or pencil design... i need PHOTO :D"*
**No image-gen tool available** (standing constraint) → built a proper **hand-authored isometric SVG "product render"**
instead: true axonometric projection generated in Python (scale 20 px/in, 0.866/0.5 iso basis), gradient-shaded
top/front/right faces, drop shadow, contact shadow, coarse mesh drawn as projected grid lines, 4 castors with
bracket + wheel + hub drawn in correct painter order (back castors → frame → front castors), callout leaders.
Generator: `/tmp/.../scratchpad/gen_ped.py` — **keep this approach for any future 3D-ish diagram.**

**Three views now in section 3 of `build-guide.html`:** (1) isometric "what it actually looks like",
(2) **side cutaway of the whole stack** floor→castors→frame+mesh→case feet→case filter→floor fans→PRO 6000→5090→
roof rad, with airflow, (3) the original dimensioned workshop drawing kept for the actual cutting.
**First attempt at view 2 was an isometric and FAILED** (case ran off the top of the viewBox, castors drew on top of
the frame due to z-order) — replaced with a 2D side elevation, which reads better anyway. Lesson: isometric is good
for a single low object, bad for a tall object stacked on a short one.

**TWO CORRECTIONS SHIPPED:**
- **The Amazon "SPYLOCK metal CPU trolley" link I gave was WRONG — it has a SOLID DECK**, which is exactly the thing
  that suffocates the flow-through GPU. Bob spotted it. Link removed from the page; pedestal is now
  **build-only (carpenter/fabricator, ~₹800–1,500)**. Do not re-suggest a ready-made trolley — every one found has a
  solid base.
- **Bob pushed back on 13 in wide + "steel frame" (Rev 12b):** 13 in is NOT padding — **the EVO XL is 304 mm = 11.97 in
wide**, so the pedestal is case width + a small margin. Range relaxed to **12.5–13 in**; **never below 12 in** (a 40 kg
tower on a base narrower than itself tips). Depth relaxed to 21.5–22 in. **WOOD IS FINE and the "STEEL FRAME" label on
the render was misleading — fixed.** Spec is now **hardwood (teak/sheesham/sal), 1.5 × 1.5 in section**, corners
half-lap/mortise or butt + steel corner brackets, castor plates on solid timber. **NOT MDF/particle board** (castor
screws pull out, it sags); plywood OK at 18 mm+ but harder to join well. Steel buys nothing here at 40 kg.

**Mesh guidance (Bob's own idea, refined):** yes to mesh across the open middle, but it must be **COARSE
  (expanded metal / grille, ~5–10 mm holes)**, NOT a fine dust mesh. The case already has its own fine dust filter
  directly above; a second fine mesh under it doubles restriction on the card's only air path. Pedestal mesh stops
  **objects**, the case filter stops **dust**.

## Rev 11 — 2026-07-26. `build-guide.html` — the standalone hand-to-the-builder page.

Bob: *"make another webpage with NO INTERLINKING"* + parts & links + accessory list matched exactly to requirement
+ **pedestal design from all sides with dimensions IN INCHES** + **exact labelled cabinet layout ("must be top
notch, even a noob can understand what to place where")** + **a from-scratch install manual** (he is stripping the
TAG Supernova and moving everything into the Lian Li).

**`/root/workspace/pcsetup/build-guide.html` — LIVE, ZERO internal links (verified: 0 relative hrefs).** 5 sections:
what he already owns · what to buy (8 lines w/ live India links) · pedestal drawings · cabinet layout · 26-step manual.

**Pedestal spec (inches, for his carpenter):** outer **22 in deep × 13 in wide**, rails **1.5 in** wide, open middle
**min 19 × 11 in**, total height **1.5 in incl. castors** (never >2 in), **130 lb / 60 kg** rated, 4 locking castors.
Hard rules: **NOTHING crossing the middle** (a solid deck suffocates the flow-through GPU) and **front edge kept
clear** so the dust filter slides out without lifting 40 kg. One-line brief for the carpenter is on the page.

**Diagrams are hand-authored SVG** (per the no-Canva/no-image-gen constraint). Rendered with headless Chrome +
Read-the-PNG to check overlaps — the FIRST attempt had label collisions; fixed by switching the main layout to
**numbered badges 1-6 + a legend table below** instead of inline labels. Reuse that pattern: inline text labels on a
dense diagram WILL collide; badges + table never do.

**Layout drawn:** roof = 5090 rad OUT ① · side = CPU rad IN ② · 5090 top slot ③ · PRO 6000 lower slot ④ ·
3× 140 floor fans IN ⑤ · 120 mm rear OUT ⑥ · plus a second "cable room" diagram (PSU ⑦, SSD trays ⑧, routing ⑨).

**Manual highlights (order matters, don't reorder):** photograph the Supernova before unplugging → **look at the
existing PRO 6000 cable while it's in your hand** (Type 4? 90° or straight? — decides the ₹2,499 purchase) → pull
mobo WITH cooler attached, never unseat the CPU → **tray to MIDDLE first** → floor fans rearward+inboard → PSU +
pre-plug cables → mobo → **EPS cables BEFORE the roof rad** → roof rad → side rad + seal plates → rear fan →
**PRO 6000 FIRST into the lower slot**, then the 5090 → support stick between two floor fans → power (each GPU on
its own cable, click check) → tidy, GPU cables not bundled → side filter → panels, don't over-tighten glass →
pedestal → BIOS (Above 4G + ReBAR) → `nvidia-smi` shows 96 GB → **fan daemon BEFORE any real load** → 2 h burn-in →
monthly filter-clean reminder.

## Rev 10 — 2026-07-26. 14-retailer sweep + slot verification + owned-fan audit.

**NOTHING BEAT THE EVO XL.** 357 listings / ~50 distinct chassis across 14 Indian retailers Bob supplied.

**SLOT QUESTION ANSWERED — YES, and in ALL THREE tray positions.** Lian Li's CATIA STEP shows the 8 expansion
slots are children of `ASM-MB-EVO-XL_ASM` (the tray assembly) → they move WITH the tray, so tray height cannot
change which case slot a board slot lands on. Measured (MSI manual p.30 @300dpi, worst error 0.24mm + Lian Li CAD):
**Astral 5090 (2.5-slot) in PCI_E1 → case slots 2+3; PRO 6000 (2-slot) in PCI_E2 → case slots 6+7.**
PCI_E1→PCI_E2 = **81.0mm = exactly 4 pitches**. **33.3mm clear air between cards**, slot 8 free, both brackets on
real screwable positions. Still use MIDDLE — for COOLING (82 roof / 90 floor), not fitment.
**Practical: seat the PRO 6000 FIRST** — MSI's EZ PCIe Release is on PCI_E1 only; PCI_E2's latch is reached under
the Astral, so removing the 6000 later means pulling the 5090 first.

**CORRECTION to Rev 8's cable reasoning:** "30.5mm between the cards → straight cable needs 35mm" was the WRONG
REASON — a card's top edge faces the SIDE PANEL, not the card above. Governing number = **169mm clearance − 137mm
card = 32mm to the panel** (a 90° plug is ~22.6mm; a straight one needs ~55mm). Angled cable still mandatory,
right conclusion. Same logic re-flags the Astral's **15.3mm** as the real tightest item.

**PRO 6000 CAME BARE** (Bob imported it from China via import/export contacts — no adapter, no accessories).
**BUY: Corsair Type-4 90° 12V-2x6 cable, SKU `CP-8920348`, STYLE B** (Style B exits DOWN the card face; Style A
loops UP over the top and needs headroom he doesn't have). **AX1600i CONFIRMED Type-4** (Corsair's compat table has
an "AXi / 1600 Only" column — every other AXi is Type 3). Stock: Vishal ₹2,220 SOLD OUT · Computech ₹2,499 SOLD OUT
· Corsair US $19.99 OOS (global supply gap) · **Amazon.in grey ₹13,080 (~7× MRP, ASIN B0DM649HBM)**. Set restock
alerts. **AVOID angled ADAPTERS** — CPSC recall 24-112 covered CableMod's angled *adapters* (25,300 units, 272
melting reports), NOT angled *cables*; also rules out Corsair's own ₹5,512 GPU Power Bridge. **AVOID the Type 5
version** (sold on Amazon.in at a similar price, will NOT work — plugs are stamped Type 4/Type 5).
**Wiring:** 600W = 50A. Corsair sanctions 2×8-pin @25A/socket into **separate** sockets, never a pigtail; NVIDIA's
own quick-start for this card specifies **4** separate 8-pin runs into a quad adapter (12.5A/socket — better 24×7).
Socket budget: 2 EPS + 4 + 4 = all 10 used unless the Astral's bundled 1-to-4 is replaced by a 2nd native cable.
**Check per-socket OCP in iCUE before the first 600W run.**
**✅ CLOSED 2026-07-26: the card is the GENUINE 96GB part** — Bob has run it for a year and loaded T2V/ComfyUI models needing 94GB VRAM, which cannot fit the China-market 84GB RTX 6000D. Do not re-raise.
**⚠️ AND THE COROLLARY: Bob has been RUNNING this card for a year, so a working 12V-2x6 cable ALREADY EXISTS.** A 600W card cannot run without one. So the CP-8920348 is NOT automatically a mandatory purchase — he must first check (a) is the PSU end stamped **Type 4**, (b) is the GPU end **straight or 90°**. Type-4 90° = he already owns it, buy nothing.

**BOB ALREADY OWNS a TAG Gamerz Supernova mid-tower with 7 fans — ALL 120mm, no 140s** (3 side, 3 floor, 1 rear,
ARGB+PWM on a hub). **DO NOT use them for the floor bank** — TAG's own copy says "low-impedance applications"
(= low static pressure) and publishes NO CFM/SP/RPM/dBA/bearing data anywhere; harvesting also forfeits the 3×140
option (420mm coverage under a 305mm card vs 360mm, lower RPM). **DO reuse exactly ONE as the rear exhaust**
(EVO XL rear is 120mm anyway). Keep 6 as free spares. Check the cable end first: 4-pin PWM + separate 3-pin ARGB =
reusable; one wide keyed plug = hub-locked, just buy the fan. Total saving is only ~₹1,100.

**Cases Bob named:** **Corsair Obsidian 1000D DEAD ×3** (697mm over cap · **zero bottom fan mounts** — floor is the
dual-PSU basement · discontinued/OOS everywhere). **Corsair 7000D DEAD — and our old width kill was the WRONG
REASON**: Corsair's own "12×120 OR 7×140" cap reconciles exactly to front+top+side+rear with **zero fans left for a
floor**, and Corsair sells no bottom fan tray (only solid shroud covers); 600mm height actually passes; ₹24,879
Amazon (white, 1 unit). **ANTEC BRANCH CLOSED** — pulled all 133 live products: **the C8's 62.8mm plenum is Antec's
ceiling** and all six C8 variants are one identical 464×303×476 chassis. Antec splits into a *shroud-bank* family
(Flux Pro / Perf 1 FT / Antec 900, all 230–250mm wide **because** the narrow body is what puts the shroud under the
slots) and a *floor-plenum* family (C8/C7/C5) — **there is no wide shroud-bank Antec**. New **Antec 900 "Edge AI
Workstation" ₹36,995 DEAD**: no floor fan mount, rads capped at 52mm vs the 65mm stack, 250mm wide, 160mm GPU
clearance (tighter than 169). Also: **Antec Performance 1 FT has NO bottom fan mount either** (shroud 3×120 only) —
we killed it on 230mm width, right by accident.

**NEW FIND — `Corsair FRAME 5000D WORKSTATION` (CC-9011330-WW, launched ~22 Jul 2026), ₹19,379 Amazon.in IN STOCK.**
542×250×556, 8+3 slots, SSI-EEB, spec reads *"Fan Support Bottom: 4×120 / Radiator Bottom: **None**"* — a fan-only
floor is exactly right for a flow-through card; roof 420 + front 360 with the floor free. **The only Corsair that
passes the floor-feed test.** Rejected on 250mm width + no removable top panel + zero owner data. **Keep as the
cheap fallback if the EVO XL becomes unbuyable.**

**Best challenger: Cooler Master HAF 700 ~₹24,200** (626×291×666, 8 slots, roof alone takes 2×360 @100mm, PSU in a
rear chamber so the whole floor is open, 5 fans included) — lost on **626mm height re-opening the desk-crush
problem**, **666mm depth** vs a pedestal spec'd 537×304, 19.6kg, and 166mm published side clearance (< 169).
Also killed: NZXT H9 Flow ₹20,599 + Corsair AIR 5400 ₹18,199 (**7 slots** — PRO 6000 lands on 6+7 with nothing
below) · TT View 51 ₹15,490 (floor 120mm only, roof thickness unpublished) · Cosmos C700M/C700P · TT AX700 ·
DeepCool CH780 (vertical-GPU-only, 3 slots, 180mm PSU) · ProArt PA602 ("supports **one** 420mm radiator") ·
Arctic Xtender VG · Prolab AI888 / TAG APEX-AI / Zebronics / darkFlash (no published dimensions anywhere).
"META PCS Night Reaper ₹1.25L" is a **prebuilt PC, not a case**.

**Revised buy list: ₹30,631** (case ₹22,499 Green Apple · 3× Arctic P14 Pro ₹3,327 · cable ₹2,499 at MRP ·
support stick ₹308 · side filter ~₹800 · trolley ₹499 · MX-6 ₹699 · rear fan ₹0 harvested). ₹41,913 if the cable
is bought grey today. **UPS dropped — Bob owns a Microtek online UPS and closed the topic.**

## Rev 9 — 2026-07-26. FORMAT + Bob's decisions.

**BOB SAID THE DOCS WERE TOO LONG AND HE COULDN'T UNDERSTAND THEM.** ("you gave me such a big fucjin document to
study, that I'm just confused now"). **`buy-checklist.html` REWRITTEN into a simple ranked format he specified:**
Preference 1/2/3/4, each with *why it's best · how to get full output · what accessories + links · downsides*.
**KEEP DELIVERABLES IN THAT SHAPE. Do not dump research into the page again** — detail goes in CLAUDE.md, the page
stays action-only. See [[minimal-webpages]].

**Bob's own calls this round (accepted, do not re-argue):**
- **After-sales/RMA/EOL downsides: he does not care.** Stop leading with them. (Honest caveat given: glass shattering
  and the floor filter are NOT after-sales issues.)
- **Pedestal: he has carpenters and will have one built.** A carpenter spec is now ON the page — open frame, rails
  under the 4 feet only, **nothing crossing the middle**, ≥480×280mm clear opening, **filter slide-out path kept
  clear** (so the filter is cleanable without lifting 40kg), 25–50mm total incl. castors, 60kg+, build to the real
  **537×304mm** footprint.
- **He thinks EVO XL is top-of-line and won't be discontinued.** Tempered honestly: EOL evidence was persistent OOS
  + Lian Li not answering a roadmap question = a signal, not an announcement. Correction given: the EVO XL is NOT
  Lian Li's newest — current development is the Vision line.
- **He read a Reddit thread about Phanteks vertical radiators being mocked.** I did NOT guess at it — asked him for
  the link. Moot anyway: Enthoo Pro 2 is out on the sealed-basement floor-feed issue, not radiator orientation.

**Buy-list total on the page is now ₹40,341 case+accessories / ₹88,831 with UPS** (fan hub dropped as optional,
side filter rounded to ~₹800).

## Rev 10 — 2026-07-26. SLOT-FITMENT PROVEN FROM PRIMARY CAD + MSI MANUAL. Answer = **YES**.

**Question: "tray in MIDDLE, can the 5090 go ABOVE and the PRO 6000 BELOW?" → YES, structurally and practically.
Works in ALL THREE tray positions (slot alignment is independent of tray position — see below). MIDDLE is still
the one to use, but for radiator/plenum reasons only, never for card fitment.**

**PRIMARY SOURCES USED (both now on disk, re-usable):**
- MSI's own English manual `MPGX870ECARBONWIFI_English.pdf` (46pp, dated 2026-03-17), from
  `download.msi.com/archive/mnu_exe/mb/`. msi.com 403s plain curl; Playwright channel="chrome" on the
  `/support#manual` page yields the direct PDF links. Page 30 = to-scale "Overview of Components" drawing.
- Lian Li's own CATIA STEP `evoxlman/LIAN LI_O11D EVO XL.stp` (78 MB).

**(a) BOARD — measured off MSI p.30 at 300 dpi, calibrated on the board outline (1084 px = 305 mm, 864.5 px =
244 mm; aspect 1.2539 vs spec 1.2500 = 0.31% error):**
- **3× physically-x16 slots.** PCI_E1 = Gen5 x16 (CPU) · PCI_E2 = Gen5 x4 (CPU) · PCI_E3 = Gen4 x4 (chipset).
  Both CPU slots populated on a 9000-series → **x8 / x4** (MSI verbatim: "PCIe 5.0 x16/x0 or x8/x4"). Matches Rev 1.
- **PCI_E1 → PCI_E2 = 288.0 px = 81.0 mm = EXACTLY 4 slot pitches** (4 × 20.32 = 81.28). ✅ our "4 pitches / ~81 mm"
  note was right. **PCI_E2 → PCI_E3 = 73.0 px = 20.5 mm = exactly 1 pitch.**
- **The board's slots sit at ATX positions 2, 6 and 7 — position 1 is EMPTY** (M2_1 heatsink lives there; M2_2/3/4
  fill positions 3/4/5). Proof: measured from the board's top edge PCI_E1 = 182.6 mm / PCI_E2 = 263.6 mm /
  PCI_E3 = 284.2 mm, vs ATX-predicted 182.56 / 263.84 / 284.16 mm. Worst error 0.24 mm.
- **PCI_E1 is the ONLY slot with MSI's EZ PCIe Release button** (manual p.35). PCI_E2/E3 = conventional latches.
- Board also has **PCIE_PWR1, an 8-pin supplementary PCIe-slot 12V feed** (bottom edge). Populate it for 2×600 W.

**(b) CASE — from Lian Li's own STEP file. THE KEY STRUCTURAL FINDING:**
- Assembly `ASM-MB-EVO-XL_ASM` (the motherboard tray) has as **DIRECT CHILDREN**: `MB-PANEL-T-EVO-XL`,
  `ASM-PCI-EVO-XL`, `ASM-PCI-EVO-XL_-21ASM` and **8 × `GD04401-46A00-011-ROG_56`** (the slot covers).
  → **The expansion-slot column is PART OF the motherboard tray and MOVES WITH IT.** Manual p.28's three-position
  figure + the rear-view figure corroborate: the whole rear block (I/O aperture + all 8 slots) translates, and
  removable mesh filler strips take up the slack above/below.
  **⇒ Tray position CANNOT change which case slot a board slot lands on. Low / Middle / Top are identical for
  card mounting.** Tray position only trades the fixed 172 mm roof-vs-floor budget (Middle 82/90, Low 118/54,
  Top 46/126).
- The 8 covers sit at Z = **−7.50, 12.82, 33.14, 53.46, 73.78, 94.10, 114.42, 134.74 mm** — **seven gaps of
  EXACTLY 20.32 mm**, no anomalies. (Supersedes the "20.33 mm CAD-measured" estimate — it is exactly ATX pitch.)
- **MAP (identical in all 3 tray positions):** case slot 1 = free · **slot 2 = PCI_E1** · slots 3-5 = no board slot ·
  **slot 6 = PCI_E2** · slot 7 = PCI_E3 · slot 8 = free. (Consistent with the Rev 8 note that the bundled GB-003
  "fits the 2nd expansion slot, which is exactly where the Astral goes".)

**(c)/(d) FITMENT — all arithmetic in case-slot Z (mm):**
- **Astral 5090 LC** (48 mm) in PCI_E1: Z 12.82 → 60.82. Bracket screws into **case slots 2 + 3**; body overhangs
  ~7 mm into slot 4's band. **Real, screwable.**
- **PRO 6000** (2-slot = 40.64 mm) in PCI_E2: Z 94.10 → 134.74. Bracket screws into **case slots 6 + 7**, ending
  *exactly* level with slot 8. **Real, screwable. NOTHING hangs below the last slot.**
- **No collision.** Clear air between the cards = 94.10 − 60.82 = **33.3 mm** on ASUS's published 48 mm thickness
  (**30.5 mm** if you budget the Astral as a full nominal 2.5 slots — keep 30.5 as the planning number).
- **PCI_E3 is consumed** by the PRO 6000's second slot. Expected, nothing was planned there. **Case slot 8 stays free.**

**⚠️ CORRECTION TO OUR OWN RECORD (Rev 8 reasoning was geometrically wrong, conclusion still right):** we wrote
"only 30.5 mm between the two cards → a straight 12V-2x6 needs 35 mm → angled MANDATORY". **The PRO 6000's top-edge
connector does NOT point at the card above it** — a GPU's "top edge" in a tower faces the **SIDE PANEL**, so the
5090 does not obstruct it at all. The governing dimension is **169 mm case GPU clearance − 137 mm card =
32 mm to the side panel**. Still under the ~35 mm a straight plug needs → **90° connector still MANDATORY**, and it
must be a cable with the bend **moulded in** (CableMod *adapters* were CPSC-recalled 2024), Corsair **Type-4** for
the AX1600i. **The PRO 6000 was imported bare from China — no cable came with it, and the AX1600i (2018,
ATX12V v2.31) has no native 12V-2x6 — so this cable MUST be bought, it is not optional.**
**Same logic re-flags the real tightest item: the Astral has only 169 − 153.7 = 15.3 mm of side clearance for ITS
connector + coolant tubes, and ASUS publishes nothing about where they exit. That is the open risk, not the slot gap.**

**(e) PRACTICAL:** 33 mm between cards is enough for fingers, but **PCI_E2 has no EZ-release → seat the PRO 6000
FIRST, the Astral second**; to ever unseat the PRO 6000 you must pull the Astral. 5090-on-top is also *better* for
the Astral's tubes (short run up to the roof rad, instead of routing past the PRO 6000). Sag: bundled GB-003 serves
the Astral (slot 2); the PRO 6000 needs its own stick braced off the floor-fan rail / between fans, ~68 mm above
25 mm-thick floor fans — never a full-height stick that blocks an intake fan.

**MIDDLE is still forced, for cooling not fitment:** Middle 82 mm roof clears the Astral's 65 mm rad stack and
leaves 90 mm floor (≈65 mm plenum after 25 mm fans). Low = 54 mm floor → strangles the flow-through card's intake.
Top = 46 mm roof → won't take the 65 mm rad.

## Rev 8 — round-4 deep research, 2026-07-25 (Bob unconvinced, asked for downsides + accessories + alternatives + Reddit)

**Bob confirmed he will program a new desk minimum → the 560mm cap is GONE, band reopened to 674mm.**
10-agent workflow (6 investigation angles + 3 fitment + synthesis). **VERDICT UNCHANGED: BUY THE EVO XL. Buy it soon.**

**THREE MORE OF OUR OWN RECORDS WERE WRONG — corrected, do not regress:**
1. **Enthoo Pro 2 is 560mm TALL, not 580.** Phanteks writes `(W x D x H) = 240 x 580 x 560` — **580 is the DEPTH.**
   It was never a height problem.
2. **Corsair 9000D is 698mm, not 664mm** (Corsair's own table) — over the cap — AND verbatim
   *"Radiator Support - Bottom: None / Fan Support - Bottom: None"*. Dead twice. Worst QC on the shortlist
   (front I/O **shorting**, not fixed by RMA panels; warped panels twice). **Never reopen.**
3. **Fractal Define 7 XL DOES have a floor feed** (`Bottom fan: 2x120/140mm`, 240/280 bottom rad). Our kill reason was
   false. It still loses (240mm wide, solid damped door) — but fix the reason.

**ENTHOO PRO 2 = DEAD, two independent kills** (Bob found it in stock and asked by name):
(a) **NO FLOOR FEED.** Its bottom fan/rad bracket sits INSIDE the closed drive basement under a **solid steel lid**
(only opening = a rubber grommet). Measured off Phanteks' own drawing (calibrated on 20.32mm ATX pitch): lid sits
~11.5mm below the lowest PCI slot → **~31.8mm of SEALED dead air** vs the EVO XL's **92.9mm of actively fed plenum.**
Owner corroboration: *"the bottom was pushed up against the PSU"*; *"11 drives (12 if you don't want bottom fans)"* —
the bottom fan positions compete with DRIVE BAYS because they're in the basement. Same failure mode as ROG Hyperion.
(b) **240mm wide** — 5mm NARROWER than the 245mm Flux Pro Bob rejected as too tight, 64mm narrower than EVO XL, and
by volume it's the SMALLER case (78.0L vs 84.4L). Also roof caps at **55mm** vs the Astral's 65mm stack, side bay
32–35mm → the fat rad is forced to the FRONT (the intake face). ⚠️ Server Edition SKUs (PH-ES620PTG_BK02 /
PH-ES620PC_BK03) have NO bottom fan/rad positions at all.

**THE ONLY CASE THAT WOULD BEAT IT: Phanteks NV9 / NV9 MkII** (575×280×**615mm**) — GPU height clearance **205mm**
(Astral gets 51.3mm instead of 15.3mm, retiring the tightest unknown in the project), roof ~163mm, roof+floor
INDEPENDENT, 140mm rear, included GPU bracket that fits a bottom-slot card, 280mm wide, 99L, no basement.
**BUT:** plenum is worse (~40mm free air vs EVO XL's ~65mm), PSU bay 210mm vs the 200mm AX1600i, and **NOT confirmed
buyable in India** (Amazon.in no NV9; EliteHubs only NV5; Vedant/TheITDepot nothing; Computech reported ₹18,499 but
site search broken; PC Studio Cloudflare-blocked). **ACTION: one phone call to Computech + PC Studio for
PH-NV923TG_DBK02 before paying. If "no" → buy the Lian Li and stop.**

**OEM/WORKSTATION CATEGORY = DEAD END, and it's reassuring:** **Puget Systems builds its RTX PRO 6000-configurable
Threadripper PRO AI/ML towers in a Fractal Define 7 XL** (240mm wide, solid damped door — narrower AND more closed
than what we're buying; NASA contract BOM confirms). **Lenovo ThinkStation P8** official: *"up to three PRO 6000
Max-Q (300W); **or up to ONE** PRO 6000 Workstation Edition (600W)"*. **Dell Precision 7960**: 4x300W only — won't
take the 600W card at all. **Nobody sells an empty OEM chassis.** Supermicro bare chassis exist in India but have
redundant server PSUs + ducted fan walls + **zero radiator mounts**. Consumer cases are the correct category.

**LONGEST-STANDING UNKNOWN PARTLY CLOSED:** a Sept-2025 build documents **2x RTX PRO 6000 Blackwell Workstation on an
X870E board in a Lian Li O11 EVO XL.** Existence proof (temps not retrievable, YouTube blocked).

**MORE CORRECTIONS TO OUR OWN NUMBERS:**
- Plenum is **92.9mm** (single CAD measurement), NOT the 99–120mm range quoted in Rev 7. Lian Li's published floor
  budget is 90mm → two methods agree within 2.9mm.
- **Only 30.5mm between the two cards** (not ~40mm — the Astral is 2.5-slot). A straight 12V-2x6 needs 35mm before
  its first bend → **an angled connection is MANDATORY.**
- **GB-003 anti-sag IS useful** — it fits the 2nd expansion slot, which is exactly where the **Astral** goes. Buy ONE
  stick for the PRO 6000, and one that braces off the fan rail / sits BETWEEN fans (a full-height stick blocks an intake fan).
- Floor fans must be pushed **rearward in Z AND inboard in X**; pushed outboard they blow past the card's edge.

**⚠️ 12V-2x6 SAFETY — highest-consequence open item.** CableMod's angled 12VHPWR **adapters** were **CPSC-recalled in
2024** (~25,300 units, 270+ overheating/melting reports, $74.5k damages); CableMod exited the category. **Correct
product = a cable with the 90° MOULDED INTO the connector** (CableMod C-Series Pro ModFlex 12V-2x6 90° StealthSense
for Corsair Type-4, US$29.90, **not sold in India**, publishes no height figure). Everything buyable in India
(EZDIY-FAB ₹4,181–7,263, JOYJOM ₹2,706–3,777) is an ADAPTER = the recalled geometry. **Seat both cards, measure
connector position + latch direction, THEN order.** Consider Thermal Grizzly 90° WireView Pro ($89.97, per-pin current
alarm; India availability unconfirmed).

**BUY LIST (live 2026-07-25):** case ₹23,200 vishalperipherals · Arctic P14 PWM PST 5-pack **₹3,399 ADS Store**
(⚠️ the SAME pack is ₹14,062 on Amazon.in — 4.1x, grey import) · Arctic P12 PST 5-pack ₹2,599 ADS Store (⚠️ the ₹759
Amazon listing is the Slim 15mm, wrong part) · 2x Corsair Elite Premium **Type-4** 12V-2x6 cables ₹4,773 ea ·
GPU support stick ₹308 · SPYLOCK open-frame metal trolley ₹499 (NEVER wooden — seals the intake) · MX-6 ₹699 ·
fan hub ₹882 (optional) · side magnetic filter ₹500–1,500 (side intake is UNFILTERED) · **UPS APC SRV3KL-IN 3kVA
₹48,490 apc.estorewale.com**. **Case+accessories ₹42,132; with UPS ₹90,622.** Missing from the parts list entirely:
**2x NVMe** (buy locally — Amazon.in shows import pricing ₹1.03–1.51 lakh).

**EVO XL DOWNSIDES (Bob asked; ranked):** 1) **quietly going EOL** — persistent worldwide OOS, no XL V2, Lian Li
didn't answer a direct roadmap question, momentum on the Vision line → **buy now, and spares are the risk**;
2) out of warranty Lian Li **won't sell parts even when offered money**; 3) **tempered glass genuinely shatters**
(r/lianli 314pts/190 comments, one owner 3x) and Bob's plan hits 3 of the 4 named triggers (rolled on casters,
vibration, hard floor, frequent panel removal); 4) the floor filter is a **single point of failure** for the ₹7-lakh
card → scheduled maintenance; 5) practical dust coverage is **1 filter not 4** (side intake unfiltered, DEMCiflex
sells a kit for this exact case); 6) tray budget is zero-sum, **MIDDLE is forced**; 7) needs the support pillar when
moved (conflicts with the pedestal plan); 8) zero fans (but only 4 needed, ~₹4k); 9) **front mesh kit discontinued**
(the cheap −5°C escape hatch is gone); 10) awkward AX1600i cable routing. **The "hotbox" reputation does NOT apply** —
stale, and earned by front-fed air cards.

**REDDIT'S MOST USEFUL FINDING (again, not about cases):** 4x PRO 6000 owner — *"when I added more fans it seemed to
make it worse… even at 85C the card's fans were only at ~30%. I wrote a script… removed 3 case fans and now they run
~70C continuously."* **Good case vs great case = a few degrees. Stock firmware vs fan daemon = 15–19°C measured.**
Also independently confirms our layout: *"switched to an AIO set as INTAKE and it solved the problem"* (CPU rad as
intake). And *"the biggest problem is the temp of the 12v 2x6 plugs… so I reduced the cards to 420W."*

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

## Rev 11 — 2026-07-26. RETAILER-SWEEP CANDIDATE PASS (~150 listings, ~50 distinct chassis). Answer = **NOTHING BEATS THE EVO XL.**

**Method:** manufacturer spec sheets + official manuals (Playwright channel="chrome"; WebSearch budget was exhausted,
WebFetch/curl used for the rest). Cooler Master manuals live behind egnyte — direct-download trick that works:
`curl -L "https://coolermaster.egnyte.com/dd/<ID>/?forceDownload=true"` (the `/dl/` link is a JS viewer, `/dd/` is the file).

**FOUR NEW SURVIVORS (clear 6 of 7 outright; req 4 = GPU HEIGHT clearance is UNPUBLISHED on all four):**
| case | H×W×D mm | slots | floor feed | 2×360 + free floor | PSU | India ₹ |
|---|---|---|---|---|---|---|
| **CM HAF 700** (non-EVO) | 626×291×666 | 8 | 3×120/140 + 420 rad, **PSU is in a separate REAR chamber so the whole floor is open**; bracket tilts 0–30° | roof alone takes **2×360 @ up to 100 mm thick** | 200 mm | ~24,200–27,999 |
| **NZXT H9 Flow (2025)** | 506×**315**×481 | **7** | 3×120/140 + 360 rad, dual-chamber | top 420 (**80 mm thick budget**) + front-right 420 | 200 mm | 20,599–23,545 |
| **TT View 51 TG ARGB** | 550×**315**×525 | 8 | 3×**120 only** + 360 rad, PSU in right chamber | front 360 + top 360 (thickness UNPUBLISHED) | 200 mm | 15,490–18,200 |
| **Corsair AIR 5400 RS-R** | 467×**340**×470 | **7** | 3×120 reverse fans **preinstalled**, + 360 rad, triple-chamber | front 360 (own CPU chamber) + top 360 | 200 mm | 18,199–19,200 |

**WHY NONE OF THEM WINS:** the EVO XL's two decisive numbers are **VERIFIED** (169 mm GPU clearance; 92.9 mm floor
plenum off Lian Li's own CAD). **Not one of the four publishes a GPU height/thickness clearance or a plenum depth.**
The project's single tightest open risk is the Astral's 15.3 mm of side clearance for its connector + coolant tubes —
swapping to a chassis where that number is unknowable makes the risk worse, not better. Specifically:
- **HAF 700** is the strongest and is genuinely better on *radiator freedom* (roof takes both 360s at up to 100 mm,
  floor 100% free; separate rear PSU chamber; mesh front; **5 fans included** vs the EVO XL's zero) at the same price
  — but **626 mm tall re-opens the desk-crush problem the EVO XL uniquely eliminates** (desk underside bottoms out
  ~605–615 mm), it is **666 mm DEEP** (the carpenter's pedestal is already spec'd to 537×304), 19.6 kg, PSU limit is
  *exactly* 200 mm, and its only published side clearance is **166 mm CPU-cooler** — i.e. ≤ the EVO XL's 169 mm.
- **H9 Flow / AIR 5400** are **7-slot**: the PRO 6000 in PCI_E2 lands on case slots 6+7 with **nothing below it**
  (Rev 10 deliberately kept slot 8 free). H9 also ships **one dust filter** (bottom only) — bad for 24×7 India.
- **View 51** floor bank is **120 mm fans only** (vs 3×140) and roof rad thickness is unpublished — the 65 mm Astral stack is a coin-flip.

**KILLS WORTH REMEMBERING (don't re-litigate):**
- **Corsair 7000D — RE-VERIFIED DEAD as Bob asked by name.** Corsair's own tech-spec table has **no bottom fan and no
  bottom radiator field at all** (only Front/Top/Side; its "three simultaneous 360s" are those three). The only PSU-shroud
  accessories Corsair sells are **solid covers**. Plus 248 mm wide. Same kill applies to **iCUE 7000X** (shared chassis/accessories).
- **Antec 900 "Edge AI"** (the sweep's "best new find") — **DEAD on req 3.** It does have the 2×120 reverse-flow shroud bank,
  8 slots, 622 mm, PSU 230 mm, and it is the ONLY new candidate that publishes a **GPU thickness: 160 mm** — but radiator
  support is only **Front 420 / Top 360 and BOTH are capped "<52 mm thickness"**; the Astral's 65 mm rad+fan stack has
  nowhere to go. Also 250 mm wide (5 mm more than the Flux Pro Bob already called too tight) at ₹36,995, and 160 mm GPU
  clearance is TIGHTER than the EVO XL's 169 mm. Note it has **no bottom fan mount at all** — fewer cooling positions than
  the cheaper Flux Pro.
- **DeepCool CH780** — "dual chamber layout **limits GPU mounting to the vertical position**", **3 expansion slots**, PSU 180 mm. Dead ×3.
- **Cosmos C700M/C700P** — 306 mm wide and 651 mm tall (both pass) but bottom is **2×120/140 "(Bracket Needed)"** with bottom rad capped at 240 mm, inside the PSU-midplate basement. Dead on floor feed.
- **TT AX700 super tower** — 645×324.6×685 so height PASSES, but bottom = 2×120/140 with **no bottom radiator**, and PSU length is quoted "220 mm *with two bottom fans*" → they share the PSU basement. Dead on floor feed.
- **Corsair Obsidian 1000D** 697 mm (over 674) · **TT Core W100/W200** cube super tower · **Prolab AI888/AI858** (no published external dims anywhere, 380 mm GPU limit) · **TAG APEX-AI**, **Dawg**, **Zebronics Phantom Pro**, **Ant Esports Crystal X8**, **darkFlash ₹61,768** = unverifiable no-name · **META PCS Night Reaper ₹1.25 L is a PREBUILT PC, not a case**.
- **ASUS ProArt PA602** — ASUS's own copy: "supports **ONE** 420 mm radiator". Dead on req 3 (also 220 mm wide).
- **SilverStone RM42-502/RM44/RM400** = 4U rackmount (no floor bank under a horizontal card) · **RV05B** = 2014 Raven, no 360 rad support anywhere.
- **Fractal Meshify 2 XL** 240 mm wide + bottom capped at 2 fans / 240-280 rad in the storage basement · **Phanteks Enthoo 719 / Evolv X** 240 mm + closed basement (same as Enthoo Pro 2) · **Phanteks NV7 confirmed OOS**.
- **TT CTE E660 MX** — same rotated-board / riser "three-way GPU installation" family as the CTE C750 already rejected.
- **Arctic Xtender VG** built around a VERTICAL GPU mount → the flow-through PRO 6000 would inhale into a panel.
- **CM MasterFrame 600** 261 mm wide open frame, no bottom rad, no dust control for 24×7 India.
- **Lian Li PC-O11 Dynamic XL (₹19,299)** = the EVO XL's *predecessor* (fixed tray, no 3-position roof/floor split, shallower plenum). Strictly dominated for ₹4k more.
- **CM HAF 700 EVO** = the SAME 666×291×626 chassis as the HAF 700 and would survive identically, but ₹45,376–51,709 ≈ 2× for a front rad mount + ARGB Gen2. Dominated by the non-EVO.

**UNRESOLVED (pages 404'd / Cloudflare-blocked — only worth reopening if the EVO XL falls through):** CM Cosmos 2025
(8 slots, PSU 240 mm, GPU 400 mm, ₹33,999 — CM's spec page would not render), ASUS ROG Strix Helios II GX601S
(ASUS spec URL 404s; the GX601 it descends from is a 250 mm solid-shroud showcase tower), Gigabyte AORUS C601 / AC700G,
Thermalright TR A70 / A70 Vision, DeepCool Morpheus, Cougar Cratus.

**STOCK CAVEAT:** independently re-rendered only **HAF 700 EVO at ModxComputers (₹45,376, Add To Cart, SKU H700E-IGNN-S00)**.
The cheaper **non-EVO HAF 700 at ~₹24,200** is reported by the sweep at 5 retailers but **pchubshop/ADS/Green Apple are
Cloudflare- or JS-blocked to us — phone-confirm before quoting that price to Bob.**

## Rev 12 — 2026-07-26. FINAL ANSWER PASS (14-retailer sweep + 4 deep dives). EVO XL STANDS.

**1. SLOT QUESTION = YES, in all three tray positions.** Lian Li's own CATIA STEP proves the 8 slot covers are children
of `ASM-MB-EVO-XL_ASM` (the mobo tray) at Z = −7.50 … 134.74 mm (7 gaps of exactly 20.32 mm), so tray height CANNOT
change the board→case slot mapping. MSI's manual p.30 measured at 300 dpi: PCI_E1/PCI_E2 = 81.0 mm = exactly 4 pitches,
ATX positions 2 and 6 (worst error 0.24 mm). Astral (2.5-slot, 48 mm) in PCI_E1 → case slots 2+3, body ends Z 60.82.
PRO 6000 (2-slot) in PCI_E2 → case slots 6+7, body ends Z 134.74 = level with slot 8. **Clear air between cards 33.3 mm;
slot 8 free; nothing overhangs.** Use MIDDLE tray for COOLING only (82 mm roof clears the 65 mm Astral rad, 90 mm floor).
Assembly order: **seat the PRO 6000 FIRST** — MSI's EZ PCIe Release button is on PCI_E1 only.

**2. NOTHING BEATS THE EVO XL.** Corsair 1000D = DEAD ×3 (697 mm; **zero bottom fan mounts**, floor is the dual-PSU
basement; discontinued/OOS everywhere). Corsair 7000D = DEAD — **fix our own kill reason: it is no-bottom-fan-mount, not
width.** Corsair's 12×120/7×140 cap reconciles EXACTLY to front+top+side+rear (HEXUS enumerates every position), and the
only floor accessories Corsair sells are solid shroud covers. 248 mm is the secondary problem. Antec branch CLOSED: pulled
the whole live catalog (`antecindia.in/products.json?limit=250` via Playwright — curl gets 429; 133 products). **The C8's
62.8 mm plenum IS Antec's ceiling** and all six C8 variants are one identical 464×303×476 chassis. Antec splits into a
SHROUD-BANK family (Flux Pro / Perf 1 FT / Antec 900 — all 230–250 mm wide *because* the narrow body puts the shroud under
the slots) and a FLOOR-PLENUM family (C8/C7/C5); **there is no wide shroud-bank Antec.** Correction: **Perf 1 FT has NO
bottom fan mount at all** (shroud 3×120 only, no shroud rad) — we killed it on 230 mm width, which was right by accident.
Antec publishes GPU *height* for exactly one case in the range (Antec 900, ≤160 mm) and radiator *thickness* for exactly
one (Antec 900, 52 mm) — so the C8's ability to swallow the 65 mm Astral stack is UNVERIFIED.
**ONE new find worth a line: CORSAIR FRAME 5000D WORKSTATION (CC-9011330-WW, launched ~22 Jul 2026)** — 542×250×556, 8+3
slots, SSI-EEB, "Fan Support Bottom: 4×120 / Radiator Bottom: **None**" (fan-only floor = ideal, no rad upstream of the
card), roof 420 + front 360 with floor free, **₹19,379 Amazon.in in stock**. Only Corsair that passes floor-feed. Rejected
on 250 mm width + no removable top panel (fiddly 65 mm rad install), but it is the cheap fallback if the EVO XL falls through.

**3. TAG GAMERZ SUPERNOVA DONOR FANS = 7 × 120 mm ARGB PWM, hub-driven** (3 side + 3 floor + 1 rear; some retailer copy
says 6 — Bob should count). **NOT for the floor bank:** TAG's own A+ copy calls them optimised for "**low-impedance
applications**", zero published CFM/SP/RPM/dBA/MTBF, no manufacturer site, ~₹150–250/fan implied, and using them forfeits
the EVO XL's 3×**140** floor option (420 mm of coverage vs 360). **Reuse exactly ONE as the rear exhaust; keep the rest as
spares; BUY 3× 140 mm static-pressure for the floor.** ⚠️ First check one fan's tail: standard 4-pin PWM + 3-pin 5V ARGB =
reusable; single wide keyed plug = hub-locked, don't drag a SATA ARGB hub into a 24×7 headless box.

**4. POWER CABLE — CONFIRMED AX1600i IS TYPE 4** (Corsair's compatibility table has an "AXi / **1600 Only**" column;
all other AXi are Type 3). **Buy Corsair CP-8920348 (Type-4 90° 12V-2x6, Style B = exits DOWN along the card; Style A
loops UP over the top and needs headroom we don't have), 650 mm, 16 AWG.** India MRP ₹2,220–2,499 (Vishal / Computech)
— **both CONFIRMED SOLD OUT**, Corsair US store also OOS → global supply gap. Grey on Amazon.in ₹13,080 (ASIN
B0DM649HBM, 28-Aug delivery) = ~7× MRP. **Don't pay it unless blocked.** H+ vs H++ is a red herring — Corsair: "There is
no difference when it comes to the cable." **⚠️ Type 5 will NOT fit the AX1600i** (Amazon.in sells the Type-5 Elite
Premium at a nearly identical price — read the stamp on the 8-pin). 600 W = 50 A; Corsair sanctions 2×8-pin (25 A/socket)
but **NVIDIA's own RTX PRO Blackwell QSG mandates FOUR separate 8-pin runs into the included quad adapter** (12.5 A/socket)
— that adapter is a straight plug and is one of the things missing from the bare China import. Also: **check per-socket OCP
in iCUE before first 600 W load** (AX1600i has configurable OCP on each of its 10 sockets; 25 A can nuisance-trip a default).
Socket budget: 2 EPS + 4 (PRO 6000 quad route) + 4 (Astral's included 1-to-4 adapter) = **all 10 used**.

**5. VERIFY THE CARD:** run `nvidia-smi` on first boot. **84 GB = it's a China-market RTX 6000D** (cut-down cores, no
NVLink), not the 96 GB global RTX PRO 6000 Blackwell WS. Same 1×16-pin / 600 W either way.

**Tooling for next round:** `antecindia.in/products.json?limit=250` gives live price+availability for the whole catalog in
one Playwright call (cleanly separates "confirmed OOS" from "could not read"). CM manuals: `curl -L
"https://coolermaster.egnyte.com/dd/<ID>/?forceDownload=true"`. Blocked to us: mdcomputers/pcstudio (Cloudflare, even via
Gonzo IN residential), primeabgb (geo-block), elitehubs (429), theitdepot search (404). WebSearch budget exhausted 200/200.
