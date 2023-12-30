predict_on_image
+++++++++++++++++++++++


.. method:: YoloModel.predict_on_image(file_path=None, best=True)

    Performs prediction on an image.

    This method loads the weights of the YOLO model, performs prediction on the specified image, plots the predictions, and saves the plotted image. If 'best' is True, the best weights are used. Otherwise, the last weights are used.

    :param file_path: The path to the image file. If not specified, a ValueError is raised.
    :type file_path: str

    :param best: A flag indicating whether to use the best weights. Default is True.
    :type best: bool

    :return: The plotted image with predictions.
    :rtype: PIL.Image.Image

    :raises ValueError: If the file path is not specified.
    :raises FileNotFoundError: If the image file does not exist.