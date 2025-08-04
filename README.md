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

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/db19a20a-04ab-4d2d-9d18-289a6e4e6d08" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/f1b839c4-c3d9-40a7-a4a2-862b52a3c144" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/51750a52-2b0d-4e99-9a3d-2334b75d7c4f" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/2c0c950b-f4e7-4f63-a87f-482856ff4581" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/f6bc62f0-16a2-4d74-86c8-3f01e98246c4" />
