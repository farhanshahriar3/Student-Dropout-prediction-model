# Student Dropout Prediction Model

Machine-learning analysis for predicting whether a student will **Dropout** or **Graduate**. The project explores student demographic, admission, financial, and first- and second-semester academic indicators using a reproducible Jupyter notebook.

## Project Contents

- `ml model.ipynb` - exploratory data analysis, preprocessing, model training, tuning, and evaluation.
- `student_dropout_cleaned.csv` - cleaned input dataset with 4,424 student records.
- `CSE427 FINAL PROJECT REPORT.pdf` - accompanying project report.
- `requirements.txt` - Python dependencies used by the notebook.

## What the Notebook Does

1. Loads the cleaned student dataset.
2. Removes the `Enrolled` outcome so the task becomes binary classification: `Dropout` versus `Graduate`.
3. Checks data types, missing values, duplicates, class balance, and feature distributions.
4. Visualizes relationships between academic outcomes and selected numeric/categorical features.
5. Applies preprocessing with scikit-learn pipelines, including scaling and one-hot encoding where appropriate.
6. Trains and evaluates XGBoost, LightGBM, SVM, Logistic Regression, and Decision Tree classifiers.
7. Tunes Logistic Regression and Decision Tree hyperparameters with `GridSearchCV`.
8. Compares accuracy, weighted F1-score, ROC-AUC, confusion matrices, and classification reports.

## Setup

Python 3.10 or newer is recommended.

```bash
git clone https://github.com/farhanshahriar3/Student-Dropout-prediction-model.git
cd Student-Dropout-prediction-model
python -m venv .venv
```

Activate the virtual environment:

**Windows PowerShell**

```powershell
.venv\Scripts\Activate.ps1
```

**macOS/Linux**

```bash
source .venv/bin/activate
```

Install the dependencies and start Jupyter:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
jupyter notebook
```

Open `ml model.ipynb` and run the cells from top to bottom. The notebook expects `student_dropout_cleaned.csv` in the same directory, so it works from a fresh clone without changing a file path.

## Dataset

The cleaned data contains 37 columns, including the target column `target`. The original target has three classes:

| Class | Records |
| --- | ---: |
| Dropout | 1,421 |
| Enrolled | 794 |
| Graduate | 2,209 |

The notebook excludes `Enrolled` before modeling, leaving 3,630 observations for the binary classification analysis. Features include admission information, family and socioeconomic indicators, tuition and scholarship status, age, and first- and second-semester course performance.

## Important Notes

- This is an academic analysis, not a production decision-making system.
- Model performance should be interpreted with the class balance, feature timing, and institutional context in mind.
- Several features describe second-semester performance; using the model early in a student's enrollment would require a carefully defined prediction time and feature availability policy.
- The notebook's outputs depend on the installed library versions and the execution environment.

## License

No software license has been specified yet. Until a license is added, reuse and redistribution should be treated as restricted by default.
