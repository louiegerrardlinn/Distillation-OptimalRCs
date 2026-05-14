# Distillation-OptimalRCs

## Overview

This repository contains the Python code and analysis for my undergraduate dissertation at the University of Leeds:

**"Distillation of Optimal Reaction Coordinates using Advanced Neural Network Architectures"**

The project investigates whether modern neural network architectures can recover physically meaningful reaction coordinates from protein folding dynamics using committor theory and dynamical validation.

The study compares:

* Long Short-Term Memory (LSTM) networks
* Transformer architectures

for their ability to reproduce a rigorously validated committor function derived from HP35 protein folding trajectories.

---

## Scientific Background

Protein folding is a high-dimensional dynamical process.
A reaction coordinate provides a low-dimensional description of folding progress.

The mathematically optimal reaction coordinate is the **committor function**, which represents the probability that a system will reach the folded state before returning to the unfolded state.

While neural networks can often approximate the committor numerically, this project investigates whether they also preserve the underlying physical dynamics of the system.

To evaluate this, models were assessed using:

* Pearson correlation
* Mean squared error (MSE)
* Free energy profile (FEP) reconstruction
* Zq dynamical validation criterion

---

## Main Findings

### Generalised Models

Both LSTM and Transformer models achieved extremely high numerical agreement with the benchmark committor:

* Pearson correlation > 0.99
* Strong agreement with free energy profiles

However:

* Neither architecture satisfied the Zq dynamical validation criterion
* This suggests numerical accuracy alone does not guarantee physically correct dynamics

### Approximation Capacity Test

A Transformer trained on the entire trajectory without generalisation constraints successfully reproduced:

* the committor function
* free energy profiles
* Zq validation behaviour

This demonstrated that the limitation was not model capacity, but reconstructing full dynamical information from incomplete trajectory data.

---

## Repository Structure

| File                                        | Description                                          |
| ------------------------------------------- | ---------------------------------------------------- |
| `LSTM-Repository.ipynb`                     | LSTM architecture implementation and analysis        |
| `Transformer-Repository.ipynb`              | Generalised Transformer model implementation         |
| `Approximating power test-repository.ipynb` | Full-trajectory Transformer approximation experiment |

---

## Technologies Used

* Python
* PyTorch
* NumPy
* Matplotlib
* Jupyter Notebook

---

## Skills Demonstrated

* Deep learning model development
* Sequential data modelling
* Transformer architectures
* Scientific machine learning
* Time-series analysis
* Large-scale data processing
* Statistical model evaluation
* Dynamical systems analysis
* Scientific visualization

---

## Key Concepts

* Reaction coordinates
* Committor functions
* Protein folding dynamics
* Free energy landscapes
* Rare-event dynamics
* Dynamical validation
* LSTM memory architectures
* Self-attention / Transformers

---

## Dissertation Context

This work was completed as part of my undergraduate degree at the University of Leeds.

The project focused on combining machine learning with molecular biophysics to investigate whether neural networks can learn physically meaningful representations of complex dynamical systems.

---

## Author

Louie Gerrard-Linn

University of Leeds
BSc Biological Sciences
