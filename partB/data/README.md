# Dataset Information

## Breast Cancer Wisconsin (Diagnostic) Dataset

- **Source**: `sklearn.datasets.load_breast_cancer()`
- **Original Source**: UCI Machine Learning Repository (Dr. William H. Wolberg, University of Wisconsin)
- **Samples**: 569 (357 benign, 212 malignant)
- **Features**: 30 real-valued features computed from digitised images of breast mass FNA biopsies
- **Task**: Binary classification (malignant vs benign)

## How the Dataset Is Used

1. **Loading**: The dataset is loaded directly from scikit-learn (`load_breast_cancer()`). No manual download is needed.
2. **Preprocessing**: Features are normalised to [0, 1] range using `MinMaxScaler`. A random seed is set at the top of each notebook.
3. **Splitting**: The data is split into training (100 samples), validation (100 samples), and testing (remaining ~369 samples) sets.
4. **Purpose**: This dataset serves as a binary classification testbed for the SVM poisoning attack described by Biggio et al. (ICML 2012). The attack crafts malicious training points to degrade the SVM's test accuracy.

## Limitations Compared to the Original Paper

- The paper uses MNIST digit pairs (e.g., 7 vs 1) with 784 features, whereas Breast Cancer has only 30 features.
- The paper uses 100 training and 500 validation samples from MNIST; we use a smaller dataset.
- The paper evaluates both linear and RBF kernels on high-dimensional image data.
