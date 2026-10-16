# TRIGA Mark II Reactor Model in OpenMC

This folder contains an OpenMC model of the TRIGA Mark II reactor, developed and validated using experimental data from the TRIGA reactor at the University of Pavia.

# Contents

- _triga.ipynb_: Jupyter notebook containing the full workflow for setting up, running, and analyzing the TRIGA Mark II reactor simulation using OpenMC.

# Description

The model simulates the TRIGA Mark II research reactor using the Monte Carlo particle transport code OpenMC. It includes core geometry, material definitions, simulation parameters, and post-processing tools. The model has been verified and validated against experimental benchmarks, including:

- Criticality (keff) at various configurations
- Temperature reactivity coefficients
- Void reactivity coefficients

Additionally, the notebook includes analysis supporting the study of neutron flux shadowing effects, with simplified and full-core modeling approaches.

# Validation References

The TRIGA OpenMC model has been validated through comparison with experimental and benchmark data published in the following peer-reviewed works:

📘 _OpenMC Model Validation of the TRIGA Mark II Reactor_ https://www.researchgate.net/publication/377526674

🌡️ _OpenMC Analysis of TRIGA Mark II Reactor Void and Temperature Reactivity Coefficients_
https://www.researchgate.net/publication/377489898

🌀 _Shadowing Effect Correction for the Pavia TRIGA Reactor Using Monte Carlo Data and Reduced Modelling Techniques_
https://www.researchgate.net/publication/384146956

