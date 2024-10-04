# Customer Segmentation using K-Means Clustering

This project aims to perform customer segmentation using K-Means clustering. The dataset consists of customer demographics, purchasing behavior, and interactions with a marketing campaign. The goal is to identify distinct customer groups that can inform targeted marketing strategies.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Data Preprocessing](#data-preprocessing)
3. [Principal Component Analysis (PCA)](#principal-component-analysis-pca)
4. [K-Means Clustering](#k-means-clustering)
5. [Results](#results)
6. [Conclusion](#conclusion)
7. [Installation](#installation)
8. [Acknowledgements](#acknowledgements)

## Project Overview

In this project, we apply unsupervised learning techniques, specifically **K-Means clustering**, to segment a customer base. Customer segmentation is a powerful tool in marketing, allowing businesses to target different customer groups with personalized marketing strategies.

The dataset contains information about customer demographics, such as age and marital status, as well as data about their purchasing behavior (e.g., spending on different products and the number of web or store purchases). By clustering customers with similar behavior patterns, the business can better understand its customer base.

## Data Preprocessing

Before applying clustering algorithms, the dataset was preprocessed to ensure it was clean and consistent:

- **Handling Missing Values**: Rows with missing income values were removed, and remaining missing data were filled using mean imputation.
- **One-Hot Encoding**: Categorical variables (e.g., education, marital status) were transformed into numerical form using one-hot encoding.
- **Standardization**: Numerical data (e.g., income, spending) were standardized to have a mean of 0 and a standard deviation of 1.
- **Date Handling**: The `Dt_Customer` column was converted to a `datetime` format, and a new feature, `Customer_Since`, was created to represent the number of years since the customer enrolled with the company.

## Principal Component Analysis (PCA)

To reduce the dimensionality of the dataset and improve clustering performance, **Principal Component Analysis (PCA)** was applied. This allowed us to retain the most important features that explain the majority of the variance in the data:

- **Explained Variance**: After applying PCA, it was determined that two principal components were sufficient to explain over 90% of the variance in the dataset.

## K-Means Clustering

After dimensionality reduction, **K-Means clustering** was applied to group customers into distinct segments:

- **Optimal Number of Clusters**: Based on **Silhouette Score** analysis, the optimal number of clusters was determined to be 2.
- **Clustering**: The customers were clustered into two groups using the K-Means algorithm, allowing for meaningful segmentation of the customer base.

## Results

- **Cluster Visualization**: The clusters were visualized using the two principal components from PCA, showing clear separation between the two customer groups.
- **Silhouette Score**: The Silhouette Score for 2 clusters was approximately 0.62, indicating well-separated clusters.

## Conclusion

The analysis successfully grouped the customers into **two clusters**, providing a foundation for potential marketing strategies tailored to these segments. This segmentation can help the business better understand its customer base, allowing for targeted marketing campaigns and personalized engagement strategies. By utilizing **PCA** for dimensionality reduction and **K-Means** for clustering, we were able to identify meaningful patterns in customer behavior, which can be further explored to maximize business outcomes.

## Installation

o run this project, you'll need to have Python 3.x installed and the necessary libraries listed in the `requirements.txt` file.

To install the dependencies, run the following command:

```bash
pip install -r requirements.txt
```

## Acknowledgements

The dataset for this project is provided by **Dr. Omar Romero-Hernandez** and can be found on Kaggle: [Customer Personality Analysis Dataset](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis).

