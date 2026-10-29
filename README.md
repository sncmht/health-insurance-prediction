# HealthGuard: Insurance Cost Predictor

This project aims to predict health insurance charges based on individuals' demographic and health information, including age, gender, body mass index (BMI), number of children, smoking habits, and residential region.

## Dataset

The dataset used in this project is `insurance.csv`. It consists of 1338 rows and 7 columns:

*   **age:** Age of the primary beneficiary
*   **sex:** Insurance contractor gender (female, male)
*   **bmi:** Body Mass Index, providing an understanding of body, weights that are relatively high or low relative to height
*   **children:** Number of children covered by health insurance / Number of dependents
*   **smoker:** Smoking status (yes, no)
*   **region:** The beneficiary's residential area in the US (northeast, northwest, southeast, southwest)
*   **charges:** Individual medical costs billed by health insurance (Target variable)

There are no missing (null) values in the dataset.

## Libraries Used

*   `pandas` (Data manipulation and analysis)
*   `numpy` (Numerical computations)
*   `seaborn`, `matplotlib` (Data visualization)
*   `scikit-learn` (Machine learning models, preprocessing, and evaluation metrics)

## Data Preprocessing and EDA (Exploratory Data Analysis)

1.  **Visualization:** Relationships between various features (BMI, age, smoking status, gender, region, etc.) and the target variable were analyzed using `seaborn` (histograms, bar plots, scatter plots, and box plots).
2.  **Categorical Encoding:** The categorical variables `sex`, `smoker`, and `region` were converted into numerical values using `LabelEncoder`.
3.  **Data Splitting:** The dataset was separated into independent variables (features) and the dependent variable (`charges`), and then split into 80% training and 20% testing sets.
4.  **Feature Scaling:** The independent variables (`X_train`) were scaled using `StandardScaler` to improve model performance.

## Models Trained

Two different machine learning models were trained and evaluated using 5-fold Cross-Validation.

### 1. Linear Regression

*   **RMSE (Root Mean Squared Error):** ~6105.79
*   **MAE (Mean Absolute Error):** ~4208.76

### 2. Random Forest Regressor

*   **RMSE:** ~1919.76
*   **MAE:** ~1046.80

## Results

The Random Forest Regressor significantly outperformed the Linear Regression model, achieving much lower error rates (RMSE and MAE) and demonstrating a better predictive capability on this dataset.
