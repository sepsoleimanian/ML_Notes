## Classification
### Machine learning with scikit-learn

#### 1. What is Machine Learning?

- Process where computers learn to make decisions from data without explicit programming.

#### 2. Examples of Machine Learning

- **Spam classification:** Predicting whether an email is spam or not based on content and sender.
- **Book categorization:** Clustering books into categories based on their content.

#### 3. Unsupervised Learning

- Uncovering hidden patterns and structures from **unlabeled data**.
- Example: **Customer segmentation**
    - Businesses group customers into categories based on purchasing behavior (clustering).

#### 4. Supervised Learning

- Predicting values where the **true values** are already known.
- Uses **features** to predict a **target variable**.
- Example: Predicting a basketball player's position based on points per game.
- **This course focuses on supervised learning.**

#### 5. Types of Supervised Learning

- **Classification:** Predicts a categorical label.
    - Example: Fraud detection in bank transactions.
    - **Binary classification:** Two possible outcomes (e.g., fraudulent or not fraudulent).
- **Regression:** Predicts continuous values.
    - Example: Predicting house prices based on number of bedrooms and size.

#### 6. Naming Conventions

- **Feature** (also called: predictor variable, independent variable).
- **Target Variable** (also called: dependent variable, response variable).

#### 7. Pre-requisites for Supervised Learning

- Data requirements:
    - No missing values.
    - Numeric format.
    - Stored as pandas **DataFrames**, **Series**, or **NumPy arrays**.
- **Exploratory Data Analysis (EDA)**
    - Ensure data is in the correct format.
    - Use pandas methods for descriptive statistics and data visualizations.

#### 8. scikit-learn Syntax & Workflow

- **Consistent syntax** across all supervised learning models.
- **Workflow steps:**
    1. **Import** a model from an `sklearn` module.
        - Example: `k-Nearest Neighbors (k-NN)` uses distance to predict labels or values.
    2. **Instantiate** the model as a variable.
    3. **Fit** the model to the data:
        - `X` (features) and `y` (target variable values).
    4. **Make predictions** using `.predict(X_new)`.
        - Example: Predict spam emails using six new email observations.
        - **Output:** `1` (spam) or `0` (not spam).
    ```
        - from sklearn.module import Model
        - model = Model()
        - model.fit(X,y)
        - predictions = model.predict(X_new)
        - print(predictions)
    ```

