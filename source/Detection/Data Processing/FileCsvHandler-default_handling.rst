FileCsvHandler.default_handling
+++++++++++++++++++++++

.. method:: FileCsvHandler.default_handling()

   Performs default handling of the CSV file:

   1. Reads the CSV file and extracts image links and labels.
   2. Fetches images from the provided image links.
   3. Pairs images with labels.
   4. Removes pairs with empty images or labels.

   :returns: A list of non-empty tuples, each containing a paired image and label NamedBytesIO.
   :rtype: list
