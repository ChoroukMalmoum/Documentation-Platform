Handling missing values

.. class:: handle_missing_data(df, method='drop', threshold=0.7, imputation_method='mean', constant_value=None, k_neighbors=2)

   The `handle_missing_data` class provides functionality for handling missing values in a DataFrame.

   :param df: Input DataFrame with missing values.
   :type df: pd.DataFrame

   - **method (str):** ``drop`` to remove rows or columns, 'impute' to fill missing values. The provided impute methods are: ``mean``, ``median``, and ``constant``.

   - **threshold (float):** Threshold for dropping rows or columns based on missing values percentage.
   - **imputation_method (str):** Method for imputation when 'method' is set to 'impute'.
     Options: 'mean', 'median', 'constant', 'knn'.
   - **constant_value:** Constant value to fill missing values if 'imputation_method' is set to 'constant'.
   - **k_neighbors (int):** Number of neighbors to consider for KNN imputation.

   :return: DataFrame with missing values handled according to the specified method.
   :rtype: pd.DataFrame

   - **Note:**
     - Refer to the `scikit-learn SimpleImputer documentation <https://scikit-learn.org/stable/modules/generated/sklearn.impute.SimpleImputer.html>`_ for more details on the ``mean``, ``median``, and ``constant`` imputation methods.
     - Refer to the `scikit-learn KNNImputer documentation <https://scikit-learn.org/stable/modules/generated/sklearn.impute.KNNImputer.html>`_ for more details on the ``Knn`` imputation method.
     - Refer to the `Pandas.DataFrame.dropna documentation <https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dropna.html>`_ for more details on the ``drop`` rows or columns method.
