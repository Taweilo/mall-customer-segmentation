# Mall Customer Segmentation 

![Python version](https://img.shields.io/badge/Python%20version-3.10%2B-lightgrey)
![GitHub last commit](https://img.shields.io/github/last-commit/Taweilo/Mall_Customer_Segmentation)
![GitHub repo size](https://img.shields.io/github/repo-size/Taweilo/Mall_Customer_Segmentation)
![Type of ML](https://img.shields.io/badge/Type%20of%20ML-Clustering%20-blue)
![License](https://img.shields.io/badge/License-MIT-green)

Badge [source](https://shields.io/)
 <img src="https://www.cleartouch.in/wp-content/uploads/2023/02/Customer-Segmentation.png" width="1100">

The objective of this study is to utilize Machine Learning methods to perform customer segmentation. Customer segmentation involves dividing a market into distinct groups of customers who exhibit similar characteristics. By leveraging customer segmentation, companies can effectively identify and address unmet customer needs, gaining a competitive edge through the development of highly appealing products and services.

## Repository structure 
```
├── Image
│   ├── evaluation.jpg                           <- model summary table used in the README
│   ├── heatmap.jpg                              <- heatmap image used in the README
│   ├── lr summary table.jpg                     <- linear regression model summary table used in the README
│   ├── original dataset.jpg                     <- original dataset image used in the README
│   ├── pairplot.jpg                             <- pairplot of different variables used in the README
│   ├── statistics.jpg                           <- statistics of variables used in the README
│   ├── y_pred vs y_test.jpg                     <- scatterplot of the predictions with test value used in the README                                
│
├── Code_Sales_Prediction_.ipynb                 <- python code
├── Data_Dummy Data HSS.csv                      <- dataset
├── LICENSE.txt                                  <- license 
```
## 1. Business Understanding
Clustering, an unsupervised machine learning technique, is employed for customer segmentation. Clustering aims to discover inherent groups or clusters within data, without prior knowledge of their existence. The following highlights the advantages and disadvantages of utilizing clustering for customer segmentation.

**Advantages of clustering**:<br>

- Facilitates the identification of unexpected or unknown customer groups.
- Provides flexibility and can be applied to diverse datasets.
- Reduces the necessity for extensive expertise in understanding the relationship between customer demographics and behaviors.
- Offers quick and scalable analysis, even with large datasets.

**Disadvantages of clustering**:<br>
- Generated customer groups may lack interpretability and clarity.
- If the data does not incorporate customer behavior information, such as purchase history or service usage, the practical utilization of identified clusters might be challenging.

By considering these factors, businesses can make informed decisions when leveraging clustering techniques for customer segmentation, ensuring meaningful and actionable insights that drive strategic success.

## 2. Data Understanding 
2.1 Data source: This project is a part of the Mall Customer Segmentation Data competition held on Kaggle. <br>
2.2 Exploratory data analysis (EDA): it is used to analyze and investigate data sets and summarize their main characteristics, often employing data visualization methods. The purpose is to understand data and encourage the following analytics. <br>
2.3 Feature engineering: this step is to clean data and deal with the data issue. Since our data is pretty clean, we just rename the feature in an intuitive way.

* Original Dataset
 <img src="https://github.com/Taweilo/Sales_Prediction_from_Media_Spend/blob/main/Image/original%20dataset.jpg" width="400">
 
| Name | Modeling Role | Measurement Level| Description|
| ---- | ------------- | ---------------- | ---------- |
| **TV** | input | float | TV promotion budget (in million) |
| **Radio** | input | float | Radio promotion budget (in million) |
| **Social Media** | input | float | Social Media promotion budget (in million) |
| **Influencer** | input | Object | Type of Influencers |
| **Sales** | target | float | Sales in million |

* Statistics
 <img src="https://github.com/Taweilo/Sales_Prediction_from_Media_Spend/blob/main/Image/statistics.jpg" width="300">
 
* Heatmap
 <img src="https://github.com/Taweilo/Sales_Prediction_from_Media_Spend/blob/main/Image/heatmap.jpg" width="300">

* Pairplot
 <img src="https://github.com/Taweilo/Sales_Prediction_from_Media_Spend/blob/main/Image/pairplot.jpg" width="400">
 
## 3. Data Preparation 
### 3.1. Standardize the data:To calculate their z-score.
This is done in two steps, for each column:
1. First, subtract the mean of the data from each data point. This centers the data
around 0, to make the data easier to look at and interpret, although this is not
strictly required for clustering.
2. The second step is to divide the parameters by their standard deviation.
### 3.2 Different appraches to Decide K (How many clusters)
1. Simple Visual Inspection to Choose the Optimal K
2. The Elbow Method with Sum of Squared Errors
3. The Silhouette Score to Pick Optimal Number of Clusters

 
## 4. Modeling   
   <img src="https://global-uploads.webflow.com/5d3ec351b1eba4332d213004/6026b7494be6481c635b0f84_axkJOrqGKDEK3a6U4mf8fRr5t0FKQIVvbJhDFVFyINVnpkEcv54vLydIg4BOcmyl-cSRakxD3L5-JR8GXMuNU67F5eTXD7ZpL6-MEekv50k8lkEMvIT8ludrUxWOjhAZ8i1_-7eY.png" width="400">
   
The trade-off between interpretability and performance of these ML models. Highly interpretable algorithms such as linear regression, are often inaccurate because of high bias but low variance. Very accurate DNNs are a classic example of black boxes, with low bias but high variance. However, the model performance is highly associated with the data type. Several models were included for further evaluation:

* K-means
* Hierarchical Clustering
  
## 5. Evaluation
 <img src="https://github.com/Taweilo/Sales_Prediction_from_Media_Spend/blob/main/Image/evaluation.jpg" width="500" >
 
## 6. Recommendation
The advantage of machine learning-based clustering is its ability to expedite the segmentation process and discover patterns without requiring extensive domain knowledge. There are various methods available for ML clustering, such as K-means, K-medians, and hierarchical clustering, each with its own strengths and limitations. In our specific case, K-means necessitates predefining the number of clusters (K), whereas hierarchical clustering can generate cluster groups based on different K values. It is crucial to compare the results of these techniques objectively.

Moreover, the choice of the number of segments (K) should align with business requirements. Fewer segments can provide a simplified and interpretable understanding of customers, while more segments allow for finer-grained customer segmentation. However, the clusters, regardless of their quality, hold no significance if they are not actionable for the business. Non-actionability can arise in two ways:

The clusters lack business rationale.
The number of clusters is excessively large.
In essence, machine learning techniques must consider business value and strategy to ensure that the insights derived are meaningful and actionable. By doing so, these insights become invaluable and can drive impactful business decisions.

## 7. Reference
- Baig, M. R., Govindan, G., & Shrimali, V. R. (2021). Data Science for Marketing Analytics: A practical guide to forming a killer marketing strategy through data analysis with Python (2nd ed.), Chapter 3: Unsupervised Learning and
Customer Segmentation (pp. 113-159). Packt Publishing. 
- Sagar, A. (2019, August 24). Customer Segmentation Using K Means Clustering. https://towardsdatascience.com/customer-segmentation-using-k-means-clustering-d33964f238c3. 
 
