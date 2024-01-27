predict_on_video
+++++++++++++++++++++++

.. method:: YoloModel.predict_on_video(file_path=None, mode='webcam', best=True)

    Performs prediction on a video or webcam feed.

    This method loads the weights of the YOLO model, performs prediction on the specified video or webcam feed, plots the predictions, and saves the plotted frames as a new video. If 'best' is True, the best weights are used. Otherwise, the last weights are used.

    :param file_path: The path to the video file. If not specified and mode is 'video', a ValueError is raised.
    :type file_path: str

    :param mode: The mode of prediction. Can be 'video' or 'webcam'. Default is 'webcam'.
    :type mode: str

    :param best: A flag indicating whether to use the best weights. Default is True.
    :type best: bool

    :return: None

    :raises ValueError: If the file path is not specified and mode is 'video'.
    :raises FileNotFoundError: If the video file does not exist.