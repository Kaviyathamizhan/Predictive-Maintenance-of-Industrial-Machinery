# Predictive-Maintenance-of-Industrial-Machinery
# Predictive Maintenance AI — Built on IBM Cloud

Welcome to the garage where machines don't just break — they **warn you before they die**.

This project uses **machine learning** and **sensor data** to predict failures in industrial machinery before they turn into costly downtime. Trained it, tested it, deployed it — and yep, it's alive on **IBM Cloud Lite**.

---

##  What It Does

It answers one critical question:

> “Is this machine about to fail?”  
> (Spoiler: It tells you yes or no, and it’s right about 90% of the time.)

---

##  Tech Stack

| Tech | What It Does |
|------|---------------|
| **Python** | My weapon of choice |
| **Scikit-learn** | Trained a Random Forest to sniff out failing machines |
| **IBM Watson Studio** | Where the magic was built and tested |
| **IBM Cloud Object Storage** | Stored the dataset |
| **IBM Watson Machine Learning** | Deployed the trained model |
| **Jupyter Notebooks** | For getting my hands dirty with data |

---

##  The Dataset

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

##  The ML Part

- **Model**: Random Forest Classifier
- **Accuracy**: ~91%  
- **Bonus**: Didn’t overfit like a noob
- Trained with proper preprocessing, scaling, and split into train/test  
- Evaluated using confusion matrix, F1-score, etc.

---

## Deployed On IBM Cloud

🔹 Model deployed as a **REST API** using Watson Machine Learning  
🔹 Takes in fresh sensor data  
🔹 Returns a sweet little JSON telling if maintenance is due

## Result 
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/08e4ee31-e0c4-48fd-8a56-a6489988270e" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/35baae53-8607-44de-85fd-5a177722686c" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/03083cb4-b26c-4dac-ae68-0946920e0157" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/36c67659-796f-4d08-87e4-a0a6ff742e43" />


```json
{
  "machine_id": "L13567",
  "prediction": 1,
  "confidence": 0.93
}
