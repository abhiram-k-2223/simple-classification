# Blood Donation Prediction

This project aims to predict whether a donor will donate blood in a given time period using a logistic regression model. The dataset used is a blood donation dataset, and the target variable is 'Class', which indicates whether a donor donated blood. The workflow includes data loading, preprocessing with scaling, and model training and evaluation.

## Project Description

### Data Loading

The dataset is loaded using pandas, and an initial exploration is done using the `head()` method to understand the structure and content of the data. The target variable 'Class' is identified for prediction.

### Data Splitting

The dataset is split into training and testing sets using an 80-20 split with a fixed random state of 42 to ensure reproducibility. The target variable 'Class' is separated from the feature set.

### Data Preprocessing

#### Scaling with ColumnTransformer and StandardScaler

Numerical features are scaled using StandardScaler to ensure they have zero mean and unit variance. This step is implemented using ColumnTransformer to apply scaling only to specific columns (in this case, columns 1, 2, and 3). Scaling helps improve the model's performance by standardizing the range of the features.

### Model Training

A logistic regression model is trained on the scaled training data. Logistic regression is a widely used classification algorithm that is suitable for predicting binary outcomes, such as whether a donor will donate blood.

### Prediction

The trained model is used to predict the 'Class' on the test data. The predicted values are then compared to the actual values to assess the model's performance.

### Evaluation

The model's performance is evaluated using the accuracy score, which measures the proportion of correct predictions out of the total predictions made. A higher accuracy score indicates better model performance.

## Usage

1. **Clone the repository**:
    ```bash
    git clone https://github.com/abhiram-k-2223/simple-classification.git
    cd simple-classification
    ```

2. **Install dependencies**:
    ```bash
    pip install pandas scikit-learn
    ```

3. **Run the Jupyter notebook or script**:
    - If using a Jupyter notebook, open `simple_classification.ipynb` and run the cells sequentially.

4. **Output**:
    - The accuracy score indicating the model's performance on the test set.

This project demonstrates how to preprocess data, scale features using ColumnTransformer and StandardScaler, and train a logistic regression model to predict blood donations effectively.
