export
+++++++++++++++++++++++

.. method:: YoloModel.export(img_size=640, export_format='onnx', keras=False, best=True)

    Exports the YOLO model to the specified format.

    This method loads the weights of the YOLO model and exports the model to the specified format. The image size and keras flag can be specified. If 'best' is True, the best weights are used. Otherwise, the last weights are used.

    :param img_size: The size of the images for the exported model. Default is 640.
    :type img_size: int

    :param export_format: The format to export the model to. Default is 'onnx'. Valid formats are 'onnx', 'torchscript', 'openvino', 'engine', 'coreml', 'pb', 'tflite', 'edgetpu', 'tfjs', 'paddle', 'ncnn', 'saved_model'.
    :type export_format: str

    :param keras: A flag indicating whether to export the model to Keras format. Default is False.
    :type keras: bool

    :param best: A flag indicating whether to use the best weights. Default is True.
    :type best: bool

    :raises ValueError: If the export format is not valid.