TensorflowModels.update_config_basic
+++++++++++++++++++++++++++++++++++++

.. method:: TensorflowModels.update_config_basic(batch_size=4, num_train_steps=10)

    Updates the basic configuration of the model.

    This method reads the 'pipeline.config' file and updates the number of classes, 
    batch size, fine tune checkpoint, fine tune checkpoint type, and number of training steps 
    based on the model type and the provided parameters. The updated configuration is then 
    written back to the 'pipeline.config' file.

    :param batch_size: The batch size for training. Default is 4.
    :type batch_size: int, optional
    :param num_train_steps: The number of training steps. Default is 10.
    :type num_train_steps: int, optional
    :raises ValueError: If the model type is not supported.
    :raises FileNotFoundError: If the 'pipeline.config' or 'CLASSES_TXT' file does not exist.

    .. note::
        'pipeline.config' is the file that contains the configuration of the model.