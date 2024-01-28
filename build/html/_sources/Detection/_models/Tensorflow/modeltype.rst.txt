TensorflowModels.get_model_type
++++++++++++++++++++++++++++++++++

.. method:: TensorflowModels.get_model_type()

    Determines the type of the model.

    This method reads the 'pipeline.config' file and checks which model type field 
    is set (ssd, faster_rcnn, or center_net). The model type is then returned as a string.

    :return: The type of the model ('ssd', 'faster_rcnn', or 'center_net').
    :rtype: str
    :raises ValueError: If the model type in the config file is not supported.
    :raises FileNotFoundError: If the 'pipeline.config' file does not exist.

    .. note::
        'pipeline.config' is the file that contains the configuration of the model.