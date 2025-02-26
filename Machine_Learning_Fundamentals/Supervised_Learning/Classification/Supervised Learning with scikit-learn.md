## Classification
### Machine learning with scikit-learn
- **Machine learning** is when computers learn to make decisions from data without explicit programming.
- **Supervised learning** involves predicting values using a model built on known values, utilizing features to predict a target variable.
- **Types of supervised learning:**
    - **Classification:** Predicts the label or category of an observation (e.g., whether a bank transaction is fraudulent). Binary classification involves two outcomes.
    - **Regression:** Predicts continuous values (e.g., property price based on features like bedrooms and size).
- **Naming conventions:**
    - Features are also known as predictor variables or independent variables.
    - Target variables are also known as dependent variables or response variables.
- **Requirements before using supervised learning:** Data must not have missing values, must be in numeric format, and stored as pandas DataFrames or Series, or NumPy arrays. Exploratory data analysis is required.
- **scikit-learn syntax** for supervised learning models is consistent, making the workflow repeatable.
    - Import a Model (algorithm) from an sklearn module (e.g., k-Nearest Neighbors).
    - Instantiate the Model.
    - Fit the model to the data (X for features, y for the target variable).
    - Use the model's dot-predict method, passing new observations (X_new).
```
    - from sklearn.module import Model
    - model = Model()
    - model.fit(X,y)
    - predictions = model.predict(X_new)
    - print(predictions)
```

### The classification challenge
- Supervised learning uses labels.
- Goal: Build a classification model to predict labels for unseen data.
- **Classifying labels of unseen data**
    - Four steps in classification:
        1. Build a classifier that learns from labeled data.
        2. Pass unlabeled data as input.
        3. Predict labels for unseen data.
        4. Labeled data used for learning is called training data.
- **k-Nearest Neighbors (KNN) Algorithm**
    - KNN predicts labels based on the k closest labeled data points.
    - Uses majority voting to assign a label to the unlabeled observation.
    - Example: If k = 3, the prediction is based on the majority label among the three nearest neighbors. 
    - 
- **KNN Classification Examples**
    - If k = 3, the black observation is classified as red (majority of three neighbors).
    - If k = 5, it is classified as blue.
- **KNN Intuition**!
    - Scatter plot example: Total evening charge vs. total day charge for telecom customers.
    - Observations are color-coded:
        - Blue = churned customers.
        - Red = non-churned customers.
    - KNN with k = 15 creates a decision boundary:
        - Gray background = predicted churn.
        - Red background = predicted no churn.
- **Using scikit-learn to fit a KNN classifier**
    - Import `KNeighborsClassifier` from `sklearn.neighbors`.
    - Split data into:
        - `X`: 2D array of feature values.
        - `y`: 1D array of target values (churn status).
    - Convert `X` and `y` to NumPy arrays using `.values`.
    - Example dataset: 3333 observations, two features, and corresponding target labels.
    - Instantiate `KNeighborsClassifier` with `n_neighbors = 15`.
    - Fit classifier using `.fit(X, y)`.
- **Predicting on unlabeled data**
    - New dataset `X_new`: 3 observations, 2 features.
    - Use `.predict(X_new)` to classify unseen data.
    - Predictions:
        - First observation → 1 (churn).
        - Second and third observations → 0 (no churn).