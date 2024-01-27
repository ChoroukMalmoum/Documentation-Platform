FilesHandler
+++++++++++++++++++++++++++++++++

.. class:: FilesHandler(files, image_types=None, label_types=None)

   Handles a collection of files, separating them by type and performing default handling.

   :param files: List of file-like objects to be processed.
   :type files: list
   :param image_types: List of allowed image file extensions. Defaults to ["png", "jpg", "jpeg"].
   :type image_types: list, optional
   :param label_types: List of allowed label file extensions. Defaults to ["txt", "yaml"].
   :type label_types: list, optional

   :ivar files: List of file-like objects to be processed.
   :ivar image_types: List of allowed image file extensions.
   :ivar label_types: List of allowed label file extensions.
   :ivar fails: List to store files that failed processing.
   

   * `remove_empty <FilesHandler-remove_empty.html>`_
   * `pair <FilesHandler-pair.html>`_
   * `separate_files_by_type <FilesHandler-separate_files_by_type.html>`_
   * `default_handling <FilesHandler-default_handling.html>`_