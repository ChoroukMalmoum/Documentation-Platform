Feature Selection
++++++++++++++++++

.. function:: apply_pca(df, excluded_features=[], num_components=None)

   The :func:`apply_pca` method performs Principal Component Analysis (PCA) on a DataFrame for feature selection.

   :param df: The input DataFrame.
   :type df: pd.DataFrame
   :param excluded_features: A list of column names to retain without applying PCA.
   :type excluded_features: list, optional
   :param num_components: Specify the number of desired features. If not provided, it retains all features.
   :type num_components: int, optional

   :return: DataFrame with PCA applied, explained_variance_ratios.
   :rtype: pd.DataFrame

   - **Explanation:**
     PCA is applied to the input DataFrame, excluding specified features if provided. The resulting DataFrame contains the transformed data based on the specified number of desired features (`num_components`).
     
     - If `num_components` is not provided, all features are retained.
     - `excluded_features` allow users to specify a list of features they want to keep without applying PCA.

     The resulting DataFrame includes the transformed data and provides insights into the proportion of variance explained by each selected principal component through the `explained_variance_ratios` attribute.
     - Refer to the `sklearn.decomposition.PCA documentation <https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html>`_ for more details on the ``PCA`` method.