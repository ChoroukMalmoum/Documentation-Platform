train
+++++++++++++++++++++++

.. method:: YoloModel.train(n_epochs=2, learning_rate=0.01, batch_size=16, optimizer='auto', resume=False, img_size=640, patience=50, callback=True)

    Trains the YOLO model.

    This method loads the model, optionally adds a callback for plotting metrics, and starts the training of the model. The training is performed with the specified number of epochs, learning rate, batch size, optimizer, image size, and patience. If 'resume' is True, the training is resumed from the last checkpoint. If 'callback' is True, a callback for plotting metrics is added.

    :param n_epochs: The number of epochs for training. Default is 2.
    :type n_epochs: int

    :param learning_rate: The learning rate for training. Default is 0.01.
    :type learning_rate: float

    :param batch_size: The batch size for training. Default is 16.
    :type batch_size: int

    :param optimizer: The optimizer for training. Default is 'auto'.
    :type optimizer: str

    :param resume: A flag indicating whether to resume the training from the last checkpoint. Default is False.
    :type resume: bool

    :param img_size: The size of the images for training. Default is 640.
    :type img_size: int

    :param patience: The patience for early stopping. Default is 50.
    :type patience: int

    :param callback: A flag indicating whether to add a callback for plotting metrics. Default is True.
    :type callback: bool

    :return: The results of the training.
    :rtype: dict

    :raises FileNotFoundError: If the model file does not exist.