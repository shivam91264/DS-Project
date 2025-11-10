# 🎓 Student Performance Prediction Project

A simple **web application** that predicts a student's **math score** based on key factors like gender, parental education level, and reading/writing scores.

---

## 🌐 Live Demo

🚀 **Try the App Here:**  
👉 [https://student-performance-ds-project.onrender.com](https://student-performance-ds-project.onrender.com)

---

## 🚀 What It Does

This web app allows users to enter information about a student and predicts their **math score** using a trained machine learning model.

You can input details such as:

- Gender  
- Race or Ethnicity  
- Parental Level of Education  
- Lunch Type (standard or free/reduced)  
- Test Preparation Course (completed or not)  
- Reading Score (out of 100)  
- Writing Score (out of 100)

Once you fill out all the fields and click **“Predict Math Score”**, the app displays the predicted math score below the form.

---

## 🧭 How to Use It

1. Visit the live app → [https://student-performance-ds-project.onrender.com](https://student-performance-ds-project.onrender.com)  
2. On the **Welcome Page (`index.html`)**, click **“Go to Predictor.”**  
3. On the **Prediction Page (`home.html`)**, fill out all input fields.  
4. Click **“Predict Math Score”** to view the predicted result.

---

## 🧠 How the Model Works

This project uses a **machine learning pipeline** trained on real student performance data.

### 1. Data Processing
- The app first converts categorical data (like gender or group) into numerical values using a **preprocessor**.  
- Numerical features are scaled to standardize the data before prediction.

### 2. Model Training
- A **machine learning model** (tested with multiple algorithms) was trained on the `stud.csv` dataset.  
- **GridSearchCV** was used to tune hyperparameters and select the best model.  
- Model performance was evaluated using the **R² score**.

### 3. Saving the Model
- The **best-performing model** and the **preprocessor** were saved as `.pkl` (pickle/dill) files in the `artifacts/` directory.

### 4. Making Predictions
- When a user submits the form:
  - The app loads the saved `.pkl` files.
  - User input is transformed using the preprocessor.
  - The trained model predicts the math score and returns it to the UI.

---

## 📊 Dataset

The model was trained on the **`stud.csv`** dataset, which contains information on students’ demographics and their math, reading, and writing scores.

---

## 🛠️ Technologies Used

**Languages & Libraries:**
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- CatBoost  
- XGBoost  
- Dill / Pickle  

**Frameworks:**
- Flask (for backend web server)  
- Gunicorn (for deployment on Render)

**Frontend:**
- HTML / CSS (for the web interface)

---
