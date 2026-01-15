# Dataset Card for Cotton Growth and Yield Data from Bushland, Texas

## Dataset Summary
This dataset, sourced from the USDA Ag Data Commons, contains **field-measured growth and yield data** for upland cotton *(Gossypium hirsutum L.)* grown in Bushland, Texas. It is widely used in agricultural water use research, crop modeling, and irrigation optimization studies, especially in semi-arid environments.

## Dataset Details

### Dataset Description
- **Title:** Growth and Yield Data for the Bushland, Texas, Cotton Datasets  
- **Source:** USDA National Agricultural Library Ag Data Commons  
- **Collected by:** USDA-ARS Conservation & Production Research Laboratory, Soil and Water Management Research Unit  
- **URL:** https://agdatacommons.nal.usda.gov/... *(dataset entry)*  
- **Licence:** Open public research use (USDA data)

This dataset documents cotton growth and yield across multiple seasons under varying irrigation treatments, including full irrigation and deficit irrigation protocols. :contentReference[oaicite:4]{index=4}

### Dataset Structure
The dataset is typically **tabular** (e.g., Excel or CSV format) with observations from multiple growing seasons. Variables include:

| Category | Examples |
|----------|----------|
| Field metadata | Year, Field ID, Irrigation type |
| Crop growth metrics | Plant height, leaf area index, growth stage |
| Yield components | Lint mass, seed mass, final yield, fiber quality |
| Biomass metrics | Total above-ground biomass, leaf/stem biomass |
| Irrigation data | Irrigation amount (full vs. deficit) |
| Environmental context | Soil moisture, weather/context (if available) |

Data may come as **multiple sheets** representing seasons, replications, or sub-plots. :contentReference[oaicite:5]{index=5}

## Uses
This dataset supports:
- Predictive modeling of cotton water demand and irrigation scheduling
- Crop water productivity and evapotranspiration analysis
- Comparative irrigation strategy evaluation (full vs deficit)
- Calibration and testing of agronomic water use models

## Dataset Creation & Collection
### Source Data
Data were collected via **field experiments** on lysimeter plots within a larger cotton field layout in Bushland, Texas. Measurements included both destructive and non-destructive sampling, alongside soil moisture and irrigation treatments. :contentReference[oaicite:6]{index=6}

### Data Processing
- Data cleaning (handling missing values)
- Consistent formatting across years
- Aligning dates and season metadata
- Standardization of units

### Annotations
Annotations are inherent dataset metrics collected and labeled during field experiments; no manual post-labeling is required beyond experimental design metadata.

## Biases, Risks, and Limitations
- Data are from a **specific semi-arid region** (Bushland, TX) and might not generalize to all cotton-growing regions.
- The dataset includes specific irrigation methods and may lack other modern irrigation technologies.
- Environmental data granularity may vary by year and field.

## Citation
Please cite this dataset if used:
> Evett, S.R., Marek, G.W., Copeland, K.S., Howell, T.A., Colaizzi, P.D., Brauer, D.K., Ruthardt, B.B. (2023). *Growth and Yield Data for the Bushland, Texas, Cotton Datasets.* USDA Ag Data Commons. :contentReference[oaicite:7]{index=7}
