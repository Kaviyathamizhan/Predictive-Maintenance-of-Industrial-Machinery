# Predictive-Maintenance-of-Industrial-Machinery
# ⚙️ Predictive Maintenance AI — Built on IBM Cloud

Welcome to the garage where machines don't just break — they **warn you before they die**.

This project uses **machine learning** and **sensor data** to predict failures in industrial machinery before they turn into costly downtime. Trained it, tested it, deployed it — and yep, it's alive on **IBM Cloud Lite**.

---

## 🚀 What It Does

It answers one critical question:

> “Is this machine about to fail?”  
> (Spoiler: It tells you yes or no, and it’s right about 90% of the time.)

---

## 🔧 Tech Stack

| Tech | What It Does |
|------|---------------|
| **Python** | My weapon of choice |
| **Scikit-learn** | Trained a Random Forest to sniff out failing machines |
| **IBM Watson Studio** | Where the magic was built and tested |
| **IBM Cloud Object Storage** | Stored the dataset |
| **IBM Watson Machine Learning** | Deployed the trained model |
| **Jupyter Notebooks** | For getting my hands dirty with data |

---

## 🧠 The Dataset

Pulled from [Kaggle](https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification)

**Key Features:**
- Air & process temperature
- Torque
- Rotational speed
- Tool wear
- Product type

**Label:**
- `Target` → 0 = Working fine, 1 = Something’s about to explode 💥

---

## 🧪 The ML Part

- **Model**: Random Forest Classifier
- **Accuracy**: ~91%  
- **Bonus**: Didn’t overfit like a noob
- Trained with proper preprocessing, scaling, and split into train/test  
- Evaluated using confusion matrix, F1-score, etc.

---

## ☁️ Deployed On IBM Cloud

🔹 Model deployed as a **REST API** using Watson Machine Learning  
🔹 Takes in fresh sensor data  
🔹 Returns a sweet little JSON telling if maintenance is due

```json
{
  "machine_id": "L13567",
  "prediction": 1,
  "confidence": 0.93
}
