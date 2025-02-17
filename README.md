# Rohlik Sales Forecasting Challenge 2025

## Overview

Rohlik Group, a leading European e-grocery innovator, operates across 11 warehouses in the Czech Republic, Germany, Austria, Hungary, and Romania. This project focuses on predicting the sales of selected warehouse inventory for the next 14 days using historical sales data, enabling more efficient inventory management and demand planning.

## Problem Statement

This is a cross-sectional time series forecasting regression problem, where the goal is to predict daily sales for each unique_id, segmented by warehouse, discount type, and product type, while accounting for seasonal factors and holiday effects.

## Modeling Approach

Several modeling approaches were tested:

Deep Neural Networks with Entity Embeddings: Attempted to handle product names, but required excessive computational power without significant improvement.

Lasso & Elastic Net Regression: Due to the dataset's inherent non-linearity, these models performed poorly, with WMAP exceeding 50, making them unsuitable for ensembling.

XGBoost vs. LightGBM: XGBoost consistently outperformed LightGBM, leading to the decision to use only XGBoost in later stages.

## Dataset

Time Period: From 2022 onwards

Size: ~2.8 million samples

Features: 33 features including categorical and numerical data

## Training & Optimization

Subscribed to Google Colab Pro to accelerate training.

Due to computing limitations, only manually selected periods were used as the validation set.

Extensive hyperparameter tuning was performed to optimize the model.

## Results

Best WMAP Achieved: 19.63

Leaderboard Rank: 164th out of 777 participants

Performance Comparison: 1.8 WMAP higher than the 4th place result in the competition.

## Future Improvements

Explore alternative ensembling strategies beyond XGBoost.

Optimize feature engineering for better generalization.

Improve computational efficiency to enable full cross-validation.

Investigate deep learning architectures with more computational resources.
