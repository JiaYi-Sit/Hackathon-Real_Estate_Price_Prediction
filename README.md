# Hackathon:Housing Price Prediction--2025.6

This project focuses on **predicting residential housing prices** using structured, spatial, and textual features, with an emphasis on **feature engineering and model comparison**.

---
## Project Overview
- Predict housing prices based on property characteristics, location, and listing descriptions
- Compare linear models, tree-based models, neural networks, and ensemble methods
---

## Repository Contents
- `housing_price_prediction.ipynb / .py`  
  Main modeling and feature engineering code
- `Presentation_Slide.pdf`  
  Summary slides presenting key ideas, feature engineering highlights, and model performance
---

## Feature Engineering Highlights
- **Structural features**: floor level, orientation, building age, layout
- **Derived features**: area segmentation, rent-per-area, rent-per-bedroom
- **Spatial features**:
  - Latitude/longitude standardization
  - KNN-based neighborhood price statistics (mean, std)
  - K-means clustering with optimal K selection
  - Distance to geographic center and density indicators
- **Text features**:
  - Chinese text cleaning and segmentation (jieba + regex)
  - TF-IDF vectorization of listing descriptions
  - Keyword dictionaries for amenities, transportation, and property advantages
  - Text richness metrics (unique words / total words)
---

## Models and Training
- **Linear models**: OLS, Ridge, Lasso  
- **Tree-based models**: Random Forest, XGBoost  
- **Neural network**: ANN with Optuna tuning  
- **Custom model**:
  - Quantile-weighted GBDT to emphasize high-price properties
- **Ensemble methods**:
  - Feature-selection-based model averaging
  - Stacking with tree models and regularized linear meta-models

Evaluation metrics include **RMSE, MAE**, and an external benchmark score.

## Results (Hackathon Benchmark)
The final XGBoost-based ensemble achieved a **Datahub score of 84.1**, outperforming linear and single-model baselines.

---

## Key Takeaways
- Feature engineering delivers larger performance gains than model complexity alone
- Spatial and neighborhood-based features significantly improve predictive accuracy
- Tree-based models outperform linear and neural models on this dataset
- Ensemble methods offer marginal but consistent improvements over single models
---
