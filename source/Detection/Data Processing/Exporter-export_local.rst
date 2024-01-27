Exporter.export_local
++++++++++++++++++++++

.. method:: Exporter.export_local(train_data, val_data, test_data)

   Exports the paired data to a local directory.

   This method takes the subsets of paired data for training, validation, and test sets and exports them to the specified
   local directory. It organizes the exported data into subdirectories for each set and further categorizes the data based
   on whether it is an original or augmented image.

   :param train_data: Subset of paired data for training.
   :type train_data: list
   :param val_data: Subset of paired data for validation.
   :type val_data: list
   :param test_data: Subset of paired data for testing.
   :type test_data: list

   Example:
   ::

       train_data, val_data, test_data = exporter.split_data()
       exporter.export_local(train_data, val_data, test_data)
