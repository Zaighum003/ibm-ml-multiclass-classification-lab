# Multi-class Classification Lab - IBM Machine Learning Course

## Overview

This repository contains my completed lab work from the IBM Machine Learning course, specifically focusing on **Multi-class Classification** techniques. The lab demonstrates the implementation and comparison of different strategies for multi-class classification problems using real-world data.

## Lab Objectives

After completing this lab, I was able to:

1. **Understand one-hot encoding** for categorical variables
2. **Implement logistic regression** for multi-class classification using:
   - **One-vs-All (OvA)** strategy
   - **One-vs-One (OvO)** strategy
3. **Evaluate model performance** using appropriate metrics

## Dataset Information

### Obesity Risk Prediction Dataset
- **Source**: UCI Machine Learning Repository
- **License**: CCA 4.0
- **Dataset**: [Estimation of obesity levels based on eating habits and physical condition](https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition)
- **Size**: 2,111 samples with 17 attributes
- **Target Variable**: Obesity level classification

### Features
The dataset includes various health and lifestyle factors:
- **Demographics**: Gender, Age, Height, Weight
- **Family History**: Family history with overweight
- **Eating Habits**: 
  - High caloric food consumption (FAVC)
  - Vegetable consumption frequency (FCVC)
  - Number of main meals daily (NCP)
  - Food consumption between meals (CAEC)
- **Health Behaviors**:
  - Smoking status (SMOKE)
  - Daily water consumption (CH2O)
  - Calorie monitoring (SCC)
  - Physical activity frequency (FAF)
  - Technology usage time (TUE)
- **Lifestyle**:
  - Alcohol consumption frequency (CALC)
  - Transportation method (MTRANS)

## Multi-class Classification Strategies

### One-vs-All (OvA) Strategy
- **Approach**: Trains one binary classifier per class
- **Number of Classifiers**: k (where k = number of classes)
- **Advantages**: 
  - Simpler implementation
  - More efficient for algorithms with confidence scores
- **Disadvantages**: 
  - May struggle with class imbalance
  - Each classifier must distinguish one class from all others

### One-vs-One (OvO) Strategy
- **Approach**: Trains binary classifier for every pair of classes
- **Number of Classifiers**: k(k-1)/2
- **Advantages**:
  - Better for computationally expensive algorithms
  - Can be more accurate as classifiers focus on specific class pairs
- **Disadvantages**:
  - Computationally expensive for many classes
  - May lead to ambiguous predictions with voting ties

## Implementation Details

### Data Preprocessing
1. **Exploratory Data Analysis**: Analyzed class distribution and data quality
2. **Feature Scaling**: Standardized numerical features using StandardScaler
3. **One-Hot Encoding**: Converted categorical variables to numerical format
4. **Target Encoding**: Encoded target variable for classification

### Model Training
- **Algorithm**: Logistic Regression
- **Strategies**: Both OvA and OvO approaches
- **Evaluation**: Accuracy metrics and performance comparison

## Results

The lab successfully demonstrated:
- **Data preprocessing** techniques for multi-class classification
- **Implementation** of both OvA and OvO strategies
- **Model evaluation** and performance comparison
- **Practical understanding** of when to use each approach

## Course Context

This lab is part of the **IBM Machine Learning** course, which covers:
- Supervised and unsupervised learning
- Classification and regression techniques
- Model evaluation and validation
- Real-world applications of machine learning

## Files Included

- `Multi-class_Classification.ipynb`: Complete Jupyter notebook with the lab implementation
- `README.md`: This comprehensive documentation

## Technologies Used

- **Python**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Scikit-learn**: Machine learning algorithms and preprocessing
- **Matplotlib & Seaborn**: Data visualization
- **Jupyter Notebook**: Interactive development environment

## Learning Outcomes

Through this lab, I gained practical experience in:
- Handling multi-class classification problems
- Understanding the trade-offs between different classification strategies
- Implementing data preprocessing pipelines
- Evaluating model performance
- Working with real-world datasets

This repository serves as a portfolio piece demonstrating my understanding of multi-class classification concepts and practical implementation skills in machine learning.

---

*This lab was completed as part of the IBM Machine Learning course, showcasing hands-on experience with advanced classification techniques and real-world data analysis.*