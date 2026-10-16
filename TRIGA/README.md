# TRIGA Mark II Reactor — OpenMC Model

![OpenMC](https://img.shields.io/badge/OpenMC-0.15.2-blue)
![Python](https://img.shields.io/badge/Python-3.12-blue)
![Status](https://img.shields.io/badge/status-validated-brightgreen)

Full-core OpenMC model of the **TRIGA Mark II** research reactor of the **University of Pavia** (LENA), developed and validated against experimental data from the facility.

---

## 📂 Contents

| File | Description |
|------|-------------|
| [`triga.ipynb`](triga.ipynb) | Complete workflow: materials, geometry, plots, settings, tallies, run. |

## ⚛️ Model overview

- **Materials** — UZrH fuel (elements 101 and 103), samarium burnable poison disks, graphite reflector, aluminium and steel claddings, light water with S(α,β) thermal scattering.
- **Geometry** — full core with the circular fuel lattice, central channel, the three control rods (**SHIM**, **REG**, **TRANS**), graphite dummy elements, rabbit and source channels, radial graphite reflector with its irradiation channels.
- **Control rods** — positions are set at the top of the geometry section (`z0_shim_value`, `z0_reg_value`, `z0_trans_value`; 0 = fully inserted, 47 = fully withdrawn).
- **Void studies** — the `void_water` flag fills the central-channel case with water or void.
- **Tallies** — neutron energy spectrum (100 log-spaced groups, 10⁻⁵ eV – 20 MeV), 3D flux map on a 60×60×100 mesh, and deposited energy for power normalisation.
- **Settings** — 300 batches (100 inactive) × 120 000 particles, uniform initial source, temperature interpolation.

Reference result (rods at 45 cm): **k<sub>eff</sub> = 1.05004 ± 0.00022**.

## ▶️ How to run

1. Install [OpenMC](https://docs.openmc.org/en/stable/quickinstall.html) (tested with **v0.15.2**) and a nuclear data library, then point `OPENMC_CROSS_SECTIONS` to its `cross_sections.xml`.
2. Open the notebook and run all cells:
   ```bash
   jupyter notebook triga.ipynb
   ```
3. The XML inputs and the `statepoint.300.h5` output are written next to the notebook; geometry plots go to `pictures/geometry/`.

> A full run takes roughly 10 minutes on a modern workstation.

## ✅ Validation

The model has been verified and validated against experimental benchmarks of the Pavia TRIGA reactor:

- Criticality (k<sub>eff</sub>) at different control-rod configurations
- Temperature reactivity coefficients
- Void reactivity coefficients

It also supports the study of **neutron flux shadowing effects**, with simplified and full-core modelling approaches.

## 📚 References

1. 📘 *OpenMC Model Validation of the TRIGA Mark II Reactor* — [ResearchGate](https://www.researchgate.net/publication/377526674)
2. 🌡️ *OpenMC Analysis of TRIGA Mark II Reactor Void and Temperature Reactivity Coefficients* — [ResearchGate](https://www.researchgate.net/publication/377489898)
3. 🌀 *Shadowing Effect Correction for the Pavia TRIGA Reactor Using Monte Carlo Data and Reduced Modelling Techniques* — [ResearchGate](https://www.researchgate.net/publication/384146956)

If you use this model in your work, please cite the relevant papers above.

---

<sub>Originally published in [MP-OFELIA](https://github.com/ERMETE-Lab/MP-OFELIA). Developed at [ERMETE-Lab](https://github.com/ERMETE-Lab), Politecnico di Milano.</sub>
