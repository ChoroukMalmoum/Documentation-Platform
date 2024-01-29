Machine Learning
+++++++++++++++++


**Prediction**
---------------


The predictive module processes the user-uploaded dataset along with specified parameters, including:

- The target column
- Chosen epochs
- Desired prediction type

For regression tasks, users can opt for:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regression
- k-Nearest Neighbors
- Support Vector Machine Regressor
- Random Forest
- XGBoost Regressor

For classification, choices include:

- Logistic Regression
- k-Nearest Neighbors
- Support Vector Machine Classifier
- Decision Tree
- Random Forest
- Gradient Boosting

**OUTPUT:**

Once users provide these inputs, the function generates metric results. For regression, the outputs consist of mean squared error (MSE), mean absolute error (MAE), and root mean squared error (RMSE). For classification, the function produces a confusion matrix, accuracy score, precision score, recall score, and F1 score.




**Clustering**
---------------

a. **Determining the Optimal Number Of Clusters**
=================================================

  The `OptimalNumberOfClusters <OptimalNumberOfClusters.html>`_ function determines the optimal number of clusters using different methods like the Elbow method, Silhouette method, or Dendrogram visualization. Users can start by selecting one of the 3 next methods:
      - **Elbow Method** : This method visualizes the relationship between the number of clusters and the within-cluster sum of squares. Users provide a range (k_min to k_max) to explore, and the function identifies the "elbow" point, a crucial inflection where the rate of decrease in variance begins to decelerate, indicating a diminishing return on adding more clusters.
      - **Silhouette Method** : By computing silhouette scores for different cluster sizes within the specified range, this approach quantifies the quality of clustering. Higher silhouette scores suggest better-defined clusters, and the function returns the cluster number corresponding to the peak silhouette score.
      - **Dendrogram Visualization** : This method presents a dendrogram, a tree-like structure revealing cluster relationships. Users can visually inspect this tree and infer the number of clusters based on the hierarchical divisions.

b. **Clusters Prediction**
========================
  
  The `predict <predict.html>`_ helps users to easily group their data points into clusters. It simplifies the process of choosing and using a clustering method, making it user-friendly. When users use this function, they can pick a clustering method and set it up according to their needs. The function offers the next 4 methods to choose from:
      - **KMeans** :  A classic centroid-based approach.
      - **Agglomerative Clustering** :  hierarchical method that constructs a tree of clusters.
      - **DBSCAN** : A density-based algorithm identifying clusters as high-density regions separated by low-density areas.
      - **Gaussian Mixture Model (GMM)** : A probabilistic model capturing underlying Gaussian distributions within data.24-hour
      

c. **Clustering methods Testing**
==============================
  The `test <test.html>`_ function offers users a robust framework for comparative analysis of various clustering algorithms. Recognizing the sensitivity of clustering to algorithmic choices, this function aims to elucidate performance disparities across methods. Users are encouraged to input their dataset and desired clustering parameters. Users are presented with a choice of 4 distinct clustering algorithms: KMeans, Agglomerative Clustering, DBSCAN, Gaussian Mixture Model (GMM).
  
  .. warning::
    This function is employed when the user already possesses a column that categorizes their data points into clusters. It evaluates the selected models and contrasts their outcomes with the user-defined clusters using the F1 score.
  
.. note::
  For examples of usage, refer to the `Google Colab Notebook <https://colab.research.google.com/drive/1z-tb0K0ESR4pKrS7imZ3tBV8a6JLiLnh?usp=sharing>`_

**Time series**
-----------------

a. **Preprocessing**
=================

  The `extract_temporal_features_existing <extract_temporal_features_existing.html>`_ function extracts temporal features such as Year, Month, Day, Weekday, Hour, Minute, Second, and Date_Only from a given time series dataset that already includes a timestamp column. It first converts the timestamp data into a standardized format using the provided or inferred timestamp format and then computes the aforementioned temporal features for each timestamp entry, appending them as new columns to the original dataset.

  The `create_timestamp_column <create_timestamp_column.html>`_ function is designed for time series datasets without a unified timestamp column, this function synthesizes a new timestamp column by merging user-specified columns for Year, Month, Day, Hour, Minute, and Second. After constructing the timestamp, the function appends it as a new column to the input dataset, providing a consolidated temporal reference for each data entry.

c. **Charts**
==========
  The `plot_time_series_with_anomalies <plot_time_series_with_anomalies.html>`_ function visualizes a time series data along with identified anomalies using the plotly library. The primary time series is depicted as a continuous line plot, while anomalies, marked with red dots, overlay on top of the original data. This visualization aids in quickly identifying periods or data points deviating significantly from the norm.

  The `create_anomaly_score_plot <create_anomaly_score_plot.html>`_ function generates a graphical representation of anomaly scores derived from a specified anomaly detection method, along with a threshold delineating normal from anomalous behavior. This visualization assists in setting and understanding thresholds for anomaly detection, ensuring that genuine anomalies are accurately distinguished.


d. **Anomaly Detection**
======================
  The `anomalies_detection <anomalies_detection.html>`_ function offers multiple detection methods, including Hotelling's T^2, One-Class SVM, Isolation Forest, Local Outlier Factor, ChangeFinder, and Sigma Thresholding. Depending on the chosen method, the function calculates anomaly scores and determines anomalies based on predefined thresholds or statistical measures, returning a DataFrame annotated with anomaly labels.

  The `models_test <models_test.html>`_ function serves as a comparative evaluation tool for various anomaly detection methods applied to a given time series dataset. By iterating through specified methods, the function computes anomaly labels and evaluates their performance using the F1 score metric, aggregating the results into a DataFrame for easy comparison and further analysis.

  The `plot_f1_scores_plotly <plot_f1_scores_plotly.html>`_ function creates a bar chart illustrating the F1 scores of different anomaly detection methods. Each bar represents a method, and its height corresponds to the computed F1 score, offering a visual benchmark to assess the relative effectiveness of each method in detecting anomalies within the dataset.

.. note::
  For examples of usage, refer to the `Google Colab Notebook <https://colab.research.google.com/drive/1H5MSjPEfX5ZLpY13rGExV5jFHgFrepyv?usp=sharing>`_