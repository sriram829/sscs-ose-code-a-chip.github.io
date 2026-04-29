# tt_um_pedometer — IEEE SSCS Code-a-Chip VLSI 2026 Submission

An ultra-low-power 870 nW digital step-counter ASIC, designed entirely with open-source EDA tools (LibreLane 2.4.2 / OpenLane 2 / Yosys / Magic / KLatout / OpenSTA) on the SkyWater **SKY130** open PDK and accepted on the **Tiny Tapeout TTSKY26a** shuttle.

---

## Author and Contact

| Field | Details |
|---|---|
| **Author (Team Lead)** | Dr. A. Sriram Anbalagan |
| **Designation** | Post Doctoral Fellow, MeitY Visvesvaraya PhD Scheme |
| **Affiliation** | School of Electrical and Electronics Engineering (SEEE),<br> SASTRA Deemed University, Thanjavur – 613 401,<br> Tamil Nadu, India |
| **Supervisor** | Dr. T. N. Prabakar, Associate Professor, SEEE, SASTRA |
| **ORCID** | [0000-0003-3528-7462](https://orcid.org/0000-0003-3528-7462) |
| **Scopus Author ID** | 59573168000 |
| **Google Scholar** | [dj7owLoAAAAJ](https://scholar.google.com/citations?user=dj7owLoAAAAJ) |
| **GitHub** | [github.com/sriram829](https://github.com/sriram829) |
| **IEEE Membership** | IEEE Madras Section, VLSI Technical Community |
| **Email** | sriram_a@eee.sastra.edu |

---

## Files in this directory

| File | Purpose |
|---|---|
| `Pedometer_CAC_Submission.ipynb` | Self-contained design notebook — abstract, motivation, architecture, RTL hierarchy, verification, full RTL-to-GDSII flow, verified PPA, references |
| `README.md` | This file |
| `LICENSE`  | Apache 2.0 |

---

## Headline numbers (from public CI artefacts, all SKY130 sky130A sign-off)

| Metric | Value |
|---|---|
| Process | SkyWater SKY130 (open PDK) |
| Shuttle | Tiny Tapeout TTSKY26a |
| Total power | **870 nW** at 1.8 V, 32.768 kHz |
| Total cells | 1,506 (359 FFs + 1,147 combinational) |
| Core area | 34,255 µm² (1×2 tile) |
| Placement utilisation | 76.2 % |
| DRC / LVS / Antenna | 0 / 0 / 0 violations |
| Setup TNS / hold WNS | 0 ns / +0.42 ns |
| CI runs (green) | 81 / 81 |

## Tools and versions

| Tool | Version |
|---|---|
| LibreLane | 2.4.2 |
| OpenLane 2 (Nix flake) | `efabless/librelane#default` |
| Yosys | 0.43+ |
| OpenROAD | 2.0+ |
| Magic | 8.3.x |
| KLayout | 0.28.x |
| Netgen | 1.5.x |
| OpenSTA | 2.5+ |
| cocotb | 1.8.x |
| SKY130 PDK | sky130A (open_pdks 1.0.469+) |

## Reproducing the flow

```bash
git clone https://github.com/sriram829/tt_um_pedometer.git
cd tt_um_pedometer
nix develop github:efabless/librelane#default --command \
    librelane --pdk sky130A --flow Classic ./src/config.json
```

The same command runs in CI on every push — see `.github/workflows/gds.yml`.

## License

This work is released under the **Apache License, Version 2.0**. See `LICENSE`.

## Citation

If you reuse this design or notebook, please cite:

> A. S. Anbalagan and T. N. Prabakar, *"A 870 nW Pedometer ASIC in SKY130 with a Fully Open-Source RTL-to-GDSII Flow,"* manuscript in preparation, IEEE Transactions on VLSI Systems, 2026.

---

*Submitted to the IEEE SSCS Code-a-Chip Travel Grant Award — VLSI 2026 cycle.*
