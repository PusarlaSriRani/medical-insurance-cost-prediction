# medical-insurance-cost-prediction
# 🏥 Medical Insurance Cost Prediction Using Machine Learning

## 📌 Project Overview

This project predicts annual medical insurance charges based on personal information such as age, gender, BMI, number of children, smoking habits, and geographical region.

The project uses Machine Learning regression algorithms to analyze insurance data, identify important factors affecting medical costs, and predict insurance charges for new individuals.

## 🎯 Objectives

- Analyze medical insurance data using Exploratory Data Analysis (EDA).
- Understand the relationship between personal characteristics and insurance charges.
- Build and evaluate multiple Machine Learning regression models.
- Implement Gradient Descent from scratch using NumPy.
- Improve model performance through feature engineering and regularization.
- Save the trained model using Joblib.
- Build a reusable prediction function.

## 📂 Dataset Information

**Dataset:** Medical Cost Personal Dataset

- Total records: 1,338
- Total columns: 7
- Target variable: `charges`

### Dataset Features

| Feature | Description |
|---|---|
| age | Age of the individual |
| sex | Gender |
| bmi | Body Mass Index |
| children | Number of children |
| smoker | Smoking status |
| region | Residential region |
| charges | Annual medical insurance cost |

## 🛠️ Technologies Used

- Python 3.11
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

## 🤖 Machine Learning Algorithms

The following algorithms and techniques were implemented:

1. Dummy Regressor
2. Linear Regression
3. Gradient Descent from Scratch
4. Polynomial Regression
5. Ridge Regression (RidgeCV)
6. Lasso Regression (LassoCV)

## 🔍 Project Workflow

1. Data Collection and Loading
2. Data Cleaning and Inspection
3. Exploratory Data Analysis (EDA)
4. Data Visualization
5. Train-Test Split (80:20)
6. Data Preprocessing using ColumnTransformer
7. Feature Engineering
8. Model Training and Evaluation
9. Gradient Descent Implementation
10. Residual Analysis
11. Polynomial Regression
12. Ridge and Lasso Regularization
13. Model Interpretation
14. Model Saving and Prediction

## 📊 Model Performance

The following results were obtained during model evaluation:

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 4177.046 | 5956.343 | 0.807 |
| Feature Engineering (Smoker × BMI) | 2886.667 | 4585.760 | 0.886 |
| RidgeCV | 2828.059 | 4569.763 | 0.886 |
| LassoCV | 2828.781 | 4571.931 | 0.886 |

**Observation:** RidgeCV and LassoCV achieved better results than the baseline Linear Regression model.

## 📈 Exploratory Data Analysis

The project includes visualizations such as:

- Distribution of insurance charges.
- Insurance charges by age and smoking status.
- Insurance charges by region.
- Insurance charges by gender.
- Box plots for smoking status and region.
- Residuals versus predicted values.
- Polynomial Regression training and validation RMSE.
- Gradient Descent learning rate comparison.
- Learning Curve analysis.

## ⚙️ Installation and Setup

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/medical-insurance-prediction.git
```

Navigate to the project directory:

```bash
cd medical-insurance-prediction
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate the environment on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `notebooks/medical_insurance.ipynb` and run the notebook cells.

## 🔮 Model Prediction

The trained Ridge Regression model is saved using Joblib.

Example prediction:

```python
import joblib

loaded_model = joblib.load(
    "../models/medical_insurance_model.pkl"
)

prediction = predict_charges(
    age=30,
    sex="male",
    bmi=25.5,
    children=1,
    smoker="no",
    region="southeast"
)

print("Predicted Insurance Charges:", prediction)
```

**Example Output:**

```text
Predicted Insurance Charges: $5267.64
```

## 📁 Project Structure

```text
medical-insurance-prediction/
│
├── app/
│
├── data/
│
├── models/
│   └── medical_insurance_model.pkl
│
├── notebooks/
│   └── medical_insurance.ipynb
│
├── README.md
│
└── requirements.txt
```

## 🚀 Future Improvements

- Develop an interactive web application using Streamlit or FastAPI.
- Deploy the trained model to a cloud platform.
- Improve prediction performance through additional feature engineering.
- Build a user-friendly interface for insurance cost estimation.

## 👩‍💻 Author

**Sri Rani Pusarla**

B.Tech – Computer Science and Engineering (AI & ML)

GitHub: https://github.com/PusarlaSriRani

LinkedIn: https://www.linkedin.com/in/sri-rani-pusarla-0238b32b7/

---

⭐ If you find this project interesting, feel free to explore the repository!
