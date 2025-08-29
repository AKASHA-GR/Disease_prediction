# Disease_prediction
# Heart Disease Prediction using Machine Learning

This project uses the [Heart Disease Dataset](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data) from Kaggle to predict the presence of heart disease based on patient health data.  
The notebook demonstrates data preprocessing, visualization, model training, and prediction using **Logistic Regression** and **Random Forest** classifiers.  

---

## 📂 Dataset
- Source: [Heart Disease Dataset on Kaggle](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data)  
- File used: `heart_disease_uci.csv`  

The dataset contains attributes such as:
- Age, sex, cholesterol, blood pressure, etc.  
- Various categorical values like chest pain type, resting ECG, slope, thal, etc.  
- Target column (`num`) indicates the presence of heart disease (`0` = no disease, `1+` = disease present).

---

## ⚙️ Code Explanation

### 1. Kaggle API Setup & Dataset Download
- Upload `kaggle.json` (API token) to Colab.  
- Configure Kaggle CLI.  
- Download and unzip the dataset into `/content/heart-disease`.

### 2. Data Loading & Exploration
- Load CSV with **pandas**.  
- Check column names, missing values, and data types.  
- Visualize distributions with histograms and correlation heatmaps.

### 3. Data Preprocessing
- Handle missing values (fill numeric with mean, categorical with placeholders).  
- One-hot encode categorical features.  
- Scale numeric features with **StandardScaler**.  
- Split data into training and testing sets.

### 4. Model Training
- **Logistic Regression**: Train and evaluate with accuracy, classification report, and confusion matrix.  
- **Random Forest**: Train and evaluate for comparison. Also visualize feature importance.

### 5. Model Saving
- Save trained **Random Forest model** and **scaler** using `joblib`.  
- Create a `heart_user_template.csv` for users to input their own patient data.

### 6. User Prediction
- Accept a user-uploaded CSV with patient data.  
- Preprocess the input data (align columns with training data, handle missing values, one-hot encoding, scaling).  
- Predict using the saved Random Forest model.  
- Add predictions to the uploaded dataset.

---

## 🚀 How to Run
1. Open the notebook in **Google Colab**.  
2. Upload your Kaggle API key (`kaggle.json`).  
3. Run all cells step by step.  
4. (Optional) Upload your own `heart_dataset.csv` following the provided `heart_user_template.csv`.  
5. The model will predict heart disease presence (`0 = No disease, 1 = Disease present`).  

---

## 📦 Files in Repository
- `heart_disease_uci.csv` – Original dataset from Kaggle.  
- `heart_rf_model.pkl` – Trained Random Forest model.  
- `heart_scaler.pkl` – Scaler for numeric features.  
- `heart_user_template.csv` – Sample input template for users.  
- `notebook.ipynb` – Jupyter/Colab notebook with full workflow.  
- `README.md` – Documentation of the project.  

---

## 📖 References
- Kaggle Dataset: [Heart Disease Data](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data)  
- Scikit-learn Documentation: [https://scikit-learn.org/](https://scikit-learn.org/)  

---
