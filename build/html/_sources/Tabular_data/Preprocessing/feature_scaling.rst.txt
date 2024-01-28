Feature Scaling
+++++++++++++++

.. function:: scale_features(df, columns=None, method='minmax')

   The :func:`scale_features` method scales numerical features in a DataFrame using standardization or min-max scaling.

   :param df: Input DataFrame.
   :type df: pd.DataFrame
   :param columns: List of numerical feature names to scale. If not provided, all numerical columns will be scaled.
   :type columns: list, optional
   :param method: Scaling method ('standard' for standardization, 'minmax' for min-max scaling).
   :type method: str, optional

   :return: DataFrame with scaled numerical features.
   :rtype: pd.DataFrame
   
   - Refer to the `sklearn.preprocessing.StandardScaler documentation <https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html>`_ for more details on the ``Standardization`` method.
   - Refer to the `sklearn.preprocessing.MinMaxScaler documentation <https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html>`_ for more details on the ``Minmax`` method.
