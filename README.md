# De-tection-Pr-dictive-des-Criquets-P-lerins-au-Maroc
#  Intelligent Desert Locust Prediction System in Morocco (FAO Simulation)

This project developed a machine learning pipeline to predict the presence of desert locusts (*Criquet pèlerin*) in Morocco based on ecological and satellite remote sensing variables.

## Project Overview
Due to data scarcity, we built a **calibrated synthetic dataset** tailored to Morocco's geographic boundaries (Lat 21°N to 36°N) and climatic conditions. We addressed severe class imbalance using **SMOTE** and trained a **Random Forest** classifier to predict locust presence.

##  Dataset & Variables
*   **Geographic:** Realistic GPS coordinates across Moroccan regions (Dakhla, Guelmim, Errachidia, Souss, etc.).
*   **Climatic & Remote Sensing (Features):** Temperature, Soil Moisture, and Vegetation Index (NDVI).
*   **Target:** `Presence_Criquets` (Binary: 0 for Absence, 1 for Presence).

##  Methodology & Architecture
1.  **Data Generation & Calibration:** Setting biological rules (e.g., locusts proliferate when soil moisture ~0.24 and NDVI ~0.35 in desert areas).
2.  **Handling Imbalance:** Applied **SMOTE** to balance the dataset (initially 15% presence / 85% absence).
3.  **Model Training:** Random Forest Classifier (achieved an F1-Score of 1.0 due to strict programmed biological rules).
4.  **Explainable AI (XAI):** Used **SHAP** to interpret features and understand model decision boundaries.
5.  **Visualization:** Interactive mapping of risk zones using **Folium**.

## Tech Stack
*   **Environment:** Google Colab (CPU-bound)
*   **Libraries:** Python 3.13, Scikit-Learn, Imbalanced-Learn (SMOTE), SHAP, Folium, Pandas, NumPy.
