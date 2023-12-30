TensorflowModels
+++++++++++++++++++++++++++++++++


.. class:: TensorflowModels(model_name=None, model_url=None)

    This class manages the training, evaluation, and inference of TensorFlow models for object detection.

    :param model_name: The name of the TensorFlow model to be used. If not provided, it will be inferred from the model_url.
    :type model_name: str, optional
    :param model_url: The URL from where the TensorFlow model can be downloaded. If not provided, it will be inferred from the model_name.
    :type model_url: str, optional
    :raises ValueError: If both model_name and model_url are not provided, or if the model_url does not match the expected URL for the given model_name.

    :ivar BASE_URL: The base URL from where the TensorFlow models can be downloaded.
    :ivar TF_RECORD_SCRIPT_NAME: The name of the script used to generate TensorFlow records.
    :ivar LABEL_MAP_NAME: The name of the label map file.
    :ivar model_name: The name of the TensorFlow model to be used.
    :ivar model_url: The URL from where the TensorFlow model can be downloaded.
    :ivar detection_model: The model that will be loaded from the last checkpoint for performing object detection.
    :ivar CUSTOM_MODEL_NAME: A custom name for the model, prefixed with 'my_'.
    :ivar paths: A dictionary containing various paths related to the model, such as the workspace path, the annotation path, the data path, etc.
    :ivar files: A dictionary containing various files related to the model, such as the pipeline configuration file, the TF record script, and the label map.
    :ivar TRAINING_SCRIPT: The path to the training script for the model.


    * `download_model <download_model.html>`_: Downloads the model from the TensorFlow Model Zoo if url is provided.
    * `create_label_map <labelmap.html>`_: Creates a label map for the dataset.
        .. note::
            A label map is a text file that maps each of the used labels to an integer value. This file is used to map the labels to indices, which are then used to construct the ground truth and prediction tensors.
    * `data_to_tfrecord <tfrecords.html>`_: Converts the dataset to `TFRecord format <https://www.tensorflow.org/tutorials/load_data/tfrecord>`_.
        .. note::
            TFRecord is the format required by TensorFlow Object Detection API for training.
    * `get_model_type <modeltype.html>`_: Returns the model type based on the configuration of the model. This can be used to modify the configuration of the model.
    * `update_config_basic <config.html>`_: Updates the configuration of the model based on the provided parameters.
    * `train <train.html>`_: Trains the model on the dataset.
    * `evaluate <eval.html>`_: Evaluates the model's performance on the dataset.

    .. note::
        In order to test the model, we provide two functions that can be used to perform inference on images and webcam videos:

        - `test_model_on_image <testimage.html>`_: Performs inference on a single image.
        - `test_model_on_camera <testvideo.html>`_: Executes inference on a webcam.