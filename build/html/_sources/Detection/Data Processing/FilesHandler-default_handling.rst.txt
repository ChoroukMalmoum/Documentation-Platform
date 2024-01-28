FilesHandler.default_handling
++++++++++++++++++++++++++++++

.. method:: FilesHandler.default_handling()

   Performs default handling of files:

   1. Removes empty files.
   2. Separates files by type (images and labels).
   3. Pairs images and labels based on names.

   :return: A list of tuples, each containing a paired image and label file.
   :rtype: list
