models_test Function
======================

.. function:: models_test(df, anomaly_column, y_axis, methods=[])

    Evaluates various anomaly detection models on a dataset using the F1-score metric. The function performs the following operations:

    1. **Model Evaluation**: For each specified method, the function trains the model on the dataset and computes the F1-score.
    
    2. **Results Aggregation**: Collects the F1-scores for each method and returns them in a structured format.

    Supported Methods:
       - **hotelling**: Hotelling's T-squared method.
       - **ocsvm**: One-Class Support Vector Machine.
       - **iforest**: Isolation Forest.
       - **lof**: Local Outlier Factor.
       - **cf**: ChangeFinder.
       - **sigma**: Standard deviation-based thresholding.

    :param df: DataFrame, input dataset for anomaly detection.
    :param anomaly_column: str, column name indicating true anomalies in the dataset.
    :param y_axis: str, column name representing the feature or variable to be analyzed for anomalies.
    :param methods: list, optional, list of methods to evaluate. If empty, all supported methods are evaluated.
    :return: dict, a dictionary containing the F1-scores for each evaluated method, and a dataframe with the anomalies detected using each model.
