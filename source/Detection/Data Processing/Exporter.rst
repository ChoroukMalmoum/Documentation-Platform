Exporter
+++++++++++++++++++++++++++++++++

.. class:: Exporter(paired_files, split_parameters=(0.8, 0.1, 0.1))

   Class for exporting paired image and label data to a local directory.

   :param paired_files: List of paired image and label files.
   :type paired_files: list
   :param split_parameters: Tuple containing train, validation, and test split percentages. Defaults to (0.8, 0.1, 0.1).
   :type split_parameters: tuple, optional

   * `split_data <Exporter-split_data.html>`_
   * `export_local <Exporter-export_local.html>`_
   * `default_handling <Exporter-default_handling.html>`_

   .. note::
      The `random_split` function from the `torch.utils.data` module is used for data splitting. For more information, refer to the `PyTorch documentation <https://pytorch.org/docs/stable/data.html#torch.utils.data.random_split>`_.

   .. note::
      The `os` module is used for directory creation and file writing. For more information, refer to the `Python documentation <https://docs.python.org/3/library/os.html>`_.
