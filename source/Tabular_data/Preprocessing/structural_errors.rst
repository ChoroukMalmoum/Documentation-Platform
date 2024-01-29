Basic unstructured data
+++++++++++++++++++++++

.. function:: fix_structural_errors(df, column=[])

   The :func:`fix_structural_errors` method addresses basic structural errors in a DataFrame selected column or all columns.

   :param df: The input DataFrame.
   :type df: pd.DataFrame
   :param column: A list with the names of the columns to check for structural errors. If not provided, all columns will be checked.
   :type column: list of str, optional

   :return: A DataFrame with structural errors fixed.
   :rtype: pd.DataFrame
