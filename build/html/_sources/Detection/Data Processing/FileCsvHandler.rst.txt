FileCsvHandler
+++++++++++++++++++++++++++++++++

.. class:: FileCsvHandler(file)

   Handles CSV files containing image links and labels.

   :param file: The CSV file to be processed.
   :type file: file-like object

   :ivar image_links: List of image links extracted from the CSV.
   :ivar labels: List of labels extracted from the CSV.
   :ivar fails: List to store files that failed processing.

   * `fetch_images <FileCsvHandler-fetch_images.html>`_
   * `pair <FileCsvHandler-pair.html>`_
   * `remove_empty <FileCsvHandler-remove_empty.html>`_
   * `default_handling <FileCsvHandler-default_handling.html>`_

