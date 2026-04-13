# Raw Data

## Overview  
This folder contains the original, unprocessed dataset used in the Tsunami Alert Classification project. The data is directly obtained from the EveryEarthquake API (via Kaggle) and serves as the starting point for all analysis and modeling.

---

## Source  
- EveryEarthquake API (Kaggle dataset)  
- Global seismic event records  

---

## Contents  
The dataset includes raw seismic event information such as:

- Magnitude  
- Depth  
- Geographic coordinates (latitude and longitude)  
- Intensity measures (CDI, MMI)  
- Seismic significance (SIG)  
- Tsunami indicator (target variable)  

---

## Important Notes  
- This data is **not modified in any way**  
- It is used exclusively as input for preprocessing pipelines  
- Any cleaning, transformation, or feature engineering is performed in the `processed/` stage or within notebooks  

---

## Purpose  
The raw dataset ensures reproducibility and transparency in the data pipeline by preserving the original structure and values as received from the source.
