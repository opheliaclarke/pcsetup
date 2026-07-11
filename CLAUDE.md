# Dual-GPU AI Workstation (pcsetup)

**What it is:** A single self-contained HTML build-plan document (case / cooling / power / desk-clearance) for Dominic's in-house 24×7 dual-GPU AI training workstation.
**Status:** **Rev 2 — LIVE.** Case decision reopened and resolved. Published 2026-07-11.

## Live assets
- **Repo:** `opheliaclarke/pcsetup` (PUBLIC — user approved public visibility for Pages). Collaborators SilentAurora245 + mary3862jon added.
- **Pages:** https://opheliaclarke.github.io/pcsetup/ — verified HTTP 200.
- `index.html` carries `<meta robots noindex>`.
- SEPARATE related projects (NOT this folder): AC buying guide at https://opheliaclarke.github.io/ac-guide/ · desk research at https://opheliaclarke.github.io/standing-desk-india/

## Key facts
- **Rig (locked):** Ryzen 9 9950X3D · MSI X870E Carbon WiFi · 64GB DDR5 · GPU1 RTX PRO 6000 Blackwell 96GB (600W) · GPU2 RTX 5090 (AIO liquid, ~575W) · Corsair AX1600i · DeepCool LT720 360 AIO · ~1.4–1.45 kW peak.
- **Desk (new constraint):** Ergosphere Balanced Desk PRO 340 L-Shape Corner, triple-motor, LOGICDATA/Bosch, **frame-only**. Published "63cm min" is to the DESKTOP TOP; the **underside bottoms out at ~605–615mm**. The PC goes UNDER it.

## THE BIG CORRECTION (Rev 1 was wrong — do not regress)
- **The RTX PRO 6000 Blackwell WS is NOT a rear-exhaust blower.** NVIDIA's datasheet: **double-flow-through** — draws air from BENEATH the card, vents UP into the case. All 600W stays in the chassis. Only the **300W Max-Q** is a blower. Rev 1's "exhausts out the back — a good citizen" was the load-bearing error under the whole case choice.
- Every liquid RTX 5090 is **2.5-slot** (not 2). The PRO 6000 is 2-slot but **extended height: 137mm** (vs standard 112mm).
- **PCI_E2 is PCIe 5.0 ×4** (not Gen4 ×4). Populating it drops PCI_E1 from ×16 to **PCIe 5.0 ×8**. No M.2/SATA lost. Slots are **4 pitches apart** (~81mm centres).

## Decisions made
- **CASE WINNER: Antec FLUX PRO** — ₹20,865 black, IN STOCK, Antec India official store (MRP ₹25,999). **545mm tall with feet** (523mm without — Noctua publishes both; 70.77 L volume cross-checks). 8 slots; 455mm GPU-LENGTH limit vs 304mm card = huge margin. GPU HEIGHT/thickness clearance is UNPUBLISHED anywhere (Antec/Noctua/every reviewer — verification agent confirmed the spec field doesn't exist); the 137mm extended-height PRO 6000 is a measure-on-arrival, but a TALLER 150mm MSI RTX 5090 SUPRIM is spec'd into this case in the wild, so height is a non-issue in practice. Wins on the **PSU-shroud fan bank** that blows floor-ambient air straight UP into the GPU's underside — exactly what a flow-through card needs. GamersNexus noise-normalised thermal chart leader.
  - **PSU gotcha:** iShift 90° side mount caps at 180mm. The 200mm AX1600i needs the **conventional PSU bracket** + drive cage removed.
- **RUNNER-UP: Corsair 6500D Airflow** — ~₹17,000 (MD Computers), 496mm, 8 slots, 225mm PSU bay, dual-chamber floor intake. Cheaper/shorter, mid-pack airflow.
- **FAN/RAD LAYOUT (this is the performance):** LT720 360 → **FRONT, intake** (CPU only ~200W, +2–3°C). 5090's 360 AIO → **ROOF, exhaust**. **3× 120mm in the PSU shroud, pure intake, no rad** → feeds the PRO 6000. Rear → exhaust. **NEVER a radiator upstream of the PRO 6000** (GN measured 7–9°C penalty).
- **SLOT ORDER (important, corrected — was backwards in first draft):** **PRO 6000 in the LOWER slot PCI_E2** (sits over the shroud fans → fresh-air feed for the flow-through card) = **Gen5 ×4**; **5090 in the TOP slot PCI_E1** = **Gen5 ×8**. The ×4 is negligible for a 96GB card that keeps its job in VRAM; feeding the 600W air-cooled card 24/7 beats the bandwidth. This is the OPPOSITE of the "big card up top" habit, and it's correct here because the shroud fan bank is the whole reason for this case. Only keep the PRO 6000 up top (×8) if its jobs stream heavily from system RAM / NVMe offload — then feed it with a side intake fan instead. Both slots are CPU-direct.
- **DROP the vertical GPU kit AND the riser.** Cards seat natively 4 pitches apart (~40mm clear air). Vertical-mounting the PRO 6000 would face its intake into glass and choke it. (Lian Li VG4-4 V2 also isn't buyable in India — grey import at ~2.3× MSRP.) Saves ~₹15k and cools better. A plain GPU support stick is enough for a 2-slot card.
- **Fan-curve daemon is MANDATORY.** Stock NVIDIA VBIOS sits at ~30% fan at 85–90°C. Power-limited PRO 6000 under sustained LLM load: **85°C stock / 75–79°C at 80% / 66–67°C at 100%.** Use LACT or a pynvml daemon.
- **Angled 12V-2×6 adapter required** — the PRO 6000's connector is on the top middle edge.
- **DESK:** container stop at **700mm** (LOGICDATA: hold **"S" 10 s**, two clicks) + **2× steel hard-stop posts rated >2500N**. Gives 155mm air above the 545mm case; desk surface still 725mm. **Never reset the desk with the PC underneath** — reset drives BELOW the programmed limit and DISABLES anti-collision.
- Power-limit both GPUs ~80% on day one. Dedicated 16A circuit. ~3kVA online UPS. 2-ton 5-star inverter AC.

## Dead ends — do NOT redo
- **Corsair 9000D: DEAD.** 664mm — 104mm taller than the desk's lowest point. (Good case otherwise; the only documented dual-PRO-6000 build uses it. Just cannot go under this desk.)
- **Lian Li O11 EVO XL: DEAD.** Sealed glass front, no front intake without a paid mesh kit; repeatedly called a "hotbox" for air-cooled cards. It's a watercooling case, hostile to a flow-through GPU.
- **Fractal Torrent: DEAD.** No top radiator mount at all (spec sheet confirms). Needs two rads.
- **Fractal North XL: DEAD.** "Bottom radiator: N/A", no floor fan mount → nothing feeds the PRO 6000 from below.
- **Phanteks NV7/NV9/Enthoo Pro 2 + Lian Li Lancool III: DEAD on availability** — out of stock at every Indian retailer.
- Do NOT merge both cards into one ~128GB trainer (no NVLink, mismatched VRAM/clocks). Two independent workers.
- Do NOT rely on the desk's anti-collision — LOGICDATA trips at ~40kg + desk load downward, and is OFF during reset.

## Open / next
- Measure the Flux Pro's height with feet on arrival — the plan relies on 545mm (15mm margin). If it measures over, fall back to the Corsair 6500D Airflow.
- Read the label on the desk control box: **LOGICDATA or JieCang** — the container-stop procedure differs.
- Monitor motherboard VRM/PCIe temps, not just GPU temps. Documented failure mode: PCIe retimers hit 90°C and crash the fabric while the GPUs read "fine".
