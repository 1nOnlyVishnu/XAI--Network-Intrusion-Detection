# XAI-Powered Network Intrusion Detection System 🚀

This project is a high-performance machine learning model for detecting network intrusions, built on the CIC-IDS2017 dataset.

The key feature is **explainability**: the system doesn't just flag an attack; it uses **SHAP** to explain *why* a prediction was made, providing actionable insights for a security analyst.

---
## 🎯 Project Highlights

1.  **High-Performance Model:** Trained and tuned a `LightGBM` classifier to achieve over 99.9% F1-score and accuracy.
2.  **Explainable AI (XAI):** Integrated `SHAP` to generate per-alert, SOC-style reports that identify the top 3 contributing factors for any detection.
3.  **Large-Scale Data Engineering:** Overcame significant `MemoryError` limitations by using `Dask` to process a 3M+ row, multi-gigabyte dataset that was too large to fit in RAM.
4.  **Production Simulation:** Includes a production-ready model saved with `joblib` and a function simulating a real-time API endpoint.

---
## 📈 Model Results

The final tuned model is highly effective at distinguishing between benign traffic and attacks.
<img width="612" height="229" alt="image" src="https://github.com/user-attachments/assets/8384af48-d3b4-4df8-b81e-c116567c1d46" />

### Confusion Matrix
<img width="515" height="457" alt="Confusion_Matrix" src="https://github.com/user-attachments/assets/12960125-058a-4c1f-8eaa-8dde13649f33" />

### Explainable AI (XAI) in Action
The model can explain its reasoning for any prediction. Here, it flags a connection, correctly identifying the features that influenced the risk score.
<img width="464" height="680" alt="shap" src="https://github.com/user-attachments/assets/44c2cd9c-45d0-46a9-b5b0-156e41dc1fe3" />
<img width="950" height="472" alt="shap_plot" src="https://github.com/user-attachments/assets/1f92af8c-c1fa-43b1-a1c3-a14129a67321" />


## 🚀 How to Run This Project

### 1. Clone the Repository
```bash
git clone https://github.com/1nOnlyVishnu/XAI--Network-Intrusion-Detection.git 
cd XAI--Network-Intrusion-Detection
```

### 2. Set up Environment
```bash
python -m venv env
```

## Activate the environment:
```bash
source env/bin/activate  # On Windows: env\Scripts\activate
```

## Install dependencies:
```bash
pip install -r requirements.txt
```

### 3. Download the dataset
The CIC-IDS2017 dataset is not included in this repository due to its size. You must download the "GeneratedLabelledFlows" CSV files from the official dataset page(https.www.unb.ca/cic/datasets/ids-2017.html).

### 4.Prepare the Project
* Create a folder named data in the root of the project.
* Place all the downloaded .csv files inside the data folder.

### 5.Run the Notebook
Launch the Jupyter server and run the notebook: jupyter notebook
Open the NIDS-Analysis.ipynb (or whatever you named it) and run all cells.
