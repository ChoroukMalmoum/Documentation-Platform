Yolo.train.train_Custom_model
++++++++++++++++++++++++++++++

.. function:: Yolo.train.train_Custom_model(model, learning_rate=2e-5, batch_size=8, epochs=10, weight_decay=0.0005, optimizer='Adam', S=7, B=2, C=2)

    Trains a custom YOLO model.

    This function trains a custom YOLO model on a dataset. The dataset is loaded from a CSV file and 
    transformed into the appropriate format. The function also calculates the mean average precision 
    (mAP) of the model after each epoch and saves the model if the mAP is greater than 0.9.

    :param model: The model to train.
    :type model: nn.Module
    :param learning_rate: The learning rate for the optimizer. Default is 2e-5.
    :type learning_rate: float, optional
    :param batch_size: The batch size for the DataLoader. Default is 8.
    :type batch_size: int, optional
    :param epochs: The number of epochs to train for. Default is 10.
    :type epochs: int, optional
    :param weight_decay: The weight decay for the optimizer. Default is 0.0005.
    :type weight_decay: float, optional
    :param optimizer: The optimizer to use. Can be either 'Adam' or 'SGD'. Default is 'Adam'.
    :type optimizer: str, optional
    :param S: The number of cells in the output grid. Default is 7.
    :type S: int, optional
    :param B: The number of bounding boxes per cell. Default is 2.
    :type B: int, optional
    :param C: The number of classes. Default is 2.
    :type C: int, optional

    :raises ValueError: If the optimizer is not 'Adam' or 'SGD'.


