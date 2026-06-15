# 🎓 Student Performance Analysis — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-EDA-green?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-teal)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📌 Project Overview

Student academic performance is shaped by a complex interplay of demographic, socioeconomic, and preparatory factors. This project performs a thorough **Exploratory Data Analysis (EDA)** on the *Students Performance in Exams* dataset to uncover patterns, identify key performance drivers, and generate actionable insights for educators and policymakers.

**Dataset Source:** [Kaggle — Students Performance in Exams](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)

---

## 🎯 Objectives

- Understand the **distribution and central tendencies** of student scores in Math, Reading, and Writing.
- Identify how **gender, parental education level, lunch type, and test preparation** influence academic performance.
- Detect and handle **missing values, outliers, and data quality issues**.
- Visualize **bivariate and multivariate relationships** between features and scores.
- Derive **actionable insights** to support educators and institutions in improving student outcomes.

---

## 📂 Project Structure

```
student-performance-eda/
│
├── data/
│   └── StudentsPerformance.csv        # Raw dataset
│
├── notebooks/
│   └── student_performance_eda.ipynb  # Main EDA notebook
│
├── outputs/
│   ├── figures/                       # All saved plots and charts
│   └── summary_stats.csv              # Exported summary statistics
│
├── src/
│   └── eda_utils.py                   # Helper functions for plotting & analysis
│
├── requirements.txt                   # Python dependencies
└── README.md                          # Project documentation (this file)
```

---

## 📊 Dataset Description

| Column | Description |
|---|---|
| `gender` | Student's gender (`male` / `female`) |
| `race/ethnicity` | Student's racial/ethnic group (Group A–E) |
| `parental level of education` | Highest education level of parent/guardian |
| `lunch` | Lunch type — `standard` or `free/reduced` (socioeconomic proxy) |
| `test preparation course` | Whether the student completed a prep course (`none` / `completed`) |
| `math score` | Score in Mathematics (0–100) |
| `reading score` | Score in Reading (0–100) |
| `writing score` | Score in Writing (0–100) |

**Dataset size:** 1,000 students × 8 features (no missing values)

---

## 🔍 EDA Workflow

### 1. Data Loading & Inspection
- Load CSV with `pandas`
- Check shape, dtypes, missing values, and duplicates
- Generate descriptive statistics for all numeric and categorical columns

### 2. Univariate Analysis
- Distribution plots (histograms + KDE) for Math, Reading, and Writing scores
- Count plots for all categorical features
- Identify skewness, modality, and outliers via box plots

### 3. Bivariate Analysis
- Score comparisons by **gender** — violin and box plots
- Score comparisons by **lunch type** — grouped bar charts
- Score comparisons by **test preparation** — before vs. after completion
- Score comparisons by **parental education level** — heatmap and bar plots

### 4. Multivariate Analysis
- Correlation heatmap of Math, Reading, and Writing scores
- Pair plots colored by gender and lunch type
- Composite performance score (`avg_score = mean of three subjects`) analysis
- Stacked segment analysis: interaction of gender × test prep × lunch type

### 5. Key Insights & Recommendations
- Summary of top factors driving performance
- Actionable recommendations for educators and institutions

---

## 📈 Sample Visualizations

> All visualizations are saved in `outputs/figures/`.

| Plot | Description |
|---|---|
| Score Distribution | Histograms + KDE for Math, Reading, Writing |
| Gender vs. Scores | Violin plots showing score spread by gender |
| Lunch Type Impact | Box plots comparing standard vs. free/reduced lunch |
| Test Prep Effect | Side-by-side comparison of prep vs. no-prep groups |
| Parental Education | Grouped bar chart across 6 education levels |
| Correlation Heatmap | Pearson correlation among the three score columns |
| Pair Plot | Scatter matrix colored by lunch type |

---

## 💡 Key Findings (Preview)

- **Test preparation significantly boosts scores** — students who completed the course scored notably higher across all three subjects on average.
- **Lunch type is a strong socioeconomic proxy** — students on standard lunch consistently outperform those on free/reduced lunch.
- **Female students outperform in Reading and Writing**, while **male students have a slight edge in Math**.
- **Parental education level shows a clear positive correlation** with student performance — children of parents with bachelor's or master's degrees score highest.
- **Reading and Writing scores are highly correlated** (r ≈ 0.95), suggesting shared underlying literacy skills.

---

## ⚙️ Setup & Installation

### Prerequisites

- Python 3.8 or higher
- pip

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/student-performance-eda.git
cd student-performance-eda

# 2. Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch the notebook
jupyter notebook notebooks/student_performance_eda.ipynb
```

---

## 📦 Dependencies

```
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
jupyter>=1.0.0
scipy>=1.9.0
```

Install all at once:

```bash
pip install -r requirements.txt
```

---

## 🚀 Running the Analysis

```python
# Quick start — run full EDA pipeline
import pandas as pd
from src.eda_utils import run_full_eda

df = pd.read_csv("data/StudentsPerformance.csv")
run_full_eda(df)
```

Or open the notebook for an interactive step-by-step walkthrough:

```bash
jupyter notebook notebooks/student_performance_eda.ipynb
```

---

## 📋 Actionable Recommendations

| Finding | Recommendation |
|---|---|
| Test prep improves outcomes | Expand access to preparation courses, especially for underperforming groups |
| Lunch type proxies for socioeconomic status | Provide additional academic support and resources to free/reduced lunch students |
| Gender gap in Math | Introduce targeted interventions to encourage female students in STEM |
| Parental education impact | Design parent engagement programs and community literacy initiatives |
| High Reading–Writing correlation | Leverage shared literacy skill-building in curriculum design |

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/add-model`)
3. Commit your changes (`git commit -m 'Add predictive model'`)
4. Push to the branch (`git push origin feature/add-model`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- Dataset originally published on [Kaggle by SP Scientist](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)
- Inspired by open-source EDA best practices from the data science community

---

*Built with ❤️ to support data-driven education.*
