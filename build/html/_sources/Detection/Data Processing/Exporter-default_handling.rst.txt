Exporter.default_handling
++++++++++++++++++++++++++

.. method:: Exporter.default_handling()

   Performs the default handling of data export.

   This method performs the following steps:

   1. Splits the paired data into training, validation, and test sets using the specified split percentages.
   2. Exports the paired data to a local directory organized by training, validation, and test sets.
   3. Counts and tracks the number of original and augmented images in each set.

   Example:
   ::

       exporter = Exporter(paired_files, split_parameters=(0.8, 0.1, 0.1))
       exporter.default_handling()
