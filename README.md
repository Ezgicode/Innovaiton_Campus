# Innovaiton_Campus

---

# Data-Driven Irrigation Water Optimization for Cotton

## Overview
This repository contains a data-driven machine learning project focused on **irrigation water optimization for cotton cultivation**. The primary objective is to support sustainable agriculture by estimating crop water demand using real-world meteorological and field experiment data.

The project combines **agricultural domain knowledge** with **machine learning techniques** to model evapotranspiration and support informed irrigation decisions. It is designed for academic research, applied machine learning studies, and real-world decision support systems.

---

## Project Motivation
Water scarcity is a critical challenge in agriculture, particularly in semi-arid regions. Cotton cultivation requires careful irrigation management to avoid both water waste and yield loss.

This project aims to:
- Reduce unnecessary irrigation water use
- Improve irrigation efficiency through data-driven estimation
- Demonstrate how machine learning can be applied to real agricultural problems

---

## Data Source
The project is based on real-world experimental data from:

**Growth and Yield Data for the Bushland, Texas, Cotton Datasets**  
Published by the **USDA Ag Data Commons**

The dataset includes multi-year cotton field experiments conducted under different irrigation treatments in a semi-arid environment. It provides a reliable and scientifically validated foundation for modeling crop water demand.


---

## Repository Structure
The repository is organized as follows:
├── data/ # Raw and processed datasets
├── models/ # Trained machine learning models (.pkl files)
├── notebooks/ # Exploratory data analysis and experiments
├── src/ # Model training and preprocessing scripts
├── cotton_et_model/ # Evapotranspiration (ET) prediction subproject
│ ├── README.md # Model-specific documentation
│ └── modelcard.md # Model Card
├── datasetcard.md # Dataset Card
└── README.md # General project overview (this file)
---

## Core Components
- **Dataset Card**  
  Documents the origin, structure, and limitations of the agricultural dataset.

- **Evapotranspiration (ET) Prediction Model**  
  A supervised machine learning model that estimates daily evapotranspiration using meteorological and seasonal variables.

- **Model Card**  
  Provides detailed documentation of the ET prediction model, including training data, evaluation metrics, and limitations.

---

## Methodology Summary
- Use of real-world agricultural field data for training
- Feature engineering based on meteorological and seasonal variables
- Supervised regression modeling for evapotranspiration estimation
- Separation of training data and live inference data sources
- Emphasis on reproducibility and interpretability

---

## Intended Use
This project is intended for:
- Academic research in agricultural water management
- Machine learning applications in precision agriculture
- Educational purposes and portfolio demonstration
- Decision support tools for irrigation planning

It is **not intended** to be used as a fully autonomous irrigation control system without expert supervision.

---

## Limitations
- Models are trained on data from a specific geographic region
- Performance may vary under different climatic conditions
- External weather data quality directly affects inference results
- Linear modeling assumptions may not capture all nonlinear effects

---

## Author
Ezgi Öztürk  
Computer Engineering  
Focus area: Artificial Intelligence and Sustainable Agriculture

---

## License
This project is intended for academic and research purposes only.
