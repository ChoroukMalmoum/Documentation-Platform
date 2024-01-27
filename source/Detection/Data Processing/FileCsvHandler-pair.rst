FileCsvHandler.pair
+++++++++++++++++++++++

.. method:: FileCsvHandler.pair(images)

   Pairs images with labels and handles empty labels.

   :param images: List of image NamedBytesIO objects.
   :type images: list

   :returns: A list of tuples, each containing a paired image and label NamedBytesIO.
   :rtype: list