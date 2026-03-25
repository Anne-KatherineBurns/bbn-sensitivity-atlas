# BBN Sensitivity Atlas: Supplementary Material

Supplementary plots, tables, and numerical results for:

**"Inside the Black Box of Big Bang Nucleosynthesis: Parameter Sensitivity Studies in Light of New LBT Data"**

Anne-Katherine Burns — [annekatherineburns@icc.ub.edu](mailto:annekatherineburns@icc.ub.edu)

Institut de Ciències del Cosmos de la Universitat de Barcelona, Barcelona, Spain

<img width="1395" height="1037" alt="Screenshot 2026-03-19 at 10 55 30" src="https://github.com/user-attachments/assets/840e8a8d-1672-418f-a53b-f7f6e93b91a2" />

Schematic overview of the BBN calculation as implemented in [PRyMordial](https://github.com/vallima/PRyMordial). The three computational stages: background thermodynamics , neutron--proton interconversion rates and the nuclear reaction network are shown along with their three outputs: $N_\text{eff}$, the relic neutrino abundance, and the final light-element abundances. Each colored circle represents a fundamental input parameter varied in this analysis. The symbols described in the legend indicate whether a given quantity depends on the photon temperature, neutrino temperature, or scale factor. Arrows trace how each input propagates through the calculation. [View PDF Here](https://github.com/user-attachments/files/26111488/PRyMordial_BBBBN.pdf) 

---

## Overview

This repository contains the full set of numerical results accompanying the BBN sensitivity atlas. We provide response functions, sensitivity coefficients, and uncertainty budgets for **14 fundamental physics and cosmological parameters** and **63 thermonuclear reaction rates**. All results are computed using [PRyMordial](https://github.com/vallima/PRyMordial) and presented for two nuclear reaction rate compilations (PRIMAT and NACRE-II) and two weak-rate normalization schemes ($\tau_n$ and fundamental). 

---

## Plots

Each parameter directory contains plots of the predicted primordial abundances ($Y_p$, D/H $\times 10^5$, ${}^7$Li/H $\times 10^{10}$, and $N_{\text{eff}}$ where applicable) as a function of the fractional parameter variation $\Delta p / p$. All plots show results for both the PRIMAT (blue) and NACRE-II (red/orange) nuclear reaction rate compilations, with observational bands from:

- **Helium-4**: LBT ([Aver et al. 2026](https://arxiv.org/abs/2601.22238)) and EMPRESS ([Matsumoto et al. 2022](https://arxiv.org/abs/2203.09617))
- **Deuterium**: PDG world average, 2025 update ([Navas et al. 2025](https://ccwww.kek.jp/pdg/2025/reviews/rpp2025-rev-bbang-nucleosynthesis.pdf))
- **Lithium-7**: PDG recommended value, 2025 update ([Navas et al. 2025](https://ccwww.kek.jp/pdg/2025/reviews/rpp2025-rev-bbang-nucleosynthesis.pdf))
- **N_eff**: CMB+BBN+BAO ([Goldstein and Hill 2026](https://arxiv.org/pdf/2603.13226))

Plots are provided for all parameters under both the $\tau_n$ and fundamental normalization schemes. Parameters with negligible impact on the abundances ($\Delta\kappa$, $r_p$, $m_Z$) are included here for completeness but are not shown in the main paper.

---

# Parameters Studied

### Fundamental Physics and Cosmological Parameters (14)

| Symbol | Parameter | Fiducial Value |
|--------|-----------|---------------|
| τ_n | Neutron lifetime | 878.4 s |
| Q | Neutron-proton mass difference | 1.29333 MeV |
| α_EM | Fine structure constant | 0.00729735 |
| G_F | Fermi constant | 1.16638 × 10⁻¹¹ MeV⁻² |
| m_e | Electron mass | 0.510999 MeV |
| g_A | Nucleon axial coupling | 1.2753 |
| V_ud | CKM matrix element | 0.97367 |
| Δκ | Weak magnetism constant | 3.70589 |
| r_p | Proton radius | 8.409 × 10⁻¹⁴ cm |
| m_Z | Z boson mass | 91188.0 MeV |
| G_N | Gravitational constant | 6.70883 × 10⁻⁴⁵ MeV⁻² |
| Ω_b h² | Baryon abundance | 0.02237 |
| ξ_ν | Neutrino degeneracy parameter | 0 |
| ΔN_eff | Effective number of relativistic neutrino species | 0 |

### Key Thermonuclear Reaction Rates (12 of 63)

The following 12 reactions meet our significance threshold (a 1% change in the rate produces at least a 0.001% shift in any abundance). Results for all 12 are presented for both the PRIMAT and NACRE-II compilations.

| # | Reaction |
|---|----------|
| 1 | n + p → d + γ |
| 2 | d + p → ³He + γ |
| 3 | d + d → ³He + n |
| 4 | d + d → t + p |
| 5 | t + p → ⁴He + γ |
| 6 | t + d → ⁴He + n |
| 7 | t + ⁴He → ⁷Li + γ |
| 8 | ³He + n → t + p |
| 9 | ³He + d → ⁴He + p |
| 10 | ³He + ⁴He → ⁷Be + γ |
| 11 | ⁷Be + n → ⁷Li + p |
| 12 | ⁷Li + p → ⁴He + ⁴He |

### Full Nuclear Reaction Network (63 reactions)

The complete network implemented in PRyMordial contains the following 63 reactions. Sensitivity plots for all 63 are provided here; the 12 key reactions above are those exceeding the significance threshold defined in the paper.

| # | Reaction | Code label |
|---|----------|------------|
| 1 | n + p → d + γ | npdg |
| 2 | d + p → ³He + γ | dpHe3g |
| 3 | d + d → ³He + n | ddHe3n |
| 4 | d + d → t + p | ddtp |
| 5 | t + p → ⁴He + γ | tpag |
| 6 | t + d → ⁴He + n | tdan |
| 7 | t + ⁴He → ⁷Li + γ | taLi7g |
| 8 | ³He + n → t + p | He3ntp |
| 9 | ³He + d → ⁴He + p | He3dap |
| 10 | ³He + ⁴He → ⁷Be + γ | He3aBe7g |
| 11 | ⁷Be + n → ⁷Li + p | Be7nLi7p |
| 12 | ⁷Li + p → ⁴He + ⁴He | Li7paa |
| 13 | ⁷Li + p → ⁴He + ⁴He + γ | Li7paag |
| 14 | ⁷Be + n → ⁴He + ⁴He | Be7naa |
| 15 | ⁷Be + d → ⁴He + ⁴He + p | Be7daap |
| 16 | d + ⁴He → ⁶Li + γ | daLi6g |
| 17 | ⁶Li + p → ⁷Be + γ | Li6pBe7g |
| 18 | ⁶Li + p → ³He + ⁴He | Li6pHe3a |
| 19 | ⁸B + n → ⁴He + ⁴He + p | B8naap |
| 20 | ⁶Li + ³He → ⁴He + ⁴He + p | Li6He3aap |
| 21 | ⁶Li + t → ⁴He + ⁴He + n | Li6taan |
| 22 | ⁶Li + t → ⁸Li + p | Li6tLi8p |
| 23 | ⁷Li + ³He → ⁶Li + ⁴He | Li7He3Li6a |
| 24 | ⁸Li + ³He → ⁷Li + ⁴He | Li8He3Li7a |
| 25 | ⁷Be + t → ⁶Li + ⁴He | Be7tLi6a |
| 26 | ⁸B + t → ⁷Be + ⁴He | B8tBe7a |
| 27 | ⁸B + n → ⁶Li + ³He | B8nLi6He3 |
| 28 | ⁸B + n → ⁷Be + d | B8nBe7d |
| 29 | ⁶Li + t → ⁷Li + d | Li6tLi7d |
| 30 | ⁶Li + ³He → ⁷Be + d | Li6He3Be7d |
| 31 | ⁷Li + ³He → ⁴He + ⁴He + d | Li7He3aad |
| 32 | ⁸Li + ³He → ⁴He + ⁴He + t | Li8He3aat |
| 33 | ⁷Be + t → ⁴He + ⁴He + d | Be7taad |
| 34 | ⁷Be + t → ⁷Li + ³He | Be7tLi7He3 |
| 35 | ⁸B + d → ⁷Be + ³He | B8dBe7He3 |
| 36 | ⁸B + t → ⁴He + ⁴He + ³He | B8taaHe3 |
| 37 | ⁷Be + ³He → p + p + ⁴He + ⁴He | Be7He3ppaa |
| 38 | d + d → ⁴He + γ | ddag |
| 39 | ³He + ³He → ⁴He + p + p | He3He3app |
| 40 | ⁷Be + p → ⁸B + γ | Be7pB8g |
| 41 | ⁷Li + d → ⁴He + ⁴He + n | Li7daan |
| 42 | d + n → t + γ | dntg |
| 43 | t + t → ⁴He + n + n | ttann |
| 44 | ³He + n → ⁴He + γ | He3nag |
| 45 | ³He + t → ⁴He + d | He3tad |
| 46 | ³He + t → ⁴He + n + p | He3tanp |
| 47 | ⁷Li + t → ⁴He + ⁴He + n | Li7taan |
| 48 | ⁷Li + ³He → ⁴He + ⁴He + n + p | Li7He3aanp |
| 49 | ⁸Li + d → ⁷Li + t | Li8dLi7t |
| 50 | ⁷Be + t → ⁴He + ⁴He + n + p | Be7taanp |
| 51 | ⁷Be + ³He → ⁴He + ⁴He + p + p | Be7He3aapp |
| 52 | ⁶Li + n → t + ⁴He | Li6nta |
| 53 | ³He + t → ⁶Li + γ | He3tLi6g |
| 54 | ⁴He + n + p → ⁶Li + γ | anpLi6g |
| 55 | ⁶Li + n → ⁷Li + γ | Li6nLi7g |
| 56 | ⁶Li + d → ⁷Li + p | Li6dLi7p |
| 57 | ⁶Li + d → ⁷Be + n | Li6dBe7n |
| 58 | ⁷Li + n → ⁸Li + γ | Li7nLi8g |
| 59 | ⁷Li + d → ⁸Li + p | Li7dLi8p |
| 60 | ⁸Li + p → ⁴He + ⁴He + n | Li8paan |
| 61 | ⁴He + n + n → ⁶He + γ | annHe6g |
| 62 | p + p + n → d + p | ppndp |
| 63 | ⁷Li + t → ⁴He + ⁴He + n + n | Li7taann |

---

## Tables

### Sensitivity Coefficients

For fundamental physics parameters, each entry reports:
- The logarithmic sensitivity coefficient $d \ln Y / d \ln p$ evaluated at the SM fiducial value
- The linear-fit quality $R^2$
- Results for both PRIMAT and NACRE-II compilations

For the non-standard parameters $\Delta N_{\text{eff}}$ and $\xi_\nu$ (whose fiducial values are zero), we report $dY/dp$ instead.

For nuclear reaction rates, sensitivities are reported as $dY/dp$ where $p$ is the lognormal rate-shift parameter in units of the quoted $1\sigma$ uncertainty.

### Uncertainty Budgets

Each file contains the ranked decomposition of the total theoretical uncertainty for each observable, with columns:
- `Parameter`: input parameter or reaction rate
- `sigma_Yi`: absolute contribution to the uncertainty, $\sigma_{Y_i} = |dY/dp_i| \sigma_{p_i}$
- `frac_var`: fractional contribution to the total variance

---

## Observational Values Used

| Observable                         | Value                          | Source        |
|------------------------------------|--------------------------------|---------------|
| $Y_p$                             | $0.2458 \pm 0.0013$           | LBT (2026)    |
| $Y_p$                             | $0.2370^{+0.0034}_{-0.0033}$  | EMPRESS (2022)|
| D/H $\times 10^5$                 | $2.508 \pm 0.029$             | PDG (2025)    |
| Li-7/H $\times 10^{10}$           | $1.45 \pm 0.25$               | PDG (2025)    |
| $N_{\text{eff}}$                  | $2.990 \pm 0.070$             | CMB+BBN+BAO (2026)|

---

## How to Use This Atlas

The sensitivity coefficients provided here allow rapid estimates of how shifts in input parameters affect the predicted primordial abundances. For a single parameter variation:

$$\delta Y \approx \frac{d \ln Y}{d \ln p} \times Y_{\text{fid}} \times \frac{\delta p}{p_{\text{fid}}}$$

For BSM scenarios involving simultaneous variations of multiple parameters with a covariance matrix $C_{ij}$:

$$\sigma_Y^2 = \sum_{i,j} \frac{\partial Y}{\partial p_i} C_{ij} \frac{\partial Y}{\partial p_j}$$

The individual derivatives provided here are the building blocks for this calculation. Note that the sensitivities are computed locally about SM fiducial values; for large deviations, the nonlinearity indicated by $R^2 < 1$ should be taken into account.

---

## Citation

If you use the results in this repository, please cite:

```bibtex
@article{Burns:2026wlw,
    author = "Burns, Anne-Katherine",
    title = "{Inside the Black Box of Big Bang Nucleosynthesis: Parameter Sensitivity Studies in Light of new LBT Data}",
    eprint = "2603.22414",
    archivePrefix = "arXiv",
    primaryClass = "hep-ph",
    month = "3",
    year = "2026"
}
```

---

## Related Code

The BBN calculations in this work were performed using [PRyMordial](https://github.com/vallima/PRyMordial). See [Burns, Tait & Valli (2024)](https://arxiv.org/abs/2302.08281) for documentation of the code.

---

## Contact

Anne-Katherine Burns — [annekatherineburns@icc.ub.edu](mailto:annekatherineburns@icc.ub.edu)
