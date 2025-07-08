<h1 align="center">🧠 Predictive Modelling of Psychological Distress Using Daily Thought Patterns: A Novel Supervised Machine Learning Approach 🧠</h1>

This repository contains the full pipeline for classifying psychological distress using Random Forest models trained on daily ongoing thought patterns, derived from experience sampling (Ho et al., 2020). The distress dimensions follow the DASS-21 framework and include:

- **Depression**  
- **Anxiety**  
- **Stress**  
- **Overall Psychological Distress (DASS Total)**  

Classification is implemented in two forms:

- **Binary Classification:**  
  *Normal* vs *Severe*  

- **Multiclass Classification:**  
  *Normal*, *Mild*, *Moderate*, *Severe*, *Extremely Severe*
### (Cutoffs based on Lovibond & Lovibond, 1995; Gavrilescu & Vizireanu, 2019)

## 📁 Project Structure

### 🔹 **Binary/**
## 🎯 Goal

Classify psychological distress into two categories — **Normal (0)** and **Severe (1)** using daily ongoing thought features.

---

## 📂 Directory Structure

### `Preprocessing/`
- Cleans and prepares the dataset
- Applies binary classification thresholds
- Splits data into **balanced train/test sets**
- Uses `Corrected_Unscaled_thought_personality_combined.csv` as input

### `FinalData/`
- Contains final processed **training** and **testing** datasets

### `BinaryAnalysis.ipynb`
- Complete **machine learning pipeline** for binary classification
- Includes model training, evaluation, and interpretation

### `Results/`
- Stores model **outputs**, **performance metrics**, and **visualizations**

## 🔹 FiveClassesDefault/

### 🎯 Goal

Perform **five-class classification** of psychological distress based on DASS-21 subscales:

- `0` = Normal  
- `1` = Mild  
- `2` = Moderate  
- `3` = Severe  
- `4` = Extremely Severe  

---

## 📂 Directory Structure

### `Preprocessing/`
- Applies predefined **DASS-21 cutoffs** (Lovibond & Lovibond, 1995) to all subscales
- Splits data into **balanced train/test sets**

### `FinalData/`
- Contains **preprocessed multiclass datasets** for training and evaluation

### `FiveClassClassification.ipynb`
- Main notebook implementing the **multiclass classification workflow**
- Includes training, evaluation, and SHAP-based model interpretation

### `Results/`
- Stores **model performance metrics** and **visualizations** (e.g., confusion matrices, SHAP plots)


# ⚙️ Model Overview
	•	Algorithm: Random Forest Classifier
	•	Input Features:
	•	Thought content features from experience sampling (Includes task-focus, past/future orientation, intrusiveness, modality, and more)
	•	Target Variables: Depression, Anxiety, Stress, and DASS Total
	•	Evaluation:
	•	Accuracy, Precision, Recall
	•	Confusion Matrix & ROC-AUC
	•	SHAP Analysis for feature interpretability

# 📚 References

	•	Ho, N. S. P., Poerio, G., Konu, D., Turnbull, A., Sormaz, M., Leech, R., ... & Smallwood, J. (2020). Facing up to the wandering mind: Patterns of off-task laboratory             thought are associated with stronger neural recruitment of right fusiform cortex while processing facial stimuli. Neuroimage, 214, 116765.
    •	Lovibond, S.H., & Lovibond, P.F. (1995). Manual for the Depression Anxiety Stress Scales (2nd ed.). Psychology Foundation.
	•	Gavrilescu, M., & Vizireanu, N. (2019). Predicting depression, anxiety, and stress levels from speech and text using multi-task learning. Sensors, 19(14), 3045. 
