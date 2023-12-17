Merge Datasets
+++++++++++++++


.. class:: merge_datasets(dataset1, dataset2, column_dataset1, column_dataset2, merge_type='left')

   The `merge_datasets` class merges two datasets based on specified columns.

   :param dataset1: The first dataset.
   :type dataset1: pd.DataFrame
   :param dataset2: The second dataset.
   :type dataset2: pd.DataFrame
   :param column_dataset1: The column from the first dataset for merging.
   :type column_dataset1: str
   :param column_dataset2: The column from the second dataset for merging.
   :type column_dataset2: str
   :param merge_type: Type of merge to be performed. Options: 'left', 'right', 'inner', 'outer'.
   :type merge_type: str, optional

   :return: Merged dataset.
   :rtype: pd.DataFrame
   - Refer to the `pandas.DataFrame.merge documentation <https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.merge.html>`_ for more details on the ``merge`` method.

