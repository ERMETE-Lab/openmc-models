# openmc-models

A collection of reactor models developed by [ERMETE-Lab](https://github.com/ERMETE-Lab) (Politecnico di Milano) for the Monte Carlo particle transport code [OpenMC](https://openmc.org/).

Each model lives in its own folder, with a notebook to build, run and post-process the simulation and a README describing the model and its validation.

## Models

| Model | Description |
|-------|-------------|
| [TRIGA](TRIGA/) | TRIGA Mark II research reactor of the University of Pavia, validated against experimental data (k<sub>eff</sub>, temperature and void reactivity coefficients). |

## Requirements

- [OpenMC](https://docs.openmc.org/en/stable/quickinstall.html) (tested with v0.15.2) with a nuclear data library (set `OPENMC_CROSS_SECTIONS`)
- Python 3 with `numpy` and Jupyter

## History

The TRIGA model was originally published in [MP-OFELIA](https://github.com/ERMETE-Lab/MP-OFELIA) (`Tutorials/openmc/TRIGA`) and was moved here, together with its commit history, when the `openmc-*` repository family was created.

## License

Released under the [MIT License](LICENSE).
