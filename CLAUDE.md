# Dual-GPU AI Workstation (pcsetup)

**What it is:** A single self-contained HTML build-plan document (housing / cooling / power / room-heat) for Dominic's in-house 24×7 dual-GPU AI training workstation in a 10×18 ft office.
**Status:** In-progress decision-support doc. LOCAL FILE ONLY — not a git repo, not deployed, `index.html` carries `<meta robots noindex>`. Last edited 2026-06-20. Case + AC selection were still being refined via research through early July 2026.

## Live assets
- No deployment for this folder. Only file: `/root/workspace/pcsetup/index.html`.
- SEPARATE related project (NOT this folder): the AC buying guide is live at https://opheliaclarke.github.io/ac-guide/ (repo `opheliaclarke/ac-guide`, public, verified 200).

## Key facts
- **Rig config (locked):** Ryzen 9 9950X3D · MSI X870E Carbon WiFi · 64GB DDR5 · GPU1 RTX PRO 6000 Blackwell 96GB (AIR-cooled, 600W) · GPU2 RTX 5090 (AIO liquid, ~575–600W) · Corsair AX1600i 1600W PSU · DeepCool LT720 360 AIO (CPU) · 180 sq ft office, AC 24×7, India (230V mains).
- Whole rig ≈ 1.4–1.45 kW peak ≈ ~4,900 BTU/hr. Tech: static HTML, dark theme, TOC, copy buttons.

## Decisions already made
- **Use the two GPUs as INDEPENDENT WORKERS** (train on the 96GB 6000, inference/second job on the 5090) — NOT one merged trainer. Why: no NVLink, mismatched VRAM/clocks, and the 2nd PCIe slot is only ~Gen4 x4.
- **Power-limit both GPUs to ~80%** on day one (`nvidia-smi -pl`). Big heat/power cut, ~5–8% throughput loss. Single highest-value change.
- **Cooling verdict: 2-ton 5-star INVERTER AC** covers room + PC ~5× over; the real comfort fix is airflow direction (exhaust → AC return, sit upstream), not more BTU. AC model winner (from research): Panasonic CS/CU-NU24BKY5W (ISEER 5.80) — full AC detail lives in the separate ac-guide repo.
- **Case winner: Corsair iCUE LINK 9000D RGB AIRFLOW** (CC-9011273-WW black). Ranked #1 over Phanteks NV9 MkII (#2) and Lian Li O11 EVO XL (#3, needs add-ons).
- **Anti-sag fix (any case):** vertical-mount the 6000 on a steel kit (Lian Li VG4-4 **V2**) + put the 5090 on a Gen4 riser — removes weight from the board and separates the two heat sources.
- **Electrical:** dedicated 16A circuit from the DB; online double-conversion UPS ~3 kVA.

## Dead ends — do NOT redo
- Do NOT plan to merge both cards into one ~128GB trainer — no NVLink, different VRAM/clocks; frameworks assume identical GPUs.
- Do NOT custom-loop the irreplaceable 96GB card; the 5090's AIO is functional heat-separation only.
- Do NOT trust any bundled case anti-sag bracket for a ~2kg 4-slot card (Lian Li GB-003 only braces the 2nd slot; original VG4-4 is NOT 4-slot compatible — needs V2).

## Open / next
- Confirm the X870E Carbon's 2nd PCIe slot real lane width in the board manual.
- Vendor-confirm two 3–4-slot cards + two 360mm radiators physically coexist in the chosen case (send exact card dims). The 9000D's 580mm GPU-length claim was refuted.
