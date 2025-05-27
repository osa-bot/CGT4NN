# CGT4NN

---

![License](https://img.shields.io/github/license/LISA-ITMO/CGT4NN?style=flat&logo=opensourceinitiative&logoColor=white&color=blue)
[![OSA-improved](https://img.shields.io/badge/improved%20by-OSA-yellow)](https://github.com/aimclub/OSA)

---

## Overview

CGT4NN explores how well neural networks perform when faced with uncertainty and variations during training. It provides tools to systematically test these networks by intentionally adding 'noise' or changing settings while they learn, then visually comparing the results. The core goal is to understand *why* some networks are more reliable than others in real-world situations where data isn’t always perfect. 

The system automates the process of training multiple versions of a network under different conditions and generates easy-to-understand reports and charts showing how performance changes. A key approach involves treating each layer of the neural network as an independent component, analyzing their interactions to improve stability. This is achieved through a modified technique called DropGrad, which helps networks become more robust. Ultimately, CGT4NN aims to provide insights into building more dependable machine learning models and offers methods for optimizing them against unpredictable factors.

---

## Repository content

The CGT4NN repository focuses on analyzing and improving the robustness of neural networks using a game-theoretic approach. It comprises several key components working together to achieve this goal.

The `datasets` module provides access to various datasets, including those from Penn Machine Learning Benchmarks, used for training and evaluating the models. These datasets are encapsulated within `Dataset` objects, facilitating standardized data handling.

The core neural network model is defined in `AugmentedReLUNetwork.py`. This model incorporates a modified regularization technique based on DropGrad to enhance resilience to noise. The `training` module handles the training process of these models using datasets and experiment parameters. It includes functions for creating, training, and evaluating models, as well as saving results.

The `cgtnnlib` directory contains essential utilities for analysis and reporting. Specifically, `analyze.py` provides routines to analyze experimental results, generate plots, and create reports detailing model performance under different conditions. The `Report` class manages the storage and retrieval of these results.  The project also utilizes a custom layer (`GradientDropoutReLULayer`) within the neural network architecture.

The interaction between these components is as follows: Datasets are loaded and used by the training module to train AugmentedReLUNetwork models with DropGrad regularization. The trained models' performance is then analyzed using the tools in `analyze.py`, generating reports that provide insights into their robustness and behavior, ultimately supporting the project’s goal of understanding and improving neural network resilience through a game-theoretic framework.

---

## Used algorithms

The CGT4NN codebase utilizes several algorithms centered around training, analyzing, and visualizing neural network performance under varying conditions. 

**Neural Network Training:** The core algorithm involves standard supervised learning to train neural networks (specifically an `AugmentedReLUNetwork` is mentioned). This process adjusts the network's internal parameters to minimize errors on a given dataset.

**Noise Injection:** During training, noise is intentionally added. This algorithm simulates real-world imperfections or uncertainties in data and tests how well the neural network can maintain performance despite these disturbances.

**DropGrad Regularization (Modified):**  Inspired by game theory, this regularization technique randomly drops gradients during standard supervised training – unlike typical meta-learning approaches. It aims to improve the robustness of the network by preventing individual layers from becoming overly reliant on specific inputs or connections.

**Report Generation:** This algorithm compiles key metrics collected during training (like loss values and evaluation scores) into structured reports, providing a summary of each experiment's outcome.

**Statistical Analysis & Visualization:** Algorithms are used to analyze the generated reports. These include calculating mean performance curves and quantile ranges to represent uncertainty in results.  Visualization algorithms then translate this data into plots that visually compare different experimental setups (e.g., varying noise levels or regularization parameters) and highlight their impact on network behavior.

**Game-Theoretic Modeling:** While not a traditional algorithm *executed* by the code, the project employs a game-theoretic framework to *understand* neural networks. This involves modeling each layer of the network as an independent player interacting with others during learning, providing insights into how regularization affects their strategies and overall system stability.

---
