YoloModel
+++++++++++++++++++++++

.. class:: YoloModel(model_name="yolov8n.yaml")

    The ``YoloModel`` class represents a YOLOv8 (You Only Look Once) model.

    :param model_name: The name of the model file. Default is 'yolov8n.yaml'.
    :type model_name: str

    :ivar model_name: The name of the model file.
    :ivar data: The name or path of the data configuration file.
    :ivar project_dir: The path to the directory where the outputs will be saved.
    :ivar vid_id: The ID of the video to process.
    :ivar training_complete: A flag indicating whether the training of the model is complete.
    :ivar plot_complete: A flag indicating whether the plotting of the results is complete.

    .. note::
        For more information about YOLOv8, please visit the `official documentation <https://docs.ultralytics.com/>`_.

    .. note::
        The `data` attribute represents the name of the YAML file that contains data configuration. By default, it is set to "config.yaml". You can replace it with your own YAML file, ensuring it includes:
        - The path to your data directory.
        - The names of your training, testing, and validation data directories.
        - The names and indices of your classes.

        For example:

        .. code-block:: yaml

            path: C:/Path/to/your/data/directory
            test: test
            train: train
            val: val
            names:
                0: dog
                1: cat

        To use your own YAML file, assign its name to the `data` attribute, like so: 

        .. code-block:: python

            model.data = 'your_file.yaml'

    * `train <trainyolov8.html>`_
    * `predict_on_image <predict_on_image.html>`_
    * `predict_on_video <predict_on_video.html>`_
    * `export <exportyolov8.html>`_