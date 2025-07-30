# 🚀 Spaceship Titanic: Comprehensive Analysis & Predictive Modeling

Welcome to the **Spaceship Titanic** project repository! This repo contains a full end-to-end data-science workflow—from raw data through exploratory data analysis (EDA) to a production-ready predictive model—built around Kaggle’s fictional **Spaceship Titanic** passenger manifest.

---
## Repository Structure

```text
├── data/                 # Raw and intermediate datasets (✗ *not committed*)
│   ├── train.csv
│   └── test.csv
├── notebooks/
│   ├── 01_eda.ipynb      # Interactive EDA & visualisation
│   ├── 02_preprocess.ipynb
│   └── 03_modeling.ipynb
├── src/                  # Re-usable Python modules / pipelines
│   ├── features.py
│   ├── modelling.py
│   └── utils.py
├── figures/              # Auto-generated PNGs used in the report
│   ├── output.png
│   ├── output2.png
│   └── ...
├── report/
│   └── spaceship_report.tex  # Final LaTeX paper (compiled PDF in same folder)
├── requirements.txt
└── README.md             # ← you are here
```

---
## Setup & Installation

```bash
# 1. Clone the repo
$ git clone https://github.com/<user>/spaceship-titanic.git
$ cd spaceship-titanic

# 2. Create the environment (conda or venv)
$ conda env create -f environment.yml  # OR python -m venv .venv && source .venv/bin/activate

# 3. Install Python dependencies
$ pip install -r requirements.txt
```

> **Python 3.9+** is required. Major packages: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `shap`, and `jupyter`.

---
## Reproducing the Analysis

1. **Download data** from the Kaggle competition page and place `train.csv` & `test.csv` inside the `data/` directory.
2. Launch Jupyter Lab:
   ```bash
   $ jupyter lab
   ```
3. Run notebooks **in order** (`01_eda.ipynb` → `03_modeling.ipynb`). Each notebook saves cleaned data & figures to the appropriate folders.
4. The best model (Gradient Boosting) is persisted to `models/gb_best.pkl` for later inference.

---
## 📈 Key Results

| Model                | Feature Set  | Accuracy | F1-Score | ROC-AUC |
|----------------------|--------------|----------|----------|---------|
| Logistic Regression  | Raw          | 0.76     | 0.76     | 0.83    |
| Random Forest        | Raw          | 0.78     | 0.78     | 0.86    |
| Gradient Boosting    | Raw          | 0.80     | 0.80     | 0.88    |
| Logistic Regression  | Engineered   | 0.81     | 0.81     | 0.87    |
| Random Forest        | Engineered   | 0.84     | 0.84     | 0.90    |
| **Gradient Boosting**| **Engineered**| **0.85** | **0.85** | **0.92** |

Detailed tables, ROC curves, SHAP plots, and statistical tests are available in the report (next section).

---
## The Academic Report

A fully formatted **LaTeX report** (≈ 7 pages) is provided in `report/spaceship_report.tex`. It contains:

* Abstract, Introduction, Related Work
* Dataset description & cleaning methodology
* Exploratory Data Analysis with high-resolution visuals
* Hypothesis testing & statistical inference
* Feature engineering rationale
* Model selection, hyper-parameter tuning & evaluation metrics
* Discussion, limitations, ethical considerations, and future work

To compile:
```bash
$ cd report
$ latexmk -pdf spaceship_report.tex
```
A ready-made PDF is also included: `spaceship_report.pdf`.

---
## Contributing

Pull requests are welcome! Please open an issue first to discuss proposed changes. Make sure to run the unit tests in `tests/` and apply the `pre-commit` hooks.

---
## License

This project is released under the **MIT License**. See `LICENSE` for details.

---
## Citation

If you use this code or report, please cite it as:

```text
Entezari, M. (2024). Comprehensive Analysis and Predictive Modeling of the "Spaceship Titanic" Dataset. GitHub repository. https://github.com/<user>/spaceship-titanic
```

---

Enjoy exploring the final frontier of Machine Learning! 🚀
