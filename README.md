# Physics-Guided Deep Learning for Robust Exoplanet Transit Classification

## Project Overview

This project investigates the classification of synthetic exoplanet transit-like signals in NASA Kepler light curves using machine learning and deep learning.

The study evaluates whether Gaussian noise augmentation improves the robustness of a one-dimensional Convolutional Neural Network (1D CNN) under simulated observational noise and transit preprocessing errors.

**Research status:** Preliminary experimental prototype.

## Research Objectives

- Acquire and preprocess Kepler long-cadence light curves.
- Construct paired control and synthetic transit-injected samples.
- Develop local phase-folded representations of light curves.
- Train and evaluate a lightweight 1D CNN.
- Investigate Gaussian noise augmentation.
- Compare CNN performance with Logistic Regression.
- Evaluate robustness under duration and transit-centre errors.

## Dataset

- Mission: NASA Kepler
- Quarter: Q4
- Targets: 50
- Independent target groups: 50
- Samples: 100 paired examples
- Classes: Control (no artificial injection) and synthetic transit injection
- Representation: 24-bin local phase-folded light curves

The dataset uses synthetic box-shaped transit injections. Control samples are not guaranteed to be free of naturally occurring transit signals.

## Models

1. Original 1D CNN
2. Gaussian Noise-Augmented 1D CNN
3. Logistic Regression baseline

## Preliminary Results

| Model | Test Accuracy |
|---|---:|
| Original CNN | 93.75% |
| Noise-Augmented CNN | 100% |
| Logistic Regression | 100% |

The noise-augmented CNN showed improved accuracy over the original CNN at several moderate Gaussian noise levels.

## Important Limitations

- Only 50 independent Kepler targets were used.
- Transit signals were generated using a simplified box-shaped model.
- The classification pipeline uses known synthetic transit parameters for phase folding.
- Gaussian white noise does not represent all real observational noise.
- The experiment does not establish real-world planet detection or confirmation.

## Tools and Technologies

- Python
- Google Colab
- Lightkurve
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- TensorFlow / Keras
- Astropy

## Repository Structure

The repository will contain notebooks, experiment results, figures, research documentation, and model files.

## Author

Ayushi Patel

## Disclaimer

This repository presents a preliminary research prototype for synthetic transit-signal classification. Its results should not be interpreted as validated exoplanet detection performance.
