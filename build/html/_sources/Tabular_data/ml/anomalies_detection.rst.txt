anomalies_detection Function
=============================

.. function:: anomalies_detection(df, y_axis, method)

    Detects anomalies within a dataset using various statistical or machine learning-based methods. The function performs the following operations:

    1. **Method Selection**: Based on the specified method, the function applies the respective anomaly detection algorithm to the dataset.
    
    2. **Anomaly Labeling**: Assigns a binary label (1 for anomaly, 0 for normal) to each data point based on the detection results.

    Supported Methods:
    - **hotelling**: Uses the Hotelling's T-squared method for multivariate outlier detection.
    - **ocsvm**: Applies the One-Class Support Vector Machine algorithm.
    - **iforest**: Utilizes the Isolation Forest algorithm.
    - **lof**: Implements the Local Outlier Factor algorithm.
    - **cf**: Employs the ChangeFinder algorithm.
    - **sigma**: Uses standard deviation-based thresholding.

    :param df: DataFrame, input dataset for anomaly detection.
    :param y_axis: str, column name representing the feature or variable to be analyzed for anomalies.
    :param method: str, selected method for anomaly detection from the supported list.
    :return: DataFrame, the input dataset with an additional column indicating detected anomalies.
