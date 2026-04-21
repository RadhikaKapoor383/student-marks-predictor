# 📊 Student Marks Predictor

A machine learning project that predicts student exam marks using Linear Regression — both simple and multiple. Built with Python and scikit-learn inside a Jupyter Notebook.

---

## Overview

This project explores how study habits affect academic performance. It trains regression models on a synthetic student dataset and provides a function to predict marks based on input values.

Three models are built and compared:

- **Simple Linear Regression** — Marks predicted from `Hours_Studied`
- **Simple Linear Regression** — Marks predicted from `Sleep_Hours`
- **Multiple Linear Regression** — Marks predicted from `Hours_Studied`, `Sleep_Hours`, and `Play_Hours` combined

---

## 📁 Project Structure

```
student-marks-predictor/
│
├── marks-predictor.ipynb              # Main Jupyter Notebook (full pipeline)
│
├── data/
│   └── student_scores.csv             # Dataset (20 student records)
│
├── images/
│   ├── regression_plot.png            # Hours Studied vs Marks (simple regression)
│   ├── regression_plot_sleep_hours.png# Sleep Hours vs Marks (simple regression)
│   ├── regression_plot_multiple_linear.png # All 3 features vs Marks
│   └── actual_vs_predicted.png        # Actual vs Predicted scatter plot
│
└── README.md
```

---

## Dataset

The dataset (`student_scores.csv`) contains **20 synthetic student records** with the following features:

| Column | Description |
|---|---|
| `Hours_Studied` | Daily hours spent studying (0.5 – 10) |
| `Sleep_Hours` | Daily hours of sleep (0 – 8) |
| `Play_Hours` | Daily hours of leisure/play (1 – 11) |
| `Marks` | Exam score out of 100 (target variable) |

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core language |
| Pandas | Data loading and manipulation |
| NumPy | Numerical operations |
| Scikit-learn | Linear Regression, train/test split, evaluation metrics |
| Matplotlib | Data visualization and regression plots |
| Jupyter Notebook | Interactive development environment |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/RadhikaKapoor383/student-marks-predictor.git
cd student-marks-predictor
```

### 2. Install Dependencies

```bash
pip install pandas numpy scikit-learn matplotlib jupyter
```

### 3. Launch the Notebook

```bash
jupyter notebook marks-predictor.ipynb
```

Run all cells from top to bottom to reproduce the full pipeline — data creation, model training, evaluation, and visualizations.

---

## Model Results

### Simple Linear Regression — Hours Studied

Learns the equation:

```
Marks = m × Hours_Studied + c
```

**Sample predictions:**

| Hours Studied | Predicted Marks |
|---|---|
| 3 | ~37 |
| 6 | ~64 |
| 9 | ~90 |

---

### Simple Linear Regression — Sleep Hours

Learns the equation:

```
Marks = m × Sleep_Hours + c
```

A negative slope is observed — more sleep (without studying) correlates with lower marks in this dataset.

---

### Multiple Linear Regression

Combines all three features into one model:

```
Marks = m1×Hours_Studied + m2×Sleep_Hours + m3×Play_Hours + c
```

**Sample predictions:**

| Hours | Sleep | Play | Predicted Marks |
|---|---|---|---|
| 6 | 7 | 2 | ~high |
| 2 | 4 | 8 | ~low |
| 9 | 6 | 1 | ~very high |

---

## Visualizations

All plots are saved automatically when the notebook is run:

| File | Description |
|---|---|
| `regression_plot.png` | Scatter + regression line for Hours Studied |
| `regression_plot_sleep_hours.png` | Scatter + regression line for Sleep Hours |
| `regression_plot_multiple_linear.png` | Side-by-side plots for all 3 features |
| `actual_vs_predicted.png` | Diagonal parity plot for multiple regression |

---

## Evaluation Metrics

Each model is evaluated using:

- **MSE** — Mean Squared Error
- **MAE** — Mean Absolute Error
- **R²** — Coefficient of Determination (closer to 1.0 = better fit)

---

## Custom Predictions

You can call the built-in prediction functions directly in the notebook:

```python
# Simple regression (hours studied only)
predict_marks(hours=7)

# Multiple regression (all three inputs)
predict_marks(hours=6, sleep=7, play=2)
```

---

##  Author

**Radhika Kapoor**
[GitHub Profile →](https://github.com/RadhikaKapoor383)

---

## License

This project is open source and available for educational use.