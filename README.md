# Interpretable-Sine-SLP
Interpretable single-layer perceptron(SLP) with sinusoidal activation to map and interpret model parameters as data frequencies for signal analysis.

---

## 📌 Research Motivation & Overview
* **Background:** Standard neural networks often operate as black-box approximators.
* **Core Idea:** Using $\sin(Wx + b)$ activation layers to directly map network weights ($W$) to harmonic frequency components.
* **Interpretability:** Enables parameter-level explainability in the frequency domain without relying on black-box.

---

## 🔬 Mathematical Formulation
$$y = \sum_{i=1}^{K} v_i \cdot \sin(w_i x + \phi_i) + b$$

* $w_i \in W$: Learned weights corresponding to fundamental frequencies.
* $\phi_i \in \Phi$: Phase offset parameters.
* $v_i \in V$: Linear combination coefficients (spectral amplitude).

---

## 📊 Key Results & Visualizations
| Parameter Spectrum vs. Ground Truth | Signal Reconstruction |
| :---: | :---: |
| ![Spectrum](assets/weight_spectrum.png) | ![Reconstruction](assets/signal_reconstruction.png) |

---

## 📁 Project Structure
```text
Interpretable-Sine-SLP/
├── assets/                  # Figures and visualization plots
├── data/                    # Sample signal datasets
├── models/
│   └── sine_slp.py          # Custom Sine Layer and SLP implementation
├── utils/
│   ├── signal_loader.py     # Signal preprocessing
│   └── fourier_metrics.py   # Fourier analysis and frequency evaluation
├── demo_interpretability.ipynb # Interactive demo notebook
├── requirements.txt         # Dependencies
└── README.md
