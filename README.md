# Breast Cancer SVM

A small notebook project that explores the Wisconsin Breast Cancer Diagnostic dataset and trains a Support Vector Machine (SVM) classifier. The workflow includes exploratory analysis, manual feature selection based on correlations, scaling, a custom train/test split, baseline SVM training, evaluation metrics, ROC curve, and grid search for hyperparameters.

## Project Structure

- breast-cancer.csv: Dataset used for analysis and model training.
- svm- with breast cancer.ipynb: Main notebook with all steps.

## Dataset Overview

The dataset contains measurements computed from digitized images of breast mass fine needle aspirates (FNA). The target column is:

- diagnosis: M = malignant, B = benign

Feature groups:

- *_mean: Mean of each measurement.
- *_se: Standard error of each measurement.
- *_worst: Mean of the largest (worst) values for each measurement.

Common feature definitions:

- radius: Mean distance from center to points on the perimeter
- texture: Standard deviation of gray-scale values
- perimeter: Tumor perimeter
- area: Tumor area
- smoothness: Local variation in radius lengths
- compactness: (perimeter^2 / area) - 1.0
- concavity: Severity of concave portions of the contour
- concave points: Number of concave portions of the contour
- symmetry: Symmetry of the contour
- fractal_dimension: Coastline approximation (fractal dimension)

## Notebook Workflow

1. Imports and setup
2. Data analysis and visualization
3. Data preprocessing
   - Drop id
   - Encode diagnosis (M -> 1, B -> 0)
   - Correlation-based feature selection
   - Standardization
   - Train/test split
4. Model implementation
   - Custom accuracy function
5. Sklearn implementation
   - SVC training and predictions
   - Confusion matrix with class labels
   - Classification report
   - Specificity calculation
   - ROC curve
   - Grid search over C, gamma, kernel

## How to Run

1. Open the notebook svm- with breast cancer.ipynb in VS Code or Jupyter.
2. Make sure the dataset file breast-cancer.csv is in the same folder.
3. Run all cells from top to bottom.

## Notes

- This notebook uses manual scaling and a custom train/test split. If you switch to scikit-learn utilities, results may differ slightly.
- Grid search parameters can be adjusted based on runtime and desired model complexity.
