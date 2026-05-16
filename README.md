# PCA-Based Handwritten Digit Recognition

A Machine Learning project that demonstrates how **Principal Component Analysis (PCA)** can be used for **dimensionality reduction** in handwritten digit classification using the famous Digit Recognizer dataset.

This project compares the performance of a **K-Nearest Neighbors (KNN)** classifier before and after applying PCA and also visualizes high-dimensional image data in lower dimensions.

---

## Overview

Handwritten digit images contain **784 pixel features** (28×28 images). Training machine learning models directly on high-dimensional data can be computationally expensive.

This project:

* Trains a baseline **KNN classifier** on raw pixel data
* Applies **Standardization** and **PCA** to reduce dimensionality
* Retrains the classifier on transformed data
* Evaluates accuracy and performance improvements
* Visualizes digit data in 2D/3D feature space

---

## Dataset

The project uses the **Digit Recognizer** dataset.

Each row represents:

* `label` → the digit (0–9)
* `784 pixel columns` → grayscale pixel values of a 28×28 image

Dataset source:

* Kaggle Digit Recognizer Competition

---

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Plotly
* Scikit-learn

---

## Machine Learning Concepts Covered

### 1. K-Nearest Neighbors (KNN)

A supervised learning algorithm used for classification.

### 2. Principal Component Analysis (PCA)

PCA reduces the number of features while preserving maximum variance in the data.

### 3. Standardization

Feature scaling using `StandardScaler` before applying PCA.

### 4. Dimensionality Reduction

Reducing 784 dimensions into a smaller feature space for faster computation.

### 5. Data Visualization

Visualizing high-dimensional digit data in 2D/3D space using Plotly.

---

## Project Workflow

### Step 1 — Load Dataset

* Read dataset using Pandas
* Explore shape and sample records

### Step 2 — Visualize Digits

* Convert flattened pixel values into 28×28 images
* Display images using Matplotlib

### Step 3 — Train Baseline Model

* Split dataset into train/test sets
* Train KNN classifier on original 784-dimensional data
* Measure prediction time and accuracy

### Step 4 — Apply PCA

* Standardize the data
* Reduce dimensions using PCA
* Transform train and test data

### Step 5 — Retrain KNN

* Train KNN on PCA-transformed data
* Compare performance with baseline model

### Step 6 — Experiment with Components

* Test multiple PCA component values
* Observe impact on accuracy

### Step 7 — Visualization

* Reduce data to 2D/3D
* Visualize clusters using Plotly scatter plots

---

## Results

### Without PCA

* Accuracy: ~96%
* Prediction time: ~10 seconds

### With PCA

* Reduced dimensionality
* Faster computation
* Comparable classification accuracy

---

## PCA Insights

The notebook also explores:

* Eigenvalues
* Eigenvectors
* Explained variance ratio
* Cumulative explained variance graph

This helps determine the optimal number of principal components required to preserve most of the information.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/pca-digit-recognition.git
cd pca-digit-recognition
```

Install dependencies:

```bash
pip install numpy pandas matplotlib plotly scikit-learn
```

---

## Running the Project

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Run:

```bash
pca-digit-recognition.ipynb
```

---

## Example Visualizations

The project includes:

* Handwritten digit image visualization
* PCA-based 2D scatter plots
* Variance explained plots

---

## Future Improvements

Possible enhancements:

* Hyperparameter tuning for KNN
* Compare PCA with t-SNE or UMAP
* Use deep learning models
* Deploy as a web application
* Add confusion matrix and classification report


