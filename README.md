# Maintenance-Prediction-for-CNC-Machines
This project uses machine learning models to analyse CNC machine data, including air and process temperature, rotational speed, torque and tool wear, to predict equipment failures and classify failure types for improved maintenance planning.


**Type of Problem:** Binary Classification (Failure vs No Failure)
**Domain:** Manufacturing / Industrial Systems

---

**Dataset Description**

The dataset contains machine operating conditions and sensor readings used to monitor equipment performance.

**Features:**

* Air temperature [K]
* Process temperature [K]
* Rotational speed [rpm]
* Torque [Nm]
* Tool wear [min]
* Type (machine category)

**Target Variable:**

* `Target` → 0 = No Failure, 1 = Failure

**Additional Column:**

* `Failure Type` → Type of failure (used for future extension)

---

**Project Structure**

```bash
cnc_failure_prediction/
├── data/               # Dataset files
├── notebooks/          # Colab/Jupyter notebooks
├── models/             # Saved models (.pkl/.joblib)
├── README.md           # Documentation
└── requirements.txt    # Dependencies
```

---

**Project Workflow**

**1. Data Preprocessing**

* Removed irrelevant columns (`UDI`, `Product ID`)
* Encoded categorical variable (`Type`) using one-hot encoding
* Handled missing values (if any)
* Scaled numerical features

---

**2. Exploratory Data Analysis (EDA)**

* Analyzed distribution of sensor readings
* Visualized relationships between features and machine failure
* Checked correlation between variables

---

**3. Model Development**

* Split dataset into training and testing sets
* Trained a **Random Forest Classifier**
* Applied scaling and preprocessing pipeline

---

**4. Model Evaluation**

The model was evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

**Key Focus:**

* Minimizing **False Negatives** to avoid missing machine failures

---

## **Results**

* **Precision:** 68% 
* **Recall:** 76% 
* Model successfully identified failure patterns based on sensor data

---

Confusion Matrix Insight

The confusion matrix was used to evaluate model performance:

* True Positives → Correct failure predictions
* True Negatives → Correct normal predictions
* False Positives → False alarms
* False Negatives → Missed failures (critical to minimize)

---

**Business Impact**

* Enables early failure detection
* Reduces unplanned downtime
* Optimizes maintenance scheduling
* Improves machine reliability and lifespan

---

**Future Improvements**

* Extend model to predict Failure Type (multi-class classification)
* Implement real-time monitoring system
* Use advanced models like XGBoost or LSTM
* Deploy as a web-based dashboard (Streamlit)

---

**How to Run the Project**

1. Clone Repository

```bash
git clone https://github.com/YourUsername/cnc-failure-prediction.git
cd cnc-failure-prediction
```

2. Install Dependencies

```bash
pip install -r requirements.txt
```

3. Run Notebook

```bash
jupyter notebook notebooks/project.ipynb
```

---

Conclusion

This project demonstrates how machine learning can be applied to industrial systems to transition from reactive maintenance to predictive maintenance, improving efficiency and reducing operational risks.


