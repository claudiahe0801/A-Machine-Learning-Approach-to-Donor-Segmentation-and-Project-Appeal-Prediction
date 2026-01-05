<div align="center">

# 🎯 Donor Analysis

**Identifying Exciting Projects & Understanding Donor Segmentation**

[![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)](https://www.r-project.org/)
[![Random Forest](https://img.shields.io/badge/Random_Forest-228B22?style=for-the-badge&logo=tree&logoColor=white)](#predictive-modeling)
[![K-Means](https://img.shields.io/badge/K--Means-FF6B6B?style=for-the-badge&logo=cluster&logoColor=white)](#donor-segmentation)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

*A comprehensive data science project combining predictive modeling and customer segmentation to optimize charitable fundraising strategies.*

[📊 View Interactive Analysis](./DonorAnalysis.html) · [📄 Read Full Report](./DonorAnalysisReport.pdf) · [🌐 Portfolio Website](#)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Findings](#-key-findings)
- [Methodology](#-methodology)
- [Results](#-results)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Technologies](#-technologies)
- [Author](#-author)

---

## 🎯 Overview

This research project addresses two critical challenges faced by educational charity organizations:

| Challenge | Objective |
|-----------|-----------|
| **Project Identification** | Identify "exciting" projects that effectively encourage donations to enhance student education |
| **Donor Understanding** | Develop deeper insights into donor behavior to improve user experience and foster long-term contributions |

The analysis leverages machine learning techniques to build predictive models and segment donors into actionable personas, enabling data-driven fundraising strategies.

---

## 🔑 Key Findings

<table>
<tr>
<td align="center" width="25%">
<h3>95%</h3>
<p>Model AUC Score</p>
</td>
<td align="center" width="25%">
<h3>4</h3>
<p>Donor Personas</p>
</td>
<td align="center" width="25%">
<h3>10+</h3>
<p>Key Variables</p>
</td>
<td align="center" width="25%">
<h3>11%</h3>
<p>Exciting Projects</p>
</td>
</tr>
</table>

### 🏆 Top Predictors for Exciting Projects

1. **Teacher Referrals** — Projects with teacher-referred donors average 2 referrals per exciting project
2. **Unique Comment Proportion** — Critical threshold identified at 60%
3. **Project Recency** — Recently posted projects significantly more likely to be classified as exciting

### 👥 Donor Personas Discovered

| Persona | Characteristics | Recommended Strategy |
|---------|-----------------|---------------------|
| **The Majority** | Cash/PayPal users, onsite event driven | Host more onsite donation events |
| **Incentive-Driven** | Corporate matching, campaign page users | Increase 1-1 matching campaigns |
| **Exploration Needed** | Low engagement, requires investigation | Conduct further research |
| **Wealthy & Generous** | High-value donors (>$100), credit-focused | Personalized follow-up emails |

---

## 🔬 Methodology

![Methodology Flowchart](https://private-us-east-1.manuscdn.com/sessionFile/uaur4CbjhSDhTaFpym3MFG/sandbox/AiqBGICarIPxsX0bLIh1pr-images_1767570220857_na1fn_L2hvbWUvdWJ1bnR1L2Rvbm9yX2FuYWx5c2lzX2dpdGh1Yi9pbWFnZXMvbWV0aG9kb2xvZ3ktZmxvd2NoYXJ0.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvdWF1cjRDYmpoU0RoVGFGcHltM01GRy9zYW5kYm94L0FpcUJHSUNhcklQeHNYMGJMSWgxcHItaW1hZ2VzXzE3Njc1NzAyMjA4NTdfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwyUnZibTl5WDJGdVlXeDVjMmx6WDJkcGRHaDFZaTlwYldGblpYTXZiV1YwYUc5a2IyeHZaM2t0Wm14dmQyTm9ZWEowLnBuZyIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTc5ODc2MTYwMH19fV19&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=NMOuwx35vXp5emc332~2KNOeGWJhJr-9swg1K8yY1M~i0A7T8j0Dky9OO75xlCfWa~gCchcCOoFl66Qt~WMvJYKnVgf51kyLYswMinoDfcbhlZYVdsMX3-AxBmSjevKfNMICW-rXLad78d16jE-YoBW6cfGZspXlKdxh1qrFJRlm2el-5W8ngCIQ9GkyDju67n4xk-C7O3fvjM7jsm~uvzk4MtAX1iBELobMEFK~rzeNki0yZ9ijz75F0iNPgD~jlJf9XjjhlxaH276Tj9JeW0rF~w4ca5UluKZDQRUKeJ6jL4gQiEsrFZVy5CEfRQQYpO0EYnULXGOvm31cXqpVXw__)

### Phase 1: Data Preparation
- Removed high-cardinality variables (e.g., donation ID)
- Applied dummy encoding for categorical features
- Detected and removed outliers using IQR method
- Imputed missing values with median

### Phase 2: Exploratory Data Analysis
- Analyzed target variable distribution (11% exciting projects)
- Created boxplots for numeric variable patterns
- Explored categorical variable relationships
- Identified key correlations

### Phase 3: Predictive Modeling
- Compared multiple classification algorithms
- **Random Forest** achieved highest performance (AUC ≈ 1)
- Extracted top 10 feature importance rankings
- Validated model on held-out test set

### Phase 4: Customer Segmentation
- Implemented K-Means clustering algorithm
- Identified 5 distinct donor clusters
- Developed actionable personas for each segment
- Mapped targeted engagement strategies

---

## 📊 Results

### Model Performance Comparison

```
┌─────────────────────┬───────────┬──────────┬─────────┐
│ Model               │ Precision │ Recall   │ AUC     │
├─────────────────────┼───────────┼──────────┼─────────┤
│ Random Forest       │ 0.95      │ 0.94     │ ~1.00   │
│ Logistic Regression │ 0.72      │ 0.68     │ 0.78    │
│ Decision Tree       │ 0.81      │ 0.79     │ 0.85    │
└─────────────────────┴───────────┴──────────┴─────────┘
```

### Feature Importance (Top 5)

```
Teacher Referrals     ████████████████████████████████████ 95%
Unique Comments       ████████████████████████████████     82%
Project Recency       ██████████████████████████████       78%
School Type           █████████████████████████            65%
Donation Amount       ██████████████████████               58%
```

---

## 📁 Project Structure

```
donor-analysis/
├── 📊 DonorAnalysis.html      # Interactive R analysis with visualizations
├── 📄 DonorAnalysisReport.pdf # Comprehensive research report
├── 📁 data/
│   ├── raw/                   # Original dataset
│   └── processed/             # Cleaned data
├── 📁 scripts/
│   ├── 01_data_cleaning.R     # Data preprocessing
│   ├── 02_eda.R               # Exploratory analysis
│   ├── 03_modeling.R          # Predictive modeling
│   └── 04_clustering.R        # K-Means segmentation
├── 📁 images/                 # Visualizations and figures
└── 📄 README.md
```

---

## 🚀 Getting Started

### Prerequisites

- R (≥ 4.0.0)
- RStudio (recommended)

### Installation

```r
# Install required packages
install.packages(c(
  "tidyverse",
  "randomForest",
  "caret",
  "cluster",
  "ggplot2",
  "knitr"
))
```

### Usage

```r
# Clone the repository
git clone https://github.com/yourusername/donor-analysis.git

# Open the R project
# Run scripts in order: 01 → 02 → 03 → 04

# Or view the complete analysis
browseURL("DonorAnalysis.html")
```

---

## 🛠 Technologies

<div align="center">

| Category | Tools |
|----------|-------|
| **Language** | R 4.x |
| **Machine Learning** | Random Forest, K-Means |
| **Data Wrangling** | tidyverse, dplyr |
| **Visualization** | ggplot2, plotly |
| **Reporting** | R Markdown, knitr |

</div>

---

## 👤 Author

**Yuxia (Claudia) He**

- 🎓 PhD Candidate in Data Science
- 📧 Email: [your.email@example.com](mailto:your.email@example.com)
- 💼 LinkedIn: [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- 🐙 GitHub: [@yourusername](https://github.com/yourusername)

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**⭐ If you found this project helpful, please consider giving it a star!**

</div>
