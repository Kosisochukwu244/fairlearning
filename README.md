# Fairness in Income Prediction — Tutorial Notebook

A concise, hands-on tutorial demonstrating fairness auditing and mitigation for an income prediction task using Fairlearn and scikit-learn.

This project is centered on a Jupyter notebook that walks through data exploration, baseline model training, fairness evaluation by subgroup, and bias mitigation techniques on the UCI Adult (Census) Income dataset.

## Repository contents

- `fairness_income_tutorial.ipynb` — original tutorial notebook (Jupyter)
- `fairness_income_tutorial_converted.ipynb` — cleaned/validated copy of the notebook
- `README.md` — this file

## Goals

- Explore the Adult Census Income dataset and identify potential sources of bias.
- Train a baseline classifier to predict whether income exceeds $50K/year.
- Evaluate overall and subgroup performance using fairness-aware metrics.
- Apply mitigation strategies from Fairlearn and compare results.

## Key concepts covered

- Data exploration and preprocessing (categorical encoding, missing values)
- Baseline classification with scikit-learn
- Fairness metrics and MetricFrame (demographic parity, equalized odds, FPR/FNR by group)
- Mitigation strategies (reduction-based methods, post-processing)
- Trade-offs between accuracy and fairness

## Requirements

- Python 3.12 (recommended)
- Internet access to download the UCI Adult dataset (not bundled)

Recommended Python packages (installed via pip):

- fairlearn
- scikit-learn
- pandas
- matplotlib
- seaborn
- jupyterlab or notebook

## Quick setup (Windows PowerShell)

```powershell
# create a virtual environment
python -m venv .venv
# activate in PowerShell
.\.venv\Scripts\Activate.ps1
# install the core dependencies
pip install fairlearn scikit-learn pandas matplotlib seaborn jupyterlab
# start Jupyter Lab
jupyter lab
```

Or install the packages directly (no virtualenv):

```powershell
pip install fairlearn scikit-learn pandas matplotlib seaborn jupyterlab
```

If you prefer a `requirements.txt`, create one with the packages listed above and run:

```bash
pip install -r requirements.txt
```

## Running the notebook

1. Open `fairness_income_tutorial_converted.ipynb` (or the original `fairness_income_tutorial.ipynb`) in Jupyter Lab / Notebook or VS Code.
2. Run cells in order. The notebook downloads the dataset from the UCI repository and executes model training and evaluation steps.
3. To run headless (execute all cells) from the command line:

```bash
jupyter nbconvert --to notebook --execute fairness_income_tutorial_converted.ipynb --output executed_notebook.ipynb --ExecutePreprocessor.timeout=600
```

## Reproducibility notes

- The notebook fetches the dataset at runtime from UCI: https://archive.ics.uci.edu/ml/datasets/adult
- For deterministic results, set the random seed(s) in the notebook before training models (the notebook includes seed-setting where appropriate).
- Long-running cells may require network access and sufficient memory for training.

## Files of interest

- `fairness_income_tutorial.ipynb` — full narrative with plots and code cells.
- `fairness_income_tutorial_converted.ipynb` — cleaned JSON copy created to ensure the notebook opens correctly.

## References

- Fairlearn documentation: https://fairlearn.org
- scikit-learn: https://scikit-learn.org
- UCI Machine Learning Repository — Adult dataset: https://archive.ics.uci.edu/ml/datasets/adult

## Contributing

Contributions, improvements, and corrections are welcome. If you make substantive changes (new analyses, additional mitigation algorithms, or reproducible experiments), please add a short note in the notebook or open a PR (if you move this project to a versioned repo).

## License

No license file is included with this local copy. If you plan to publish this project, add an appropriate `LICENSE` file (e.g., MIT, Apache-2.0) and update the README.

## Author / Contact

Created from the `fairness_income_tutorial.ipynb` notebook. Add author name and contact details here if you want to publish or share the notebook.

---

If you'd like, I can also:
- generate a `requirements.txt` for easy installs,
- convert the notebook to a Python script, or
- extract a short summary of results from the executed notebook cells.
