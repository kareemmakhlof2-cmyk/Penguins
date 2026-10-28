Palmer Penguins Species Classifier

A multi-class classification project that predicts a penguin's species (Adelie, Chinstrap, or Gentoo) from its island, sex, and body measurements, using Logistic Regression.

Dataset
Source: the palmerpenguins Python package (load_penguins())
344 records, 8 columns: species, island, bill length, bill depth, flipper length, body mass, sex, year
Class counts: Adelie 152, Gentoo 124, Chinstrap 68
Workflow
Exploration: info(), describe(), missing-value check, and a species count plot.
Missing values: filled numeric columns with the median and sex with the mode (2 missing values in each numeric column, 11 in sex).
Split: 80/20 stratified train-test split (random_state=42).
Preprocessing: one-hot encoding for island and sex, then StandardScaler fitted on the training set.
Training: Logistic Regression.
Evaluation: accuracy, classification report, and confusion matrix.
Results
Metric	Value
Train accuracy	99.6%
Test accuracy	98.6% (69 test samples)
Adelie precision / recall	1.00 / 0.97
Chinstrap precision / recall	0.93 / 1.00
Gentoo precision / recall	1.00 / 1.00
Limitations
Missing values were filled before the train-test split; computing the median and mode on the training set only would be cleaner.
The test set is small (69 samples), so cross-validation would give a more reliable estimate.
Tools

Python, Pandas, NumPy, scikit-learn, Matplotlib, Seaborn

Files
Penguins.ipynb: full notebook
Run it
bash
pip install palmerpenguins pandas numpy matplotlib seaborn scikit-learn
jupyter notebook Penguins.ipynb
