# Robust High-Speed 16-QAM Demodulation for UWOC 🌊

An optimized, data-driven machine learning pipeline for demodulating high-speed 16-Quadrature Amplitude Modulation (16-QAM) signals in Underwater Wireless Optical Communication (UWOC) systems. 

This project addresses the severe computational bottlenecks of traditional temporal receivers by utilizing a custom spatial feature engineering pipeline and an Attention-Based Residual Network (Attention-ResNet). 

## 🚀 Key Achievements

* **Massive Throughput Increase:** Replaced heavy temporal oversampling with a single-sample ($M=1$) spatial classification framework, increasing the theoretical Effective Bit Rate (EBR) limit from ~3.1 Gbps to 50.0 Gbps.
* **Extreme Resilience:** Successfully mitigated constellation collapse at the critical -28.0 dBm failure threshold, maintaining a functional link state where traditional algorithms completely fail.
* **Optimized for the Edge:** Implemented a computationally lightweight Histogram-based Gradient Boosting model that achieves near-parity with deep neural networks, heavily optimizing runtime for power-constrained underwater vehicles.

## 🧠 The Problem & Solution

Underwater optical signals suffer from severe absorption, scattering, and refractive index fluctuations. At low Received Optical Power (ROP), this causes amplitude scintillation (Log-Normal fading) and phase jitter, heavily distorting the signal.

Instead of forcing a model to map these raw, non-linear distortions, this project engineered a highly optimized $\mathbb{R}^{7}$ spatial feature vector. By extracting mathematical features like Symbol Energy ($E_{sym}$) and an I-Q Cross-Product ($P_{IQ}$), we provided the models with synthetic diagonal decision boundaries, allowing them to rapidly resolve quadrant-crossing errors and radial dispersion.