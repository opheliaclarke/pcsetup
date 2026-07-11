# Dual-GPU AI Workstation (pcsetup)

**What it is:** A single self-contained HTML build-plan document (case / cooling / power / desk-clearance) for Dominic's in-house 24×7 dual-GPU AI training workstation.
**Status:** **Rev 3 — LIVE, QA-verified.** Case switched to Lian Li O11 EVO XL (roomier) after user confirmed the 5090 is a ROG Astral LC with a fat 65mm radiator + wants build room. Published 2026-07-11. Independent sub-agent QA read the final page (no contradictions); CPU figure reconciled to ~180W throughout, stale "rear fan" removed, airflow diagram redrawn.

## Live assets
- **Repo:** `opheliaclarke/pcsetup` (PUBLIC — user approved public visibility for Pages). Collaborators SilentAurora245 + mary3862jon added.
- **Pages:** https://opheliaclarke.github.io/pcsetup/ — verified HTTP 200.
- `index.html` carries `<meta robots noindex>`.
- SEPARATE related projects (NOT this folder): AC buying guide at https://opheliaclarke.github.io/ac-guide/ · desk research at https://opheliaclarke.github.io/standing-desk-india/

## Key facts
- **Rig (locked):** Ryzen 9 9950X3D · MSI X870E Carbon WiFi · 64GB DDR5 · GPU1 RTX PRO 6000 Blackwell 96GB (600W) · GPU2 RTX 5090 (AIO liquid, ~575W) · Corsair AX1600i · DeepCool LT720 360 AIO · ~1.4–1.45 kW peak.
- **Desk (constraint):** Ergosphere Balanced Desk PRO 340 L-Shape Corner, triple-motor, LOGICDATA/Bosch, **frame-only**. Published "63cm min" is to the DESKTOP TOP; the **underside bottoms out at ~605–615mm**. The PC goes UNDER it. Case must be ≤560mm tall.
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
- Power-limit both GPUs ~80% on day one. Dedicated 16A circuit. ~3kVA online UPS. 2-ton 5-star inverter AC.

## Dead ends — do NOT redo
- **Corsair 9000D: DEAD.** 664mm — 104mm taller than the desk's lowest point. (Good case otherwise; the only documented dual-PRO-6000 build uses it. Just cannot go under this desk.)
- **Lian Li O11 EVO XL: was flagged DEAD in Rev 2, REINSTATED as WINNER in Rev 3.** The "hotbox" reputation is real ONLY for front-fed conventional air cards starved by the glass front. A bottom-ingesting flow-through card (PRO 6000) is fed from the FLOOR, so the glass front is irrelevant; run the top rad as exhaust and it breathes fine. Needs the mesh SIDE panel for the CPU rad only. Do NOT re-disqualify it on the generic hotbox reasoning.
- **Fractal Torrent: DEAD.** No top radiator mount at all (spec sheet confirms). Needs two rads.
- **Fractal North XL: DEAD.** "Bottom radiator: N/A", no floor fan mount → nothing feeds the PRO 6000 from below.
- **Phanteks NV7/NV9/Enthoo Pro 2 + Lian Li Lancool III: DEAD on availability** — out of stock at every Indian retailer.
- Do NOT merge both cards into one ~128GB trainer (no NVLink, mismatched VRAM/clocks). Two independent workers.
- Do NOT rely on the desk's anti-collision — LOGICDATA trips at ~40kg + desk load downward, and is OFF during reset.

## Open / next
- Confirm the exact Lian Li EVO XL mesh side-panel SKU + India price at purchase (needed for the CPU rad to breathe).
- ROG Astral LC is scarce/OOS in India — check live stock before committing the rest of the build.
- Read the label on the desk control box: **LOGICDATA or JieCang** — the container-stop procedure differs.
- Monitor motherboard VRM/PCIe temps, not just GPU temps. Documented failure mode: PCIe retimers hit 90°C and crash the fabric while the GPUs read "fine".
