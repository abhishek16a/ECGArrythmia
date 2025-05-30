# 🫀 ECG Arrhythmia Detection and Risk Classification using Hybrid Machine Learning

This repository contains a machine learning-based system for detecting and classifying cardiac arrhythmias from ECG signals, using a hybrid model of **Random Forest and SVM**. The system also assigns **risk levels (Low/Moderate/High)** based on the proportion of abnormal heartbeats detected in an ECG segment.

---

## 📁 Dataset

We use the publicly available **MIT-BIH Arrhythmia Database** from [PhysioNet](https://physionet.org/content/mitdb/1.0.0/).  
It includes annotated ECG recordings sampled at 360 Hz and manually labeled by expert cardiologists.

---

## ⚙️ Features

- **Signal Processing**: RR interval extraction from R-peak annotations
- **Exploratory Data Analysis (EDA)**: Class distribution, RR interval histograms, boxplots
- **Feature Engineering**: RR interval, ΔRR, RR ratio, and rolling average
- **SMOTE Resampling**: For class imbalance mitigation
- **Hybrid ML Model**: Soft-voting ensemble of Random Forest and Support Vector Machine
- **Risk Evaluation**: Classifies ECG segments into Low, Moderate, or High risk
- **User Interface (UI)**: Built using **Streamlit** for ease of use

---

## 📂 Repository Structure

📦 ecg-arrhythmia-project
├── ECG_Classification_Notebook.ipynb # Main Jupyter Notebook for modeling
├── ECG_Visualization_Analysis.ipynb # EDA and Visualization Notebook
├── ecg_ui.py # Streamlit-based UI script (created using %%writefile)
├── README.md # Project documentation
├── 📁 mit-bih-arrhythmia-database-1.0.0/ # Folder containing local ECG data (.dat, .hea, .atr)

yaml
Copy
Edit


---

## ▶️ Running the Project

### 1. Install Requirements

```bash
pip install wfdb pandas numpy matplotlib seaborn scikit-learn imbalanced-learn streamlit
2. Download MIT-BIH Dataset
Download the records from PhysioNet MIT-BIH Database and place them inside a local folder named:

mit-bih-arrhythmia-database-1.0.0/
Make sure it includes files like:

100.atr

100.dat

100.hea

3. Run the Jupyter Notebook
Open the notebook ECG_Classification_Notebook.ipynb in Jupyter Notebook or JupyterLab and run each cell to:

Process ECG signals

Train hybrid models

Evaluate risk levels

Save outputs and results
4. Launch the Streamlit UI
In the notebook, the UI file is generated using:
%%writefile ecg_ui.py
# (Streamlit code here)
Then open a new terminal and run:
streamlit run ecg_ui.py

The UI will allow you to:

Select ECG record

Visualize the waveform

Classify beats

Download predictions

See risk classification

