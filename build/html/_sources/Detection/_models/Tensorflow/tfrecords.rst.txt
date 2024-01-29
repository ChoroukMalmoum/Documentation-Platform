TensorflowModels.data_to_tfrecord
+++++++++++++++++++++++++++++++++++++

.. method:: TensorflowModels.data_to_tfrecord(mode='train')

    Converts the data to the TFRecord format.

    This method runs a script that converts the data in the specified mode 
    (train or test) to the TFRecord format. The resulting TFRecord file is 
    saved to the 'ANNOTATION_PATH'.

    :param mode: The mode of the data to convert. This should be either 'train' or 'test'. Default is 'train'.
    :type mode: str, optional
    :raises subprocess.CalledProcessError: If there is an error during the execution of the script.

    .. note::
    TFRecord is the format required by TensorFlow Object Detection API for training.