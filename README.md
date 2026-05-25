# Robust High-Speed 16-QAM Demodulation for UWOC 🌊

[cite_start]An optimized, data-driven machine learning pipeline for demodulating high-speed 16-Quadrature Amplitude Modulation (16-QAM) signals in Underwater Wireless Optical Communication (UWOC) systems[cite: 11, 12]. 

[cite_start]This project addresses the severe computational bottlenecks of traditional temporal receivers by utilizing a custom spatial feature engineering pipeline and an Attention-Based Residual Network (Attention-ResNet)[cite: 13, 15]. 

## 🚀 Key Achievements
* [cite_start]**Massive Throughput Increase:** Replaced heavy temporal oversampling with a single-sample $(M=1)$ spatial classification framework, increasing the theoretical Effective Bit Rate (EBR) limit from ~3.1 Gbps to 50.0 Gbps[cite: 13, 17].
* [cite_start]**Extreme Resilience:** Successfully mitigated constellation collapse at the critical -28.0 dBm failure threshold, maintaining a functional link state where traditional algorithms completely fail[cite: 16, 320].
* [cite_start]**Optimized for the Edge:** Implemented a computationally lightweight Histogram-based Gradient Boosting model that achieves near-parity with deep neural networks, heavily optimizing runtime for power-constrained underwater vehicles[cite: 183, 323].

## 🧠 The Problem & Solution
[cite_start]Underwater optical signals suffer from severe absorption, scattering, and refractive index fluctuations[cite: 25]. [cite_start]At low Received Optical Power (ROP), this causes amplitude scintillation (Log-Normal fading) and phase jitter, heavily distorting the signal[cite: 27]. 

[cite_start]Instead of forcing a model to map these raw, non-linear distortions, this project engineered a highly optimized $\mathbb{R}^{7}$ spatial feature vector[cite: 13, 319]. [cite_start]By extracting mathematical features like Symbol Energy $(E_{sym})$ and an I-Q Cross-Product $(P_{IQ})$, we provided the models with synthetic diagonal decision boundaries, allowing them to rapidly resolve quadrant-crossing errors and radial dispersion[cite: 147, 154].