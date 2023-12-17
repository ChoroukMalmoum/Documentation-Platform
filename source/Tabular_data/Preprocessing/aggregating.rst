Aggregation and Grouping
+++++++++++++++++++++++++++++++++

.. class:: aggregate_and_group(df, grouping_columns, aggregation_functions)

   The `aggregate_and_group` class aggregates data by grouping rows based on specific criteria.

   :param df: The input DataFrame.
   :type df: pd.DataFrame
   :param grouping_columns: A list of column names to group by.
   :type grouping_columns: list
   :param aggregation_functions: A dictionary where keys are column names and values are aggregation functions.
   :type aggregation_functions: dict

   :return: A new DataFrame with aggregated and grouped data.
   :rtype: pd.DataFrame

   - Refer to the `pandas.DataFrame.agg documentation <https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.agg.html>`_ for more details on the ``Aggregation`` method.

