Exporter.split_data
++++++++++++++++++++

.. method:: Exporter.split_data()

   Splits the paired data into training, validation, and test sets.

   This method calculates the size of each subset based on the provided split percentages and then randomly splits the
   paired files into training, validation, and test sets.

   :returns: A tuple containing three subsets of paired data: training data, validation data, and test data.
   :rtype: tuple

   Example:
   ::

       train_data, val_data, test_data = exporter.split_data()
