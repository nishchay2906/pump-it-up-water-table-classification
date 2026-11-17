# Pump it Up water pump classification

This project explores multiclass prediction of water pump operating status in Tanzania. The main notebook cleans the competition data, encodes predictors, compares classifiers, and exports a submission CSV.

## Run the notebook

From the repository root, create and activate a Python virtual environment, then install the notebook dependencies.

```sh
python -m venv .venv
. .venv/bin/activate
python -m pip install jupyterlab pandas numpy matplotlib seaborn scikit-learn category-encoders mlxtend lightgbm xgboost optuna
python -m jupyterlab
```

Open [PUmp1.ipynb](PUmp1.ipynb) and select the virtual environment's Python kernel. Run the cells in order.

## Data

The training features, training labels, and unlabeled test features from the [DrivenData competition](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/) are bundled at the repository root. The target column is `status_group`.

The other two notebooks are earlier experiments. The early `pump it up.ipynb` also needs `imbalanced-learn` and resamples before its split, so its saved validation metrics can be optimistic. Full model searches in the main notebook may be slow. The repository includes historical notebook outputs.
