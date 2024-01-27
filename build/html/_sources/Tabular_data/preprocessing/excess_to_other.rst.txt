Replace Excess Categories with "Other"
++++++++++++++++++++++++++++++++++++++

.. function:: replace_excess_values_with_other(df, columns_to_replace, top_n=3)

   The :func:`replace_excess_values_with_other` method replaces values in categorical columns not in the top N most common values with 'other'.

   :param df: The input DataFrame.
   :type df: pd.DataFrame
   :param columns_to_replace: List of column names to perform replacement.
   :type columns_to_replace: list
   :param top_n: Number of top values to keep. Default is 3.
   :type top_n: int, optional

   :return: DataFrame with specified columns values replaced with 'other'.
   :rtype: pd.DataFrame
