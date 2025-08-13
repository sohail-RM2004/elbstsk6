# Iris Species Classification — KNN

## Overview
K-Nearest Neighbors (KNN) on the Iris dataset to classify *Setosa*, *Versicolor*, *Virginica*. We scale features, try multiple K values, evaluate with accuracy & confusion matrix, and plot 2D decision boundaries.

---

## Dataset
**Columns:** `Id`, `SepalLengthCm`, `SepalWidthCm`, `PetalLengthCm`, `PetalWidthCm`, `Species`  
We **drop** `Id` (not predictive).

---

## Steps
1) Train/test split (stratified)  
2) **Standardize** features (KNN is distance-based)  
3) Train `KNeighborsClassifier`  
4) Sweep **K = 1…15**  
5) Accuracy + **confusion matrix**  
6) **Decision boundary** (PetalLength vs PetalWidth)

---

## Key Results

### Accuracy vs K
| K  | Accuracy |
|----|----------|
| 1  | 0.967 |
| 2  | 0.933 |
| 3  | 1.000 |
| 4  | 1.000 |
| 5  | 1.000 |
| 6  | 0.967 |
| 7  | 0.967 |
| 8  | 0.967 |
| 9  | 1.000 |
| 10 | 1.000 |
| 11 | 0.967 |
| 12 | 0.967 |
| 13 | 0.967 |
| 14 | 0.967 |
| 15 | 0.967 |

- **Best K:** 3, 4, 5, 9, 10 (perfect accuracy on test split)

### Confusion Matrix

<img width="582" height="438" alt="image" src="https://github.com/user-attachments/assets/ef4c87b4-805b-4965-b33a-6ddb058668e3" />

- Perfect classification for the best K values (all test samples correct).

### Decision Boundaries

<img width="565" height="455" alt="image" src="https://github.com/user-attachments/assets/844b710e-8b8a-4a5b-b00c-8506b62e988e" />

- Using scaled **PetalLength–PetalWidth**, KNN shows clean class separation.

  
### Conclusion
Highest Accuracy: 100% (for K = 3, 4, 5, 9, 10)

Dataset is linearly separable in chosen features, making it ideal for KNN.

Feature scaling is crucial for correct distance measurement.

---


