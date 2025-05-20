# CGT4NN

---

![License](https://img.shields.io/github/license/LISA-ITMO/CGT4NN?style=flat&logo=opensourceinitiative&logoColor=white&color=blue)
[![OSA-improved](https://img.shields.io/badge/improved%20by-OSA-yellow)](https://github.com/aimclub/OSA)

Built with:

![jinja2](https://img.shields.io/badge/Jinja-B41717.svg?style={0}&logo=Jinja&logoColor=white)
![numpy](https://img.shields.io/badge/NumPy-013243.svg?style={0}&logo=NumPy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458.svg?style={0}&logo=pandas&logoColor=white)
![pydantic](https://img.shields.io/badge/Pydantic-E92063.svg?style={0}&logo=Pydantic&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikitlearn-F7931E.svg?style={0}&logo=scikit-learn&logoColor=white)
![scipy](https://img.shields.io/badge/SciPy-8CAAE6.svg?style={0}&logo=SciPy&logoColor=white)
![spacy](https://img.shields.io/badge/spaCy-09A3D5.svg?style={0}&logo=spaCy&logoColor=white)

---

## Overview

CGT4NN investigates using game theory to better understand and improve neural networks. It provides a framework for analyzing network behavior, evaluating robustness, and potentially enhancing training processes by modeling network components as interacting players in a strategic environment.

---

## Table of Contents

- [Core features](#core-features)
- [Installation](#installation)
- [Examples](#examples)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)
- [Citation](#citation)

---
## Core features

1. **Compositional Game Theory Application**: The core of the project lies in applying compositional game theory to analyze and improve neural networks, representing network components as players in open games.
2. **CGTNN Library (cgtnnlib)**: A dedicated library providing classes and modules for performing research related to compositional game theory applied to neural networks. Includes components for datasets, analysis, training, and plotting.
3. **Report Generation & Analysis**: The project generates detailed reports (JSON format) containing model parameters, loss curves, evaluation metrics, and noise factor data. These reports are designed for analysis using the `analyze.py` script.
4. **Experiment Management**: The project supports running experiments with configurable parameters (e.g., learning rate, epochs, noise levels) and provides mechanisms for iterating through different experiment configurations.
5. **Neural Network Architectures**: The `nn` subdirectory contains PyTorch modules representing various neural network architectures used in the experiments, including AugmentedReLUNetwork and its variants.
6. **Data Handling & Preprocessing**: The project includes utilities for downloading, preprocessing, and managing datasets from various sources (e.g., PML Benchmark datasets, custom CSV files).

---

## Installation

Install CGT4NN using one of the following methods:

**Build from source:**

1. Clone the CGT4NN repository:
```sh
git clone https://github.com/LISA-ITMO/CGT4NN
```

2. Navigate to the project directory:
```sh
cd CGT4NN
```

3. Install the project dependencies:

```sh
pip install -r requirements.txt
```

---

## Examples

Examples of how this should work and how it should be used are available [here](https://github.com/LISA-ITMO/CGT4NN/tree/main/examples).

---

## Documentation

A detailed CGT4NN description is available [here](https://github.com/LISA-ITMO/CGT4NN/tree/main/doc).

---

## Contributing

- **[Report Issues](https://github.com/LISA-ITMO/CGT4NN/issues)**: Submit bugs found or log feature requests for the project.

---

## License

This project is protected under the MIT License. For more details, refer to the [LICENSE](https://github.com/LISA-ITMO/CGT4NN/tree/main/LICENSE.md) file.

---

## Citation

If you use this software, please cite it as below.

### APA format:

    LISA-ITMO (2025). CGT4NN repository [Computer software]. https://github.com/LISA-ITMO/CGT4NN

### BibTeX format:

    @misc{CGT4NN,

        author = {LISA-ITMO},

        title = {CGT4NN repository},

        year = {2025},

        publisher = {github.com},

        journal = {github.com repository},

        howpublished = {\url{https://github.com/LISA-ITMO/CGT4NN.git}},

        url = {https://github.com/LISA-ITMO/CGT4NN.git}

    }

---
