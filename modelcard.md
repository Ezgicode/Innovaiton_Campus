# Cotton Evapotranspiration (ET) Prediction Model
## Data-Driven Irrigation Water Optimization

## Project Overview
This project focuses on predicting daily evapotranspiration (ET) for cotton fields using meteorological and seasonal variables. Evapotranspiration is a critical indicator of crop water demand, and accurate estimation enables efficient irrigation planning and significant water savings in agriculture.

The model is trained on real-world field experiment data collected under controlled irrigation conditions and is designed to operate with live weather data during deployment. This makes the system suitable for real-world decision support in precision agriculture.
---

##Technologies Used

This project was developed using:
- Python
- Pandas
- NumPy
- Scikit-learn
- Joblib
---

##Author

Ezgi Öztürk
Computer Engineering
Focus area: Artificial Intelligence for Sustainable Agriculture

---
##License

This project is intended for academic and research purposes only.
---

## Project Objectives
The main objectives of this project are:
- To predict daily evapotranspiration (ET) for cotton crops
- To support sustainable and water-efficient irrigation strategies
- To demonstrate the application of machine learning to real agricultural problems
- To bridge academic research with real-world deployment scenarios

---

## Dataset
The model is trained using the **Growth and Yield Data for the Bushland, Texas, Cotton Datasets**, published by the USDA Ag Data Commons.

This dataset is based on multi-year field experiments conducted in Bushland, Texas, a semi-arid cotton-growing region. It includes cotton growth, yield, and meteorological measurements collected under different irrigation treatments.

Key characteristics of the dataset include:
- Multi-year observations
- Semi-arid climate conditions
- Real field-scale experimental data
- Widespread use in agricultural water management research

The dataset is used only during the training phase to ensure reproducibility and scientific validity.

---

## Model Description
The evapotranspiration prediction model is implemented as a supervised regression pipeline.

Model details:
- Model type: Ridge Regression (L2-regularized linear regression)
- Pipeline structure:
  - StandardScaler for feature normalization
  - Ridge Regression with regularization parameter α = 1.0
- Target variable: Evapotranspiration (ET)
- Programming language: Python
- Machine learning framework: scikit-learn

Ridge Regression was selected to balance predictive performance and interpretability while controlling overfitting.

---

## Input Features
The model uses the following input features:
- Year
- Air temperature (°C)
- Relative humidity (%)
- Solar radiation (Rs, MJ/m²)
- Net radiation (Rn, MJ/m²)
- Wind speed at 2 meters (m/s)
- Seasonal encoding of Day of Year (DOY) using sine and cosine transformations

Seasonal encoding of DOY allows the model to capture annual climatic cycles smoothly without introducing artificial discontinuities.

---

## Training Procedure
The training workflow consists of the following steps:
- Data cleaning and column normalization
- Removal of rows with missing values
- Seasonal transformation of DOY into sine and cosine components
- Train/test split with an 80% / 20% ratio
- Fixed random seed (42) for reproducibility

---

## Model Evaluation
Model performance is evaluated using standard regression metrics:
- Mean Absolute Error (MAE)
- R² Score

Evaluation is performed on a held-out test set. The results indicate stable performance in predicting evapotranspiration under typical cotton-growing conditions.

---

## Live Data Integration (API Usage)
During deployment, the model can retrieve meteorological input variables (such as temperature, humidity, radiation, and wind speed) from external weather data APIs.

Important clarifications:
- External APIs are used only at inference time
- No API-based data is used during model training
- API keys, tokens, and provider-specific details are not stored or shared in this repository

This design ensures reproducible training and real-time applicability in operational environments.

---

## Limitations
- The model is trained on data from a single semi-arid region (Bushland, Texas)
- Performance may decrease under extreme or previously unseen climatic conditions
- Predictions depend on the accuracy and availability of external weather data during deployment
- Linear assumptions may limit performance in highly nonlinear climate–crop interactions

---

## Recommendations
- Model predictions should be validated with local agronomic expertise before real-world use
- Retraining is recommended when applying the model to different regions or crops
- The model should be used as a decision-support tool rather than a fully autonomous irrigation controller

---

## Getting Started

```python
import joblib
import pandas as pd
import numpy as np

model = joblib.load("cotton_et_model2.pkl")

input_data = pd.DataFrame([{
    "Year": 2020,
    "NW Air Temp in degrees C": 25,
    "NW RH in %": 45,
    "NW Rs in MJ/m^2": 20,
    "NW Rn in MJ/m^2": 15,
    "NW 2-m Wind Speed in m/s": 3,
    "DOY_sin": np.sin(2 * np.pi * 180 / 365),
    "DOY_cos": np.cos(2 * np.pi * 180 / 365)
}])

prediction = model.predict(input_data)

