# Cervical Cancer Detection

## What This Project Does

This project uses machine learning to predict whether a patient might have cervical cancer, based on their medical and lifestyle data. It has two main parts:

### Part 1 — Prediction from Patient Data (XGBoost)

1. **Loaded a dataset** of patient records with details like age, number of sexual partners, smoking habits, contraceptive use, STD history, and test results.
2. **Cleaned the data** — replaced missing values (marked as `?`) with averages, and dropped columns with too many missing entries.
3. **Explored the data** using correlation heatmaps and histograms to understand patterns.
4. **Trained an XGBoost classifier** to predict the `Biopsy` result (positive or negative for cancer).
5. **Evaluated the model** using accuracy, precision, recall, F1-score, and a confusion matrix.
6. **Saved the trained model** as a `.pkl` file using Pickle so it can be reused for new predictions without retraining.

### Part 2 — Prediction from Cell Images (CNN)

1. **Built a Convolutional Neural Network (CNN)** using TensorFlow/Keras to classify cervical cell images into 5 categories: Dyskeratotic, Koilocytotic, Metaplastic, Parabasal, and Superficial-Intermediate.
2. **Used image augmentation** (rescaling) and loaded images from train/validation/test folders.
3. **Trained the CNN for 32 epochs**, saving the best model based on validation accuracy.
4. **Plotted accuracy and loss curves** for training vs. validation to check for overfitting.
5. **Created a prediction function** that takes a cell image path and outputs the predicted cancer cell type.

## Tools & Libraries Used

- **Python** — main programming language
- **Pandas / NumPy** — data loading and processing
- **Matplotlib / Seaborn** — charts and visualizations
- **Scikit-learn** — data splitting, scaling, and evaluation metrics
- **XGBoost** — gradient-boosted tree model for tabular data
- **TensorFlow / Keras** — deep learning model for image classification
- **Pickle** — saving and loading trained models
