# Computational Neuroscience: Reproduction of Ben-Yishai et al. (1995)

A numerical implementation and qualitative reproduction of the recurrent ring attractor model of orientation selectivity in the primary visual cortex (V1), originally proposed in:

> **R. Ben-Yishai, R. Lev Bar-Or, and H. Sompolinsky (1995).**  
> *Theory of orientation tuning in visual cortex.*  
> Proceedings of the National Academy of Sciences (PNAS), 92(9), 3844–3848.

---

## Full Notebook & Report
* **[View Complete Jupyter Notebook & Analysis (PDF)](./Benyishai1995-Reproduction-Priyanshi.pdf)** — Contains all mathematical derivations, simulation code, parameter sweeps, and generated figures.

---
## 🧠 Overview & Key Results Reproduced

This project implements a discretized firing-rate ring model with *N* orientation-selective neuronal populations arranged on a ring θ ∈ [-π/2, π/2):

    τ · dm(θ, t)/dt = -m(θ, t) + [ I_ext(θ) + ∫_{-π/2}^{π/2} (dθ' / π) J(θ - θ') m(θ', t) - T ]

where synaptic connectivity follows a cosine-tuned profile `J(θ - θ') = -J₀ + J₂ cos(2(θ - θ'))`.



### Replicated Phenomena
1. **Orientation Selectivity & Tuning Curves:** Demonstrated sharp, contrast-invariant orientation tuning emerging from recurrent cortical amplification even under weakly tuned feedforward thalamic input.
2. **Phase Transitions (Uniform vs. Marginal Phase):** Explored stability boundaries between uniform inhibition ($J_2 < J_{2c}$) and the marginal phase ($J_2 > J_{2c}$), where spontaneous symmetry breaking sustains localized activity bumps without tuned external input.
3. **Virtual Rotation of Activity Bumps:** Simulated dynamic tracking and smooth rotation of neuronal activity bumps in response to shifting stimulus orientations.
4. **Temporal Cross-Correlation Dynamics:** Reproduced characteristic cross-correlation profiles across pairs of neurons with preferred orientations $\theta_1$ and $\theta_2$, illustrating network-driven temporal fluctuations.

---

## Tech Stack
* **Language:** Python 3
* **Scientific Computing & Visualization:** NumPy, SciPy, Matplotlib

---

## Author
**Priyanshi**  
B.E. Computer Science & Engineering (Artificial Intelligence), Chitkara University  
[GitHub](https://github.com)
