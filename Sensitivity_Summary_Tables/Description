## Sensitivity Summary Table

These table report the sensitivity of Big Bang Nucleosynthesis (BBN) observables to variations in fundamental and nuclear parameters, computed using [PRyMordial](https://github.com/valluri/PRyMordial). Each row corresponds to a single (parameter, compilation, observable) combination. 

An easy to read version of this table is available here: https://docs.google.com/spreadsheets/d/1Ti9dJcO_a7xftWVwTKQciguHgpE_WNq3TINKYAiSZGs/edit?usp=sharing

### Column Descriptions

| Column | Description |
|--------|-------------|
| **Parameter** | The scanned input parameter (e.g., $\alpha_{\rm EM}$, $G_F$, $\tau_n$, nuclear rate shifts $p_$, etc.). |
| **Compilation** | The nuclear reaction rate compilation used: PRIMAT or NACRE-II. |
| **Fiducial parameter value** | The Standard Model (or default) value of the parameter at which derivatives are evaluated. |
| **Observable** | The BBN observable: $Y_p$ (helium-4 mass fraction), D/H $\times 10^5$ (deuterium-to-hydrogen ratio), ${}^7$Li/H $\times 10^{10}$ (lithium-7-to-hydrogen ratio), or $N_{\rm eff}$ (effective number of neutrino species). |
| **$Y_{\rm fid}$** | The predicted value of the observable at the fiducial parameter value. |
| **$d\ln Y/d\ln p$** ($dY/dp$) | The logarithmic derivative of the observable with respect to the parameter, evaluated at the fiducial point via finite differences. The absolute derivative $dY/dp$ is given instead for parameters in which the fiducial value is 0. |
| **$\text{lin\_R}^2$** ($\text{flat\_R}^2_{\rm tol}$) | The $R^2$ of a linear fit to the scan data across the full scan range, indicating how well a straight line describes the observable's response. The tolerance-based flatness score $\text{flat\_R}^2_{\rm tol}$ is given instead when the sensitvity curve is so flat that numerical noise causes the value of $\text{lin\_R}^2$ to be nonsensical. $\text{flat\_R}^2_{\rm tol}$ are marked with an *.|

### Note on nuclear rate parameters

For nuclear reaction rate parameters (those labeled `NP_delta_*`, e.g., `NP_delta_npdg`, `NP_delta_ddHe3n`, etc.), the scan parameter is **not** the rate itself but the number of standard deviations ($\sigma$) by which the rate is shifted in the lognormal uncertainty model. For example, `NP_delta_npdg = 1` corresponds to a $+1\sigma$ shift in the $n + p \to d + \gamma$ rate, and `NP_delta_npdg = -2` corresponds to a $-2\sigma$ shift. The fiducial value for all nuclear rate parameters is therefore 0 (no shift from the central rate). Since the fiducial value is zero, the logarithmic derivative $d\ln Y/d\ln p$ is undefined for these parameters; only the absolute derivative $dY/dp$ (i.e., the change in the observable per sigma shift) is meaningful.


### Interpreting special values

- **$d\ln Y/d\ln p = 0$ (or $dY/dp = 0$):** The observable is insensitive to the parameter at the fiducial point — the finite-difference slope across the bracketing scan points is zero. This typically means the observable does not respond to variations in that parameter over the scan range beyond the numerical noise floor.

- **$\text{lin\_R}^2 = 1$:** The linear fit has zero residuals across the scan. This can arise in two distinct situations:
  1. The observable responds **perfectly linearly** to the parameter over the entire scan range.
  2. The observable is **effectively flat** (constant) over the scan range, in which case the total variance is smaller than the numerical noise floor and the $R^2 = 1$ is vacuous.

- **$d\ln Y/d\ln p = 0$, $dY/dp = 0$, and $\text{lin\_R}^2 = 1$ together:** The observable is constant with respect to the parameter over the scan range. 
