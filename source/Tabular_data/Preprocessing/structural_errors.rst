Basic unstructured data
+++++++++++++++++++++++

.. class:: handel_basic_structured_data(df, column=[])

   The `handel_basic_structured_data` class addresses basic structural errors in a DataFrame selected column or all columns.

   :param df: The input DataFrame.
   :type df: pd.DataFrame
   :param column: A list with the names of the columns to check for structural errors. If not provided, all columns will be checked.
   :type column: list of str, optional

   :return: A DataFrame with structural errors fixed.
   :rtype: pd.DataFrame
