Handling Outliers
++++++++++++++++++

.. class:: drop_outliers(df, column_name, method='auto', z_threshold=3, iqr_multiplier=15)

   The `drop_outliers` method is a preprocessing subclass.

   This method provides options for handling outliers in a DataFrame, allowing users to choose between automated methods or customized approaches.

   - **Z-Score Method:**
     Suited for datasets with a normal distribution, this method identifies outliers based on their deviation from the mean in terms of standard deviations using the ``z_threshold``.

   - **IQR Method:**
     Ideal for datasets with skewed distributions, this method uses the Interquartile Range (IQR) to detect and manage outliers using the ``iqr_multiplier``.

   :param df: The input DataFrame with missing values.
   :type df: pd.DataFrame

   :param method: Method for handling missing data. Options: 'auto', 'z-score', or 'iqr'. Default is 'drop'.
   :type method: str

   :param threshold: Threshold for dropping rows or columns based on missing values percentage. Default is 0.7.
   :type threshold: float

   :param imputation_method: Method for imputation when 'method' is set to 'impute'. Options: 'mean', 'median', 'constant', 'knn'. Default is 'mean'.
   :type imputation_method: str

   :param constant_value: Constant value to fill missing values if 'imputation_method' is set to 'constant'. Default is None.
   :type constant_value: float or None

   :param k_neighbors: Number of neighbors to consider for KNN imputation. Default is None.
   :type k_neighbors: int or None

   :param z_threshold: Z-score threshold for outlier removal. Default is 2.0.
   :type z_threshold: float

   :param iqr_multiplier: Multiplier for IQR-based outlier removal. Default is 1.5.
   :type iqr_multiplier: float

   :return: DataFrame with missing values handled according to the specified method.
   :rtype: pd.DataFrame

   .. note::
      - If the specified method is set to 'auto', the code calculates the skewness of the data in the given column using the skew() function. Skewness is a measure of the asymmetry of the data distribution. If the skewness is less than 1, it assumes a normal distribution ('z-score'); otherwise, it assumes a skewed distribution ('iqr').
      - Refer to the `Pandas.DataFrame.skew documentation <https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.skew.html>`_ for more details on the ``skew()`` function.


