# Boston House Price Prediction

**ShadowFox Beginner Machine Learning Task**  
**Author:** Shreeraj Singh Bais

## Overview
A regression project using the Boston Housing CSV supplied for this task. It predicts the dataset's historical median-value target, `MEDV`.

> **Important:** `MEDV` is a historical median home value in thousands of US dollars, not today's market price. The classic Boston Housing dataset has known limitations. This is an educational exercise, not a real-world valuation, lending, or policy tool.

## Dataset
- Source: CSV supplied in this conversation for the ShadowFox task.
- Records used: 506
- Input features: 13
- Target: `MEDV`
- Split: 80% training / 20% testing (`random_state=42`).
- The uploaded CSV begins with a metadata row (`506, 13`); the project reads the following row as the column header and stores the normalized CSV in `data/`.

## Models and test results
Models are ranked by RMSE (lower is better).

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Gradient Boosting | 1.912 | 2.492 | 0.915 |
| Decision Tree | 2.308 | 2.925 | 0.883 |
| Random Forest | 2.120 | 3.159 | 0.864 |
| Linear Regression | 3.189 | 4.929 | 0.669 |

**Selected model:** Gradient Boosting

## Structure
- `data/` — normalized supplied dataset
- `notebooks/` — executed Jupyter notebook
- `results/` — saved charts and model comparison
- `models/` — saved best model
- `requirements.txt` — dependencies
- `.gitignore` — excludes virtual environments and generated Python files

## Run on Windows
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
jupyter notebook notebooks/Boston_House_Price_Prediction.ipynb
```
Then choose **Kernel → Restart & Run All**.

## Technologies
Python, Pandas, NumPy, Matplotlib, Scikit-learn, Jupyter, Joblib.

## Reproducibility
The split and model random states are fixed. README scores were computed using the supplied CSV and the model configurations in the notebook. Results may change if the dataset or configuration changes.
