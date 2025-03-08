# Customer Segmentation Project

## Overview

This project involves analyzing a dataset containing information about customers, their transactions, branches, and merchants from an e-commerce platform. The primary goal is to segment customers based on their transactional behavior and demographic information to optimize marketing strategies, particularly for offering targeted coupons.

## Dataset

The dataset consists of six tables stored in `E-commerce_data.xlsx`:

1. **Customers**: Contains customer IDs, join dates, city IDs, and gender IDs.
2. **Genders**: Maps gender IDs to gender names.
3. **Cities**: Maps city IDs to city names.
4. **Transactions**: Details of transactions including transaction IDs, customer IDs, transaction dates, statuses, coupon names, burn dates, and branch IDs.
5. **Branches**: Maps branch IDs to merchant IDs, such as:

   | branch_id | merchant_id |
   |-----------|-------------|
   | 1         | 11          |
   | 2         | 18          |
   | 3         | 8           |
   | 4         | 15          |
   | ...       | ...         |

6. **Merchants**: Maps merchant IDs to merchant names, such as:

   | merchant_id | merchant_name               |
   |-------------|-----------------------------|
   | 1           | Rivas Group                 |
   | 2           | Peters-Acosta               |
   | 3           | Duran, Perry and Stout      |
   | ...         | ...                         |

## Model Approach

The project employs unsupervised machine learning techniques to segment customers. The primary steps include:

1. **Data Preparation**: Load and merge tables to create a comprehensive dataset. Ensure data is clean and structured for analysis.
2. **Feature Engineering**: Select relevant features for clustering, such as transaction frequency, transaction status, and demographic information.
3. **Data Scaling**: Normalize features to ensure they are on a similar scale, crucial for effective clustering.
4. **Clustering**: Use K-Means clustering to segment customers. Experiment with different numbers of clusters to find the optimal segmentation.
5. **Evaluation**: Evaluate cluster quality using the Silhouette Score, ensuring clusters are distinct and well-defined.

## Evaluation Metrics

- **Silhouette Score**: Measures how similar an object is to its own cluster compared to other clusters. A higher score indicates well-separated clusters.
- **Inertia (for K-Means)**: Represents the sum of squared distances of samples to their closest cluster center. Lower inertia indicates better clustering.

## Key Findings

1. **Cluster Analysis**: The optimal number of clusters was determined using the Elbow Method and Silhouette Analysis, leading to meaningful customer segments.
2. **Customer Segments**: Each segment exhibits distinct behaviors and demographics, such as different transaction patterns and preferences for specific merchants or branches.
3. **Marketing Insights**: Insights from the segmentation can inform targeted marketing strategies, such as offering personalized coupons to different segments to increase engagement and loyalty.

## Future Work

- **Feature Expansion**: Incorporate additional features such as time since joining or frequency of specific coupon usage for more nuanced segmentation.
- **Algorithm Exploration**: Explore other clustering algorithms like DBSCAN or Hierarchical Clustering to capture more complex customer behaviors.
- **Real-Time Segmentation**: Implement real-time segmentation to adapt to changing customer behaviors rapidly.

## Conclusion

This project successfully demonstrates the use of unsupervised learning for customer segmentation, offering valuable insights for targeted marketing. By refining the model and expanding features, the segmentation can be further optimized to drive customer engagement and satisfaction.
