# Heart Attack Prediction: Unsupervised Learning Clustering Analysis

## Project Overview

This project explores the application of unsupervised machine learning techniques for heart attack risk assessment and pattern discovery in cardiac health data. Using clustering algorithms, the study identifies hidden patterns and patient groupings without prior labeled data, demonstrating the potential of unsupervised learning in cardiovascular medicine.

## Objective

Investigate the feasibility of unsupervised learning methods in medical contexts, specifically for discovering natural groupings in heart attack risk factors and exploring emergent relationships in cardiovascular health data.

## Dataset & Preprocessing

### Data Source
- **Origin**: Kaggle heart attack dataset
- **Features**: 14 clinical and demographic variables
- **Target Variable**: Heart attack occurrence (binary)
- **Data Quality**: Minimal preprocessing required (only 1 duplicate record)

### Key Features
- **age**: Patient age
- **sex**: Gender 
- **cp**: Chest pain type
- **trestbps**: Resting blood pressure
- **chol**: Cholesterol levels
- **fbs**: Fasting blood sugar
- **restecg**: Resting ECG results
- **thalach**: Maximum heart rate achieved
- **exang**: Exercise-induced angina
- **oldpeak**: ST depression induced by exercise
- **slope**: Peak exercise ST segment slope
- **ca**: Number of major vessels colored by fluoroscopy
- **thal**: Thalassemia type

### Preprocessing Steps
- **Data Splitting**: 70% training, 30% testing
- **Class Balancing**: Applied RandomOverSampler for uniform target distribution
- **Feature Selection**: Used 3 key variables (age, thalach, oldpeak) for visualization
- **Correlation Analysis**: Confirmed minimal linear dependence between variables

## Unsupervised Learning Algorithms

### 1. K-Means Clustering
- **Algorithm**: Partitions data into k clusters by minimizing within-cluster sum of squares
- **Distance Metric**: Euclidean distance to centroids
- **Cluster Selection**: Elbow method determined optimal k=2 clusters
- **Implementation**: Scikit-learn KMeans

### 2. Mean-Shift Clustering
- **Algorithm**: Non-parametric technique finding density maxima in feature space
- **Advantage**: Automatically determines number of clusters and centroids
- **Results**: Identified 2 natural clusters in the data
- **Implementation**: Scikit-learn MeanShift

## Methodology

### Cluster Optimization
- **Elbow Method**: Systematic evaluation of cluster numbers for K-means
- **Automatic Selection**: Mean-Shift self-determined optimal cluster count
- **Visualization**: 3D scatter plots for cluster interpretation
- **Validation**: Cross-comparison between both algorithms

### Exploratory Analysis
- **Correlation Matrix**: Identified feature independence
- **Target Distribution**: Analyzed heart attack occurrence patterns
- **Feature Combinations**: Visualized variable relationships and cluster separability

## Results & Findings

### Clustering Outcomes
- **Convergent Results**: Both algorithms identified 2 distinct patient clusters
- **Cluster Characteristics**: Groups showed similar risk factor patterns
- **Data Complexity**: Dataset presented challenging separability
- **Validation**: Consistent clustering across different algorithms suggests meaningful patterns

### Key Insights
- **Patient Segmentation**: Natural groupings exist in heart attack risk profiles
- **Risk Stratification**: Clusters may represent different risk categories
- **Feature Importance**: Age, maximum heart rate, and ST depression are key clustering variables
- **Pattern Discovery**: Unsupervised approach revealed hidden data structures

## Technical Implementation

### Tools & Libraries
- **Language**: Python
- **Clustering**: scikit-learn (KMeans, MeanShift)
- **Data Processing**: pandas, numpy
- **Visualization**: matplotlib, seaborn
- **Sampling**: imblearn (RandomOverSampler)

### Evaluation Methods
- **Visual Assessment**: 3D cluster plots
- **Elbow Analysis**: Optimal cluster determination
- **Cross-Algorithm Validation**: Consistency between methods
- **Correlation Analysis**: Feature relationship mapping
