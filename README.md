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

## Insights 
1. Insights from the Correlation Heatmap:
* ΔECO (KPI) has a strong negative Pearson correlation with εd (-0.88), indicating that a lower d-band center energy leads to stronger CO binding.
* Wd and *Vad² *(0.84) are strongly correlated, aligning with the theoretical relationship from the provided methodology.
* χ0 and IE (0.96) exhibit near-perfect Pearson correlation, suggesting redundancy. Moderate Correlations:
* γ1 and f (0.72) suggest a relationship between d-band filling and its skewness.
* χ and EA (0.72) show that electron affinity and local electronegativity are linked.
* Some descriptors, like χ0 and Vad², show weak relationships, which might indicate their lesser importance in the binding energy prediction.

2. PCA Insights:
* Explained Variance: The first two principal components capture a significant portion of the variance (~70%). Adding more components does not drastically increase explained variance, suggesting a low-dimensional structure in the dataset.
* PC1 (Primary Axis of Variation): Strongly influenced by εd, γ1, γ2, and Wd, confirming the importance of d-band characteristics.
* PC2 (Secondary Axis of Variation): Dominated by χ, χ0, EA, and IE, indicating a role for electronegativity and ionization energy.
Clustering
* Clusters correspond to distinct descriptor groupings, possibly separating different alloy types.
* Descriptors like εd, γ1, and γ2 strongly influence Cluster 1 (Cu), while χ0 and IE seem more relevant to Cluster 3 (Pt).

3. PLS Regression Insights:
* The PLS model achieves an R² of ~0.95, indicating a strong ability to predict ΔE*CO based on the descriptors. Most predicted values align well with actual values, but slight deviations exist.
* The strongest contributors (from PLS loadings) align with εd, Wd, Vad², and γ1, reinforcing their influence on CO binding energy. χ and EA also contribute but to a lesser extent.

4.   raph-Based Correlation Insights:
* Clusters of Strongly Related Descriptors: (εd, Wd, γ1, γ2) form a tightly connected group, confirming their role in d-band characteristics. The d-band model descriptors (εd, γ1, γ2, Wd) remain central in explaining CO binding energy.
* χ0, IE, and EA are probably redundant in their information and could be replaced with fewer fingerprint descriptors.
* Vad² and Wd show a high correlation, consistent with their theoretical relationship.

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





