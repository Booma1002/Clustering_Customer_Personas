# Project Overview
* This project performs an end-to-end unsupervised machine learning workflow to segment customers from the "Mall Customer" dataset. The goal is to identify distinct customer groups based on their annual income and spending score. The final output is a set of actionable customer personas that can be used to develop targeted marketing strategies.

# Dataset
### Source: 
Mall Customer Segmentation Dataset -> https://www.kaggle.com/datasets/abdallahwagih/mall-customers-segmentation

### Description:
The dataset contains basic information about mall customers, including their ID, age, gender, annual income (in k$), and a calculated spending score (from 1 to 100).

### Features Used:
* Annual Income
* Spending Score

# Methodology & Workflow
### Data Cleaning & EDA:
* Loaded the raw data and cleaned column names for easier access.
* Performed exploratory data analysis to understand the distributions of age, income, and spending.
  
- <img width="500" height="500" alt="b07ec0ff-1012-492b-b1e1-07d35128650f" src="https://github.com/user-attachments/assets/dc47b61a-9e74-46d1-ba87-d6fe81fb36ec" />

* Converted the categorical Gender feature into a numerical format.

### Feature Engineering:
* Applied StandardScaler to the Annual Income and Spending Score features. This was a critical step to normalize the data and ensure that the K-Means algorithm, which is distance-based, would treat both features equally.
* Modeling & Interpretation:

### Elbow Method:
- Implemented the Elbow Method to programmatically determine the optimal number of clusters (k). This was done by analyzing the Within-Cluster Sum of Squares (WCSS) to find the "point of diminishing returns."
<img width="700" height="500" alt="11e565e2-cdcd-4bd9-bb4f-97d063e91358" src="https://github.com/user-attachments/assets/c18b44bc-8127-401d-bc90-5878a564f2c2" />

### K-Means Clustering:
- Applied the KMeans algorithm using the optimal 'k' value of 8 to segment the customers.

### Persona Creation:
- Grouped the original, unscaled data by the newly assigned cluster labels and calculated the mean for each feature. This allowed for the interpretation of each cluster and the creation of meaningful personas.

# Results & Key Findings
The project successfully segmented customers into distinct, interpretable groups. The final annotated chart below visualizes these personas based on their income and spending habits, with each centroid ranked by marketing priority (1 = highest).

<img width="1003" height="704" alt="93675f9e-ffdc-413e-9194-dfaf67d89ca9" src="https://github.com/user-attachments/assets/db374090-e1dc-4cb9-8f52-a8b54f5da922" />

## The key personas identified (sorted according to customer prominence) were:

* **The Gold Mine**
* **Young High Spenders**
* **Young Enthusiasts**
* **Wealthy & Cautious**
* **Standard & Careful**
* **Standard Earners**
* **Standard Low Earners**
* **Frugal Seniors**

# Conclusion
#### This project successfully demonstrates a robust workflow for unsupervised learning. By properly preprocessing the data, using the Elbow Method to select an optimal 'k', and applying K-Means clustering, we were able to transform a simple customer dataset into actionable business intelligence. These identified personas can now be used to create highly targeted and effective marketing campaigns.
