# menstrual-pomdp

## Menstrual POMDP: Belief-Based Personalization for Cycle Phase Tracking

**Author:** Alina Gavrilov | Stanford University | CS 238: Decision Making Under Uncertainty

## Overview

A proof-of-concept POMDP framework for personalized menstrual onset prediction, modeling latent cycle phase as a hidden state inferred from multimodal Oura Ring wearable data and symptom surveys. The framework maintains a belief distribution over eight latent states (cycle phase x symptom risk level) and selects among four actions: WAIT, QUERY, ALERT, and CARE. Two planning policies are evaluated: a threshold policy with hyperparameter grid search, and Point-Based Value Iteration (PBVI).

Full methodology and results are described in the paper included in this repository.

## Notebook Structure

The notebook follows this sequence:

1. Data loading and preprocessing (Oura biometrics + survey risk flags)
2. HSMM fitting and phase transition model
3. Gaussian Process smoothing of HRV and temperature signals
4. POMDP model construction (states, actions, transitions, observations, rewards)
5. Belief update implementation (Bayesian filtering in log-space)
6. Threshold policy with grid search over hyperparameters
7. PBVI implementation and evaluation
8. Results and diagnostics

## Repository Structure

menstrual-pomdp/
- README.md
- Gavrilov_CS238_Final_Project.pdf
- generative_transition_models.ipynb

## Data

Data was collected as part of an IRB-approved study at Stanford University. It is not included in this repository due to PHI protections.

## Dependencies

Python 3.11, numpy, pandas, scipy, matplotlib

## Paper

Gavrilov_CS238_Final_Project.pdf
