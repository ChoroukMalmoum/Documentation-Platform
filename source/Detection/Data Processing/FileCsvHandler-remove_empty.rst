FileCsvHandler.remove_empty
+++++++++++++++++++++++

.. method:: FileCsvHandler.remove_empty(pairs)

   Removes pairs with empty images or labels.

   :param pairs: List of tuples containing paired image and label NamedBytesIO.
   :type pairs: list

   :returns: A list of non-empty image and label pairs.
   :rtype: list
