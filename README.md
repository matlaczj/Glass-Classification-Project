# Glass Classification Project

<p align="center">
  <img src="logo.png" alt="Logo" width="400"/>
</p>

## Table of Contents

1. [Overview](#overview)
1. [Prerequisites](#prerequisites)
2. [Getting Started](#getting-started)
2. [Dataset Insight](#dataset-insight)
   - [Class Labels](#class-labels)
3. [Data Exploration](#data-exploration)
   - [Comprehensive Analysis](#comprehensive-analysis)
4. [Exploratory Data Analysis](#exploratory-data-analysis)
   - [Unveiling Patterns](#unveiling-patterns)
5. [Model Testing](#model-testing)
   - [Unraveling Effectiveness](#unraveling-effectiveness)
   - [Model Scores Comparison](#model-scores-comparison)
   - [Best Model Discovery](#best-model-discovery)

Feel free to navigate through the sections and delve into the details of the Glass Classification Project!

## Overview

Welcome to the Glass Classification Project! This project aims to classify different types of glass based on their distinct attributes. By leveraging a dataset available on Kaggle [here](https://www.kaggle.com/uciml/glass), our goal is to thoroughly analyze the data, overcome challenges, build precise models, and ultimately identify the most effective model for accurately classifying glass samples.

## Prerequisites

Before running the code, make sure you have the right dependencies installed.

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/matlaczj/Glass-Classification-Project
   cd Glass-Classification-Project
   ```

2. Follow the steps outlined in the project documentation to replicate the analysis and results.

    ```bash
   src\code.ipynb
   ```

## Dataset Insight

The dataset comprises 214 glass samples, each characterized by 9 attributes and categorized into 7 classes. Note that one class (Class 4) has no instances, effectively resulting in 6 classes. These classes represent diverse types of glass objects, spanning from building and vehicle windows to containers, tableware, and headlamps.

### Class Labels

- 1: Building windows float processed
- 2: Building windows non-float processed
- 3: Vehicle windows float processed
- 4: Vehicle windows non-float processed (none in this database)
- 5: Containers
- 6: Tableware
- 7: Headlamps

## Data Exploration

### Comprehensive Analysis

Upon exploration, it was discovered that the original dataset contains no missing values, ensuring the reliability and completeness of our analysis. The dataset includes key attributes such as Refractive Index (RI), Sodium (Na), Magnesium (Mg), Aluminum (Al), Silicon (Si), Potassium (K), Calcium (Ca), Barium (Ba), and Iron (Fe).

## Exploratory Data Analysis

### Unveiling Patterns

1. **Box Plots:** A closer look at box plots revealed significant variations in the attribute 'Si' compared to others, providing valuable insights into the dataset's characteristics.

2. **Correlation Matrix:** The correlation matrix highlighted relationships between different attributes, guiding the selection of features for model training.

## Model Testing

### Unraveling Effectiveness

The project employs a range of supervised learning models, including the k-Nearest Neighbors (kNN) classifier. To address class imbalance, StratifiedKFold is utilized for cross-validation, and the Synthetic Minority Over-sampling Technique (SMOTE) is applied to balance the training set.

### Model Scores Comparison

The following table provides an overview of the performance metrics for each tested model:

| Model                  | Learn Error | Test Error | Test Precision | Test Recall | Test F1 Score |
|------------------------|-------------|------------|-----------------|-------------|---------------|
| k-Nearest Neighbors   | 0.000       | 0.276      | 0.731           | 0.751       | 0.721         |
| Decision Tree         | 0.017       | 0.257      | 0.738           | 0.734       | 0.720         |
| Gaussian Naive Bayes  | 0.323       | 0.625      | 0.531           | 0.578       | 0.485         |
| Nearest Centroid      | 0.343       | 0.566      | 0.488           | 0.562       | 0.476         |


### Best Model Discovery

The k-Nearest Neighbors (kNN) classifier with k=1 emerged as the most effective model. It showcased high F1 scores, low training error, and strong generalization capabilities.