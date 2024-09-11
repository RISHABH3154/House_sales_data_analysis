# 🏡 House Sales Data Analysis

This project focuses on analyzing house sales data using **data wrangling**, **exploratory data analysis (EDA)**, and **machine learning** techniques. The goal is to handle missing data, visualize key trends, build regression models, and evaluate the overall performance of predictions.

## 📁 Dataset Information

The dataset includes multiple features that provide insights into house sales. Key columns include:

- **price**: Price of the house
- **bedrooms**: Number of bedrooms
- **bathrooms**: Number of bathrooms
- **sqft_living**: Square footage of living space
- **waterfront**: Whether the house has a waterfront view (`0` or `1`) And more...

Some columns contain missing values, which are handled during the data wrangling phase.

## 🛠️ Libraries and Tools

- **Python**: Data processing and machine learning
- **Pandas**: Data manipulation
- **NumPy**: Numerical operations
- **Seaborn** & **Matplotlib**: Data visualization
- **Scikit-learn**: Machine learning algorithms
- **Jupyter Notebook**: Development environment

## 📋 Project Workflow

1. **Data Wrangling**
   - Load the dataset and inspect its structure.
   - Handle missing values in columns such as `bedrooms` and `bathrooms`.
   - Drop unnecessary columns like `id` and `Unnamed: 0`.
   - Generate a statistical summary using `df.describe()`.

2. **Exploratory Data Analysis (EDA)**
   - Count the unique values for categorical variables (e.g., `floors`) using `df['floors'].value_counts()`.
   - Analyze outliers in `price` using **boxplots** for waterfront properties.
   - Perform correlation analysis between numerical features and `price` using **Seaborn's** `regplot`.
   - Visualize correlation heatmaps to understand feature interactions.

3. **Model Development**
   - Build a **Simple Linear Regression** model to predict house prices based on `sqft_living`.
   - Develop a **Multiple Linear Regression** model using additional features like `floors`, `waterfront`, and `lat`.
   - Evaluate the models using **R²** scores.

4. **Model Evaluation and Refinement**
   - Split the dataset using `train_test_split()`.
   - Use cross-validation (`cross_val_score()`) for reliable model evaluation.
   - Build a **machine learning pipeline** to scale features, apply polynomial transformation, and fit the final model.

---

## 💻 Instructions

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Rishabh3154/House_sales_data_analysis.git
---

## 📊 Analysis

### Data Wrangling
- Columns `bedrooms` and `bathrooms` had missing values, which were filled with their respective means.
- Dropped unnecessary columns (`id`, `Unnamed: 0`) to streamline the dataset.

### Exploratory Data Analysis (EDA)
- Visualized price distributions and identified outliers using **boxplots**.
- Found that the feature most correlated with `price` is `sqft_living`, with a correlation coefficient of **0.70**.

### Feature Correlation Heatmap
- Heatmap for better understanding.

---

## 🤖 Modeling and Evaluation

### Simple Linear Regression
- **Feature**: `sqft_living`
- **R² value**: 0.49

### Multiple Linear Regression
- **Features**: `sqft_living`, `bedrooms`, `bathrooms`, `floors`, `waterfront`, etc.
- **R² value**: 0.65

### Polynomial Regression and Scaling
- **Pipeline**: Feature scaling + Polynomial transformation
- **R² value**: 0.75

---

## 🚀 Future Improvements
- Implement more advanced models such as **Decision Trees** or **Random Forests**.
- Perform **hyperparameter tuning** to improve model performance.
- Add more **feature engineering** steps to extract additional insights.

