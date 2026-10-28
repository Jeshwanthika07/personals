<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=047857,10B981,6EE7B7&height=220&section=header&text=Statistical%20Data%20Science%20Lab%20I&fontSize=38&fontColor=ffffff&fontAlignY=38&desc=Titanic%20Survival%20EDA%2C%20Demographic%20Disparities%2C%20%26%20Imputation&descSize=16&descAlignY=60&descAlign=50" width="100%" alt="Statistical Data Science Lab Banner"/>

[![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://seaborn.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)](https://matplotlib.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)](#)

</div>

---

## 📌 Executive Summary / Overview

The **Statistical Data Science Lab I** (`personals`) repository presents an empirical exploratory data analysis (EDA) and missingness treatment framework applied to historical maritime survival data (the Titanic dataset). Developed under the curriculum of Statistical Data Science (SDS), the project demonstrates disciplined exploratory workflows essential for reproducible data preparation.

Maritime survival outcomes exhibit significant demographic and socio-economic skew. This laboratory investigation isolates primary survival predictors—socio-economic passenger class (`Pclass`), biological sex (`Sex`), age brackets, and fare distribution—while rigorously resolving data quality issues such as non-random missingness in `Age`, `Cabin`, and `Embarked` features.

---

## 📖 Interactive Table of Contents

- [Executive Summary / Overview](#-executive-summary--overview)
- [Key Features & Capabilities](#-key-features--capabilities)
- [System Architecture & Analytical Workflow](#-system-architecture--analytical-workflow)
- [Tech Stack Breakdown](#-tech-stack-breakdown)
- [Data Cleaning & Imputation Strategy](#-data-cleaning--imputation-strategy)
- [Reproducible Quickstart & Setup](#-reproducible-quickstart--setup)
- [Project Directory Layout](#-project-directory-layout)
- [Author & Contributions](#-author--contributions)

---

## ✨ Key Features & Capabilities

- **Automated Missingness Remediation**: Systematically scans missing rates, applying numerical mean imputation for continuous features (`Age`) and categorical mode imputation for discrete variables (`Cabin`, `Embarked`).
- **Demographic Survival Disparity Profiling**: Evaluates the statistical impact of the "women and children first" maritime evacuation protocol through univariate and bivariate contingency comparisons.
- **Socio-Economic Gradient Analysis**: Quantifies survival odds disparities between first-class, second-class, and third-class ticket holders relative to fare magnitude.
- **Seaborn Statistical Visualizations**: Deploys distribution curves, grouped countplots, boxplots, and categorical factor plots examining cross-feature interactions.
- **Parametric Descriptive Statistics**: Summarizes skewness, variance, interquartile ranges, and central tendencies across passenger subsets.

---

## 🏗️ System Architecture & Analytical Workflow

```mermaid
flowchart TD
    A[Raw Titanic Passenger Data] --> B[Data Inspection: info & describe]
    B --> C{Missingness Auditing}
    C -->|Continuous Nulls in Age| D1[Statistical Mean Imputation]
    C -->|Categorical Nulls in Cabin| D2[Frequency Mode Imputation]
    C -->|Categorical Nulls in Embarked| D3[Modal Port Imputation]
    D1 & D2 & D3 --> E[Cleaned Analysis-Ready DataFrame]
    E --> F[Univariate Exploratory Analysis: Distributions & Outliers]
    F --> G[Bivariate Demographic Cross-Tabulation: Sex & Pclass]
    G --> H[Seaborn Statistical Graphics & Heatmaps]
    H --> I[Empirical Survival Insights & Policy Conclusions]
```

---

## 🛠️ Tech Stack Breakdown

| Category | Technologies & Tools |
| :--- | :--- |
| **Language** | Python 3.9+ |
| **Data Manipulation** | Pandas (DataFrames, Missingness Imputation, GroupBy) |
| **Scientific Library** | NumPy (Array manipulation and vector math) |
| **Statistical Graphics** | Seaborn, Matplotlib |
| **Interactive Notebook**| Jupyter Notebook (`SDS 1 (1).ipynb`) |

---

## 🔬 Data Cleaning & Imputation Strategy

| Feature | Missing Count | Imputation Strategy | Justification |
| :--- | :--- | :--- | :--- |
| `Age` | High | Mean Imputation (`titanic['Age'].fillna(mean)`) | Retains sample size without introducing systematic directional bias |
| `Cabin` | Very High | Modal String Imputation (`titanic['Cabin'].mode()[0]`) | Normalizes categorical missingness for string parsing |
| `Embarked` | Minimal (2) | Modal Port Imputation (`titanic['Embarked'].mode()[0]`)| Replaces rare unrecorded ports with most probable embarkation hub |

---

## 🚀 Reproducible Quickstart & Setup

### Prerequisites
- Python 3.9+
- Jupyter Notebook / Jupyter Lab

### Installation
```bash
# Clone the repository
git clone https://github.com/Jeshwanthika07/personals.git
cd personals

# Create virtual environment
python -m venv venv
# On Windows:
.\venv\Scripts\activate
# On Linux/macOS:
source venv/bin/activate

# Install dependencies
pip install numpy pandas matplotlib seaborn jupyterlab
```

### Launch the Notebook
```bash
jupyter lab "SDS 1 (1).ipynb"
```

---

## 📂 Project Directory Layout

```text
personals/
│
├── SDS 1 (1).ipynb            # Comprehensive 26-cell statistical EDA & imputation pipeline
└── README.md                  # Detailed laboratory documentation and methodology
```

---

## 👩‍💻 Author & Contributions

Authored by **[Jeshwanthika Pothamchetty](https://github.com/Jeshwanthika07)**  
*Alliance University | Department of Computer Applications*

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=047857,10B981,6EE7B7&height=100&section=footer" width="100%" alt="Footer Banner"/>

</div>
