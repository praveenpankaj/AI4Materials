# AI4Materials

## Overview

AI4Materials is a machine-learning-based framework designed for **materials science research**, particularly focusing on **predicting material properties, stability, and performance** using computational techniques and for understanding the fundamental science. The repository provides models, datasets, and analytical tools to accelerate the discovery of novel materials and virtual throughput screening of materials.

This project builds upon key research in **machine learning for materials science**, including dataset from:


> [Ma, X., et al. (2015). "Machine-Learning-Augmented Chemisorption Model for CO2 Electroreduction Catalyst Screening."](https://pubs.acs.org/doi/10.1021/acs.jpclett.5b01660)[*The Journal of Physical Chemistry Letters*](https://pubs.acs.org/doi/10.1021/acs.jpclett.5b01660)[, 6(18), 3528-3533.](https://pubs.acs.org/doi/10.1021/acs.jpclett.5b01660)

And methodology from:
> [Pankajakshan, P., et al. (2017). "Machine Learning for Materials Science: Stability and Transferability." ](https://pubs.acs.org/doi/full/10.1021/acs.chemmater.6b04229)[*Chemistry of Materials*](https://pubs.acs.org/doi/full/10.1021/acs.chemmater.6b04229)[, 29(6), 2437-2444.](https://pubs.acs.org/doi/full/10.1021/acs.chemmater.6b04229)


## Features

- **Machine Learning Models**: Implementations of Partial Least Squares regression and clustering models for material properties.
- **Data Preprocessing**: Tools for handling materials datasets, including feature engineering and selection (not implemented yet).
- **Exploratory Data Analysis (EDA)**: Principal Component Analysis (PCA), correlation heatmaps, and network-based visualization.
- **Prediction & Validation**: Model evaluation using cross-validation and performance metrics.

## Installation

To set up the repository locally, follow these steps:

### Prerequisites

- Python 3.8+
- Git
- Virtual environment (optional but recommended)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/praveenpankaj/AI4Materials.git
   cd AI4Materials
   ```
2. (Optional) Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

For EDA, visualization, refer to the Jupyter notebook `EDA.ipynb` 

```bash
jupyter notebook
```

## Contributing

We welcome contributions! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature-name`)
3. Commit your changes (`git commit -m "Added new feature"`)
4. Push to the branch (`git push origin feature-name`)
5. Open a Pull Request

## Citations
Machine Learning and Statistical Analysis for Materials Science: Stability and Transferability of Fingerprint Descriptors and Chemical Insights
Praveen Pankajakshan, Suchismita Sanyal, Onno E. de Noord, Indranil Bhattacharya, Arnab Bhattacharyya, and Umesh Waghmare
Chemistry of Materials 2017 29 (10), 4190-4201
DOI: 10.1021/acs.chemmater.6b04229

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

# requirements.txt

```
numpy
pandas
scikit-learn
matplotlib
seaborn
networkx
jupyter
```





