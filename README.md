# Micro-Macro Modeling of Statistical Collapse and Spurious Homogeneity

This repository contains a collection of large-scale Monte Carlo simulation codes designed to demonstrate the collapse of Euclidean distance, the loss of Fisher Information due to cognitive biases, and the resulting phenomena of "Spurious Homogeneity" and computational collapse in high-dimensional subjective data (e.g., 5-point Likert scales). 
It also includes simulation codes for the Information Epidemic Model (TMFG) on scale-free networks.

## Overview
We verify and demonstrate, hypothesis by hypothesis, how conventional statistical approaches, distance-based clustering (such as K-means), and supervised generalized linear models fail in high-dimensional, sparse, and subjective data spaces. 
All simulations are based on a randomized Data Generating Process (DGP) that eliminates initial-value dependencies, and statistical sufficiency is mathematically guaranteed by the Monte Carlo Standard Error (MCSE).

## File Structure

### 1. Information Epidemic & Network Models (TMFG)
* **`TMFG_Hypothesis１.ipynb`**
  * Investigates the dynamics of topological defect accumulation in scale-free networks (BA model). Compares information diffusion originating from hub nodes (superspreaders) versus random general nodes.
* **`TMFG_Hypothesis2.ipynb`**
  * Simulates the propagation of peer pressure and metastasis to the majority (cascade dynamics) within clustered scale-free networks.
* **`TMFG_Hypothesis３.ipynb`**
  * Evaluates the asymmetry of intervention effects between preventive additive measures (simplicial complex models via triad construction) and subtractive post-BAN interventions.

### 2. Hypothesis Testing Simulations (Statistical Collapse & Brittleness)
* **`hypothesis2_fisher_collapse.ipynb`**
  * Verifies the non-linear loss of Fisher Information (forming an inverse U-curve) caused by variations in cognitive confidence ($\beta$).
* **`hypothesis3_integrated_collapse.ipynb`**
  * Demonstrates the non-linear explosion of the critical sample size ($N^*$) required to capture identical populations, driven by the combined effects of physical sparsity (H1) and cognitive noise (H2).
* **`hypothesis3_phase_transition.ipynb`**
  * Fits the phase transition curves of statistical collapse using sigmoid functions and analyzes the collapse acceleration parameter ($\kappa$) as dimensionality increases.
* **`hypothesis3_brittleness_boundary.ipynb`**
  * Identifies the absolute "Brittleness Threshold" where the phase transition converts into a near-vertical cliff through a high-resolution granular scan.

### 3. Collapse of Clustering and Regression Analysis (Spurious Clustering & Silent Degeneracy)
* **`hypothesis4_combinatorial_collapse.ipynb`**
  * Simulates the collapse of Euclidean distance contrast caused by the intersection of demographic segments (D) and Likert-scale dimensions (M).
* **`hypothesis4_spurious_clustering_10M (1).ipynb`**
  * Verifies through an ultra-fast scan that K-means clustering continuously generates "Spurious Homogeneity" (ARI collapse) at macroscopic observational scales up to 10,000,000 samples.
* **`regression_calibration_results.ipynb`**
  * Demonstrates "Silent Degeneracy" in high-dimensional logistic regression, where the algorithm converges without warnings while the Mean Squared Error (MSE) of coefficients explodes and spurious significance (FWER $\to 1.0$) is systematically manufactured.

## Requirements and Execution Environment
These codes are designed to run in a Python 3.x environment. Due to the heavy reliance on `joblib` and `numba` for parallel processing and acceleration, executing them in **Google Colaboratory** is highly recommended.

The required libraries are listed below:

```bash
pip install -r requirements.txt
