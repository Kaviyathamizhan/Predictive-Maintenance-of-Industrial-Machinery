# Predictive Maintenance for Industrial Machinery (IBM Cloud + ML)

This project uses machine learning to **predict the specific type of failure** that could occur in an industrial machine — *before* it actually happens. Powered by real-time sensor data and built using IBM Cloud services, this AI solution enables proactive maintenance, reduces downtime, and cuts costs in industrial environments.

---

## Problem Statement

Industrial machines are prone to different types of failures like:
- Tool Wear
- Heat Dissipation Issues
- Power Failures
- Overstrain
- Random Failures

These unexpected breakdowns lead to **unplanned downtime** and high maintenance costs. The goal of this project is to develop an ML model that can **predict the failure type** based on operational sensor data — enabling scheduled maintenance before problems escalate.

---

## Dataset

- Source: [Kaggle - Predictive Maintenance Dataset](https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification)
- Key Features:
  - `Air temperature`, `Process temperature`
  - `Rotational speed`, `Torque`
  - `Tool wear`, `Product type`
- Failure Types (labels in raw data): `TWF`, `HDF`, `PWF`, `OSF`, `RNF`
- **Target Column Used**: `failure_type` *(created by combining the 5 binary failure labels)*

---

## Project Highlights

| Feature | Description |
|--------|-------------|
| **ML Type** | Multi-class classification |
| **Algorithm** | Random Forest Classifier |
| **Tools Used** | Python, Scikit-learn, IBM Watson Studio |
| **Deployment** | IBM Watson Machine Learning (REST API) |
| **Accuracy** | ~91% on test data |

---

## How We Built It

1. **Data Preprocessing**
   - Combined 5 binary failure columns into a single `failure_type` label
   - Cleaned and normalized sensor data

2. **Model Training**
   - Random Forest Classifier trained in IBM Watson Studio
   - Evaluated using Accuracy, Precision, Recall, F1-Score

3. **Deployment**
   - Exported model as `.pkl`
   - Deployed using **IBM Watson Machine Learning**
   - REST endpoint created for live predictions

4. **Prediction Example**
```json
{
  "rotational_speed": 1600,
  "torque": 45,
  "air_temp": 300,
  "tool_wear": 35
}
↓
Prediction: "TWF" (Tool Wear Failure) 
```
## Results:

<img width="1916" height="928" alt="Image" src="https://github.com/user-attachments/assets/40830204-04e3-4a64-aad8-8e035a8e4533" />
<img width="1919" height="981" alt="Image" src="https://github.com/user-attachments/assets/9f10f6b5-c7ee-4c0c-84fc-96cd726314c6" />
<img width="1919" height="986" alt="Image" src="https://github.com/user-attachments/assets/84892697-539e-41ed-93fd-32659620dd03" />
<img width="1919" height="984" alt="Image" src="https://github.com/user-attachments/assets/8efdcbcb-9cdb-4bd2-bf99-c05cebd62dfc" />
<img width="1915" height="923" alt="Image" src="https://github.com/user-attachments/assets/2f9ba2c6-507b-4980-b9b1-5485a05545e9" />
